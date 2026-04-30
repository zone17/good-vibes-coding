---
title: Starter Revenue Activities — First 30–60 Days
date: 2026-04-30
type: services-research
---

## TL;DR — top 5 starter offerings to ship now

Three of the ten candidate categories pass every filter (real demand, on-brand, ladders to retainer, GVC-differentiated, no $5/hr Fiverr competition). Two more pass with caveats. Five are rejected.

**Ship these in the next 30 days, in order:**

1. **Restaurant Menu & Reviews Sprint — $4,500 flat (2 weeks)** — digital menu rebuild + AI review-response system + Google Business Profile cleanup, productized for hospitality. *Mel's wedge.* Ladders to a $1,500/mo Hospitality Operations Retainer.
2. **AI-Ready Site Refresh — $7,500 flat (3 weeks)** — replace pre-AI SMB sites with a fast, content-clean, schema-marked, AI-search-discoverable site. Sized to surface the deeper Build Sprint. Ladders to the $2,500/mo Operations Retainer.
3. **SOP Capture Sprint — $6,500 flat (2 weeks)** — film/transcribe an owner's tribal knowledge, ship a searchable, AI-queryable internal manual. *Direct WikiFold gateway.* Ladders to a $2,500/mo retainer where the manual stays alive.

**Maybe-tier (ship if the right customer asks, don't put on homepage yet):**

4. **GBP + Reviews Tune-up — $1,500 flat (1 week)** — only as a *door-opener* into restaurants/services that aren't ready for the full $4,500 Sprint. Used for warm-list seeding, not a primary SKU.
5. **Pilot Sprint — $9,500** *(already in `04`)* — kept on the homepage; the offerings above sit *below* it as faster on-ramps, not replacements.

**Net effect on Year-1 ramp:** the productized-package floor moves earlier (first revenue week 2–3 instead of week 5–6), Pilot Sprint conversions become *easier* because customers have a starter receipt, and the path to retainer-engine MRR by month 6 is more credible. The Year-1 base-case revenue line in `07` does not need to move; the *time-to-first-dollar* does. See §6.

---

## Method

Reviewed `04-revenue-model-analysis.md`, `05-smb-ai-gap.md`, `09-business-plan-synthesis.md`, `07-financial-projections.md`. Ran 10 web searches across the candidate categories for 2026 published agency rates, productized comps, and demand signals. Attempted to fetch the Chris Everest X post (`https://x.com/everestchris6/status/2048855885620162603`) — both `WebFetch` and `WebSearch` returned no content (X gates tweet HTML behind auth in 2026; the `/tmp/last30days-everest.out` file was empty). The thesis the founder extracted — *"high-frequency, low-friction services like outdated SMB websites and digital restaurant menus might be a faster path"* — is treated as an input hypothesis, **strongly corroborated** for website refreshes and restaurant menu/review work, **weakly corroborated** for GBP setup, **disconfirmed** for chatbots and social media. Categories scored on: demand, going rate, cycle, AI angle, GVC fit (Matt eng / Mel hospitality), brand alignment (Playbook B), ladder to retainer. Anti-patterns refused: $5/hr Fiverr competition, no recurring path, SaaS-template language, staff-replacement framing.

---

## Category-by-category evaluation

| # | Category | Demand | $ range (mkt) | Cycle | AI angle | GVC fit | Brand fit | Recommend |
|---|---|---|---|---|---|---|---|---|
| 1 | Outdated SMB site rebuilds | **Strong** | $3K–$15K productized | 2–4 wk | High (AI-SEO, schema, content) | Strong (Matt) | Strong | **YES** |
| 2 | Restaurant digital menus + AI copy | **Strong** | $300–$2K SaaS / $2K–$8K builds | 1–3 wk | High (allergen tagging, menu copy, dynamic specials) | **Best fit** (Mel) | Strong | **YES** |
| 3 | Local SEO + Google Business Profile | Medium | $125–$475/mo retainer; $300–$500 setup | 1–2 wk | Low–medium (review automation = AI) | Medium | Medium | Maybe (door-opener only) |
| 4 | AI review management | Strong | $30–$300/mo SaaS; $99–$300/mo svc | 1 wk | High | Strong (Mel) | Strong | **YES — bundled into #2** |
| 5 | Booking system modernization | Medium | $24–$700/mo SaaS; $40K–$250K customs | 4–10 wk | Low–medium | Medium | Medium | No (use vertical SaaS, don't replace) |
| 6 | Email migration (Mailchimp→Klaviyo) | Medium-low (e-com only) | $2K–$10K migrations | 2–6 wk | Medium | Weak (e-com tilt) | Medium | No |
| 7 | Social media content automation | Strong demand, weak fit | $59–$5K/mo packages | 0–2 wk | High (commoditized) | Weak | **Off-brand** | No |
| 8 | Customer service chatbots | Medium | $5K–$30K simple; $75K+ AI | 4–12 wk | High (failure-rate trap) | Medium | Risky (88% prefer humans) | No (refer out) |
| 9 | Internal SOP / knowledge capture | **Strong (latent)** | $5K–$15K productized | 1–3 wk | **Best AI angle (RAG/wiki)** | **Best fit** (both) | **Best fit** | **YES — WikiFold gateway** |
| 10 | Bookkeeping / invoicing automation | Strong | $300–$800/mo svc | 4–8 wk | Medium | Weak (regulated) | Medium | No (refer to a bookkeeper partner) |

---

### 1. Outdated SMB site rebuilds — **YES**

61% of SMB site buyers spent under $10K on their most recent project (DigitalApplied 2026). Sites built 2015–2020 are functionally broken for AI-mediated discovery: no schema, no LLM-legible content, weak Core Web Vitals. **The fresh framing isn't "your site looks old," it's "ChatGPT and Google AI Overview don't see you, and competitors do."** Pricing: $3K–$8K freelancer, $8K–$15K boutique, productized $5K–$10K. A $7,500 productized rebuild sits below boutique-agency floor and inside SMB comfort. Cycle 2–4 wk. AI angle is real: JSON-LD/FAQ schema for AI search, owner-voice content rewrite from a 30-min interview, live content blocks pulled from POS/Google/OpenTable so the site doesn't go stale. Matt's eng depth (Vercel/Next, the GVC site itself is the proof — recent commits 8e3a670 fonts, 68b2162 SEO foundations) ships materially better than 95% of local shops. On-brand. **YES.**

### 2. Restaurant menu modernization — **YES (Mel's wedge)**

Strongest demand of the ten:
1. **Regulatory tailwind.** CA SB-68 (effective July 1 2026) mandates top-9 allergen disclosure on every standard menu item (printed, digital, drive-thru, app). NY following. Multi-state operators must comply for CA locations *now*; FL-only operators are pre-complying voluntarily. (Sources: Kafoodle SB-68 guide, FoodOnDemand Apr 2026, FranchiseTimes.)
2. **Customer voice.** Cuban thread already named a restaurant owner who'd pay for help; hospitality is GVC's 5/5 fit segment per `09`.
3. **Universal pain.** Indie restaurants run six out-of-sync menus (printed, Toast, Google, Yelp, Instagram, delivery apps).

Pricing: menu SaaS $10–$30/mo, AI add-ons $59–$199/mo, done-for-you regional-agency packages $1.5K–$5K one-time + $300–$800/mo. **No published South Florida competitor combines "menu single-source-of-truth + AI review responses + allergen tagging" as one fixed-price offer.** Cycle 1–3 wk — fastest-to-revenue. AI angle: menu-copy generation in venue voice, allergen tagging *with* cross-contamination disclaimers (the FoodOnDemand "70% of AI menu bots fail safety claims" stat becomes GVC's quality differentiator), daily-specials → IG/GBP automation, brand-voice review-response drafting with sentiment alerts. **Best GVC fit on the list** — Mel writes the rules ("don't tag GF unless the fryer's clean"), Matt builds. Local web shops have no hospitality operator; vertical SaaS (Toast) has no implementation consultants. **YES — homepage hero for hospitality.**

### 3. Local SEO + GBP — **MAYBE (door-opener only)**

Commoditized. $125–$475/mo retainers, $300–$500 setup; every local agency offers it; AI angle is thin. Don't put on homepage. Use as a $1,500 first-foot-in-the-door for venues not yet ready for the $4,500 Sprint. Loss-leader, not profit center.

### 4. AI review management — **YES, BUNDLED INTO #2**

Half-star Yelp lift = 5–9% revenue (Socinova). Standalone competes with Bloom/EmbedSocial/Birdeye at $30–$300/mo SaaS — GVC can't win on tool price. *Bundled* into #2 with Mel's brand-voice rules + Matt's behavior wiring (no apology without ticket lookup, cluster-1-star escalation), it's differentiated. **YES as a feature of #2, never standalone.**

### 5. Booking system modernization — **NO**

Buy decision is "switch SaaS," not "build custom." Resos $24–$149/mo undercuts OpenTable ($249+) by 90%; custom builds $40K–$250K (Appinventiv). Refer to vertical SaaS during audit. Possible future Build Sprint or SaaS Replacement scope.

### 6. Email migration (Mailchimp→Klaviyo) — **NO**

E-commerce-tilted; SMB hospitality/service get marginal lift. Saturated done-for-you category (SmartMail, Beena, Radicalz). $2K–$10K agency band. Off-vertical. One-off Build Sprint deliverable only if it surfaces in an audit.

### 7. Social media content automation — **NO**

AI-first tools at $15–$79/mo are replacing $1.5K–$3K/mo agencies (Apaya 2026). Knife fight with Hashmeta, Apaya, Predis.ai, Ocoya, 50 Fiverr sellers. "Bronze/Silver/Gold calendar" is the canonical Playbook-B-rejected template (`04` §5). Refer to a $79/mo SaaS in audit.

### 8. Customer service chatbots — **NO**

Failure data is brutal: AI customer service fails at **4× the rate** of other AI tasks (Qualtrics); **77% find it frustrating, 88% prefer humans** (Ipsos); CNBC Apr-2026 *"I Hate Customer Service Chatbots"*. Shipping a chatbot SKU when 88% of customers prefer humans is the canonical "fire your staff with AI" anti-pattern. The right GVC move is the Audit: diagnose whether chat fits, often say no.

### 9. Internal SOP / knowledge capture — **YES (WikiFold gateway)**

Latent and enormous. Every SMB has *"Maria knows how we do everything; if Maria leaves we're cooked."* 73% of SMB owners want training (Goldman Sachs Feb 2026); the prerequisite is a written-down business, which most don't have. Productized SOP packages run $5K–$15K from training shops. Transcription itself is $24/mo (Sonix, Rev) — the markup lives in turning transcripts into a *usable AI-queryable manual*. Cycle 1–3 wk. **Strongest AI angle on the list** — RAG, embeddings, semantic search, assistant-grade summarization (i.e., what WikiFold already does). **Best GVC fit, tied with #2** — Matt's WikiFold IP is the vehicle, Mel's ops experience is the interview credibility. On-brand: protects staff knowledge, doesn't replace staff. **YES — the most important offering because every SOP Sprint is a future WikiFold $99/mo customer (per `04` §7 secondary engine).**

### 10. Bookkeeping / invoicing automation — **NO**

Regulated; QuickBooks AI handles 85–95% of categorization already; SMBs save $400–$800/mo on automation alone. The residual (reconciliation, exceptions, tax) needs a bookkeeper license. Build the partner channel `09` already calls out as a top-3 GTM source. Refer outbound; take warm referrals inbound.

---

## Recommended starter offerings — productized

### Offering A: **Restaurant Menu & Reviews Sprint — $4,500 flat (2 weeks)**

**What's included (homepage copy):**
> Two weeks. We rebuild your menu (printed + Google + Yelp + Toast/Square + Instagram bio) as one source of truth. We tag your top-9 allergens correctly with cross-contamination disclaimers, in your venue's voice. We wire AI review-response drafting that sounds like *you*, not a chatbot. You approve everything. You keep everything. Flat $4,500.

**ICP / first 5 named introductions** (Matt and Mel can DM these contacts this week):

1. **Three Boca Raton independent restaurants on East Palmetto Park Rd or Mizner Park** that Mel has worked with or has 1st-degree connection to (e.g., from her hospitality network — Mel to name 3 from her contacts; the §14 open question #2 in `09` lists this as already needed).
2. **One Delray Beach Atlantic Ave restaurant** (high foot traffic, allergen-forward customer base).
3. **One West Palm Beach Clematis St or Rosemary Square restaurant** — vibrant indie scene, owner-operators, no Toast-implementation budget.
4. **One Lake Worth or Lantana family-owned spot** — exactly the "owner does six menus by hand" pain.
5. **One Fort Lauderdale Las Olas restaurant** — first cross-county case study.

**1-week MVP to ship the offer:**
- Homepage adds a 4th SKU card: **"Menu & Reviews Sprint — $4,500"** above the Audit.
- One Loom (60–90s) of Mel walking through the offering, Matt walking through what gets shipped technically.
- One sample deliverable mockup (a fake menu site for a fake "Bistro Mizner" — public, linkable, demonstrably good).
- Calendly intro-call event tightened to disqualify chains > 5 locations (those need Toast/Bloom, not us).

**Ladder to retainer:**
- Sprint completion → offer **Hospitality Operations Retainer @ $1,500/mo** (12 active hours, monthly menu refresh, weekly review-cluster check-in, quarterly allergen audit).
- The $1,500/mo retainer is *intentionally below* the published $2,500/mo Operations Retainer — hospitality margins are tighter than professional services, and the higher *volume* (8 hospitality retainers vs. 4 professional-services retainers) is the trade. **Keep $2,500/mo as the published headline; offer $1,500/mo only as a Hospitality SKU spelled out as such.** This is honest tier-by-vertical, not Bronze/Silver/Gold.

---

### Offering B: **AI-Ready Site Refresh — $7,500 flat (3 weeks)**

**What's included (homepage copy):**
> Three weeks. We rebuild your site on modern infrastructure (fast, secure, mobile-perfect). We add the schema markup that makes ChatGPT, Google AI Overviews, and Perplexity see your business. We rewrite your content from a 30-minute interview with you, in your voice. You get the source code. Flat $7,500.

**ICP / first 5 named introductions:**

1. **Two professional-services firms** (Boca/West Palm — accountant, attorney, financial planner) that Matt or Mel has 1st-degree contact with — sites typically built 2015–2018, currently invisible to AI search.
2. **One regional service business** in Broward (HVAC, roofer, plumber, landscaper) — high commercial intent, terrible 2017-vintage WordPress site.
3. **One Mel-network venue's adjacent vendor** (the catering equipment supplier, the wine importer, the linen company) — pre-warmed by Mel's intro.
4. **One Matt eng-peer-introduced startup** ($1–5M ARR, has a launch-era Webflow that's now embarrassing).
5. **One niche e-commerce / DTC** (the hospitality vertical's wine/spirits brand) — site built on Shopify 2019-vintage theme.

**1-week MVP:**
- Homepage adds **"AI-Ready Site Refresh — $7,500"** as a 5th SKU card.
- The GVC site itself becomes the live demo (it already self-hosts fonts, ships JSON-LD, scores 100 on Lighthouse — leverage the recent commits 8e3a670, d60f890, 68b2162 as proof artifacts).
- One Loom showing Matt running an AI-Overview audit on a prospective client's existing site, then on the rebuilt version — *visible delta*.
- A "before/after" measurable: Lighthouse score, schema-validator clean, ChatGPT-can-find-you check.

**Ladder to retainer:**
- Refresh completion → offer **$2,500/mo Operations Retainer** as documented in `04`. The retainer covers ongoing content keep-alive, AI-search monitoring, schema additions as the business grows, monthly working session.
- *Critical:* the retainer is *not* "ongoing site maintenance" (that's $400/mo agency work) — it's **"the AI implementation layer for the whole business, with the site as the first deliverable."** That framing keeps the price honest.

---

### Offering C: **SOP Capture Sprint — $6,500 flat (2 weeks)**

**What's included (homepage copy):**
> Two weeks. We sit with you and your top operator for two days, film the work, transcribe everything, and build a private searchable manual you can ask in plain English: "how do we close on Sundays?" — and get the right SOP back, in the right person's voice. You keep the manual. We make it possible to onboard your next hire in days, not months. Flat $6,500.

**ICP / first 5 named introductions:**

1. **One Mel-network restaurant where the GM is approaching retirement** (Mel knows two such situations from her network — the brain-drain risk is acute).
2. **One Matt-network engineering-led startup** at the "we hired our 4th engineer and onboarding is broken" stage.
3. **One regional service business** with a star tech the owner is terrified of losing.
4. **One professional-services firm** where the founder wants to take a sabbatical and can't.
5. **One hospitality group** (2–4 location operator) where each location is run differently because no one wrote it down.

**1-week MVP:**
- Homepage adds **"SOP Capture Sprint — $6,500"** as a 6th SKU card.
- A WikiFold demo wiki seeded with a fictional restaurant SOP (5 articles: opening, closing, fryer protocol, allergen handling, complaint protocol) — public, linkable, demonstrably searchable.
- One Loom of Matt running a search on the wiki, asking it a plain-language question, showing the AI assistant answer with citations.
- A short essay (Matt's first Substack post per `09` §10 weeks 5–8) — *"What we built for Maria before she retired"* — anonymized real-world framing.

**Ladder to retainer:**
- Sprint completion → **$2,500/mo Operations Retainer** with an explicit "your wiki stays alive" deliverable: every retainer month includes 2 hours of new SOPs captured, plus the AI assistant tuning. **This is the cleanest path into WikiFold productization** — every SOP retainer client is the natural alpha customer when the WikiFold $99/mo SKU launches in Q3 2026 (the secondary engine in `04` and `09`). The retainer is the bridge.

---

## Anti-patterns refused (and why)

| Refused offering | Why |
|---|---|
| Generic social media calendar package | Off-brand (Bronze/Silver/Gold template); knife-fight with $79/mo SaaS; no GVC differentiation |
| Standalone customer-service chatbot | 88% of customers prefer humans; 4× failure rate; "fire your staff with AI" anti-pattern |
| Standalone Mailchimp→Klaviyo migration | Off-vertical (e-commerce-tilted); commoditized done-for-you category |
| Custom restaurant booking system rebuild | $40K–$250K is out of starter band; vertical SaaS does it better — refer out |
| Standalone bookkeeping automation | Regulated; not GVC's competence; build a partner channel instead |
| Standalone GBP setup | $300–$500 commodity work; only viable as a $1,500 door-opener |
| "We'll fire your call-center with AI" anything | Brand-violating; financial-model-violating (would alienate Mel's hospitality referrals) |
| Hourly $200/hr "AI consulting" listed on homepage | The 10x trap (`04` §1); reserved as $450/hr internal-only existing-client rate |

---

## Updated Year-1 ramp expectation

`07-financial-projections.md` Base Case Year 1 is **$281K revenue** with first cash-positive month at month 3 (after the first sprint lands) and ~$15K/mo MRR by month 12.

**With these starter offerings shipped in the next 30 days, the realistic adjustment is:**

| Metric | Per `07` Base | With starters | Delta |
|---|---|---|---|
| First $1 booked | Week 5–6 | **Week 2–3** | -3 weeks (faster validation) |
| Months 1–3 revenue | ~$30K | **$35–55K** | +$5–25K (1–2 starter sprints + 1 Audit + 1 Pilot) |
| Months 1–3 retainer signups | 1 | **1–2** | +0–1 (starter-sprint conversion is faster than Pilot conversion) |
| Year-1 total revenue | $281K | $260–310K | ±$20K (the starters substitute, don't pure-add — they replace some Pilot Sprints in the early-stage mix) |
| Time to retainer-engine MRR ≥ $15K/mo | Month 12 | **Month 9–10** | -2–3 months |
| Number of "first 5 customer" case studies by month 6 | 2 | **4–5** | +2–3 case studies (the volume difference is the marketing flywheel difference) |

**Reasonable expectation to commit to in writing:**

> GVC books **$35–55K in starter-offering revenue in months 1–3** across 4–7 productized sprints (Menu & Reviews, AI-Ready Site Refresh, SOP Capture). That revenue funds the operating reserve and produces 4–5 named case studies. **By month 6, retainer MRR reaches $9–12K/mo** (3–4 retainers at $1,500–$3,000), on track for **$15K+/mo MRR by month 9–10** instead of month 12. The Year-1 base-case revenue line stays in the $260–310K band; the *time-to-retainer-engine* shifts left by 2–3 months, which is the load-bearing improvement.

The existing $9,500 Pilot Sprint stays on the homepage — **it remains the right offering for prospects who want the full audit-then-build experience.** The starter offerings are the *narrower, faster* options for prospects who already know exactly what's broken.

**The downside risk** of these starter offerings is *not* margin (they're priced at 65–75% gross margin like the rest of the product line). It's **founder-time discipline** — three new productized SKUs across 30 days is a lot of homepage and Loom production. The single mitigation: ship Offering A (Menu & Reviews) first, prove it converts, *then* ship B and C in weeks 3–4. Don't ship all three on day 1.

---

## Sources

**Demand & adoption baseline**
- [SBA Office of Advocacy 2025 Small Business Profiles](https://advocacy.sba.gov/2025/06/30/new-advocacy-report-shows-the-number-of-small-businesses-in-the-u-s-exceeds-36-million/) — 36.2M SMBs.
- [Goldman Sachs 10KSB AI Survey, Feb 2026](https://www.goldmansachs.com/pressroom/press-releases/2026/small-businesses-embrace-ai-but-need-training-and-support-to-fully-harness-it) — 76% use, 14% integrated, 73% want training.
- [Fortune, Mar 18 2026](https://fortune.com/2026/03/18/small-business-ai-slow-integration-across-operations/) — "downloaded the app, haven't read the manual."

**Website rebuild pricing**
- [DigitalApplied: Website Development Cost 2026](https://www.digitalapplied.com/blog/website-development-cost-2026-complete-pricing-data) — 61% of SMBs spent <$10K.
- [Clique Studios: Website Redesign Cost 2026](https://cliquestudios.com/faq/website-redesign-cost) — $3K–$15K SMB band.
- [Yuktis: 2026 Digital Agency Pricing Benchmarks](https://yuktis.com/blog/2026-digital-agency-pricing-benchmarks).

**Restaurant menu / allergen / reviews**
- [FoodOnDemand: Allergen Laws Pushing Restaurants to AI (Apr 2026)](https://foodondemand.com/04012026/why-food-allergen-laws-are-pushing-restaurants-to-ai/).
- [Kafoodle: SB-68 Allergen Law Guide 2026](https://www.kafoodle.com/blog/sb-68-allergen-law-for-restaurants-guide).
- [FDA Law Blog: California's New Allergen-Disclosure Law](https://www.thefdalawblog.com/2025/10/californias-new-allergen-disclosure-law-a-sign-of-things-to-come/).
- [Bloom Intelligence: AI Reputation Management for Restaurants](https://bloomintelligence.com/blog/reputation-management-ai-for-restaurants/).
- [Socinova: AI Google Review Responses](https://socinova.com/ai-review-responses-restaurants/) — half-star = 5–9% revenue.
- [TechCrunch: Yelp Updated AI Assistant (Apr 21 2026)](https://techcrunch.com/2026/04/21/yelps-updated-ai-assistant-can-answer-questions-and-book-a-restaurant-or-service-in-one-conversation/).

**GBP / SEO / booking / email / social pricing**
- [Renew Local GBP Pricing](https://renewlocal.com/prices/); [Merchynt GBP Pricing Guide](https://www.merchynt.com/post/google-my-business-management-pricing).
- [RestaurantBookingSystem: OpenTable Alternatives 2026](https://restaurantbookingsystem.com/compare/opentable-alternatives/); [Appinventiv: Custom Reservation App Cost](https://appinventiv.com/blog/cost-to-build-restaurant-reservation-app-like-opentable/).
- [Hibeena Mailchimp→Klaviyo](https://hibeena.com/mailchimp-to-klaviyo/); [Radicalz Migration Math](https://www.radicalz.io/blogs/the-mailchimp-to-klaviyo-migration-math-when-switching-actually-pays-off-for-e-commerce-brands).
- [Hashmeta AI Social Pricing](https://www.hashmeta.ai/en/blog/ai-social-media-content-creation-pricing-complete-cost-guide-and-package-benchmarks); [Apaya: Social Media Management Costs 2026](https://apaya.com/blog/ai-social-media-management-costs).

**Chatbot failure data**
- [Qualtrics: AI Customer Service Fails 4× Other Tasks](https://www.prnewswire.com/news-releases/ai-powered-customer-service-fails-at-four-times-the-rate-of-other-tasks-302576858.html).
- [CNBC, Apr 1 2026: I Hate Customer Service Chatbots](https://www.cnbc.com/2026/04/01/ai-chatbot-customer-service-complaints-refunds.html).
- [Tidio: Chatbot Pricing 2026](https://www.tidio.com/blog/chatbot-pricing/); [Builts.ai: Customer Service AI 2026](https://builts.ai/blog/ai-customer-service-trends-2026/).

**SOP / transcription / bookkeeping**
- [Sonix](https://sonix.ai/pricing); [Rev](https://www.rev.com/pricing).
- [QuickBooks AI Accounting](https://quickbooks.intuit.com/ai-accounting/); [Booke AI](https://booke.ai/en-us).

**Internal**
- `04-revenue-model-analysis.md`, `07-financial-projections.md`, `09-business-plan-synthesis.md`, `docs/research/2026-04-28-marketing-refresh/05-smb-ai-gap.md`, `docs/research/2026-04-28-marketing-refresh/08-competitive-landscape.md`.

**Unfetchable**
- Chris Everest X post (`https://x.com/everestchris6/status/2048855885620162603`) — X gates tweet HTML behind auth in 2026 (WebFetch 402; `/tmp/last30days-everest.out` empty). Thesis treated as input hypothesis, corroborated/disconfirmed against the corpus above.
