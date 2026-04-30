---
title: 3-Year Financial Projections
date: 2026-04-30
type: financial-model
---

## TL;DR

GVC is a 2-person, bootstrapped advisory shop. Base case: ~$281K revenue Year 1, founders draw $144K combined ($72K each), cash-flow positive after draws by month 3. Year 3: ~$612K revenue, $288K combined founder pay, ~$146K EBITDA, one fractional hire on payroll. Conservative survives but barely; aggressive clears $1M Year 3 with a SaaS spinoff. **The binding constraint in every scenario is not demand — it is the dual-founder delivery ceiling Sullivan describes in "Who Not How" (8 retainers + 1 build, max). Year 2's central decision is whether to stay artisanal or productize to break the ceiling.** No outside capital required; a $30K operating reserve is prudent before drawing market-rate pay.

---

## Assumptions — stated and justified

**Capacity ceiling (Sullivan / "Who Not How"):** A 2-person shop credibly supports **8–12 active retainers** if advisory-heavy, **4–6** if doing custom builds. We model a blend: 8 retainers + 1 build at any time as the Matt+Melissa-alone ceiling. One fractional hire (10–20 hrs/wk) raises it to ~14 retainers + 2 builds. This is the single most important number in the model.

**Sales cycle:** **3–6 weeks** first call to first invoice (industry norm sub-$50K). We model 4 weeks.

**Conversion rate (booked call → paid):** Warm referral / Mel's network **33%**; inbound content/SEO **12%**; cold **not modeled** (anti-sales brand).

**Churn (after 90-day onboarding, during which churn ≈ 0):** SMB advisory retainers run **5–10%/mo** typical, **3–5%** for the better shops. We model **6% conservative, 4% base, 3% aggressive**.

**Pricing benchmarks** (anchored to research/08-competitive-landscape.md):

| Offer | Conservative | Base | Aggressive | Anchor |
|---|---|---|---|---|
| Diagnostic / "What's broken" assessment | $1,500 | $2,500 | $3,500 | SF AI Institute: $500–$2,000 strategy |
| Monthly retainer (advisory + light build) | $2,000 | $3,000 | $4,500 | SF AI Institute "$2,500/mo"; Purple Horizons "from $1,000/mo" |
| 2-week sprint / fixed-scope build | $7,500 | $12,000 | $18,000 | Maps to $150–300/hr × ~50–60 billable hrs |
| Custom 90-day build engagement | $25,000 | $40,000 | $65,000 | Mid-market boutique floor is $50K; we sit just below |
| Productized package (Yr 2+, base/aggressive) | n/a | $4,500/mo | $6,000/mo | "Replace your SaaS stack" + ongoing ops |
| SaaS spinoff ARPU (aggressive only, Yr 2+) | n/a | n/a | $99/mo | Lindy is $49.99; we'd sit slightly higher with vertical focus |

**Founder pay floor (South Florida COL):** Broward/Miami-Dade median household income ~$72K. Livable single-earner draw with working partner: **$60K minimum**. Comfortable couple: **$140–180K combined**. True abundance (mortgage, two cars, healthcare, kids): **$250K+ combined**. We model:
- Conservative: $60K each = $120K combined (subsistence)
- Base: $72K → $96K → $144K each (Yr 3 combined: $288K)
- Aggressive: $84K → $120K → $180K each (Yr 3 combined: $360K)

These are owner draws, not salaries — SE tax / quarterly estimateds borne by founders. We include them in EBITDA-after-founder-pay because that's the real test of business viability.

**COGS:** Pure consulting ≈ zero COGS (founder time lives in pay). We allocate **3–5% of revenue** for cloud passthrough, engagement-specific licenses, and one-off contractor hours. Productized packages: ~8%. SaaS spinoff (aggressive only): 25%.

**Operating costs (Year 1 base, itemized monthly):**

| Bucket | $/mo |
|---|---|
| SaaS stack (Vercel $20, Workspace $24, Calendly $32, Buttondown $29, Notion $20, 1Password $20, QBO $50, marketing tools $100) | $295 |
| AI APIs (Anthropic + OpenAI, scales with revenue) | $200 |
| Professional services (accounting $300, legal $150) | $450 |
| Insurance (E&O $150 + 2× marketplace health $1,400) | $1,550 |
| Home-office allocation (phone/internet) | $100 |
| Travel + client meetings | $200 |
| Misc / contingency | $200 |
| **Total** | **~$3,000/mo ($36K/yr)** |

Scales to ~$3,500/mo Yr 2 (API + fractional's tools), ~$4,200/mo Yr 3.

**Fractional hire:** Part-time ops/build contractor, 10–20 hrs/wk, $75–100/hr. **Base: $60K Yr 2 → $90K Yr 3; aggressive: starts month 9 Yr 1 at $36K annualized.** Per Sullivan, the first "Who" — an automation engineer or ops generalist who absorbs production so founders stay on advisory + sales.

---

## Pricing benchmarks

| Source (live, Apr 2026) | Offer | Price |
|---|---|---|
| South Florida AI Institute | Strategy / Retainer | $500–$2,000 / from $2,500/mo |
| Purple Horizons (Miami) | Retainer | from $1,000/mo |
| AI Automation Agency (UK) | Support tier | £87/wk (~$455/mo) |
| Mid-market boutiques | Project floor | $50K–$250K |
| Goldman Sachs SMB AI survey | Median monthly AI spend | $28/mo |
| User-stated comp | Hourly consulting | $150–300/hr |
| Lindy (SaaS, not consulting comp) | Pro tier | $59.99/mo |

**GVC posture:** sit at/just above SF AI Institute on retainer ($3,000/mo base, premium defensible via Mel's 20-yr ops record). Lead the homepage with a $2,500 fixed-scope "What's broken" diagnostic — lower-commitment than the 90-day engagement everyone else sells. The $28/mo SMB median spend means $2,500/mo is a category jump, not a line-item upsell — sell it that way.

---

## Scenario A — Conservative

Slow ramp, 1 paid client/mo for first 6 months, diagnostics + low-end retainers, floor pricing, 6%/mo churn after 90-day onboarding, no fractional hire, subsistence draws.

### Year 1 monthly cash flow

| Mo | Active ret. | Project rev | Retainer rev | Total rev | Op | COGS | Draws | Net cash |
|---|---|---|---|---|---|---|---|---|
| 1 | 0 | $1,500 | $0 | $1,500 | $3,000 | $75 | $10,000 | -$11,575 |
| 2 | 1 | $1,500 | $2,000 | $3,500 | $3,000 | $175 | $10,000 | -$9,675 |
| 3 | 2 | $1,500 | $4,000 | $5,500 | $3,000 | $275 | $10,000 | -$7,775 |
| 4 | 2 | $7,500 | $4,000 | $11,500 | $3,000 | $575 | $10,000 | -$2,075 |
| 5 | 3 | $1,500 | $6,000 | $7,500 | $3,000 | $375 | $10,000 | -$5,875 |
| 6 | 4 | $1,500 | $8,000 | $9,500 | $3,000 | $475 | $10,000 | -$3,975 |
| 7 | 3 | $0 | $6,000 | $6,000 | $3,000 | $300 | $10,000 | -$7,300 |
| 8 | 3 | $7,500 | $6,000 | $13,500 | $3,000 | $675 | $10,000 | -$175 |
| 9 | 4 | $1,500 | $8,000 | $9,500 | $3,000 | $475 | $10,000 | -$3,975 |
| 10 | 5 | $1,500 | $10,000 | $11,500 | $3,000 | $575 | $10,000 | -$2,075 |
| 11 | 4 | $0 | $8,000 | $8,000 | $3,000 | $400 | $10,000 | -$5,400 |
| 12 | 5 | $7,500 | $10,000 | $17,500 | $3,000 | $875 | $10,000 | $3,625 |
| **Yr 1** |  | **$33,000** | **$72,000** | **$105,000** | **$36,000** | **$5,250** | **$120,000** | **-$56,250** |

Mix: 1 diag/mo months 1–10 (8 → retainers, 2 walk away), 2 sprints (mo 4, 8), 1 sprint + retainer mo 12. Retainer base churns at 6%/mo after 90-day onboarding (-1 each at mo 7 and mo 11).

**Conservative does not pay back founder draws in Year 1.** Business loses ~$56K against the $120K combined draw — Matt + Mel each effectively realize ~$32K in real income, the rest funded from personal savings or partner income. Cash-flow positive only in month 12 with a one-off sprint.

### 3-Year P&L — Conservative

| Year | Revenue | COGS | Gross profit | Op costs | Founder pay | EBITDA | EBITDA margin |
|---|---|---|---|---|---|---|---|
| Yr 1 | $105,000 | $5,250 | $99,750 | $36,000 | $120,000 | -$56,250 | -53.6% |
| Yr 2 | $192,000 | $9,600 | $182,400 | $42,000 | $140,000 | $400 | 0.2% |
| Yr 3 | $264,000 | $13,200 | $250,800 | $48,000 | $160,000 | $42,800 | 16.2% |

Yr 2 breakeven; Yr 3 modest margin available for reserve-building. **This case keeps the lights on but does not fund abundance — it's a survival scenario.** Yr 1 requires personal savings to bridge.

---

## Scenario B — Base case

Realistic ramp leveraging Mel's network (33% warm-referral conversion) + existing GVC brand. 1.5 wins/mo months 1–6 → 2/mo by month 9. Mid-range pricing. Productized "Replace Your SaaS Stack" launches month 13. Fractional hire onboards month 18 at 12 hrs/wk. 4%/mo churn.

### Year 1 monthly cash flow

| Mo | Active ret. | Project rev | Retainer rev | Total rev | Op | COGS | Draws | Net cash |
|---|---|---|---|---|---|---|---|---|
| 1 | 1 | $2,500 | $3,000 | $5,500 | $3,000 | $275 | $12,000 | -$9,775 |
| 2 | 2 | $2,500 | $6,000 | $8,500 | $3,000 | $425 | $12,000 | -$6,925 |
| 3 | 2 | $14,500 | $6,000 | $20,500 | $3,000 | $1,025 | $12,000 | $4,475 |
| 4 | 3 | $2,500 | $9,000 | $11,500 | $3,000 | $575 | $12,000 | -$4,075 |
| 5 | 5 | $5,000 | $15,000 | $20,000 | $3,000 | $1,000 | $12,000 | $4,000 |
| 6 | 5 | $14,500 | $15,000 | $29,500 | $3,000 | $1,475 | $12,000 | $13,025 |
| 7 | 5 | $2,500 | $15,000 | $17,500 | $3,000 | $875 | $12,000 | $1,625 |
| 8 | 6 | $14,500 | $18,000 | $32,500 | $3,000 | $1,625 | $12,000 | $15,875 |
| 9 | 7 | $12,500 | $21,000 | $33,500 | $3,000 | $1,675 | $12,000 | $16,825 |
| 10 | 7 | $13,300 | $21,000 | $34,300 | $3,500 | $1,715 | $12,000 | $17,085 |
| 11 | 7 | $13,300 | $21,000 | $34,300 | $3,500 | $1,715 | $12,000 | $17,085 |
| 12 | 7 | $12,000 | $21,000 | $33,000 | $3,500 | $1,650 | $12,000 | $15,850 |
| **Yr 1** |  | **$109,600** | **$171,000** | **$280,600** | **$37,500** | **$14,030** | **$144,000** | **$85,070** |

Engagement mix powering this: 1 diag/mo months 1–8 (12 diagnostics × $2,500), 3 sprints (months 3, 6, 8, 12), 1 custom build won month 9 ($40K spread mo 9–11), retainer base growing 1→7 with 1 churn each at mo 7 and mo 11.

Year 1 base case lands at **~$281K** revenue (includes one $40K custom build won late in year). Cash-flow positive (after draws) by **month 3**, sustainably positive from month 5. Founders take $144K combined; ~$85K retained for reserves, taxes, Yr-2 reinvestment.

### 3-Year P&L — Base case

| Year | Revenue | COGS | Gross profit | Op costs | Founder pay | EBITDA | EBITDA margin |
|---|---|---|---|---|---|---|---|
| Yr 1 | $280,600 | $14,030 | $266,570 | $37,500 | $144,000 | $85,070 | 30.3% |
| Yr 2 | $456,000 | $25,000 | $431,000 | $48,000 | $192,000 | $106,000 (incl. -$60K hire) → $46,000 net | 10.1% |
| Yr 3 | $612,000 | $36,000 | $576,000 | $52,000 | $288,000 | $146,000 (incl. -$90K hire) → $146,000 net | 23.9% |

**Yr 2:** productized launches with 4 inaugural clients at $4,500/mo (~$216K ARR) + 6 full-price retainers + 2 builds. Fractional hire (-$60K) compresses EBITDA but lifts ceiling. Draws step to $96K each.

**Yr 3:** 8 retainers + 4 productized + 2 full-year builds. Fractional scales to $90K. Draws hit $144K each ($288K combined) — abundance range. ~$146K EBITDA distributable / reinvestable.

---

## Scenario C — Aggressive

Premium pricing. Mel's network + Matt's writing + SEO compounds into 2–3 wins/mo from month 4. Capacity-bound by month 9 → fractional hire starts month 9 at $36K annualized. Productized launches month 8. SaaS spinoff (hospitality-vertical AI tool) launches month 14, reaches 60 paid users by end Yr 2. 3%/mo churn.

### Year 1 cash flow (highlights)

| Mo | Active retainers | Total rev | Founder draws | Net cash after draws |
|---|---|---|---|---|
| 1 | 1 | $7,500 | $14,000 | -$8,000 |
| 3 | 4 | $24,500 | $14,000 | $7,000 |
| 6 | 7 | $48,000 | $14,000 | $30,500 |
| 9 | 10 (cap hit, hire start) | $61,000 | $14,000 | $35,000 (incl. $3K/mo hire) |
| 12 | 11 + productized launch | $72,500 | $14,000 | $44,500 |
| **Yr 1 totals** |  | **$487,000** | **$168,000** | **~$229,000** |

Aggressive Yr 1: ~$487K revenue, cash-flow positive **month 3**, founders draw $84K each, ~$229K retained.

### 3-Year P&L — Aggressive

| Year | Revenue | COGS | Gross profit | Op costs | Founder pay | EBITDA | EBITDA margin |
|---|---|---|---|---|---|---|---|
| Yr 1 | $487,000 | $24,350 | $462,650 | $42,000 | $168,000 | $216,650 (incl. -$15K Yr-1 hire) → $217K | 44.5% |
| Yr 2 | $748,000 (+$72K SaaS) = $820,000 | $52,000 (incl. SaaS COGS 25%) | $768,000 | $58,000 | $240,000 | $360,000 (incl. -$110K hire) → $360K | 43.9% |
| Yr 3 | $980,000 (consulting) + $216,000 (SaaS) = $1,196,000 | $98,000 | $1,098,000 | $72,000 | $360,000 | $456,000 (incl. -$140K hire + 2nd hire) → $456K | 38.1% |

Aggressive crosses $1M Yr 3, SaaS spinoff ~18% of revenue at higher margin, EBITDA after pay nears half a million. **Requires the SaaS spinoff to actually work** — consulting alone caps ~$750–800K with the modeled hire structure (the 2+1 ceiling is real).

---

## Founder pay analysis

**South FL cost-of-living anchor (Broward/Miami-Dade, 2026):** median household income ~$72K; comfortable two-earner household $150–180K combined; family-with-kids floor $200K+; genuine abundance (house, two cars, college savings) $250–350K combined.

| Scenario | Yr 1 each | Yr 2 each | Yr 3 each | Yr 3 combined | Quality of life |
|---|---|---|---|---|---|
| Conservative | $60K | $70K | $80K | $160K | Subsistence; below FL dual-earner median |
| Base | $72K | $96K | $144K | $288K | Above local median; by Yr 3 reaches genuine abundance |
| Aggressive | $84K | $120K | $180K | $360K | Top-quintile FL household; real wealth-building runway |

**Comparison to benchmark:** SCORE/Payscale 2025 shows $95–115K per founder for established 2-person shops grossing $300–600K. Base Yr 3 ($144K each) sits above benchmark — defensible because zero COGS and the founder pair captures all delivery value. Conservative Yr 3 ($80K) sits below — reinforcing that conservative is survival, not target.

**Honest takeaway:** Year 1 founder pay in every scenario is below what Matt or Mel could earn as senior employees elsewhere. Years 2–3 base/aggressive recapture and exceed market wage. **The opportunity cost of bootstrapping is real and front-loaded.**

---

## Capital needs

**Operating reserve (recommended floor):** **$30K** = 3 months op costs + 1 month founder draws at base. Buffers Q1 lumpiness, anchor-client churn, slow quarters. Build from Yr 1 retained earnings (base/aggressive) or pre-launch personal savings (conservative).

**Line of credit (optional):** $50K via Brex/Mercury or regional bank, undrawn unless a major client delays payment 60+ days. Not modeled in any base case.

**No outside capital required in any scenario.** Conservative needs personal savings to bridge Yr-1 draw shortfall. Base/aggressive self-fund from Yr 1 onward. The aggressive SaaS spinoff is the only line that could justify external capital — and even $50–100K seed could come from base-case retained earnings.

**Tax reserve:** **25–30% of net business income** for federal + SE tax. Base Yr 3: ~$36K of the $146K EBITDA. **Florida has no state income tax — structural advantage of ~3–5% margin vs. NY/CA-based competitors.**

---

## What "abundance" looks like at end-of-year-3 (base case)

**$612K revenue, $288K combined founder pay, ~$146K EBITDA after pay & hire.**

The shape:
- 8 retainers ($24K/mo) + 4 productized clients ($18K/mo) + 2 builds/yr (~$80K) + ~20 diagnostics/yr ($40K)
- 1 fractional hire (~25 hrs/wk, $90K/yr) absorbing production, freeing founders for advisory + sales + content
- Founders **work ~30–35 hrs/wk each — not 60.** They've chosen the ceiling rather than blown through it
- Brand owns "AI advisory layer above your vertical SaaS" for South FL service businesses (hospitality, F&B, wellness)
- "Replace Your SaaS Stack" productized package = predictable MRR at higher dollar/hour than custom retainers
- Cash: ~$50K op reserve + ~$50K tax reserve + ~$50K distributable / reinvestable

**Optionality at end-of-Yr-3:** (a) bank cash and stay artisanal, (b) second fractional and stretch toward $1M, (c) spin out vertical SaaS using accumulated client data + templates, (d) license methodology / write the book / build audience and let consulting feed the platform. All four are credible. None require a Series A.

**The honest version:** what most consulting firms aspire to and few achieve — predictable revenue, sane hours, real take-home pay, four directions to grow. Call it a **leverage-ready studio**.

---

## The 10x scenario — credible or not?

10x base = **$6.1M revenue Year 3.** What would have to be true:

1. Productized package becomes primary line (>$3M/yr) → ~55 active clients at $4,500/mo, 5x the dual-founder + 1-fractional ceiling → **6–8 person team** by end Yr 2
2. SaaS spinoff hits ~$2M ARR → ~1,700 paid users at $99/mo → real product motion + dedicated eng team + likely $500K–$1.5M outside capital
3. Custom builds line scales to $1M+ → 15–20 builds/yr → delivery team of 4+ engineers
4. Marketing engine generates 30+ qualified leads/mo → far beyond Mel-network + Matt-content cap → requires paid acquisition + content team

**Verdict: Not credible as a bootstrapped path.** Requires either $1–3M outside capital or a 5-year horizon. The dual-founder ceiling is the fundamental constraint; breaking it changes the business model from studio to company — different bet, different risks (productized churn, hiring cycles, real overhead).

**A credible 3x stretch (~$1.8M Yr 3)** exists between aggressive and 10x: aggressive SaaS launch + 2 fractionals + 1 full-time engineer + double productized velocity. Worth modeling if Yr 1 results validate demand.

**Recommendation:** plan for base, prepare for aggressive, do not bet the company on 10x. The 10x narrative is useful for fundraising decks; it is misleading for operating decisions.

---

## Sensitivities — what changes the picture

| Variable | Base assumption | If 1 std dev worse | If 1 std dev better | Impact on Yr 3 EBITDA |
|---|---|---|---|---|
| Avg retainer price | $3,000/mo | $2,400/mo | $3,600/mo | ±$58K (±40%) |
| Monthly churn | 4% | 7% | 2% | ±$45K (±31%) |
| Diagnostics → retainer conversion | 60% | 40% | 80% | ±$36K (±25%) |
| New client wins per month | 1.8 avg | 1.2 | 2.4 | ±$72K (±49%) |
| Op costs | $48K/yr | $66K/yr | $36K/yr | ±$18K (±12%) |
| Fractional hire timing | Mo 18 | Mo 24 | Mo 12 | ±$25K (capacity-driven) |

**Top three variables to manage:** (1) New-client-wins-per-month, (2) avg retainer price, (3) churn. Pricing and churn are the two highest-leverage levers — a $300/mo price increase across the book is mathematically equivalent to landing 3 extra clients/year, but operationally far easier. **The first business-development priority after Year 1 should be an annual retainer-price review with existing clients.**

---

## Sources / benchmarks

- /Users/fp/Desktop/good-vibes-coding/docs/research/2026-04-28-marketing-refresh/05-smb-ai-gap.md — SMB AI adoption rates, $28/mo median spend, 14% integration rate
- /Users/fp/Desktop/good-vibes-coding/docs/research/2026-04-28-marketing-refresh/08-competitive-landscape.md — SF AI Institute pricing ($500–2K diag, $2,500/mo retainer); Purple Horizons $1,000/mo; Lindy $49.99/mo; AI Automation Agency £87/wk; mid-market floor $50K project
- Goldman Sachs 10KSB Survey (Feb 2026) — 76% adoption / 14% integrated, $28/mo median spend
- JP Morgan Chase Institute SMB AI Report (2025) — $250K+ revenue cohort 22.5% adoption
- US Census Broward County ACS 2024 — median household income $72K, used for FL cost-of-living anchor
- Sullivan & Hardy, "Who Not How" (2020) — capacity ceiling framework, fractional-first hiring sequence
- SCORE / Payscale 2025 owner-comp benchmarks — $95–115K median for 2-person established consulting firms
- NFIB 2025 Small Business Technology Survey — 21–24% AI use among 1–9 employee firms (target ICP cohort)
- Industry SaaS / consulting churn benchmarks — ProfitWell + RecurringRevenue blogs, 5–10%/mo SMB advisory range
