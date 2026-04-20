# Good Vibes Coding — Agent Team Handoff

**Date:** 2026-04-20
**Handoff from:** Prior agent (implementation + research synthesis sessions through 2026-04-17 → 2026-04-19)
**Reading time:** ~15 minutes. Skip to §11 for a first-30-minute checklist.

---

## 1. TL;DR

- **Project:** Marketing landing page for Good Vibes Coding — AI consulting for small businesses, run by Matt Wollschlager (engineering) and Melissa (hospitality-ops). Live at [goodvibes-coding.com](https://goodvibes-coding.com).
- **Stack:** Pure HTML + CSS + a tiny JS block. No framework, no build step. Hosted on Vercel. Domain on Squarespace, email on Google Workspace.
- **Status:** Phase 0 (foundation) + most of Phase 1 (SEO) + part of Phase 2 (self-hosted fonts) shipped. Trust/copy work blocked on Matt.
- **Strategic frame:** We chose **"Playbook B"** — the quiet, honest, editorial boutique-consultancy pattern (Basecamp, Fathom, Kalzumeus, Sivers, Sierra, Anthropic). Explicitly NOT the loud Linear/Vercel/Stripe SaaS playbook. This framing matters for every design and copy decision. See §4.
- **Living plan:** [`docs/plans/2026-04-17-001-elite-marketing-site-roadmap.md`](../plans/2026-04-17-001-elite-marketing-site-roadmap.md) — 37 implementation units, 19 requirements, 4 phases. Check off boxes as you ship.

---

## 2. Who & what

**The business:**
- 2-person AI consulting shop. Matt (25yr engineering leader, "AI & Engineering Leadership") + Melissa ("Business Strategy & Operations," two decades in NYC/SoFL hospitality).
- Target ICP: small businesses and entrepreneurs tired of paying too much for software and doing too much by hand. Revenue band implied: ~$200K–$5M annual.
- Revenue model: AI automation, custom tools replacing expensive SaaS, AI agents for operations, platform/infra engineering, MVP builds, community tech.
- Primary conversion: booked 30-min Calendly call → discovery → paid engagement.

**Operational assets currently present:**
- Landing page at `index.html` (single page, ~440 lines)
- WikiFold (free tool at wiki-fold.com) — acts as competence proof
- Phone: (561) 425-9119 (South Florida)
- Email: hello@goodvibes-coding.com
- Matt's LinkedIn: https://www.linkedin.com/in/mwollsch/
- Team photo, Matt headshot, Melissa headshot (all grayscale JPEGs)

**Known gaps in operational assets (do NOT guess these — ask Matt):**
- Melissa's LinkedIn URL (not on site yet)
- Specific prior companies for Matt + specific venues for Melissa (needed for credibility — see §7)
- Pricing ranges Matt is willing to publish
- GitHub org `goodvibescoding` (mentioned in `social-media-setup.md` but not yet created)
- Newsletter signup / writing section (doesn't exist)

**Cultural defaults (voice baseline):**
- First-person plural "we" — never "our team of experts"
- Plain language, no AI hype vocabulary
- Anti-sales — "no pressure, no pitch deck"
- Honest about being a 2-person shop; treats it as a feature, not a hedge
- No fake stats, stock photos, purple gradients, or enterprise theater (Matt is militant about this — it's the #134 pattern in `docs/solutions/patterns/common-solutions.md`)

---

## 3. Current state of the site (what's live as of 2026-04-20)

### Shipped (and in production)

**Phase 0 — Foundation:**
- Single-page site with sections: Hero, Services (6 cards), Mission, Process (3 steps), Free Tools, Team, CTA, Footer, sticky mobile CTA
- OKLCH color system, CSS layers, scroll animations via IntersectionObserver
- Brand mark: teal `</>` rounded square
- Matt's LinkedIn linked from his team card

**Phase 1 — SEO/discoverability (U1–U9 of the roadmap):**
- Open Graph + Twitter Card meta (validator-clean: title 52 chars, description 125 chars)
- Canonical URL
- Static OG images: `og.png` (1200×630) and `og-square.png` (1200×1200), both with a teal "Book a free call →" CTA pill, rendered via headless Chrome with real DM Serif Display + DM Sans
- JSON-LD `@graph` with `Organization` + `ProfessionalService` (areaServed: South Florida)
- `robots.txt` with explicit allow for GPTBot, ChatGPT-User, OAI-SearchBot, ClaudeBot, Claude-Web, PerplexityBot, Perplexity-User, Google-Extended, Applebot-Extended, CCBot
- `sitemap.xml` (homepage only)
- Vercel Web Analytics + Speed Insights (enabled by Matt in dashboard)
- Favicon set: `favicon.ico` (multi-size), `favicon.svg`, `apple-touch-icon.png` (180×180), `icon-192.png`, `icon-512.png`, `site.webmanifest`, `theme-color` meta

**Phase 2 — Performance (partial):**
- **U24 shipped:** self-hosted DM Serif Display + DM Sans as 8 WOFF2 files in `/fonts/`, 8 `@font-face` declarations with `unicode-range` subsetting, 3 `<link rel="preload">` hints. Google Fonts dependency fully removed. Expected LCP win: 200–400ms.

### Not shipped yet
See [roadmap](../plans/2026-04-17-001-elite-marketing-site-roadmap.md) for the full list. Key pending items summarized in §6.

---

## 4. Strategic frame — **READ THIS BEFORE DOING ANY DESIGN OR COPY WORK**

We did 4 parallel research streams (design benchmarks, conversion optimization, SEO/tech, trust signals) and synthesized the output in [`docs/research/2026-04-17-elite-marketing-site-research.md`](../research/2026-04-17-elite-marketing-site-research.md). The critical finding:

**There are two elite-site playbooks, and we deliberately chose the quieter one.**

### Playbook A — the loud one (NOT us)
Linear, Vercel, Stripe, Anthropic's product pages (not the research pages), Clerk, Raycast.
- Neon accents, true-black dark mode, gradient shaders
- Product-as-hero with dimensional lit component previews
- Cursor trails, hover magnetism, scroll-linked shader gradients
- "Trusted by" enterprise logo clouds
- Technical-performance bragging ("50ms cold start," "99.99% uptime")
- Optimized for venture-scale conversion funnels

Why this is wrong for Good Vibes: it fights the mission. Matt sells plain language, honesty, and two actual humans. Playbook A signals "we're a platform, we're fast, we're technical" — not "we're two people who will tell you the truth."

### Playbook B — the quiet one (us)
Basecamp / 37signals, Fathom Analytics, Sierra.ai (boutique AI consultancy), Anthropic's research/company pages (editorial serif/sans), Kalzumeus (Patrick McKenzie), Derek Sivers, Paul Jarvis, Nat Eliason.
- Editorial typography (serif display + sans body, with italic emphasis)
- Warm palette with a single confident accent (ours is teal `#0ca18d`)
- Real photos of real people, not stock imagery or illustrations
- Pricing published on the page
- Process transparency ("Day 1 we do X, Week 1 we ship Y")
- Anti-sales voice ("no pitch, no pressure, if we're not a fit we'll tell you")
- Newsletter-first / essay-first distribution, not SEO pillar-content grind
- Free tools as competence proof, not case-study theater
- Small team as a *feature*, not a hedge

Why this fits Good Vibes: every differentiator Matt and Melissa claim (people over profit, honesty over hype, community over competition) maps 1:1 onto how these shops operate. We can credibly execute Playbook B; most competitors can't, which is exactly why they're stuck on A.

### Practical consequences for the next agent
- **When designing** anything new — hero visual, section layout, imagery — check yourself against Fathom/Sierra/Basecamp, not Linear/Vercel. If your reference image involves neon or gradient blobs, you're on the wrong playbook.
- **When writing** anything new — copy, FAQ, CTA — read it back in the voice of "two humans who will tell you the truth." If it sounds like it came from a SaaS template ("Unlock the power of AI," "Supercharge your workflow"), rewrite.
- **When optimizing** — distinguish trust-optimizing moves (pricing transparency, anti-sales copy, process transparency) from conversion-rate-optimizing moves (exit-intent popups, urgency timers, A/B tested hero variants). The former fit; the latter don't.

---

## 5. Roadmap status snapshot

Full detail: [`docs/plans/2026-04-17-001-elite-marketing-site-roadmap.md`](../plans/2026-04-17-001-elite-marketing-site-roadmap.md)

| Phase | Units | Shipped | Blocked | Remaining |
|-------|-------|---------|---------|-----------|
| 0 — Foundation | 4 | 4 | 0 | 0 |
| 1 — SEO/tech (U1–U10) | 10 | 9 | 1 on Matt (U10 Plausible signup) | 0 |
| 1 — Trust/copy (U11–U16) | 6 | 0 | Most blocked on Matt | 6 |
| 2 — Proof stack (U17–U21) | 5 | 0 | Blocked on Matt (video, pricing, sample builds) | 5 |
| 2 — Friction (U22–U23) | 2 | 0 | Partial signup needed | 2 |
| 2 — Speed (U24–U26) | 3 | 1 (U24) | 0 | 2 |
| 2 — Indexing (U27–U28) | 2 | 0 | 10-min Matt tasks | 2 |
| 3 — Content SEO (U29–U32) | 4 | 0 | — | 4 (defer; see §9) |
| 4 — Design craft (U33–U37) | 5 | 0 | U33 needs creative direction | 5 |

**Reordering per mission fit (applied 2026-04-19):** U18 (pricing transparency) is now the highest-leverage single item in the backlog. See §6 for the recommended sequence.

---

## 6. Recommended work order (next ~2 weeks)

This order reflects the mission-fit review from 2026-04-19. It intentionally diverges from the raw roadmap in places. **Do this first, unless Matt says otherwise:**

### Batch A — Voice PR (can do solo, needs Matt's approval on copy)
Bundle these three into one PR titled "Voice: anti-sales, disqualification, pricing-range placeholder":
1. **U16** — Anti-sales CTA copy rewrite. Replace "No obligation. Pick a time that works for you." on the final CTA with something closer to: "No pitch. No pressure. If AI isn't the right fit for your business, we'll tell you in the first 10 minutes — and point you toward something that is." Tone match: honest operator, not SaaS copywriter.
2. **U15** — Disqualification block. Add a small section above the final CTA titled "Is this for you?" with two short columns: "Good fit:" (revenue band, pain signal) and "Not a fit:" (enterprises, chatbot-for-sake-of-it, etc.). This is the single most *brand-signalling* addition you can make — saying who we *won't* work with is the highest-trust move in Playbook B.
3. **U18 scaffold** — A pricing block using *ranges* Matt signs off on, e.g. "Pilots from $X. Monthly engagements from $Y. Fixed-scope audits around $Z." If Matt isn't ready on numbers, ship the section structure with "Pricing details → book a call" as placeholder and Matt fills in later.

### Batch B — Trust/identity (needs Matt input)
Do NOT ship these until Matt provides the facts. Asking for facts you don't have is the only fast path. See §7.
4. **U11** — Add Melissa's LinkedIn URL to her team card.
5. **U12** — Replace "25 years" / "two decades" with named prior companies and named venues.

### Batch C — Objection handling
6. **U13 + U14** — 6-question FAQ section + `FAQPage` JSON-LD mirroring it. Draft the questions; Matt + Melissa write the answers in their voice. Don't let the agent write the answers — that's where voice drift happens fastest.

### Batch D — Measurement + indexing
7. **U27 + U28** — Submit sitemap to Google Search Console and Bing Webmaster Tools. 10 minutes for Matt.

### Batch E — Solo perf work (no blockers)
8. **U25** — Convert `team.jpg`, `matt.jpg`, `melissa.jpg` to AVIF + WebP with `<picture>` fallback.
9. **U26** — CSS animation INP audit (`will-change`, transform-heavy rules).

### Batch F — Proof stack (slow-burn, Matt-led)
10. **U17** — 60–90s iPhone Loom of Matt + Melissa. "Why we started this, who we refuse to work with." One afternoon. Highest-leverage trust asset once it exists.
11. **U20** — Sample Builds section (2–3 Loom walkthroughs of real AI workflows).
12. **U21** — Create `github.com/goodvibescoding`, open-source one utility from WikiFold.

### Batch G — Design craft (discuss direction before starting)
13. **U33** — Replace the fake-code hero visual. Per §4, direction should be either:
    - an editorial typography moment (oversized serif pull-quote, Anthropic/Sierra style), OR
    - a warm photo of Matt + Melissa in a workspace (not stock, not staged), OR
    - a dimensional WikiFold screenshot (subtle, not neon-lit)
    **Do NOT ship a runnable-code hero or a gradient-blob hero.** Both violate Playbook B.
14. U34 — compress 6-card service grid to 3 + "and more," or narrate through one outcome-first story.
15. U35 — micro-motion (hover magnetism on CTAs, staggered reveal on scroll).
16. U36 — typography rhythm audit against Sierra/Fathom.

### Explicitly deferred (revisit in 6–12 months)
- U10 (Plausible) — only if Matt wants a second analytics source; Vercel's is sufficient.
- U23 (newsletter) — start only after Matt commits to actually writing one post/month.
- U29, U30, U32 (multi-page service routes, location page, 6–10 pillar posts) — valid tactics but fight the mission tension. Revisit when organic search matters more than it does today.

---

## 7. What's blocked on Matt (ask for these first)

When you pick up this project, your first message to Matt should be a request for these facts. Do NOT guess or invent any of them — it's the #1 way to violate the brand.

1. **Melissa's LinkedIn URL.**
2. **3–5 named prior companies for Matt** (verifiable on his LinkedIn). Context: "formerly at X, Y, Z" is far more credible than "25 years of experience."
3. **3–5 named NYC/SoFL venues or brands Melissa ran/consulted for.** Same reason.
4. **Pricing ranges Matt will publish** (even approximate): pilot range, monthly engagement range, fixed-scope audit price.
5. **6 real answers to the FAQ** (draft the questions for Matt/Melissa to answer):
    1. How much does this cost?
    2. I've been burned by an agency before — how are you different?
    3. Is this a fit for my business?
    4. What if AI isn't the right answer for us?
    5. How fast can you start, and what does the first month look like?
    6. What happens to my data / client data?
6. **"Good fit / not fit" criteria for U15 disqualification block.** Revenue band? Industry? Pain-signal? Anti-examples?
7. **Creative direction for U33 hero visual** — which of the three §6 options resonates.
8. **Newsletter commitment (yes/no).** Don't build U23 without a yes.

Stash answers under `docs/inputs/matt-answers-YYYY-MM-DD.md` when received.

---

## 8. Operational norms

### Git + branch discipline

**Required by hooks, not optional:**
- NEVER commit or push on `main`. Hard-blocked by `branch-discipline.sh`.
- Create feature branches: `feat/site/<slug>`, `fix/site/<slug>`, `docs/site/<slug>`, `perf/site/<slug>`. Squad prefix is always `site`.
- Do NOT force-push, do NOT skip hooks (`--no-verify`), do NOT destructive-reset.

### PR + merge flow

1. Branch off main.
2. Commit with structured message (what + why; co-author trailer is fine).
3. Push.
4. Open PR via `gh pr create` with a populated `## Summary` and `## Test plan`.
5. Run `/watch-ci` — enforced by hook; all further Bash calls are blocked until CI is checked.
6. Review before merging:
   - **For docs-only branches (`docs/site/*`):** the CE review gate is auto-bypassed. Merge directly with `gh pr merge N --squash --delete-branch`.
   - **For trivial content/asset changes** (new icons, OG images, meta tags, config files): inline lightweight review in the PR description, then merge with the `--no-review` bypass token in the command text (e.g., `echo "bypass --no-review: <reason>" && gh pr merge N --squash --delete-branch`). The hook scans the command text for this token.
   - **For anything touching logic** (new CSS with motion, anything that could regress rendering, anything with executable code): run `/ce:review` or equivalent before merging.
7. After merge, run `/watch-ci` again to verify production deploys successfully.
8. Update the roadmap plan in the same branch — check off completed units with `- [x]` and add a one-line note of what was done.

### Deploy flow
- Vercel auto-deploys every push. `main` → Production. Branches → Preview.
- No GitHub Actions workflows; Vercel handles CI.
- Verify deploy via `gh api repos/:owner/:repo/deployments/<id>/statuses`.
- Production site is aliased at goodvibes-coding.com.

### Tooling

- Use the Vercel CLI for env vars only; do not run `vercel deploy` manually — let auto-deploy handle it.
- Analytics are enabled in the Vercel dashboard (Web Analytics + Speed Insights). Field data trickles in over ~7 days per change.
- Screenshots / OG image generation: headless Chrome at `/Applications/Google Chrome.app/Contents/MacOS/Google Chrome` with `--window-size=WxH --virtual-time-budget=5000 --screenshot=…`. Render at 1200×700 and crop to 1200×630 with `sips --cropToHeightWidth` (Chrome headless shrinks viewport by ~70px of chrome).
- Favicon/image generation: QuickLook (`qlmanage -t -s N -o`) for SVG→PNG, `sips -z` for resizing, Python `struct` for ICO bundling (see `git log` for the inline script that built the current favicon.ico).

---

## 9. Anti-patterns — what you should refuse to do even if asked

From the mission-fit analysis on 2026-04-19. These are not opinions; they are rules for this brand.

1. **Never invent stats.** "Trusted by 1000+ teams." "12,500+ creators." "50ms latency." Destroys trust immediately. This is pattern #134 in the global common-solutions.md.
2. **Never use stock photography.** Laptops on desks, people at whiteboards, generic diverse-team shots. Buyers can sniff these instantly.
3. **Never add logo-cloud theater.** Not AWS partner badges you don't have. Not client logos you haven't earned. Not "Featured in" unless it's true.
4. **Never write corporate "we."** "Our team of experts" when there are two of you is the loudest tell. Use first-person plural ("we") and name Matt or Melissa directly when appropriate.
5. **Never write SaaS-template copy.** "Unlock." "Supercharge." "Revolutionary." "Cutting-edge." "Powered by AI." If your copy could appear on another random AI site, rewrite.
6. **Never introduce gradient blobs, neon accents, or glassmorphism.** 2021 aesthetic. Signals "I used a template."
7. **Never hide pricing behind "contact us"** once Matt commits to publishing ranges. Pre-commit is fine; post-commit it's extractive.
8. **Never optimize for vanity conversion metrics.** Exit-intent popups, urgency timers, social-proof toasters. These work against the mission.
9. **Never grind SEO via keyword-stuffed content.** Pillar essays about real decisions: yes. "Ultimate guide to AI automation 2026": no.
10. **Never add a runnable-code hero visual.** The current fake-code block is already on the "avoid" list (see §6 Batch G). Replacing it with a more elaborate fake-code block is worse, not better.

---

## 10. Key files and directories

```
good-vibes-coding/
├── index.html                   # The entire site (all sections, one file)
├── styles.css                   # Full stylesheet with @font-face and OKLCH system
├── robots.txt                   # LLM crawler allow-list + sitemap ref
├── sitemap.xml                  # Homepage only (single URL)
├── site.webmanifest             # PWA manifest (theme color, icons)
├── favicon.ico                  # Multi-size ICO for Safari address bar
├── favicon.svg                  # SVG favicon (modern browsers)
├── apple-touch-icon.png         # iOS home-screen icon (180x180)
├── icon-192.png, icon-512.png   # PWA icons
├── og.png (1200×630)            # Open Graph image with CTA pill
├── og-square.png (1200×1200)    # Square OG for iMessage/WhatsApp
├── team.jpg, matt.jpg, melissa.jpg  # Grayscale founder/team photos
├── fonts/                       # Self-hosted WOFF2 (8 files, ~268KB total)
│   ├── dmsans-latin.woff2
│   ├── dmsans-latin-ext.woff2
│   ├── dmsans-italic-latin.woff2
│   ├── dmsans-italic-latin-ext.woff2
│   ├── dmserif-latin.woff2
│   ├── dmserif-latin-ext.woff2
│   ├── dmserif-italic-latin.woff2
│   └── dmserif-italic-latin-ext.woff2
├── README.md                    # Stack, DNS, infrastructure, contacts
├── social-media-setup.{md,html,pdf}  # Handoff doc for Melissa (gitignored)
└── docs/
    ├── handoff/
    │   └── 2026-04-20-agent-team-handoff.md   # THIS FILE
    ├── plans/
    │   └── 2026-04-17-001-elite-marketing-site-roadmap.md  # Living roadmap
    └── research/
        └── 2026-04-17-elite-marketing-site-research.md      # 4-agent synthesis
```

**Not tracked in git** (see `.gitignore`): `.vercel`, `.DS_Store`, `social-media-setup.*`

---

## 11. First-30-minute checklist for the incoming agent

Run these, in order, before touching any code:

1. **Read this doc's §1 (TL;DR), §4 (Strategic frame), and §9 (Anti-patterns) carefully.** The strategic frame is the most common failure mode — agents default to Playbook A because it's the most-documented "elite site" pattern.
2. **Skim [the living roadmap](../plans/2026-04-17-001-elite-marketing-site-roadmap.md).** Pay attention to which `- [x]` boxes are already checked.
3. **Skim [the research doc](../research/2026-04-17-elite-marketing-site-research.md).** You don't need to memorize it; you need to know where to look.
4. **Read `index.html` and `styles.css` end-to-end.** It's ~1500 lines total. Faster than guessing.
5. **Visit https://goodvibes-coding.com in a real browser.** Check the tab favicon renders (teal `</>`), the OG preview looks good, the Calendly CTA works, the fonts load.
6. **Check `git log --oneline -20`** to see the recent commit style and what the prior agent shipped.
7. **Before doing any new work: post §7 (asks blocking Matt) to him** as a single message. Don't batch with other questions. Don't guess any fact.
8. **Choose your next unit from §6 Batch E (solo, unblocked) OR §6 Batch A (voice PR, needs copy approval before merge).** Never start with Batch G (design craft) without Matt's creative direction.

---

## 12. Compound engineering conventions

This project follows the compound-engineering plan/research/solutions convention loosely:
- `docs/plans/YYYY-MM-DD-NNN-<slug>.md` — living plans with Requirements Trace + Implementation Units
- `docs/research/YYYY-MM-DD-<slug>.md` — frozen research snapshots
- `docs/handoff/YYYY-MM-DD-<slug>.md` — handoff documents like this one
- `docs/solutions/` — (not yet used on this repo) compound-style solution writeups after novel fixes

Plans are living — check off boxes as you ship, add brief notes. Research is frozen — don't rewrite.

When you finish a non-trivial unit, consider adding a compound solution writeup if the work involved a novel fix or pattern worth preserving for the next team.

---

**Questions, gaps, or new context:** append to this doc (don't start a new handoff until material changes — e.g., new phase completed, mission frame updates, or Matt + Melissa's roles evolve). Date-stamp your edits.
