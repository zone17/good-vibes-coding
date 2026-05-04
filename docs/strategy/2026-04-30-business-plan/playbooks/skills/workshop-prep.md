---
name: workshop-prep
description: Prepare the 75-minute "AI for Small Business" workshop for a specific library, Chamber, or coworking venue. Use when the user says "prep workshop for {venue}", "build the {date} {venue} deck", or 7-10 days before a workshop date.
---

# Skill: Workshop Prep

## When to use this skill
A workshop is on the calendar 7–14 days out and needs the agenda, slides, two real-business worked examples, and the closing CTA built. Phrases: "prep workshop for Western Sullivan PL", "build the Boca library deck", "workshop materials for {date}".

## Skip if
- Date is < 4 days out (use the abbreviated "rapid prep" path: skip the worked-example research step, reuse the most recent same-vertical examples).
- The workshop is solo-led (one founder only) — refused per `22`. Pair-up before invoking.
- Venue isn't on the approved list (libraries, Chambers, coworking) and isn't free or under $150 — refer to founders for pricing review.
- Previous workshop at this venue ran < 60 days ago (audience overlap; pick a new venue or a fresh angle).

## Inputs
**Required:**
- `venue` (e.g., "WPB Mandel Library", "Boca Raton Public Library", "Western Sullivan PL Narrowsburg", "Wayne County PL Honesdale", "1909 Coworking", "Cooperage Honesdale")
- `date` (YYYY-MM-DD)
- `expected_count` (e.g., 18, 25 — used to size the agenda's small-group section)
- `vertical_focus` — one of: `mixed`, `restaurants`, `lodging-bnb`, `home-services`, `professional-services`, `medical-wellness`

**Optional:**
- `geography` (auto-inferred from venue: PB venues → palm-beach; Sullivan/Wayne/Pike/Monroe venues → poconos)
- `co-host` (default: both founders — Mel MCs, Matt builds)

## Steps
1. **Create folder.** `mkdir -p workshops/{date}-{venue-slug}/`.
2. **Build the agenda.** Save `agenda.md` with the standard run-of-show:
   - 0–5 Mel intro + round-robin: "What's your biggest weekly time-sink?" Each attendee 30 sec.
   - 5–15 The "SaaS layer is dying" thesis (90 sec) + two 2026 examples (45 sec each). Examples are *real businesses in the geography*, not hypotheticals.
   - 15–35 Live build: Matt takes one attendee's actual problem and builds a working AI assistant in 15 min. Document the fallback (a pre-built example to demo if no attendee volunteers).
   - 35–55 Open Q&A.
   - 55–70 Small-group "what's your one AI question": founders circulate. Group sizes scale to `expected_count` — 4 groups of 4–6 people.
   - 70–75 ONE CTA: "Want a free 30-min look at your business? Sign up here. We'll do 3 next week." iPad opt-in passes around. No second CTA.
3. **Build the slides.** Save `slides.md` with 8–10 content slides, plain language, no logos:
   - **Slide 1 — Title.** "AI for Small Business: What Actually Works in 2026 (and What's Hype)" + venue + date + Mel & Matt names.
   - **Slide 2 — Who we are.** Two-bullet bio. Matt 25-year engineer. Mel 20-year hospitality operator. We run a small AI shop in {Palm Beach / Narrowsburg}.
   - **Slide 3 — The thesis.** "Most small businesses are paying $200–$800/mo for SaaS that doesn't quite fit. AI lets a 2-person shop replace it with code you own." One sentence per line, three lines max.
   - **Slide 4 — What's hype.** Three things to ignore: the AI agent that "runs your whole business", the chatbot replacing your front desk staff (88% of customers prefer humans, 4× failure rate), the $79/mo tool that says "powered by GPT".
   - **Slide 5 — What works.** Three things to pay attention to: making your business findable to AI search (ChatGPT, Perplexity, Google AI Overview), replacing the receptionist SaaS with a custom one you own, replacing menu/review tools with one source of truth.
   - **Slide 6 — Real example #1.** A real business in this venue's geography, named (with consent) or anonymized as "a Boca Italian restaurant" / "a Lake Wallenpaupack inn" / "a Honesdale HVAC contractor". What they paid in SaaS before, what we built, what they pay now. Plain numbers.
   - **Slide 7 — Real example #2.** Different vertical from example #1. Same structure.
   - **Slide 8 — The 5-day visibility audit.** What we cover, who it's for, what it costs ($750), what it doesn't cover.
   - **Slide 9 — Live build setup.** "Who in this room has a problem we can take a swing at right now?" — handoff slide for the 15–35 segment.
   - **Slide 10 — Closing.** "Sign up for a free 30-min look. We'll do 3 next week." iPad QR-or-URL (URL only for Poconos venues — no QR for rural per `22`).
4. **Build two worked examples.** Save `examples.md`:
   - Pick examples relevant to `vertical_focus` and `geography`. Use real prior client wins if any exist (read `case-studies/{geo}/` if present). If no real ones yet, use the named scenario from `21-product-portfolio-options.md`: Boca Italian restaurant on East Palmetto Park, West Palm Clematis café, Narrowsburg gallery, Honesdale inn-keeper, Hawley charter, etc.
   - Each example has: business type + size, SaaS stack before with $/mo, what we built, what it cost (one-time + retainer), what it replaced, the one number that got better. Plain prose.
   - Total each example ≤ 200 words. They get spoken, not slide-dumped.
5. **Build the CTA flow.** Save `cta.md`:
   - The 5-min closing script verbatim (same every workshop, do not re-invent).
   - The iPad opt-in form fields: name, business name, email, phone (optional), best time for a 30-min call this week or next.
   - The 24-hr post-workshop follow-up sequence: same-day thank-you email with the slide PDF link, 48-hr Calendly nudge to non-bookers ("here's the link if it gets buried"), no third email — workshops earn the trust, automation kills it.
6. **Build the handout.** Save `handout.md`:
   - One physical page printed and stacked at the door.
   - Front: 5 questions to ask before paying for any new SaaS (e.g., "Does this lock my data into their format? What does it cost to leave? Can I see a real customer in my business size?").
   - Back: GVC's 3 starter sprints with public prices. Phone number + URL. Both founders' names.
7. **Logistics checklist.** Save `logistics.md`:
   - Venue contact, room setup, projector + cable check, attendee count cap, coffee/snacks budget ($100), iPad charged, handouts printed (count = `expected_count` × 1.4), backup demo if live-build volunteer doesn't materialize, both founders' arrival time (45 min early).
8. **Append to ops log.** `Edit` `workshops/log.md` adding a line: `{date} — {venue} workshop prepped. Vertical: {vertical_focus}. Expected: {count}.`
9. **Print the workshop folder path** so the founder knows where to grab everything.

## Outputs
Inside `workshops/{date}-{venue-slug}/`:
- `agenda.md` — the 75-min run-of-show
- `slides.md` — 8–10 content slides in markdown (founder converts to Keynote/Slides as needed)
- `examples.md` — two real-business worked examples relevant to the geography + vertical
- `cta.md` — closing script + opt-in form fields + post-workshop follow-up sequence
- `handout.md` — printed front/back single-page handout
- `logistics.md` — pre-event checklist
Plus a one-line append to `workshops/log.md`.

## Quality checklist
- [ ] Title slide reads "AI for Small Business: What Actually Works in 2026" — not "Free AI Audit" (refused per `22`).
- [ ] No logos, no firm-pitch slides, no Bronze/Silver/Gold.
- [ ] Both founders named on the title slide. Both expected to attend (the duo IS the brand).
- [ ] Two worked examples are named businesses in the geography (or anonymized with real numbers).
- [ ] Closing has exactly ONE CTA — the 30-min consult signup. No "follow our podcast" tacked on.
- [ ] Handout includes 3 sprint prices publicly. No "contact us for pricing".
- [ ] Poconos workshops have NO QR code. URL + phone only.
- [ ] Live-build segment has a fallback example pre-staged in case no volunteer.

## Anti-patterns
- Don't sell from the podium. The workshop is the pitch's quality, not a delivery vehicle for one.
- Don't use generic stock examples ("imagine a restaurant…"). Use real geography-specific businesses.
- Don't leave gaps in the run-of-show — every 5-min block is named.
- Don't promise outcomes ("triple your bookings"). Promise structure ("here's what's hype, here's what works, here's what we'd build for $750").
- Don't include slides about the firm's own awards, history, or team size beyond the 2-bullet bio.
- Don't run the workshop with one founder. Reschedule before going solo.
- Don't add a second CTA at the end ("…and follow us on Instagram"). One ask. iPad opt-in.

## Example invocation
> "Prep workshop for Western Sullivan PL Narrowsburg, 2026-06-12, 22 attendees, lodging-bnb focus."

Skill creates `workshops/2026-06-12-western-sullivan-pl-narrowsburg/`, builds agenda + 9 slides + two examples (a Lake Wallenpaupack inn replacing $400/mo Lodgify+Hostfully+Airbnb-take with a $2,400 direct-booking site, and a Hawley B&B that replaced $200/mo Hostfully Guidebook with a $900 + $100/mo AI concierge), iPad opt-in CTA without a QR code, single-page handout with the 3 sprint prices, and a logistics checklist. Founder reviews, converts slides to Keynote, prints handouts.
