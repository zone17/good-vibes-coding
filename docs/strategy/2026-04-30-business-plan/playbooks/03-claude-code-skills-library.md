---
title: GVC Claude Code Skills Library
date: 2026-04-30
type: skills-library-catalog
audience: Matt + Melissa
related:
  - 21-product-portfolio-options.md
  - 22-cold-acquisition-gtm.md
  - 23-business-plan-synthesis-v3.md
---

This document is the catalog of Claude Code skills that turn the recurring parts of GVC's day-in-the-life into one-line invocations. The five highest-leverage skills are fully built and ready to install. The rest are speced and queued.

The point: when the founders find themselves typing the same prompt twice, that prompt becomes a skill. Skills compound. A new client intake takes 90 seconds the second time you do one — and the form gets sharper every month because the skill file is version-controlled.

---

## 1. What a Claude Code skill is (90 seconds)

A skill is a small markdown file with a YAML header and a procedure. Claude Code reads the header to decide *whether to invoke the skill* (it pattern-matches the user's prompt against the `description`), and reads the body to decide *what to do* once invoked.

You install skills, then talk to Claude Code like you always do. When the request matches a skill's trigger conditions, Claude follows the steps in that file rather than improvising. If you want to invoke explicitly, type `/skill-name` and the skill runs.

Skills are not prompts. Skills are operating procedures the LLM follows the same way every time. The first run of `/intake` for a Boca Raton restaurant produces the same artifact shape as the 50th run for a Honesdale B&B. That's the compounding asset.

---

## 2. Where skills live and how to install them

Two locations:

| Scope | Path | When to use |
|---|---|---|
| **User-level (global)** | `~/.claude/skills/<skill-name>.md` | Skills you want available across all projects. Most GVC skills live here. |
| **Project-level** | `<repo>/.claude/skills/<skill-name>.md` | Skills tied to a specific repo (e.g., a client engagement folder with custom delivery rules). |

**Install (global):**
```bash
mkdir -p ~/.claude/skills
cp docs/strategy/2026-04-30-business-plan/playbooks/skills/*.md ~/.claude/skills/
```

**Install (project, e.g., a client folder):**
```bash
mkdir -p .claude/skills
cp docs/strategy/2026-04-30-business-plan/playbooks/skills/sprint-ai-visibility.md .claude/skills/
```

**Verify:** start a new Claude Code session in the relevant directory, type `/` — the skill should appear in the menu. Or just say "run intake for Bistro Mizner" and watch Claude pick the skill.

**Updating a skill:** edit the markdown file. No restart needed for most changes; new skills require a session restart to register.

**Convention:** every skill produced by GVC writes its outputs as local markdown files inside `clients/`, `outreach/`, `workshops/`, or `weekly-reviews/` directories at the repo root. No SaaS, no hosted state. Plain files committed to git.

---

## 3. The 15-skill inventory

Organized by category. Each row: name, one-line purpose, when to invoke, primary outputs.

### Sales & outreach

| Skill | One-liner | When to invoke | Output |
|---|---|---|---|
| `/cold-batch` | Generate N personalized cold-pitch drafts for an industry × city pair | Mondays before the weekly outreach push, or when a workshop wave produces a target list | `outreach/YYYY-MM-DD-{industry}-{city}/batch-NN.md` (numbered drafts) |
| `/proposal` | Draft a fixed-fee proposal page for a sprint after a discovery call | Within 48 hrs of a discovery call where the prospect didn't say no | `clients/{name}/proposal-{sprint}-{date}.md` |
| `/discovery-prep` | Pre-call research dossier — GBP, SaaS-stack scrape, AI-search audit, named pain hypothesis | Day-of any 30-min Calendly discovery call | `clients/{name}/discovery-prep-{date}.md` |
| `/follow-up` | Generate a stage-appropriate follow-up message for a prospect that's gone quiet | Wednesday/Friday cadence; or when a prospect has been silent ≥7 days | Appended to `clients/{name}/log.md` |

### Delivery

| Skill | One-liner | When to invoke | Output |
|---|---|---|---|
| `/intake` | Tailored client intake form generator (business basics, SaaS stack, pains, credentials, success criteria) | After the prospect signs the proposal, before kickoff | `clients/{name}/intake.md` |
| `/sprint-ai-visibility` | End-to-end runner for the AI Visibility Tune-Up sprint (5 days) | When a $750 AI Visibility sprint is sold | `clients/{name}/sprint-{N}/day-1..day-5.md` per-day deliverables |
| `/sprint-menu-reviews` | End-to-end runner for the Menu+Reviews Lite sprint (1 week) | When a $1,500 Menu+Reviews sprint is sold | `clients/{name}/sprint-{N}/menu.md`, `reviews-rules.md`, `voice.md` |
| `/sprint-front-desk` | End-to-end runner for the AI Front-Desk Sprint (2 weeks) | When a $1,800 + $200/mo Front-Desk sprint is sold | `clients/{name}/sprint-{N}/twilio-config.md`, `prompt.md`, `escalation.md` |
| `/case-study` | Turn a finished sprint into a 1-page case study + Loom outline | The Friday a sprint completes, after the retainer is offered | `case-studies/{geo}/{vertical}/{name}.md` plus `loom-script.md` |

### Marketing & content

| Skill | One-liner | When to invoke | Output |
|---|---|---|---|
| `/workshop-prep` | Build the 75-min "AI for Small Business" workshop for a specific venue + audience | 7–10 days before the workshop | `workshops/{date}-{venue}/agenda.md`, `slides.md`, `examples.md`, `cta.md` |
| `/postcard-wave` | Design a 2-step direct-mail wave (postcard + signed letter) for a Poconos list | Quarterly, plus on-demand when a fresh list of 200+ exists | `outreach/postcards/{wave}/postcard.md`, `letter.md`, `list-targeting.md` |
| `/episode-prep` | Outline a podcast episode + show-notes scaffolding | Sunday night for the week's 4 episodes (Mon–Thu) | `podcast/{ep-NNN}-{slug}/outline.md`, `show-notes.md` |
| `/newsletter-recap` | Compile the week's podcast episodes into a Friday newsletter | Friday morning | `newsletter/YYYY-Www.md` |

### Operations

| Skill | One-liner | When to invoke | Output |
|---|---|---|---|
| `/weekly-review` | Friday afternoon review ritual — Gap-and-Gain dashboard + 3 reflection questions | Every Friday by 4pm | `weekly-reviews/YYYY-Www.md` |
| `/qbr` | Quarterly business review — pipeline, MRR cohort, hiring decisions, the M3/M6/M9 trigger table | Last Friday of each quarter | `qbr/YYYY-Q{N}.md` |

---

## 4. Per-skill specs

For each skill: purpose, trigger conditions, inputs, outputs, trigger phrases (so Claude can auto-invoke), and skip conditions.

### `/cold-batch`
- **Purpose.** Produce N personalized cold-pitch drafts using the v3 anti-SaaS frame: *"You're paying [SaaS X] $Y/mo for [function]. We replace it with code you own, fixed fee, monthly retainer."*
- **Inputs.** `industry` (e.g. "indie restaurant"), `geography` (e.g. "Delray Beach"), `count` (default 8), optional `list_path` if you've already pulled real businesses.
- **Outputs.** A numbered markdown file with: subject + body + Loom suggestion + named-research instructions per draft. Each draft cites the specific SaaS the prospect likely pays for.
- **Trigger phrases.** "cold batch", "draft 10 cold emails for", "outreach round for".
- **Skip if.** Prospect list contains chains > 3 locations, or the geography is a 3rd market beyond PB/Poconos.

### `/proposal`
- **Purpose.** Draft a 1-page fixed-fee proposal that names the SaaS being replaced, the price, and the retainer ladder.
- **Inputs.** Client name, sprint type (visibility / menu / front-desk / bundle), discovery-call notes path.
- **Outputs.** `clients/{name}/proposal-{sprint}-{date}.md` — single page, public price, scope, timeline, Stripe link placeholder.
- **Trigger phrases.** "draft a proposal for", "send a scope to".
- **Skip if.** Client hasn't had a discovery call yet (route to `/discovery-prep` first).

### `/discovery-prep`
- **Purpose.** 20-min research dossier so Mel walks into the call already knowing what they pay for.
- **Inputs.** Business name, website URL, GBP URL (optional).
- **Outputs.** `clients/{name}/discovery-prep-{date}.md` — likely SaaS stack, monthly spend estimate, AI-search audit (does ChatGPT know they exist?), one named pain hypothesis, 5 questions Mel should ask.
- **Trigger phrases.** "prep me for the call with", "research before tomorrow's discovery".
- **Skip if.** Call is < 30 min away (insufficient time; produce abbreviated 1-page version).

### `/follow-up`
- **Purpose.** Stage-aware follow-up. Knows whether the prospect is post-discovery, post-proposal, or post-sprint, and uses voice appropriate to each.
- **Inputs.** Client log path (`clients/{name}/log.md`).
- **Outputs.** Appended to the log + a draft message file.
- **Trigger phrases.** "follow up with", "nudge {name}".
- **Skip if.** Prospect is < 7 days silent at any stage (no nag); or has explicitly said no.

### `/intake`
- **Purpose.** Tailored intake form for a sold client. Replaces the generic Google-form intake.
- **Inputs.** Client name, sprint type, optional industry tag.
- **Outputs.** `clients/{name}/intake.md` — sectioned: business basics, current SaaS stack (named line items + monthly spend), pain points, access credentials needed, success criteria, communication preferences.
- **Trigger phrases.** "create intake for", "send {name} the intake".
- **Skip if.** No signed proposal exists.

### `/sprint-ai-visibility`
- **Purpose.** End-to-end runner for the 5-day $750 sprint. Produces deliverables per day.
- **Inputs.** Client name, GBP URL, target queries (e.g. "best Italian restaurant Boca Raton").
- **Outputs.** Daily files Day 1–Day 5: audit, GBP optimization log, schema JSON-LD, NAP citation list, AI-search test results, dashboard, handoff doc + retainer offer.
- **Trigger phrases.** "run the visibility sprint for", "Day 1 of {name} visibility".
- **Skip if.** Client doesn't have a website yet (route to a Visibility prerequisite scope).

### `/sprint-menu-reviews`
- **Purpose.** End-to-end runner for the 1-week $1,500 sprint.
- **Inputs.** Client name, restaurant/B&B URL, FL allergen mode or Poconos amenity mode.
- **Outputs.** Single-source menu/amenity page draft, AI review-response rules in owner voice, GBP cleanup checklist, brand-voice doc, retainer offer.
- **Trigger phrases.** "run menu sprint", "menu+reviews for".
- **Skip if.** Client has > 3 locations.

### `/sprint-front-desk`
- **Purpose.** End-to-end runner for the 2-week $1,800 + $200/mo sprint.
- **Inputs.** Client name, current phone number, business hours, FAQ corpus, escalation rules.
- **Outputs.** Twilio config doc, LLM prompt, Cal.com booking config, escalation playbook, dashboard URL placeholder, owner training Loom outline.
- **Trigger phrases.** "front desk sprint for", "build receptionist for".
- **Skip if.** Client expects 24/7 human coverage (mismatch — refer to live answering service).

### `/case-study`
- **Purpose.** Convert a finished sprint into a published case study + a 90s Loom script.
- **Inputs.** Client name, sprint folder path, before/after metrics, owner consent flag.
- **Outputs.** `case-studies/{geo}/{vertical}/{name}.md` + `loom-script.md`.
- **Trigger phrases.** "write up the case study for", "ship the {name} story".
- **Skip if.** Owner hasn't signed off on attribution.

### `/workshop-prep`
- **Purpose.** Build the 75-min library/Chamber/coworking workshop with two real-business worked examples relevant to the geography.
- **Inputs.** Venue, date, expected attendee count, vertical focus (or "mixed").
- **Outputs.** `workshops/{date}-{venue}/agenda.md`, `slides.md`, `examples.md`, `cta.md`, `handout.md`.
- **Trigger phrases.** "prep workshop for", "build the {venue} deck".
- **Skip if.** Date is < 4 days out (use abbreviated version).

### `/postcard-wave`
- **Purpose.** Design a 2-step Poconos direct-mail wave — postcard, then signed letter T+3 weeks for non-responders.
- **Inputs.** Geography (Sullivan / Wayne / Pike / Monroe), volume (target 200–600), list source.
- **Outputs.** `outreach/postcards/{wave}/postcard.md`, `letter.md`, `list-targeting.md`, USPS cost estimate.
- **Trigger phrases.** "postcard wave for", "next mail wave".
- **Skip if.** Geography is Palm Beach (postcards work but letter ROI is lower; redirect to `/cold-batch` for PB).

### `/episode-prep`
- **Purpose.** Outline a podcast episode + show-notes scaffolding.
- **Inputs.** Episode topic, format (solo / interview / live build), runtime target.
- **Outputs.** `podcast/{ep-NNN}-{slug}/outline.md`, `show-notes.md`.
- **Trigger phrases.** "outline episode", "next ep on".
- **Skip if.** Already 5+ unrecorded episodes queued (you have a backlog problem, not a writing problem).

### `/newsletter-recap`
- **Purpose.** Compile the week's 4 episodes into a Friday newsletter with one essay-link, one client win, one CTA.
- **Inputs.** Week number (default current).
- **Outputs.** `newsletter/YYYY-Www.md`.
- **Trigger phrases.** "newsletter for the week", "Friday recap".
- **Skip if.** No new episodes shipped this week (write an "off-week note" instead, don't fake content).

### `/weekly-review`
- **Purpose.** Friday afternoon review ritual — Gap-and-Gain dashboard + 3 Sullivan/Hardy reflection questions.
- **Inputs.** Week number (default current); optional metrics file paths.
- **Outputs.** `weekly-reviews/YYYY-Www.md`.
- **Trigger phrases.** "weekly review", "wrap the week".
- **Skip if.** Already run this week (offer to revise instead).

### `/qbr`
- **Purpose.** Quarterly business review — pipeline, MRR cohort, hiring decisions, the M3/M6/M9 trigger table from the v3 plan.
- **Inputs.** Quarter (Q1/Q2/Q3/Q4), year.
- **Outputs.** `qbr/YYYY-Q{N}.md`.
- **Trigger phrases.** "quarterly review", "QBR for Q3".
- **Skip if.** Last QBR was < 75 days ago.

---

## 5. Roadmap — build order

The five fully-built skills (this delivery) are the ones that get used the most in the first 90 days. The next five build in month 3 once the first ones have produced enough usage data to refine them. The last five wait until month 6+.

### Build first (Month 1 — already shipped in this delivery)

| Skill | Reason |
|---|---|
| `/intake` | Used the day after every closed deal. Highest reuse. |
| `/cold-batch` | Used weekly during outreach waves. The first month is heavy on outreach. |
| `/sprint-ai-visibility` | Lowest-ticket sprint = first one sold = first one to systematize. |
| `/workshop-prep` | Workshops start in week 4. Without the skill the first one consumes a full week. |
| `/weekly-review` | Discipline forcing-function. Locks the Sullivan/Hardy cadence in from week 1. |

### Build at month 3 (after first 5 sprints sold)

| Skill | Reason |
|---|---|
| `/sprint-menu-reviews` | By M3 the second sprint type has been sold 2–3 times — enough to template. |
| `/sprint-front-desk` | Same logic; this one waits until the Twilio scaffolding repo is reusable. |
| `/discovery-prep` | Volume justifies it once you're taking 4+ discovery calls/week. |
| `/proposal` | Pairs with `/discovery-prep` — same trigger window. |
| `/postcard-wave` | First wave runs by hand in M1; M3 is when it becomes quarterly cadence. |

### Build at month 6+ (after the cadence is real)

| Skill | Reason |
|---|---|
| `/case-study` | Only useful once 5+ sprints have completed. |
| `/follow-up` | Pipeline is wide enough by M6 that auto-staging follow-ups starts paying. |
| `/episode-prep` | Founders write episodes themselves until M6. After that, formalize. |
| `/newsletter-recap` | Same. |
| `/qbr` | First QBR is end of Q1 — but the first one runs by hand to figure out the right structure, then the skill captures the structure for Q2 onward. |

---

## 6. Conventions across all GVC skills

Pulled from the source docs and locked in so every skill produces consistent artifacts.

1. **Plain language. Anti-SaaS frame.** Every output that touches a prospect or client says "we replace [named SaaS] with code you own." Never "AI consulting." Never "transformation." Never "platform."
2. **Public prices.** Every proposal/intake/case-study lists the price plainly: $750, $1,500, $1,800, $250/mo, $300/mo, $200/mo built-in.
3. **Local files, not SaaS.** Skills write to markdown files inside the repo. The only third-party tools the skills can mention as integrations are: Stripe (payment links), Cal.com (booking), Twilio (phone), the client's existing GBP/website. No new SaaS recommendations.
4. **Two-geography awareness.** Every skill that produces prospect-facing copy asks (or infers) which geography (`palm-beach` or `poconos`) and uses the appropriate trust-journey length, pricing tier, and cultural register (Worth Ave vs Main St Narrowsburg).
5. **No QR codes on Poconos artifacts.** USPS 2025 rural distrust. URL + phone only.
6. **Founder pairing is the brand.** Skills that produce content that mentions the firm always name both Matt and Melissa — neither alone.
7. **Refuse Bronze/Silver/Gold tiers.** If a skill catches itself producing a 3-tier pricing structure, it stops and emits one fixed price.
8. **Sullivan/Hardy default to Gain.** Anywhere a skill produces a status update, it leads with what shipped vs the start-of-week, not what's still missing.

---

## 7. What's not in this library (and why)

- **No CRM-ingestion skill.** GVC isn't running a CRM in year 1. `clients/{name}/log.md` is the CRM. If the founders adopt one later, the skills get one new helper, not 15 rewrites.
- **No "AI-audit-as-leadgen" skill.** Free-AI-Audit pop-ups are refused per the GTM doc. The audit lives inside `/discovery-prep` for prospects who've already booked, not as a top-of-funnel hook.
- **No SaaS spinoff scaffolding.** WikiFold stays free. No skills build product-as-SaaS structure.
- **No bookkeeping skill.** Goes to the fractional bookkeeper hire, not a Claude skill.
- **No social-media calendar skill.** Off-brand per `21`. Refused.

---

## 8. The five fully-built skills (delivered with this catalog)

- `/Users/fp/Desktop/good-vibes-coding/docs/strategy/2026-04-30-business-plan/playbooks/skills/intake.md`
- `/Users/fp/Desktop/good-vibes-coding/docs/strategy/2026-04-30-business-plan/playbooks/skills/cold-batch.md`
- `/Users/fp/Desktop/good-vibes-coding/docs/strategy/2026-04-30-business-plan/playbooks/skills/sprint-ai-visibility.md`
- `/Users/fp/Desktop/good-vibes-coding/docs/strategy/2026-04-30-business-plan/playbooks/skills/workshop-prep.md`
- `/Users/fp/Desktop/good-vibes-coding/docs/strategy/2026-04-30-business-plan/playbooks/skills/weekly-review.md`

To install all five globally:

```bash
mkdir -p ~/.claude/skills
cp docs/strategy/2026-04-30-business-plan/playbooks/skills/*.md ~/.claude/skills/
```

Restart Claude Code, type `/`, confirm the five appear in the list, and run one. The first invocation pays back 30+ minutes. The hundredth invocation runs the business.
