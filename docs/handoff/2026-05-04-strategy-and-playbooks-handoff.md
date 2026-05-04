# Good Vibes Coding — Strategy + Playbooks Handoff

**Date:** 2026-05-04
**Supersedes:** [`2026-04-20-agent-team-handoff.md`](./2026-04-20-agent-team-handoff.md) (preserved as historical reference)
**Reading time:** ~20 minutes. Skip to §13 for a first-30-minute checklist.

---

## 1. TL;DR

- The previous (April 20) handoff covered marketing-site polish. Since then, GVC has graduated to a full strategy + operations layer: validated thesis, market sizing, revenue model, cold-acquisition GTM, financial projections, podcast strategy, recipe book, operations playbook, Claude Code skills library, and an AI search visibility playbook. **The site is no longer the bottleneck — execution is.**
- **The bet, in one sentence:** *Stop renting your business from five SaaS companies. Own it once.* Sell three productized cold-conversion sprints ($750 / $1,500 / $1,800) that ladder into recurring retainers. Build via cold acquisition (local SEO + workshops + owned podcast) across two geographies (Palm Beach County FL + Narrowsburg/Poconos region NY/PA). Target **$20K MRR by month 9–10**.
- **PR #14 is open** ([github.com/zone17/good-vibes-coding/pull/14](https://github.com/zone17/good-vibes-coding/pull/14)) with 30+ strategy artifacts, the recipe book, the operations playbook, the Claude Code skills library, an AI-search-visibility playbook, and the v3 PowerPoint deck. Read this handoff, then read `23-business-plan-synthesis-v3.md`. Everything else is detail.

---

## 2. What's changed since the 2026-04-20 handoff

The April 20 handoff documented the marketing-site state (Phase 1 SEO foundation shipped; Phase 2 self-hosted fonts shipped; trust/copy work blocked on Matt). The work since then has moved up the stack:

1. **Marketing soft-refresh shipped to production** (PR #11–13).
   - Hero mission line corrected (`mission: "add value to the world"`).
   - Socials cluster restyled to circle-icons + Email pill (semantic `<ul><li>` markup, accessibility a11y-clean).
   - Channel cluster label tightened ("Or reach us here").
   - Soft messaging refresh — five surgical line edits across Hero subhead, Services subtitle, Mission ¶1, Process step 3, CTA reassurance — softly inject the AI-as-growth + access-wedge framing.
   - 9-artifact marketing-refresh research bundle produced (positioning, voice audit, copy variants, competitive landscape, etc.) and merged.
2. **Mel's business-setup runbook produced** (md/html/pdf trio, gitignored alongside the existing socials runbook).
3. **Strategy bundle v1** (9 artifacts) — thesis validation, Sullivan/Hardy operating philosophy, market sizing, revenue model, GTM, moats, financials, build-from-zero paths, business-plan synthesis.
4. **Strategy bundle v2** (8 artifacts) — podcast asset re-spawn (GTM v2, moats v2, financials v2, build-from-zero v2, podcast strategy, podcast economics, starter-revenue research, synthesis-v2).
5. **Strategy bundle v3** (5 artifacts) — major pivot driven by founder reality-check: dropped Mel-warm-network primary motion, dropped Path C SaaS spinoff, picked dual-geography cold-acquisition (PB + Poconos). Lower starter pricing ($750 / $1,500 / $1,800). Synthesis-v3 is the current source of truth.
6. **PowerPoint deck v3** (52 slides) built by surgical edits to the original Claude Design v2 deck + 3 new appended slides. Reproducible Python build script committed.
7. **Playbook layer** — recipe book (9 products full delivery specs), operations playbook (day/week/month rhythms, 10 lifecycle workflows, 32 anti-patterns), Claude Code skills library (15-skill catalog + 5 fully-built installable skills), AI search visibility playbook (top 5 methods).

All of #3 through #7 lives on branch `docs/site/business-plan-research` (PR #14, open).

---

## 3. The validated thesis (current source of truth)

Mark Cuban's April 21, 2026 X post — the AI implementation layer for SMBs — survives stress-testing in `01-thesis-validation.md`. **Two numbers got corrected:**

- **36.2M total US small businesses** (SBA 2025), not 33M. Convertible buyer pool ~3–5M (employer firms 2–50 employees, $200K–$5M revenue).
- **US implementation-services TAM is $20–45B today, $60–110B by 2028** — not the rhetorical "$10T" that one X commenter coined.

The 76% claim-use / 14% integrated gap (Goldman Sachs Feb 2026) is the empirical leg. The AI for Main Street Act (2026) legislatively names the gap and funds SBDC implementation training. **GVC has a clean 12-month window** before vertical SaaS bundling (Toast/ServiceTitan/Mindbody) and interface commoditization (GPT-6 / Claude 5 "describe your business" UX) pressure the model.

---

## 4. The recommended path (v3)

**Path A only** — stay 2-person, productize, no SaaS spinoff. Path C (WikiFold productization) explicitly deferred to Year 3+. Paths B (scale via fractional team), E (Media + Tools + Consulting flywheel), F (Acquirable Media) all evaluated and rejected for GVC specifically. WikiFold stays free as proof of capability, not a SaaS product.

**Walk-away values (v3):** Path A = $700K–$1.4M. Path C = $14M–$55M only if WikiFold productizes later (not the primary plan).

**Year-3 base case:** $612K revenue, $288K combined founder draws, 30% EBITDA margin, ~33-hour weeks, with one fractional ops/PM coordinator + one fractional bookkeeper + one Content+Ops VA on the roster. **Year-1 base ~$510K** (workshop sprint volume layers on top of recurring revenue).

**Year-5 SOM ceiling:** $1.8M–$2.4M revenue, 5–6 person team, $780K–$1M combined founder draw. That's 0.035% of SAM — tiny slice required to be life-changing.

No outside capital needed in any scenario. $30K operating reserve recommended.

---

## 5. The product portfolio (9 SKUs)

Full delivery recipes in [`playbooks/01-recipe-book.md`](../strategy/2026-04-30-business-plan/playbooks/01-recipe-book.md). Quick reference:

| # | Product | Sprint price | Retainer | Replaces | Geo | Repro |
|---|---|---|---|---|---|---|
| 1 | **AI Visibility Tune-Up** | $750 / 5 days | $250/mo Watch | Yext, BrightLocal | Both | 5/5 |
| 2 | **Menu + Reviews Lite** | $1,500 / 1 wk | $300/mo Hospitality Lite | Bloom + Birdeye + OpenMenu | Both | 5/5 |
| 3 | **AI Front-Desk** | $1,800 / 2 wks | $200/mo built-in | Goodcall / Numa / Rosie | Both | 5/5 |
| 4 | **Vacation Rental Direct-Booking** | $2,400 / 2 wks | $400/mo | Hostfully + Airbnb take | Pocs-led | 4/5 |
| 5 | **SOP Lite** | $2,200 / 2 wks | $300/mo wiki keep-alive | Notion AI / Trainual | Both | 4/5 |
| 6 | **Restaurant Full Stack (bundle)** | $3,500 / 3 wks | $500/mo | Yext + Birdeye + OpenMenu + Goodcall | FL-led | 4/5 |
| 7 | **B&B Stack Consolidator** | $7,500 / 3 wks | $850/mo | (multiple) | Pocs post-trust | 3/5 |
| 8 | **Wedding-Venue Inquiry System** | $6,500 / 3 wks | $600/mo | (multiple) | Pocs post-trust | 3/5 |
| 9 | **Outfitter Booking + Waiver Modernizer** | $5,500 / 3 wks | $700/mo | (multiple) | Pocs post-trust | 3/5 |

**Cold-conversion ceiling is ~$3K** for first-touch; products 7–9 are *post-trust* offers — sold only after 1–2 reference customers exist in a town and physical presence is established.

**Anti-SaaS frame on every product:** *"You're paying [SaaS X] $Y/mo for [function]. We replace it with code you own — one fixed up-front fee, small monthly retainer to keep it sharp."* Never lead with "AI consulting."

---

## 6. The cold-acquisition GTM motion

Full playbook in `22-cold-acquisition-gtm.md`. Channel ranking:

| # | Channel | Founder fit | Time-to-result |
|---|---|---|---|
| 1 | Local SEO + GBP (two SABs: PB + Upper Delaware/Poconos) | Matt | 3–6 months |
| 2 | Workshop circuit (libraries / Chambers / coworking, 2/geo/month) | Both | 4–8 weeks |
| 3 | Owned podcast + newsletter recap | Both | 8–16 weeks |
| 4 | Chamber/BNI/Rotary engagement | Both | 6–12 weeks |
| 5 | Direct mail (Poconos only — 2-step postcard → letter) | Matt designs, Mel signs | 4–8 weeks |
| 6 | Cold direct outreach (email + LinkedIn + Loom) | Both | 4–8 weeks |
| 7 | Sponsored events / festivals / fairs | Both | seasonal |
| 8 | Geo-targeted Google / Meta ads | Matt | 2–4 weeks |

**Workshop circuit is the load-bearing channel** — 75-min library/Chamber format, ~$60K/mo run-rate by M6 if conversion benchmarks hold.

**Multi-market reality:** 2-week PB / 2-week Poconos rotation, 60/40 PB lean through M6. **3 residency weeks/year in Poconos non-negotiable** (Feb chamber circuit, Memorial Day, mid-September). Part-time field rep $1,500/mo at month 12 for Poconos market sustainability.

**Trust journey is geography-specific:** Palm Beach = 5 touches / 3–6 weeks; Poconos = 7–8 touches / 6–14 weeks. **Rural buyers call before they Calendly.**

**Warm referrals are upside, not plan.** Mel's hospitality network and Matt's eng peers count when they happen, but the ramp doesn't depend on either.

---

## 7. The podcast as a known asset

Daily ≤15-min co-hosted news show ("AI as augmentation/restoration" beat) at `/Users/fp/Desktop/good-vibes-coding-podcast/`. **5+ episodes produced before this strategy round saw it.**

**Per `15-podcast-strategy.md`:**
- Cadence recommendation: **4×/week (Mon–Thu) + Friday short**, not daily — recovers ~6 hr/wk vs daily.
- Format: story-owner + reactor (Format 2), not equal-time alternating dialogue.
- Cold-open: 12-second Mel-led number-first hook.
- 35-second voice-block cap.
- Sign-off ritual lock candidate: *"Good vibes only."*
- Editorial framework name candidate: **"The Augmentation Lens"** — without a named frame, the editorial position is copyable in 6 months.

**Per `12-moats-v2-with-podcast.md`:** the podcast is **NOT a structural moat by itself** — conditional moat at episode ~150 only if four conditions hold (narrowed editorial position, real founder-pairing chemistry, <8 founder-hours/wk by M6, audience routed into the GVC funnel).

**Per `13-financials-v2-with-podcast.md`:** ~17 hr/wk founder block DIY observed. **Fractional podcast editor at M6–9 is the load-bearing gate** ($2,500/mo). Without it, the show is founder-grinding. Y3 base $756K with podcast (vs $612K without; ~$78K extra EBITDA + ~6 hr/wk less founder production time).

**Honest Y1 podcast attribution math:** at 1,200 listeners/ep base case → 2–4 direct calls/mo + 3–6 assist conversions → **~$150–250K Y1 revenue (25–35% of base-case Y1 target).** Material, not transformative.

**Kill criterion:** if at month 12 retainer MRR is below $15K and listeners are below 5K, **pause the podcast** — don't double down.

**Refuse podcast sponsorship before month 18 regardless of offer size.**

---

## 8. AI search visibility (the new SEO)

Full playbook in `playbooks/04-ai-search-visibility.md`. Shipped 2026-05-01.

**The discipline is real, the acronyms are not.** GEO (Generative Engine Optimization) has the only academic origin — Aggarwal et al., Princeton/Georgia Tech/AI2/IIT Delhi (KDD 2024) — content edits can lift answer-visibility up to 40%. LLMO, AEO, "AI SEO" are practitioner re-skins.

**Top 5 methods, ranked:**

1. **Entity clarity** — GBP + Wikidata + consistent NAP. Free. Already in Recipe 1.
2. **Chunk-friendly content** — BLUF answers (40–60 words at top), owner-voice FAQ, clean headings, tables. Already in Recipe 1.
3. **Earned third-party citations** — Reddit, local press, niche directories. **NOT in Recipe 1 yet.** Best v2 retainer add-on.
4. **Attribute-rich schema** — LocalBusiness + FAQPage + vertical type. Most contested method — the reconciling story is *schema feeds retrieval, not generation*. Already in Recipe 1.
5. **Bing infrastructure** — Seer Interactive correlation: **87% match between SearchGPT citations and Bing top-20 organic.** ChatGPT visibility is largely a Bing problem. **NOT in Recipe 1 yet.** Strongest single Day-3 sprint upgrade.

**Recipe 1 v2 upgrades the playbook recommends:**
- Promote **Bing Places + Bing Webmaster Tools** to a primary Day 3 deliverable.
- Add an **earned-mention starter** to Day 4 + bake into the Watch retainer (Reddit answer in r/[city], one local-press pitch, one niche-directory submission per month).

**Defensible answer to "is this just SEO?"** — *No. We make a business legible to a retrieval system that no longer reads pages the way Google did in 2014.*

**Honest caveat that's load-bearing for the pitch:** AI search is unstable month-over-month. The sprint is built to be **re-runnable** — that's the actual product, not a permanent fix. The $250/mo Watch retainer is the real value capture, not the $750 sprint.

---

## 9. Operational rhythms

Full playbook in `playbooks/02-operations-playbook.md`. The shape:

- **Standard 7-day week** with 3 outcomes + 1 anti-pattern per day.
- **Hour-by-hour schedules** for Matt and Mel across M1 (cold launch) / M4 (workshop circuit running) / M9 (VA on-board, $20K MRR closing).
- **Monthly themes M1–M9** with theme, top-3 outcomes, hire decision, KPI, decision-point, anti-patterns, geographic mix.
- **Quarterly rhythm** — last-Friday-of-quarter QBR off-site, monthly Gap-and-Gain, mid-December annual planning weekend.
- **10 lifecycle workflows** — lead capture → discovery → sprint sale → kickoff → handoff → retainer rhythm → workshop production → direct mail → podcast → case study.
- **Tooling stack ~$280/mo through M5:** Folk for CRM ($50/mo), Linear (free) for PM, Buttondown for newsletter, plain markdown in `/docs` for SOPs. Anti-bloat picks throughout.
- **12 KPIs** with M3/M6/M9/M12 targets.
- **32 anti-patterns** across behavioral / operational / strategic.

**First three Whos (revised v3 order):**
1. Fractional bookkeeper — M1–2 (~$300–600/mo)
2. **Content + Ops VA** — M2–3 (~$2,500–3,000/mo) — pulled forward in v3 to enable workshop circuit
3. Fractional podcast editor — M6–9 (~$2,500/mo, conditional on podcast-attributable leads ≥1 by M6)

Plus: **Local Poconos field rep ($1,500/mo, part-time) at month 12 — non-negotiable.**

---

## 10. Claude Code skills (installed/installable)

Full catalog in `playbooks/03-claude-code-skills-library.md`. **5 skills are fully built and ready to install** at `playbooks/skills/`:

```bash
mkdir -p ~/.claude/skills && cp docs/strategy/2026-04-30-business-plan/playbooks/skills/*.md ~/.claude/skills/
```

| Skill | Purpose |
|---|---|
| `/intake` | Generate a tailored client intake doc |
| `/cold-batch` | Generate a batch of cold-pitch outreach for an industry+city pair |
| `/sprint-ai-visibility` | Run the AI Visibility Tune-Up sprint end-to-end (5-day plan) |
| `/workshop-prep` | Build a 75-min "AI for Small Business" workshop tailored to venue + audience |
| `/weekly-review` | Friday review ritual with Sullivan/Hardy Gap-and-Gain framing |

Catalog has **10 more skills** to build — `/proposal`, `/discovery-prep`, `/follow-up`, `/sprint-menu-reviews`, `/sprint-front-desk`, `/case-study`, `/postcard-wave`, `/episode-prep`, `/newsletter-recap`, `/qbr` — sequenced into M1 / M3 / M6+ tranches.

All skills write to local markdown under `clients/`, `outreach/`, `workshops/`, `weekly-reviews/`. **No SaaS state. Anti-SaaS thesis applies internally too.**

---

## 11. The deck

PowerPoint v3 lives at `docs/strategy/2026-04-30-business-plan/deck/GoodVibes-Coding-Business-Plan-v3.pptx` (52 slides). Built by surgical edits to the original Claude Design v2 deck + 3 appended new slides (tagline / two geographies / $20K MRR ramp). Reproducible Python build script at `deck/scripts/build_v3_pptx.py`.

**Polish gap noted:** the 3 appended new slides (50–52) use a simpler text-only layout vs the rest of the deck since I couldn't clone the existing master programmatically. They're functional but a 5–10 minute manual polish in PowerPoint or Keynote will bring them up to deck-master parity. The original v2 .pptx is also in the folder for reference.

---

## 12. Site state (what's live on production)

`goodvibes-coding.com` is currently running:

- Hero subhead leads with **growth + access wedge** (your version: *"We use AI to help small businesses grow by building tools and agents..."* with *"no in-house AI team required"* at the end).
- Services subtitle softly names the no-AI-team gap.
- Mission ¶1 quietly mentions AI-as-infrastructure-only-the-biggest-can-use-well.
- Process step 3 leads with team training.
- CTA reassurance line is educational, not transactional.
- Channel cluster shows circle-icons (LinkedIn + Phone) + Email pill. IG / GitHub commented in the HTML waiting for the URLs.
- Mission line in the hero code block: `mission: "add value to the world"`.

**Site has NOT been updated to reflect v3 yet.** When v3 ships, the homepage refresh will:

- Lead with the new tagline (*"Stop renting your business from five SaaS companies. Own it once."*).
- Publish three productized services with prices ($750 / $1,500 / $1,800).
- Add a "Two geographies" line.
- Probably swap the Hero subhead to be sharper about the SaaS-replacement angle.

That's a separate code PR off `main`, not yet drafted.

---

## 13. First-30-minute checklist for the incoming agent

1. **Read this handoff in full** (you're doing it).
2. **Read `docs/strategy/2026-04-30-business-plan/23-business-plan-synthesis-v3.md`** — the master strategy doc. ~3,500 words. Skim §13 (diff vs v2) and §6 (30-day roadmap).
3. **Read `docs/strategy/2026-04-30-business-plan/playbooks/01-recipe-book.md`** — what we sell. Recipe 1 (AI Visibility Tune-Up) is the load-bearing one to know cold.
4. **Read `docs/strategy/2026-04-30-business-plan/playbooks/02-operations-playbook.md`** — how we run.
5. **Skim `docs/strategy/2026-04-30-business-plan/playbooks/04-ai-search-visibility.md`** — the technical ground for Recipe 1.
6. **Skim PR #14** ([github.com/zone17/good-vibes-coding/pull/14](https://github.com/zone17/good-vibes-coding/pull/14)) — see the full diff.
7. **Check `git log --oneline -20`** for recent commits.
8. **Visit `goodvibes-coding.com`** — see what's live (still v2-of-soft-refresh, not v3).
9. **Before doing any new work:** post §14 (asks blocking Matt/Mel) to them as a single message. Don't batch with other questions. Don't guess facts.

---

## 14. Open questions blocked on Matt and Mel

Consolidated to seven from the v3 synthesis §12 (down from 17 in v2):

1. **Pricing commit** — are the v3 prices in §5 ($750 / $1,500 / $1,800 starters; $250 / $300 / built-in $200 retainer tiers) live-publishable?
2. **Workshop venue commits** — which library / Chamber / coworking for the first PB workshop? Which for the first Poconos workshop?
3. **First Poconos residency week** — when? Recommendation: late February 2027 or earlier.
4. **Direct mail list commit** — 200-postcard first wave + letter follow-up. Budget ~$300 first wave / ~$1,000 first month.
5. **Two Google Business Profiles** — Service-Area Business setup OK with both founders' addresses?
6. **VA hiring commit** — $2,500–$3,000/mo at M2–3. Confirm budget tolerance.
7. **Tagline lock** — *"Stop renting your business from five SaaS companies. Own it once."* OK as the cross-market headline?

Plus from the prior April 20 handoff (still open):
- Mel's named hospitality venues for the team bio.
- Matt's named prior companies for the team bio.
- Mel's LinkedIn URL.

Plus from the v3 podcast strategy:
- Cadence commit (4×/week vs daily).
- Editorial framework name lock ("The Augmentation Lens" or alternative).
- Sign-off ritual lock ("Good vibes only" for 8 weeks?).
- Podcast editor budget commit ($2,500/mo from M4–6).

---

## 15. Recommended next moves (ranked)

1. **Merge PR #14 to main** — the 30+ strategy artifacts should land on main so they're the source of truth, not a branch.
2. **Get the seven §14 open questions answered** by Matt and Mel.
3. **Ship the homepage refresh PR off main** (separate code PR) — new tagline + three products + prices + dual-geography line.
4. **Apply the AI Search Visibility v2 upgrades to Recipe 1** — promote Bing Places to Day 3, add earned-mention starter to Day 4 + retainer.
5. **Install the 5 Claude Code skills locally** — start using them in real work this week. Surface bugs / improvements as they emerge.
6. **First two workshop venues booked** for May 2026 — one PB, one virtual-as-Pocs-substitute (until Mel can travel).
7. **First two Google Business Profiles claimed** as Service-Area Businesses.
8. **Polish the 3 appended deck slides** (50–52) in PowerPoint to match the deck-master layout.

---

## 16. Voice and anti-pattern reminders for the next agent

These are non-negotiable across every artifact. Detailed list in `playbooks/02-operations-playbook.md` Part 8.

- **Plain language.** No SaaS-template vocabulary ("unlock," "supercharge," "leverage," "transform your business," "powered by AI"). No three-verb headlines.
- **First-person plural "we."** Named humans (Matt + Mel) where credibility helps. Never "our team of experts."
- **Anti-SaaS framing on every product.** Each offering names the SaaS being replaced and the dollar amount being saved.
- **Never lead with "AI consulting."** Lead with "we help you stop paying for SaaS that doesn't fit."
- **No fake stats.** No "trusted by 1000+ teams." No invented client names. (Pattern #134 in the global common-solutions.md.)
- **No stock photography.** Real photos of real people only.
- **No customer-service chatbots.** 88% of customers prefer humans, 4× failure rate.
- **No multi-tier subscriptions** (Bronze/Silver/Gold templates). Off-brand.
- **No "AI for AI's sake" pitches.** If AI isn't the right answer, say so on the discovery call.
- **No outside capital. No equity / rev-share. No relocation. No third geography talk before M9.**
- **Refuse podcast sponsorship before M18 regardless of offer size.**
- **Branch discipline:** never commit or push on `main`. Use `feat/site/*`, `fix/site/*`, `docs/site/*`, `perf/site/*`. Hook-blocked.

---

## 17. Key file index

**Strategy (the master plan):**
- [`docs/strategy/2026-04-30-business-plan/23-business-plan-synthesis-v3.md`](../strategy/2026-04-30-business-plan/23-business-plan-synthesis-v3.md) — current source of truth.
- [`docs/strategy/2026-04-30-business-plan/18-business-plan-synthesis-v2.md`](../strategy/2026-04-30-business-plan/18-business-plan-synthesis-v2.md) — v2 (superseded by v3 but useful for diff context).
- [`docs/strategy/2026-04-30-business-plan/09-business-plan-synthesis.md`](../strategy/2026-04-30-business-plan/09-business-plan-synthesis.md) — v1.

**Playbooks (the execution layer):**
- [`docs/strategy/2026-04-30-business-plan/playbooks/README.md`](../strategy/2026-04-30-business-plan/playbooks/README.md)
- [`01-recipe-book.md`](../strategy/2026-04-30-business-plan/playbooks/01-recipe-book.md) — what we sell.
- [`02-operations-playbook.md`](../strategy/2026-04-30-business-plan/playbooks/02-operations-playbook.md) — how we run.
- [`03-claude-code-skills-library.md`](../strategy/2026-04-30-business-plan/playbooks/03-claude-code-skills-library.md) — how to systematize.
- [`04-ai-search-visibility.md`](../strategy/2026-04-30-business-plan/playbooks/04-ai-search-visibility.md) — the technical foundation of Recipe 1.

**The deck:**
- [`docs/strategy/2026-04-30-business-plan/deck/GoodVibes-Coding-Business-Plan-v3.pptx`](../strategy/2026-04-30-business-plan/deck/) — current.
- `GoodVibes-Coding-Business-Plan-v2.pptx` — original Claude Design export (v2-anchored), reference.
- `scripts/build_v3_pptx.py` — reproducible v2 → v3 transform.

**Strategy underlying research (reference depth):**
- `01-thesis-validation.md` through `09-business-plan-synthesis.md` — v1 layer.
- `11-gtm-v2-with-podcast.md` through `17-starter-revenue-activities.md` — v2 layer (podcast asset + starter revenue).
- `19-south-florida-market.md` through `22-cold-acquisition-gtm.md` — v3 layer (cold-acquisition + dual-geography).

**Marketing-refresh research (upstream context):**
- `docs/research/2026-04-28-marketing-refresh/` — 9 artifacts on the SMB AI market and brand positioning.

**Prior handoff (historical reference):**
- [`docs/handoff/2026-04-20-agent-team-handoff.md`](./2026-04-20-agent-team-handoff.md) — what the project state was before this strategy round.

**Roadmap plan (now partly superseded):**
- [`docs/plans/2026-04-17-001-elite-marketing-site-roadmap.md`](../plans/2026-04-17-001-elite-marketing-site-roadmap.md) — the original site roadmap. Many units are still valid but the prioritization is superseded by v3.

**Top-level docs:**
- [`README.md`](../../README.md) — stack, infrastructure, contacts.
- [`social-media-setup.md`](../../social-media-setup.md) — gitignored. Mel's social accounts setup.
- [`mel-business-setup.md`](../../mel-business-setup.md) — gitignored. Mel's full business operations runbook.

---

## 18. Compound engineering conventions (unchanged)

- `docs/plans/YYYY-MM-DD-NNN-<slug>.md` — living plans with Requirements Trace + Implementation Units.
- `docs/research/YYYY-MM-DD-<slug>/` — frozen research bundles.
- `docs/strategy/YYYY-MM-DD-<slug>/` — strategy + playbooks bundles.
- `docs/handoff/YYYY-MM-DD-<slug>.md` — handoff documents like this one.
- `docs/solutions/` — (not yet used on this repo) compound-style solution writeups after novel fixes.

When you finish a non-trivial unit, consider adding a compound solution writeup if the work involved a novel pattern worth preserving for the next agent.

---

**Questions, gaps, or new context:** append to this doc (don't start a new handoff until material changes — e.g., v3 ships to production, or a major strategic pivot lands). Date-stamp your edits.
