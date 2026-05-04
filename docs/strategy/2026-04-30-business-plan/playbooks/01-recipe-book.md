---
title: GVC Recipe Book — Product Delivery Playbooks
date: 2026-04-30
type: playbook
---

## How to use this book

Line-by-line manual for the nine GVC products. Pull Recipes 1–3 for almost every cold conversation: AI Visibility is the cheapest first-yes, Menu+Reviews is the warmest restaurant pitch, AI Front-Desk has the only built-in retainer. Pull Recipe 4 on Poconos main streets, never in Boca. Pull Recipe 5 when an owner mentions a star employee retiring. Pull Recipe 6 only after 5 single-product wins. Hold Recipes 7–9 until we have physical-presence trust in the Pocs corridor — they close because the operator met us at three Chamber breakfasts and a library workshop. Every recipe replaces a named SaaS line item. If we can't name what we're killing, we don't take the deal.

## Quick reference matrix

| # | Product | Sprint | Length | Retainer | SaaS replaced | Geo | Repro |
|---|---|---|---|---|---|---|---|
| 1 | AI Visibility Tune-Up | $750 | 5 days | $250/mo Watch | Yext, BrightLocal | Both | 5 |
| 2 | Menu + Reviews Lite | $1,500 | 1 week | $300/mo Hospitality Lite | Bloom, Birdeye, OpenMenu | Both | 4 |
| 3 | AI Front-Desk | $1,800 | 2 weeks | $200/mo built-in | Goodcall, Numa, Rosie | Both | 4 |
| 4 | Vacation Rental Direct-Booking | $2,400 | 2 weeks | $400/mo | Hostfully, Lodgify, Airbnb take | Pocs | 4 |
| 5 | SOP Lite | $2,200 | 2 weeks | $300/mo wiki keep-alive | Trainual, Notion AI | Both | 3 |
| 6 | Restaurant Full Stack | $3,500 | 3 weeks | $500/mo | Yext + Birdeye + OpenMenu + Goodcall | Both (FL-led) | 4 |
| 7 | B&B Stack Consolidator | $7,500 | 3 weeks | $850/mo | eviivo + Squarespace + Mailchimp + Birdeye + The Knot | Pocs | 3 |
| 8 | Wedding-Venue Inquiry System | $6,500 | 3 weeks | $600/mo | The Knot/WeddingWire, Squarespace form-to-Gmail | Pocs | 3 |
| 9 | Outfitter Booking + Waiver | $5,500 | 3 weeks | $700/mo | Resos, Smartwaiver, paper waivers | Pocs | 3 |

---

## Recipe 1 — AI Visibility Tune-Up

**1. Pitch.** Most small businesses are invisible to ChatGPT, Google AI Overview, and Perplexity. We fix it in 5 business days for $750 flat — no Yext at $199/mo, no BrightLocal at $39. You keep the GBP, schema, FAQ, and a maintenance checklist.

**2. Deliverable.** Claimed/optimized GBP (categories, hours, services, photos, 8 Q&As). A `schema.json` block (LocalBusiness + FAQPage + vertical type) in the site head, validated. One `/faq` page, ten owner-voice answers. An `ai-search-audit.pdf` with five priority queries run pre/post against ChatGPT, Perplexity, AI Overview. A one-page `maintenance-checklist.md`. All source files in a client-owned Drive folder.

**3. Day-by-day (5 days).**
- **Day 0 (Fri):** Mel sends intake, books Monday interview. Matt runs pre-audit on five queries, saves screenshots.
- **Day 1 (Mon):** 30-min owner interview, Mel hosts, Matt records. Mel pulls owner-voice phrases for FAQ + GBP categories. Matt claims GBP if needed.
- **Day 2 (Tue):** Matt drafts schema + FAQ from transcript. Mel writes ten FAQ answers in owner voice, one Slack round of edits.
- **Day 3 (Wed):** Matt deploys schema + FAQ to live site (Squarespace code-injection / Wix custom code / WordPress snippet — no rebuild). Validates Rich Results. Seeds GBP Q&A.
- **Day 4 (Thu):** Mel uploads 8–12 photos to GBP, drafts three weekly GBP posts. Matt re-runs queries, builds side-by-side audit deck.
- **Day 5 (Fri):** 20-min handoff. Mel walks Drive + checklist. Matt offers $250/mo Watch retainer. **Total ~10 hrs first run, ~6 by client #5.**

**4. Intake.** NAP. Existing GBP login if claimed. Site CMS. Three priority queries the owner wishes they ranked for. One sentence each on who-you-serve / what-makes-you-different / what-you-wish-customers-knew. 8–12 photos.

**5. Stack.** GBP (free, client-owned). Drive. JSON-LD via Rich Results Test. ChatGPT + Perplexity + AI Overview for the audit. Loom + Stripe. Client's CMS as deploy target. **No SaaS added.**

**6. Quality checklist.** GBP claimed/verified, primary + 2 secondary categories, 8 Q&As, current hours/services, 8+ photos. Schema validates with zero errors. `/faq` indexed within 7 days. Five priority queries: AI Overview cites the business in ≥1; ChatGPT and Perplexity name it in ≥2 each. NAP citation baseline Day 1, target +5 by month 1. Maintenance `.md` in Drive. Loom in closeout email.

**7. Retainer.** Watch ($250/mo) starts Monday after closeout. Week 1: Matt re-runs queries + 5-min report; Mel writes/schedules four GBP posts. Cadence: monthly query rerun + delta report, two GBP posts/wk, schema updates as services change, quarterly review of new AI-discovery surfaces. 30-day cancel. Ladders to Recipe 2 (~25%) or to Recipe 6 at month 3+.

**8. Cold-pitch.** "We ran ChatGPT against your business this morning. Here's what it said. Want it fixed for $750 by Friday?"

**9. Geography.** Both. Identical recipe in Boca and Honesdale. PB responds to the audit screenshot (proof of competence); Pocs responds to "you keep everything" (proof of trust).

**10. Reproducibility: 5/5.** ~85% templated. Bespoke: ten owner-voice FAQ answers + photo curation.

---

## Recipe 2 — Menu + Reviews Lite

**1. Pitch.** Restaurants and small inns pay OpenMenu $30, Bloom $99, Birdeye $300 — and the menus drift, reviews go unanswered, the allergen page is a Word doc. We rebuild the menu (or amenity sheet) as one source of truth, draft weekly review responses in your voice, and tag allergens (FL) or pet/accessibility (Pocs). $1,500 flat, $300/mo. Net savings: $129/mo plus three SaaS bills off the credit card.

**2. Deliverable.** Single-page menu/amenity sheet at `/menu` or `/stay`, owner-editable through a Google Sheet that pulls into the site at build. Allergen tagging (FL — pre-empts SB-68 spread) or pet/accessibility/quiet-hours tagging (Pocs) as filterable badges. Weekly AI review-response email digest (Mondays): 3–5 drafts in owner voice, one-click approve, auto-post to Google + Yelp. A `brand-voice.md` Mel writes from a 30-min interview. GBP cleanup from Recipe 1. Source repo on client's GitHub, full admin.

**3. Day-by-day (1 week).**
- **Day 0 (Fri):** Mel sends intake + books 45-min Monday interview. Matt scaffolds from `/templates/menu-reviews-lite`.
- **Day 1 (Mon):** 45-min interview — current menu, review patterns, voice rules, allergen/pet policies. Matt sets up domain, deploys placeholder.
- **Day 2 (Tue):** Matt builds menu data model in shared Google Sheet. Mel transcribes existing menu/amenity content (block 3 hrs). Matt wires Sheet to site build.
- **Day 3 (Wed):** Mel writes `brand-voice.md`. Matt builds review-response pipeline (GBP API auth + Claude prompt + Postmark digest). First dry-run digest sent end of day.
- **Day 4 (Thu):** Owner reviews staging. Mel walks Sheet edits in 20 min. Matt connects GBP API to live profile, runs first digest in dry-run.
- **Day 5 (Fri):** Live deploy. First real digest goes Saturday. 3-min Loom. Mel runs 30-min closeout, offers $300/mo. **Total ~14 hrs, ~9 by client #5.**

**4. Intake.** Domain + CMS. Current menu PDF or amenity sheet (or "in my head"). GBP login. Yelp login if used (skip Pocs — Yelp is dead there). Three sample responses the owner liked (voice tuning). Allergen list (FL) or pet/accessibility rules (Pocs). Owner email for the Monday digest.

**5. Stack.** Vercel (client account, free tier) + Next.js static export. Google Sheets API for owner edits. Claude API Sonnet 4.6. Postmark digest ($15/mo, rolled into retainer). GBP + Yelp Business APIs (free). GitHub on client account. Stripe. **Owner cancels Bloom + Birdeye + OpenMenu the week we ship.**

**6. Quality checklist.** Lighthouse mobile ≥95, loads <1.2s on 4G. Sheet edit live within 60s. Allergen/amenity badges render on three items. First Monday digest sent, owner approves, posts to Google. `brand-voice.md` signed off. `Restaurant` or `LodgingBusiness` schema validated. Three SaaS subs cancelled before retainer billing. Repo handed off.

**7. Retainer.** Hospitality Lite ($300/mo) starts Monday after closeout. Week 1: 30-min Mel voice-tuning. Cadence: weekly digest, monthly menu refresh, quarterly allergen audit, Mel on Slack. Ladders to Recipe 6 at month 3+.

**8. Cold-pitch.** "You're paying around $400/mo to OpenMenu, Bloom, and Birdeye. We replace all three with code you own for $1,500 once and $300/mo we run."

**9. Geography.** Both. **FL lean: SB-68 allergen disclosure** — multi-state operators pre-complying; Atlantic Ave and Las Olas hear "allergen tagging built in" as risk reduction worth $1,500. **Pocs lean: pet/accessibility** for B&Bs where weekenders search "dog-friendly Lake Wallenpaupack." Same recipe, different badge set.

**10. Reproducibility: 4/5.** ~75% templated. Bespoke: menu transcription + brand-voice tuning. 80+-item restaurants take an extra half day.

---

## Recipe 3 — AI Front-Desk

**1. Pitch.** You're missing 30% of after-hours calls. The dental practice loses new-patient calls at lunch, the HVAC contractor hears the phone ring elbow-deep in a condenser, the B&B owner is asleep at 2am. The market sells Goodcall at $59/mo, Numa $49, Rosie $49–$149 — generic AI receptionists, stock prompts, your call data on their server. We build custom in 2 weeks: Twilio number, Claude under the hood, your prompts, your booking rules, your data. $1,800, $200/mo.

**2. Deliverable.** Twilio number wired to a custom Claude-powered agent — answers in 1.5s, owner's FAQs + service list + booking rules as the corpus. SMS auto-responder for after-hours and missed calls. Cal.com booking (or owner SMS handoff). Warm-transfer or "we'll call back in 5" escalation. Read-only call-log + transcript dashboard at `dash.[clientdomain].com`. Twilio + Claude + Supabase credentials all in client's name; owner pays Twilio + Claude direct. Owner-editable `prompt-corpus.md`.

**3. Day-by-day (2 weeks).**
- **Days 0–1 (Fri–Mon):** Intake + 60-min interview. Mel captures FAQs, services, booking rules, escalation prefs, voicemail. Matt provisions Twilio + Claude + Supabase in client's name.
- **Day 2 (Tue):** Matt scaffolds from `/templates/front-desk`. Wires Twilio → Claude → Cal.com / SMS. Mel drafts corpus.
- **Days 3–4 (Wed–Thu):** Matt builds call flow: greeting, intent (book/question/emergency/other), branch logic, escalation. First test calls; iterates on latency and tone.
- **Day 5 (Fri):** Mel makes ten test calls as the owner's customer types. Logs awkward moments. Matt fixes overnight.
- **Days 6–7:** Off. Owner reviews `prompt-corpus.md`.
- **Day 8 (Mon, week 2):** Owner-led walkthrough — 5 real-edge-case calls. Matt logs and fixes. Mel adjusts tone.
- **Day 9 (Tue):** Build dashboard. Wire Supabase to write transcripts + structured outcomes. Owner gets read-only login.
- **Day 10 (Wed):** Soft launch — forward line to Twilio between 6pm–8am only. Watch 24 hrs.
- **Day 11 (Thu):** Full porting if soft launch was clean.
- **Day 12 (Fri):** Closeout. 20-min Loom. Day 19 retainer touchpoint scheduled. **Total ~28 hrs first build, ~16 by client #5.**

**4. Intake.** Phone + carrier (porting LOA). Owner mobile (escalation). Top 25 weekly questions (5-min voice memo). Service list + pricing rules. Booking calendar. Tone preference. Hours + after-hours policy. Credit card for Twilio + Claude pass-through.

**5. Stack.** Twilio Voice + SMS (~$20–$40/mo pass-through). Claude API Sonnet 4.6 + Haiku 4 (~$15–$30/mo pass-through). Cal.com + Vercel + Supabase free tiers (Supabase handles ~10K calls/mo). Postmark for daily summary email ($15/mo). **Cancelled SaaS:** Goodcall / Numa / Rosie ($50–$150/mo).

**6. Quality checklist.** Agent answers within 1.5s, books in <90s. Ten Mel-driven test calls: book new, reschedule, cancel, after-hours emergency, "talk to a human," wrong-number, three FAQs, Spanish fallback (FL). Owner has placed 5 calls and signed off on tone. SMS auto-responder fires within 30s of missed call. Booking confirmation in calendar within 60s. Dashboard shows last 50 calls + transcripts. All credentials in owner's name — owner can fire us tomorrow and the agent still runs.

**7. Retainer.** $200/mo built-in from day 1. Day 19: 30-min review — go through every fumble, ship 3–5 corpus tweaks by EOD. Cadence: monthly review, prompt-tuning as needed, Mel on Slack. Month 2 upsell: SMS reply tier (+$100/mo). Month 6 upsell: $2,500/mo Operations Retainer once ROI is documented.

**8. Cold-pitch.** "You're missing calls. Goodcall is $59/mo for a stock receptionist on their server. We build the same thing custom-trained on your FAQs in 2 weeks. $1,800 + $200/mo. You own it."

**9. Geography.** Both. **PB:** HVAC, dental, salons, dermatology — missed call = $400 customer. **Pocs:** B&Bs, contractors, lake-rental owners — owner is the front desk by default. Same recipe, vertical-flavored prompts. Demo number on homepage answers as "Bistro Mizner" by default, "Pocono Plumbing" if cookie says Poconos.

**10. Reproducibility: 4/5.** ~70% templated (Twilio + Claude + Cal.com + Supabase scaffold). Bespoke: corpus, voice, escalation. New vertical adds ~4 hrs first time, drops to 0 second time.

---

## Recipe 4 — Vacation Rental Direct-Booking

**1. Pitch.** Airbnb takes 14–18% of every booking on your Lake Wallenpaupack cabin. The alternatives are Hostfully at $119/mo or Lodgify at $16–$45/mo — lock-in SaaS with a generic guest portal. We build a direct-booking site you own: Stripe checkout, iCal sync to Airbnb + VRBO so nothing double-books, AI SMS concierge for "what's the door code" texts. $2,400 once, $400/mo. Pays for itself in six to ten bookings.

**2. Deliverable.** Next.js direct-booking site at `book.[ownerdomain].com`. Stripe Checkout on owner's account, no platform fee. iCal two-way sync to Airbnb + VRBO + Google Calendar. AI SMS guest concierge trained on the property guide. A `property-guide.md` from a 60-min walkthrough — doubles as the printable in-house binder. Owner-editable nightly rates + min-stay in Notion. All credentials on owner's account.

**3. Day-by-day (2 weeks).**
- **Days 0–1 (Fri–Mon):** Intake. Mel runs 60-min walkthrough call (owner walks the house with phone on speaker). Matt scaffolds repo + buys domain if needed.
- **Day 2 (Tue):** Matt wires Stripe Checkout, calendar logic, nightly-rate model. Mel transcribes walkthrough into `property-guide.md`.
- **Day 3 (Wed):** Matt sets up iCal export + import. Tests double-booking races.
- **Day 4 (Thu):** Matt builds SMS concierge on Twilio + Claude with property guide as corpus. Mel writes welcome SMS sequence (booked / 7 days / day-of / day-after / 3-day review).
- **Day 5 (Fri):** Owner reviews staging. Test booking with $1 hold, refunded.
- **Days 6–7:** Off.
- **Day 8 (Mon, week 2):** Live launch. Airbnb description gets "book direct at [URL]" line where allowed.
- **Day 9 (Tue):** Mel writes email-blast template for past-guest list.
- **Day 10 (Wed):** First real bookings. Matt monitors Stripe + iCal hourly for 48 hrs.
- **Day 11 (Thu):** Owner-led admin tour: rates, blocked dates, dashboard.
- **Day 12 (Fri):** Closeout. **Total ~30 hrs, ~18 by client #3.**

**4. Intake.** Property address + nightly rate range + min-stay. Airbnb + VRBO listing URLs. Owner's Stripe (or we set up). Owner's domain (or we buy fresh). Door code / lock setup. Existing house manual in any form. Past-guest list if any.

**5. Stack.** Vercel + Next.js. Stripe (~2.9% + 30¢, owner's account — same processor Airbnb uses, no 14% take). Twilio (~$15/mo). Claude (~$10/mo). iCal + Notion (free). **Cancelled SaaS:** Hostfully ($119/mo) and/or Lodgify ($45/mo), plus 14–18% Airbnb take on every direct booking.

**6. Quality checklist.** Test booking in owner's calendar within 60s. iCal sync prevents a double-book in a race test. Concierge answers door code / wifi / checkout within 5s of SMS. Property guide signed off. Email-blast template ready. Credentials on owner's account. Airbnb language updated where T&Cs allow.

**7. Retainer.** $400/mo Property Concierge starts month 2. Cadence: weekly iCal audit, monthly photo refresh, monthly concierge-transcript review (we tune for repeats), quarterly rate-strategy review (AirDNA scrape — we pull, owner decides). Ladders to Recipe 7 if owner picks up a second/third property.

**8. Cold-pitch.** "Airbnb takes 17% of every booking on your cabin. We build a direct-booking site for $2,400. Pays for itself in six bookings. Keep Airbnb and the site live."

**9. Geography.** **Pocs-led, PB skip.** Pocs has 11K+ HomeToGo + 5.6K VRBO listings, owner-operator avg 1–10. PB inventory is condo/concierge-managed — pitch doesn't sing on Worth Avenue. PA STR tightening across Pike/Wayne/Monroe + NY's STR digital registry in Sullivan = 2026 conversation-starter.

**10. Reproducibility: 4/5.** ~70% templated (site, Stripe, iCal, concierge). Bespoke: property guide is highly variable — a 12-room Settlers Inn vs. a one-bedroom cabin.

---

## Recipe 5 — SOP Lite

**1. Pitch.** The most expensive software you pay for is the brain of the one employee about to retire. Maria has been opening the bakery since 2009. The SaaS market sells Trainual at $299/mo or Notion AI at $16 plus a $4K onboarding consultant. We film one workflow, transcribe it, and ship a searchable wiki the new hire can ask questions of in plain English. $2,200 once, $300/mo. WikiFold (our free tool) is the engine — no SaaS subscription on top.

**2. Deliverable.** One core workflow filmed end-to-end (Mel + Matt on site half a day, or remote Loom-led). Verbatim transcripts in `/sources` on client's Drive. WikiFold-powered searchable wiki at `wiki.[clientdomain].com`, 15–25 articles. AI search — new hire types "how do I close out the register on a Sunday" and gets the right article + relevant 30s of video. 1-page "first 90 days" checklist. Source video + transcripts owned by client.

**3. Day-by-day (2 weeks).**
- **Days 0–1 (Fri–Mon):** Intake. Mel + Matt scope the workflow: which one matters most, who runs it now, firing order if it breaks.
- **Day 2 (Tue):** Filming day (4–6 hrs). Matt camera, Mel interviews. Owner shadows the employee. Messy and raw, no script, no second takes. Don't skimp.
- **Day 3 (Wed):** Whisper transcription, saved to `/sources`.
- **Day 4 (Thu):** Mel runs WikiFold's `chunk_source` and `integrate_source`. First 8–10 articles drafted.
- **Day 5 (Fri):** Mel completes article set (15–25). Matt deploys wiki to subdomain.
- **Days 6–7:** Off. Owner reviews on phone.
- **Day 8 (Mon, week 2):** Star employee reviews articles, edits anything wrong. Mel updates.
- **Day 9 (Tue):** Matt wires AI search — Claude over wiki content with citations to source article + timestamped clip.
- **Day 10 (Wed):** "New hire test" — owner asks five real questions. Mel logs gaps, Matt fills.
- **Day 11 (Thu):** 90-day checklist + quarterly staleness audit.
- **Day 12 (Fri):** Closeout. Loom on adding a new source. **Total ~26 hrs.**

**4. Intake.** The one workflow ("if this employee left tomorrow, the business stops"). Employee name + role. Schedule a 4–6 hr filming block in the next 7 days. Owner sign-off that the employee knows we're filming and is OK with it (non-negotiable). Existing SOP docs in any form.

**5. Stack.** WikiFold (GVC's free MCP-driven wiki — `mcp__goodvibes-coding-wiki__*`). Wiki owned by client; WikiFold is the engine, not a SaaS. Whisper (locally run). iPhone or DSLR + lavalier mic (we bring the gear). Vercel (free). Claude (~$10/mo). **Cancelled SaaS:** Trainual ($299/mo) or Notion AI ($16) plus the planned $4K onboarding consultant.

**6. Quality checklist.** Workflow end-to-end captured, no gaps. All segments transcribed, in `/sources`. 15+ articles, ≤500 words each, each linked to a timestamp. AI search returns right article + clip for 8 of 10 questions. Staleness audit scheduled quarterly. Star employee signed off. 90-day checklist drafted.

**7. Retainer.** $300/mo Wiki Keep-Alive starts month 2. Cadence: monthly staleness audit + 2–3 article updates, quarterly on-site (or detailed Zoom) for one new workflow chunk, Mel on Slack. Ladders to Recipe 7 (multi-property hospitality) or a future "SOP Full" sprint.

**8. Cold-pitch.** "Maria's been opening for 17 years. When she retires, the business doesn't. We capture her workflow on video and turn it into a wiki the next hire can ask. $2,200, two weeks."

**9. Geography.** Both. Slowest cold-converter — pain is invisible until pointed out. Audit-style offer when conversation surfaces an aging employee. PB: family-owned restaurants and trades with a 60+ year-old foreman. Pocs: multi-generation B&Bs and outfitters where the operator is also the institutional memory.

**10. Reproducibility: 3/5.** ~50% templated (WikiFold pipeline, transcription, search wiring). Every workflow is its own animal. Margin holds because price tolerates variance.

---

## Recipe 6 — Restaurant Full Stack

**1. Pitch.** A single-location indie pays ~$588/mo for a SaaS stack that doesn't talk to itself: Yext $199, Birdeye $300, OpenMenu $30, Goodcall $59. Menus drift, reviews go unanswered, the receptionist sounds like a robot, Google doesn't know your hours changed. We replace all four with one integrated system you own. $3,500 once, $500/mo, three weeks. Net savings: $88/mo plus four SaaS bills off the credit card and a system that behaves like one restaurant.

**2. Deliverable.** Combined deliverables of Recipes 1, 2, 3, integrated. Plus a unified `restaurant-dashboard.[clientdomain].com` showing menu, reservations, calls, reviews on one screen. One Notion (or Sheet) source of truth feeds menu + GBP service list + agent corpus. Edit once, propagates everywhere.

**3. Day-by-day (3 weeks).**
- **Week 1:** Recipe 1 compressed (3 days) + intake for Recipes 2 + 3. Schema, GBP, FAQ shipped Day 3. Matt scaffolds Recipes 2 + 3 repos in parallel Days 4–5.
- **Week 2:** Recipe 2 cycle. Menu page + review digest live by Day 10.
- **Week 3:** Recipe 3 compressed (corpus draws on the menu and FAQ already shipped). Phone agent live Day 14, integrated dashboard Day 15, closeout. **Total ~50 hrs.** We charge less than the sum of standalones ($3,500 vs $4,050) — bundle's value is retention: one $500/mo retainer with three surfaces is stickier than three separate retainers.

**4. Intake.** Combined intake of Recipes 1, 2, 3 on one merged form. Plus a 90-min on-site or Zoom where the owner walks through a typical service — the recording is voice input for the agent and the menu rebuild simultaneously.

**5. Stack.** Combined stack of Recipes 1, 2, 3. No new tools. Unification is in the data model: one Notion page powers everything. **Cancelled SaaS:** Yext + Birdeye + OpenMenu + Goodcall (~$588/mo). Owner pockets ~$88/mo + owns the code.

**6. Quality checklist.** Combined checklists of Recipes 1, 2, 3, plus: Notion edit propagates to GBP + menu + agent corpus + FAQ within 5 min. Dashboard shows last 7 days on one screen. All four SaaS subs cancelled. First case study draft live within 30 days of launch.

**7. Retainer.** $500/mo Restaurant Operations starts month 2. Cadence: monthly review across all three surfaces, weekly digests, quarterly audit, Mel on Slack. Ladders to $1,500/mo Hospitality Operations Retainer at month 6 if owner adds a second location or wants seasonal-menu management.

**8. Cold-pitch.** "Quick question about the $588/mo your restaurant spends on Yext, Birdeye, OpenMenu, Goodcall — what if you owned it instead?"

**9. Geography.** **Both, FL-led.** PB has indie-restaurant density (Atlantic Ave Delray, Las Olas, Mizner, Clematis) + cash flow to absorb $3,500 + $500/mo. Pocs uses a stripped variant at same price (Heron, Laundrette, Sarah Street Grill) — agent skips reservation flow, adds "directions from the highway." **Reserve as homepage anchor only after 5+ standalone wins.**

**10. Reproducibility: 4/5.** Inherits templating of Recipes 1–3. Integration glue (one Notion → three surfaces) is templated by client #3. Sprint #5 runs at ~32 hrs.

---

## Recipe 7 — B&B Stack Consolidator

**1. Pitch.** A 12-room inn in Hawley or a Catskills weekender like Hotel Fauchère pays eviivo $300, Squarespace $50, Mailchimp $30, Birdeye $200, The Knot $1,200/yr — ~$680/mo total, all in different vocabularies, none talking. We replace four with one $850/mo system in your voice: booking engine, site, email, review responses, one dashboard. $7,500 build, no contract. Pays for itself in 11 months.

**2. Deliverable.** Custom booking engine (Stripe + room inventory + iCal sync) replacing eviivo / Cloudbeds / Little Hotelier. New marketing site replacing Squarespace, owner-editable through Notion. Email-marketing engine (segmented past-guest list, welcome / pre-stay / post-stay sequences) replacing Mailchimp. Recipe 2 review-response tuned for inn voice. Recipe 3 AI Front-Desk in inn mode. Unified `inn-dashboard` showing occupancy, reservations, email, reviews. All credentials on owner's account.

**3. Day-by-day (3 weeks).**
- **Week 1:** On-site discovery (both founders fly up for a Pocs residency). Inventory audit, 90-min owner interview, 60-min staff interview, 30-min walkthrough. Days 3–5: Matt scaffolds booking engine + site + email engine; Mel writes brand voice and stay sequences.
- **Week 2:** Booking engine + site on staging. iCal sync to Booking.com + Expedia (keep discovery, beat the take). Past-guest list imported + first welcome sequence drafted.
- **Week 3:** AI Front-Desk + review-response + integrated dashboard. Cutover Day 13 (parallel for 48 hrs). Day 15: closeout. **Total ~80 hrs.** Margin is in the retainer over 24 months.

**4. Intake.** Existing eviivo / Cloudbeds / Little Hotelier login + room inventory + rate schedule. Booking.com + Expedia logins (we wire iCal). Past-guest list CSV from Mailchimp. The Knot listing URL (we may keep, may kill). Squarespace login. Owner + GM + housekeeping lead names + roles. Three to five past review responses the owner liked.

**5. Stack.** Vercel + Next.js. Stripe. Custom booking engine on Supabase. Resend or Postmark (~$20/mo). Twilio + Claude (front-desk). iCal for OTA sync. **Cancelled SaaS:** eviivo + Squarespace + Mailchimp + Birdeye (sometimes The Knot). $580–$680/mo replaced.

**6. Quality checklist.** Test bookings: direct + via Booking.com, both in dashboard within 5 min. Past-guest list imported, first campaign sent without spam-trigger. Front-Desk handles 10 inn-specific calls. Review-response digest live, first batch approved. Dashboard shows occupancy + funnel + email + reviews on one screen. All four SaaS subs cancelled. On-site closeout (or Zoom + visit within 60 days).

**7. Retainer.** $850/mo starts month 2. Month 1: weekly 30-min reviews, settle booking-engine kinks, tune the agent, ship a second campaign. Cadence: monthly on-site or Zoom (anchored to one of the three Pocs residency weeks/yr), weekly digests, monthly campaign, quarterly rate-strategy session. Highest-LTV product in the book.

**8. Cold-pitch.** "Your inn pays around $680/mo for eviivo, Squarespace, Mailchimp, and Birdeye. We replace four with one $850/mo system in your voice, one dashboard. Setup $7,500. No contract."

**9. Geography.** **Pocs only, post-trust.** Do not cold-pitch. First call lands only after we've met the owner at a Wayne County Chamber breakfast, run a library workshop they attended, or got introduced by a Sullivan Catskills VA contact. First-call: Settlers Inn, Hotel Anthracite, North Branch Inn, Ledges, Glass, Hotel Fauchère, Arnold House, DeBruce. PB has hotels, not B&Bs of this profile.

**10. Reproducibility: 3/5.** ~55% templated (engines share scaffold). Bespoke: room inventory, OTA mix, owner voice. Sprint #3 hits ~60 hrs.

---

## Recipe 8 — Wedding-Venue Inquiry System

**1. Pitch.** A Catskills wedding venue loses 60% of inquiries that sit in a Squarespace form-to-Gmail pipe. The bride emails Tuesday, you see it Friday, she's already booked Roxbury Barn. Meanwhile you're paying The Knot $1,200/yr (sometimes $2,500/mo) for ad spend with no inquiry layer. We build an AI inquiry-to-tour system that drafts replies in your voice within 15 minutes, books the tour, follows up. $6,500 + $600/mo. Pays for itself in two weddings.

**2. Deliverable.** Custom inquiry intake form on the venue's site. AI auto-reply within 15 min in venue voice, customized to the bride's date and headcount, sent for owner approval (one-click) or fully automatic in "trusted mode." Tour-booking flow on Cal.com or Google. Nurture sequence at 24 hrs / 7 days / 21 days. Vendor coordination: AI-curated florists, caterers, DJs, planners mapped to bride preferences, sent post-tour. Post-event review-response automation for The Knot + Google + Wedding Wire. Inquiry-to-booked-tour funnel dashboard.

**3. Day-by-day (3 weeks).**
- **Week 1:** On-site discovery (Pocs residency). 90-min owner interview, 60-min walkthrough of typical inquiry → tour → booking. Days 3–5: Matt scaffolds pipeline; Mel transcribes 20 historical inquiries + responses for voice training.
- **Week 2:** Inquiry form on staging, AI reply pipeline in dry-run. Owner reviews 10 dry-run replies. Tour-booking flow integrated.
- **Week 3:** Nurture + vendor coordination + post-event reviews. Cutover Day 13 (Squarespace form still active in parallel, new system intercepts, Mel watches). Day 15: closeout. **Total ~70 hrs.**

**4. Intake.** Existing Squarespace form URL + email destination. Owner email (Gmail/Outlook — we forward, not take over). 20 historical inquiries (`.eml` or copy-paste — voice training). Venue calendar of available dates next 18 months. Vendor relationships (florists, caterers, DJs, planners). Pricing structure (per-event, per-guest, weekday vs weekend). Tour windows.

**5. Stack.** Vercel + Next.js. Resend (transactional). Claude (auto-replies + vendor matching). Supabase (pipeline + funnel data). Cal.com. **Cancelled SaaS:** The Knot ad spend (often, depends on lead-quality data), WeddingWire, Squarespace forms.

**6. Quality checklist.** AI reply ships within 15 min, 90%+. Owner approves first 20 replies, signs off on voice. Tour-booking tested with three inquiries. Nurture triggers at 24 hr / 7 day / 21 day. Dashboard shows inquiries / replied / tour booked / completed / contract signed. Vendor coordination sends ≥3 matched vendors post-tour. Two months of replaced ad-spend data captured for the case study.

**7. Retainer.** $600/mo starts month 2. Cadence: monthly funnel review, quarterly voice audit, seasonal date-availability push (Feb–Apr is wedding-season prep — biggest lever). The mid-Feb Pocs residency is the annual venue-by-venue review.

**8. Cold-pitch.** "You're losing 60% of inquiries that sit in a Squarespace form-to-Gmail pipe. We build an AI inquiry system that drafts replies in your voice and books the tour — $6,500 + $600/mo. Pays for itself in two weddings."

**9. Geography.** **Pocs only, post-trust.** First-call: Roxbury Barn, Callicoon Hills, Seminary Hill, Arnold House, Eden Farms, Hayfield. Catskills wedding boom is real (post-pandemic NYC weekenders, $35K avg spend). Close after a Chamber breakfast or a referral from the B&B Stack client. **Feb 1 – Apr 15 is the biggest close window** — venues lock vendors and tech for May–Oct ceremonies.

**10. Reproducibility: 3/5.** ~55% templated. Bespoke: venue voice, vendor relationships, tour logistics, pricing. Margin in the retainer over 18+ months.

---

## Recipe 9 — Outfitter Booking + Waiver Modernizer

**1. Pitch.** A Delaware River outfitter takes 800 bookings a season on a paper waiver, a Resos calendar, and a phone that rings off the hook Friday afternoons. You lose half the no-shows because nobody re-books them, can't price weekends differently, and Saturday weather cancellations melt the office. We wire one online intake (digital waivers, dynamic pricing, group discounts, weather-cancel flow) plus AI follow-up that re-books no-shows. $5,500 + $700/mo.

**2. Deliverable.** Custom booking site (Stripe + trip inventory + waiver in one flow). Digital waiver (DocuSign-style signature, IP capture, archived per PA/NY river-trip insurance standards) replacing paper. Dynamic pricing engine: weekday/weekend, group discounts, season multipliers, weather-deal triggers. Weather-cancellation flow: NWS API → automated rebook-or-refund when the river is in advisory. AI follow-up: SMS + email re-booking no-shows, pre-opening pushes to past-season customers, group-rate nudges. Recipe 3 AI Front-Desk tuned for outfitter calls. Booking + waiver dashboard.

**3. Day-by-day (3 weeks).**
- **Week 1:** On-site discovery (Pocs residency). Walk the put-in and take-out, sit in the office Friday afternoon, watch the phone burn. 90-min owner interview, 60-min staff interview. Days 3–5: Matt scaffolds booking + waiver + Stripe; Mel writes trip descriptions and policy doc.
- **Week 2:** Dynamic pricing + weather flow + AI follow-up. NWS API wired Day 8.
- **Week 3:** AI Front-Desk + dashboard + cutover (parallel with Resos Days 13–14). Day 15: closeout. **Total ~65 hrs.**

**4. Intake.** Existing booking system (Resos, FareHarbor, paper, Excel). Existing waiver template. Trip catalog: routes, durations, capacity, prices, season dates. Insurance carrier + minimum waiver requirements. Last-season volume + no-show rate. Refund/credit policy. Phone + carrier (porting).

**5. Stack.** Vercel + Next.js. Stripe. Supabase (trips + waivers + bookings). DocuSign-style signature built natively. NWS API (free). Twilio + Claude (SMS + voice). **Cancelled SaaS:** Resos, FareHarbor (~$150/mo), Smartwaiver ($25–$60/mo), separate AI receptionist if any.

**6. Quality checklist.** Test booking + waiver completes in one flow under 4 min. Digital waiver captures IP, timestamp, parent signature for minors. Insurance carrier approves waiver text (we coordinate with their underwriter — non-negotiable). Weekend pricing fires correctly across three bookings. Weather flow tested with manual NWS advisory. AI follow-up sends 24-hr reminder, post-trip review request, season-end rebook nudge. Dashboard shows day's manifest correctly.

**7. Retainer.** $700/mo Outfitter Operations starts month 2. Opening month (May–June): weekly review, pricing tuning, waiver-flow tightening. Cadence: monthly review, spring weather-flow audit, November post-season review. $700 reflects that outfitters run a 5-month season — we earn 12 months on 5 months of revenue.

**8. Cold-pitch.** "You take 800 bookings a season on a paper waiver and a Resos calendar. We wire one online intake — digital waivers, weekend pricing, weather-cancel — plus AI follow-up that re-books no-shows. $5,500 + $700/mo."

**9. Geography.** **Pocs only, post-trust.** First-call: Lander's, Kittatinny, Chamberlain, Lackawaxen River Outfitters, Pocono Whitewater, Whitewater Challengers, Edge of the Woods. Feb–March close window (lock tech before Memorial Day). Pike (Lackawaxen) and Wayne (Honesdale) are dense corridors. PB has charter-boat operators with similar pain — marine is its own beast, defer.

**10. Reproducibility: 3/5.** ~55% templated. Bespoke: waiver text per carrier, route catalog, dynamic pricing, NWS station mapping. Sprint #3 hits ~50 hrs. Insurance carrier coordination is the variable that moves the most — block 5 hrs for it every engagement.

---

## Cross-cutting playbook elements

### Standard intake form
One Google Form, branches by product. Universal: business NAP + domain; owner contact; CMS; SaaS subs the owner pays for (free-text — we want to name what we're killing); Stripe status; top three pains in the owner's words; Calendly to a kickoff call; Drive folder for brand assets. Branched fields per product follow §4 of each recipe. Form auto-creates a Notion page in `/clients/{name}`.

### Standard contract
One-page SOW, no MSA boilerplate. (1) What we'll build — the §2 deliverables. (2) Sprint price + dates — flat fee, 50% on signature, 50% on closeout. (3) Retainer — monthly Stripe auto-bill, 30-day cancel, no minimum. (4) Ownership — every artifact is the client's. (5) What we won't do — no replatforming, no generic "AI consulting hours," no customer-service chatbots, no vendor questionnaires above 5 pages. (6) Two named humans, Matt and Mel, signed. Notion → PDF → SignWell.

### Standard onboarding email sequence
**Email 1 — day of signature, "We're on. Here's what happens by Friday":**
> Hi [Name] — invoice paid, we're on. Mel will run a kickoff call [date/time] (invite incoming). Two homework items: intake form [link], Drive folder we just shared. That's the only homework we'll ever ask. — Matt & Mel

**Email 2 — 48 hrs before launch, "Quick checklist + what your week looks like":**
> Hi [Name] — kicking off [Day]. Day-by-day: [§3 build plan]. Two things from you: be reachable on Slack/SMS ~10 min on [Day X] (review) and [Day Y] (handoff). Otherwise — go run your business. We'll ping if blocked. — Matt & Mel

**Email 3 — day after closeout, "Shipped. Here's everything in one place":**
> Hi [Name] — [product] is live. Five links: the live thing, the Drive folder, the Loom walkthrough, the maintenance checklist, the retainer Stripe link if you want it. Retainer is $[X]/mo, 30-day cancel any time, covers [three-line scope]. Click if you want it. If not, we hand off and disappear — no follow-up. — Matt & Mel

### Standard close-out + retainer pitch
The retainer pitch lives at the bottom of Email 3. We never send a "did you decide" nudge. If they don't click in 14 days, Mel sends one short follow-up: *"No pressure — quick check that everything's still working on your end?"* That's it. No drip.

### Standard case-study format
One page at `/case-studies/[geo]/[vertical]-[short-name]`. Sections: (1) business — one paragraph, owner-named with permission or anonymized; (2) SaaS replaced — line items + monthly cost; (3) what we built — three bullets; (4) before/after numbers — one per row (calls captured, bookings shifted, hours saved, dollars saved/mo); (5) one raw owner quote; (6) days-to-ship; (7) cost — sprint + retainer + replaced SaaS; (8) whose work — Matt + Mel + (later) VA, named; (9) one screenshot OR one Loom (never both, never neither); (10) one CTA — "want this? 30 min, no deck. [Calendly]." One case study per shipped sprint, owner sign-off in writing or we publish anonymized after 14 days. By month 6, every cold pitch has three case studies in the prospect's vertical.

---

**Closing note.** First time through, any recipe takes 1.4× hours estimated; client #5 hits the estimate; client #20 runs at 0.7×. Mel runs relationships, Matt runs builds, the duo signs together.
