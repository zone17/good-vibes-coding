# Elite Marketing Site Roadmap

**Plan ID:** 2026-04-17-001-elite-marketing-site-roadmap
**Owner:** Matt
**Created:** 2026-04-17
**Status:** In progress
**Source research:** [docs/research/2026-04-17-elite-marketing-site-research.md](../research/2026-04-17-elite-marketing-site-research.md)

---

## Goal

Move goodvibes-coding.com from "good small-shop page" to elite (top 5%) across four dimensions: **SEO/technical**, **conversion**, **trust**, and **design craft** — without breaking the static HTML+CSS simplicity that makes it maintainable.

## Success Criteria

A visitor landing on the site should, in order:
1. Understand within 5 seconds who it's for and what changes for them
2. See at least 3 independently-verifiable trust signals before the first CTA
3. Hit an embedded booking flow with zero redirects
4. Leave the page with either a booked call, an email address captured, or a mental bookmark of something specific

Shares on LinkedIn/iMessage/Slack render with proper OG preview. The site is crawled and indexed by Google, Bing, and LLM crawlers (GPTBot, ClaudeBot, PerplexityBot). Core Web Vitals pass: LCP <2.5s, INP <200ms, CLS <0.1.

---

## Requirements Trace

### SEO / Discoverability

- **R1** — All social platforms render proper preview cards (title, description, 1200×630 image) when the URL is shared.
- **R2** — Google, Bing, ChatGPT, Perplexity can discover, crawl, and index the site. LLM crawlers are explicitly permitted.
- **R3** — Google rich results and AI Overviews can extract structured data (Organization, LocalBusiness, FAQPage).
- **R4** — Canonical URL is declared to prevent duplicate-content penalties.
- **R5** — Core Web Vitals pass the 2026 thresholds on mobile field data (via Vercel Web Analytics).
- **R6** — Top-of-funnel keyword traffic can be measured and attributed (analytics wired).

### Conversion

- **R7** — Primary CTA (booked call) is above the fold, singular, and repeated ≥3x down the page.
- **R8** — Booking flow has zero redirects (Calendly embedded inline).
- **R9** — Objection-handling content exists before the final CTA (FAQ, "is this for you" block).
- **R10** — Visitors not ready to book have a secondary capture path (newsletter, email).

### Trust

- **R11** — Every founder mention deep-links to a verifiable LinkedIn profile.
- **R12** — Founder credentials name specific prior companies, not generic tenure claims.
- **R13** — Pricing transparency exists (at minimum, a starting range or engagement tier).
- **R14** — Process transparency exists (what happens on Day 1, Week 1, after launch).
- **R15** — Anti-sales / risk-reversal language appears near every CTA.

### Design Craft

- **R16** — Hero has one memorable visual differentiator (not a generic code-block or illustration-grid).
- **R17** — Typography, spacing, and color are committed to a single system and applied consistently.
- **R18** — Micro-motion enhances 2–3 critical interactions (CTA hover, scroll reveal, one signature moment).
- **R19** — Site passes the "describe it in 5 words after closing the tab" test.

---

## Phased Implementation

### Phase 0 — Foundation (SHIPPED 2026-04-17)

- [x] Landing page published with hero, services, mission, process, free tools, team, CTA, footer
- [x] Calendly CTAs replace mailto fallbacks
- [x] README documents stack, DNS, infrastructure
- [x] `.gitignore` excludes `.vercel`, `.DS_Store`, handoff docs
- [x] SVG favicon matching brand mark
- [x] PNG/ICO favicon fallbacks (`favicon.ico`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`)
- [x] `site.webmanifest` with theme color, PWA hints
- [x] `theme-color` meta tag for mobile browser chrome

### Phase 1 — Ship this week (P0: biggest visible deltas, lowest effort) [~6 hours]

Batch into a single PR. Each checkbox is one implementation unit.

**SEO / discoverability**
- [x] **U1** Add Open Graph meta tags to `<head>`: `og:title`, `og:description`, `og:image`, `og:url`, `og:type`, `og:site_name` (satisfies R1)
- [x] **U2** Add Twitter Card meta tags: `twitter:card` (summary_large_image), `twitter:title`, `twitter:description`, `twitter:image` (R1)
- [x] **U3** Add canonical link: `<link rel="canonical" href="https://goodvibes-coding.com/">` (R4)
- [x] **U4** Generate static OG image at `/og.png` (1200×630) — teal background, brand mark, H1 tagline, URL. Also `/og-square.png` (1200×1200) for iMessage/WhatsApp (R1)
- [x] **U5** Add JSON-LD `Organization` schema block with name, url, logo, sameAs (LinkedIn), contactPoint (R3)
- [x] **U6** Add JSON-LD `LocalBusiness` (type: `ProfessionalService`) with areaServed: South Florida, telephone, address region (R3)
- [x] **U7** Create `/robots.txt` with sitemap reference and explicit allow for `GPTBot`, `ClaudeBot`, `PerplexityBot`, `Google-Extended` (R2)
- [x] **U8** Create `/sitemap.xml` listing the homepage (R2)
- [x] **U9** Wire Vercel Web Analytics (free, one-line script include) (R5, R6) — script tag added; Matt needs to enable Web Analytics + Speed Insights in the Vercel dashboard to start collecting data
- [ ] **U10** Wire Plausible ($9/mo) with domain `goodvibes-coding.com` (R6) — needs Matt to sign up at plausible.io and add the one-line snippet

**Conversion / trust (copy + markup)**
- [ ] **U11** Add Melissa's LinkedIn link to her team card (mirror Matt's link structure) (R11)
- [ ] **U12** Replace "25 years leading engineering organizations" with named prior companies for Matt; same treatment for Melissa's "two decades … NYC and South Florida" (R12)
- [ ] **U13** Add FAQ section (6 Q&A): cost / "burned before" / "is this for us" / "what if AI isn't right" / "how fast can you start" / "what about my data" (R9)
- [ ] **U14** Add JSON-LD `FAQPage` schema mirroring U13 content (R3)
- [ ] **U15** Add "Is this for you / not for you" disqualification block above final CTA (R9, R15)
- [ ] **U16** Add anti-sales copy to final CTA section: "No pitch deck. If AI isn't right for you, we'll tell you in the first 10 minutes" (R15)

### Phase 2 — Within 2 weeks (P1: proof stack, friction, speed) [~8–12 hours]

**Proof stack**
- [ ] **U17** Record 60–90s iPhone Loom of Matt + Melissa: "Why we started Good Vibes Coding and who we don't want to work with" — embed below hero (R13–R14)
- [ ] **U18** Add pricing transparency block: "Pilots from $X. Monthly engagements from $Y. Fixed-scope sprints available." (R13)
- [ ] **U19** Add transparent process block expansion: "Day 1: X. Week 1: Y. Week 4: Z." with concrete deliverables (R14)
- [ ] **U20** Add "Sample Builds" section with 2–3 Loom walkthroughs of AI workflows (WikiFold build, one internal automation, one pro-bono build). Before/after metric cards where applicable (R7, R14)
- [ ] **U21** Create GitHub org `goodvibescoding`, open-source one small utility extracted from WikiFold

**Friction reduction**
- [ ] **U22** Embed Calendly inline below hero using `data-url` embed (no redirect). Keep existing button CTAs as secondary (R8)
- [ ] **U23** Add secondary capture: newsletter signup (Buttondown or ConvertKit) below mission section, framed as "Get our monthly write-up on AI wins and mistakes we've seen" (R10)

**Performance**
- [ ] **U24** Self-host DM Serif Display + DM Sans WOFF2 files; drop Google Fonts preconnects; `<link rel="preload">` the H1 weight (R5)
- [ ] **U25** Convert `team.jpg` to AVIF + WebP with `<picture>` fallback (R5)
- [ ] **U26** Audit CSS animations for `will-change` / transform-heavy INP regressions (R5)

**Indexing**
- [ ] **U27** Submit sitemap to Google Search Console; verify via DNS TXT record (R2)
- [ ] **U28** Submit sitemap to Bing Webmaster Tools (R2)

### Phase 3 — Within 1 month (P2: content moat + SEO expansion) [~20–30 hours]

- [ ] **U29** Break single-page into multi-page. New routes (static HTML, no framework):
  - `/services/ai-automation/`
  - `/services/custom-software/`
  - `/services/ai-agents/`
  - `/about/` (expanded team bios feeding `Person` schema)
  - 800–1500 words each, one H1, semantic headings, internal links (R3 extended)
- [ ] **U30** Create location page `/palm-beach-ai-consulting/` (or `/locations/south-florida/`) with LocalBusiness schema refinement
- [ ] **U31** Set up GBP (Google Business Profile) listing tied to LocalBusiness schema
- [ ] **U32** Launch `/writing/` section with 6–10 evergreen pillar posts answering actual sales-call questions:
  - "What does AI automation cost for a small business?"
  - "AI agents vs. Zapier vs. custom software: when to pick what"
  - "How to pick an AI consultant (and red flags to avoid)"
  - "What small-business AI actually looks like in 2026"
  - "Why most small-business AI projects fail"
  - "The AI integration mistakes we see hospitality/SMB teams making"

### Phase 4 — Design craft (ongoing, elite differentiation) [~10–15 hours]

- [ ] **U33** Replace the fake-code hero visual with a dimensional WikiFold preview (screenshot rendered with soft shadow + hover tilt) OR a runnable-feeling code block (real syntax tokens, cursor, subtle chrome) (R16, R19)
- [ ] **U34** Compress services grid from 6 cards to 3 + "and more" affordance, or narrate through a single outcome-first story (R17)
- [ ] **U35** Add micro-motion: hover magnetism on CTAs, scroll-linked accent on hero, staggered card reveal (R18)
- [ ] **U36** Audit typography rhythm against Sierra/Linear/Anthropic references; apply one editorial move (oversized display heading break-out, or serif/sans pairing at a single feature moment) (R17, R19)
- [ ] **U37** (Optional) Add dark mode with a warm charcoal + teal accent, not pure `#000`

---

## Out of Scope

- Enterprise SEO tooling (Ahrefs, Semrush) — overkill until organic traffic > ~500/mo
- A/B testing infrastructure (Statsig, PostHog experiments) — need baseline conversion data first
- CMS migration (Sanity, Contentful, Prismic) — stay on static HTML until content load demands it
- Dark mode before Phase 2 (nice-to-have, not ROI)
- GA4 (unless running Google Ads)
- Badge/certification theater

---

## Risks & Mitigations

| Risk | Likelihood | Mitigation |
|------|-----------|-----------|
| Pricing transparency filters too hard at the top of funnel | Medium | Use ranges, not fixed quotes. "Pilots from $X" is filter; fixed price is not. |
| Loom videos feel amateur and hurt credibility | Low | iPhone quality is 2026 norm. Script + 2 takes. Post-production = captions only. |
| Multi-page split dilutes homepage authority | Low | Keep homepage as the hub with strong internal linking. Service pages become inbound capture surfaces. |
| Self-hosted fonts increase maintenance surface | Low | WOFF2 files are static. No build step needed. |
| Newsletter capture cannibalizes Calendly conversions | Low | Newsletter sits below the primary CTA; it's the secondary path for not-ready-yet visitors. |

---

## Measurement

After Phase 1 ships, track weekly:
- Calendly-bookings / site-visitors conversion rate
- Average session duration
- Bounce rate on homepage
- Search Console impressions + click-through rate by query
- Shares with proper OG preview (spot-check via `opengraph.xyz` or `metatags.io`)

Baseline established at end of Phase 1. Targets set at end of Phase 2.

---

## Parallel Work Streams

If multiple people (or agents) execute:
- **Stream A (Matt — code):** U1–U10, U22, U24–U28, U29, U33–U37
- **Stream B (Matt+Melissa — copy/content):** U11–U16, U17, U18, U19, U20, U32
- **Stream C (Melissa — community/distribution):** U21 (GitHub), U23 (newsletter setup), U30–U31 (GBP), outreach for podcast guesting

Streams A and B are independent and can run in parallel. Stream C depends on Stream B having the pricing + process content ready.

---

## Next Action

Phase 1 — start with U1–U10 (SEO foundations) as the first PR. Estimated 2 hours end-to-end. Ship, measure baseline, then continue.
