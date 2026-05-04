---
name: cold-batch
description: Generate a numbered batch of personalized cold-pitch emails for an industry+city pair using the GVC anti-SaaS frame. Use when the user says "cold batch for {industry} in {city}", "draft N cold emails", "outreach round for {geography}", or before a Monday outreach push.
---

# Skill: Cold Batch

## When to use this skill
The founder needs N personalized cold-outreach drafts for a specific industry × geography pair. Triggered before Monday outreach pushes, after a workshop produces a fresh attendee list, or when adding a new vertical to the cold motion. Phrases: "cold batch for indie restaurants in Delray", "draft 10 cold emails for Honesdale B&Bs", "next outreach round for Boca HVAC".

## Skip if
- The geography is outside Palm Beach County or the Upper Delaware/Poconos corridor (Sullivan/Wayne/Pike/Monroe). GVC's plan limits to two markets through M9.
- The list is "Fortune 5000" or chains with > 3 locations (per the Calendly disqualifier).
- The industry is on the refused list: AI quoting (HVAC photo-to-quote), email migration, AI inventory, social-media calendaring.
- The geography is the Poconos and the channel intent is email-only — Poconos cold email scales to zero. Route to `/postcard-wave` instead.

## Inputs
**Required:**
- `industry` (e.g., "indie restaurant", "HVAC contractor", "B&B / cabin-rental owner", "single-location dental practice", "salon/spa")
- `geography` (e.g., "Delray Beach", "Boca Raton", "Honesdale PA", "Narrowsburg NY", "Hawley/Lake Wallenpaupack")
- `count` (default 8, max 20)

**Optional:**
- `list_path` — path to a CSV/markdown file with real business names, owners, websites, GBP URLs. If not provided, the skill produces *templates with research instructions* rather than fabricating businesses.
- `sprint_anchor` — which sprint to pitch first (`visibility` $750, `menu-reviews` $1,500, `front-desk` $1,800). If not provided, pick by industry: restaurants → menu-reviews; HVAC/dental/salon → front-desk; everyone else → visibility as the cheapest first-yes.

## Steps
1. **Identify the SaaS stack to attack.** Based on industry, look up the named SaaS lines from the v3 product portfolio: restaurants → Yext $199 + Bloom $99 + Birdeye $300 + OpenMenu $30; HVAC → Goodcall $59 / Numa $49 / Rosie $49–149; B&B → Lodgify $16–45 / Hostfully $119 / Airbnb take 14–18%; dental → Numa / Rosie + missed-call cost; salon → Goodcall / SimplePractice $69. Name a real monthly dollar amount.
2. **Pick the sprint anchor.** Use the input or the industry default. Confirm price + retainer (e.g., $1,800 + $200/mo for front-desk).
3. **Set geography register.** If Palm Beach: dense, faster, 5 trust touches, Calendly-link OK. If Poconos: rural, 7–8 touches, *phone-first* — include phone number not just Calendly. Adjust signature accordingly.
4. **Create the output folder.** `Bash` `mkdir -p outreach/{YYYY-MM-DD}-{industry-slug}-{city-slug}/`.
5. **Generate N drafts.** Each draft is a numbered markdown block with:
   - **Subject line.** ≤ 60 chars, no clickbait, names the SaaS dollar pain. Examples:
     - "Quick question about the $400/mo your restaurant spends on Yext + Birdeye + OpenMenu"
     - "Two humans in Narrowsburg · 90 seconds"
     - "Missed-call problem for HVAC shops in Boca?"
   - **Body, ≤ 140 words.** Open with named SaaS pain ($X/mo on [tool] for [function]). One concrete alternative ("we replace it with code you own, $750 once + $250/mo we run, fixed fee"). One real example or what we'd build for them in 5 days. One sentence of soft proof (named-humans firm in [their geography]). One CTA, geography-appropriate (PB: Calendly link; Poconos: "if it's a fit, call Mel at {phone} or grab a slot").
   - **Loom suggestion.** A 60–90s video angle for the T+48hr non-opener follow-up. Specific to *this* business — e.g., "Loom: open ChatGPT, type 'best Italian restaurant Boca Raton', show whether they appear, narrate the gap."
   - **Name-research instructions.** A 4-line checklist: find the owner's first name (LinkedIn / About page / GBP), confirm they're owner-operator (not a chain), pull their actual current SaaS from page-source / Wappalyzer / job-listing leaks, find one specific recent thing (new menu, new dock, summer hours) to namedrop in the opener.
   - **Disqualifiers.** 3 quick "skip this prospect if" rules for *this* draft (e.g., "skip if Yelp shows < 50 reviews — not enough volume to feel SaaS pain").
6. **Add a header section.** Top of the file: industry, city, count, the SaaS stack being attacked with $ totals, the anchor sprint + price, the geography register chosen, the date, and a one-paragraph framing reminder of the cold-pitch frame ("you're paying $X for [function]; we replace it with code you own, fixed fee, retainer to run").
7. **Add a sending checklist at the bottom.** 6 items: send Tue–Thu 8–10am local, no Mondays, no Fridays after 2pm, send from a personal address (not a no-reply), include sender phone in signature, never auto-follow-up — the Loom is a real recording, not an automation, T+48hrs.
8. **Print the file path.**

## Outputs
- `outreach/{YYYY-MM-DD}-{industry-slug}-{city-slug}/batch.md` — the N drafts plus header and sending checklist.
- One file per batch; founders edit-then-send manually. No bulk auto-send.

## SaaS-stack quick reference
Use these dollar pains in the cold-pitch frame. The number is what they're really paying right now.

| Industry | Named SaaS lines | Typical monthly $ | Replace with |
|---|---|---|---|
| Indie restaurant | OpenMenu + Bloom + Birdeye + Yext | $429–628/mo | $1,500 + $300/mo Menu+Reviews Lite |
| HVAC contractor | Goodcall / Numa + maybe ServiceTitan | $59–408/mo | $1,800 + $200/mo Front-Desk |
| Dental / single-location | Numa + Rosie + missed-call cost | $98–198/mo + lost-revenue | $1,800 + $200/mo Front-Desk |
| Salon / spa | Mindbody + Goodcall | $228–788/mo | $1,800 + $200/mo Front-Desk |
| B&B / cabin | Airbnb take 14–18% + Lodgify + Hostfully Guidebook | varies + $95–124 fixed | $2,400 Direct-Booking + $300/mo concierge |
| Cafe / bakery | OpenMenu + Square + maybe Bloom | $90–189/mo | $750 Visibility (cheapest first-yes) |

## Quality checklist
- [ ] Every draft names a real SaaS with a real monthly dollar amount.
- [ ] No subject line uses "AI consulting", "transformation", or "scale".
- [ ] No draft promises an outcome ("triple your bookings"). Every draft promises a sprint deliverable ("a one-page menu they can edit themselves, in a week, $1,500").
- [ ] Body ≤ 140 words. Subject ≤ 60 chars.
- [ ] Geography register matches: Calendly-first for PB, phone-first for Poconos.
- [ ] Both founder names appear in the signature: "— Matt & Mel · goodvibescoding.com".
- [ ] No Bronze/Silver/Gold tiers, no "limited time", no QR codes mentioned.
- [ ] Sprint price is public and named in the body, not "let's discuss pricing".

## Anti-patterns
- Don't fabricate business names. If `list_path` isn't provided, write templates with `[OWNER NAME]` and `[BUSINESS NAME]` placeholders + the name-research checklist.
- Don't include "free AI audit" as the CTA — refused per `22-cold-acquisition-gtm.md`.
- Don't include a P.S. with a second offer. One CTA per email.
- Don't auto-personalize via mail-merge tokens that look automated. Personalization is the manual research step before send.
- Don't write more than the requested count. If asked for 8, ship 8 — quality > volume.

## Example invocation
> "Cold batch for indie restaurants in Delray Beach, count 6, anchor on menu-reviews."

The skill creates `outreach/2026-05-04-indie-restaurants-delray-beach/batch.md` with 6 numbered drafts. Header attacks $429/mo Yext+Bloom+Birdeye+OpenMenu stack. Sprint anchor is Menu+Reviews Lite at $1,500 + $300/mo retainer. Each draft has a subject under 60 chars naming the dollar pain, a body under 140 words, a Loom angle (e.g., "open OpenMenu, show how their last update was 2024-09"), name-research checklist, and 3 disqualifiers. Footer has the Tue–Thu 8–10am sending rules. Founder spends 30 min researching real owner names, edits the personalization, sends.
