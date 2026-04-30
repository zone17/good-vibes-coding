---
name: sprint-ai-visibility
description: Run the 5-day AI Visibility Tune-Up sprint end-to-end. Use when a $750 visibility sprint is sold, when the user says "Day N of {client} visibility", "run the visibility sprint for {client}", or when a clients/{name}/intake.md exists tagged sprint=visibility.
---

# Skill: AI Visibility Sprint Runner

## When to use this skill
A $750 AI Visibility Tune-Up sprint has been sold and intake is complete. The skill runs the 5-day build plan one day at a time — invoke it daily during the sprint, naming the day. Phrases: "Day 1 of {client} visibility", "run today's visibility work for {client}", "wrap the {client} visibility sprint".

## Skip if
- No `clients/{name}/intake.md` exists (route to `/intake` first).
- The intake names a sprint type other than `visibility`.
- The client website is missing or being rebuilt during the sprint window (delivery dependency — pause and renegotiate scope).
- It's been > 5 business days since Day 1 was run and no Day file exists for today (pipeline broke; investigate before continuing).

## Inputs
**Required:**
- Client name (slug used for `clients/{name}/`)
- Day number: `1`, `2`, `3`, `4`, or `5`

**Optional but expected by Day 1:**
- GBP URL (the client's existing or claimable Google Business Profile)
- Website URL
- 5 target queries (e.g., "best Italian restaurant Boca Raton", "Italian restaurant near Mizner Park", "Boca Raton dinner reservations", "[client name] menu", "Italian Delray Boca")
- Geography (`palm-beach` or `poconos`)
- Industry vertical (used for schema type selection)

## Steps

### Day 1 — Audit
1. Create folder: `mkdir -p clients/{name}/sprint-visibility-{YYYY-MM-DD}/`.
2. Run AI-search audit. For each of the 5 target queries: query ChatGPT, Perplexity, and Google AI Overview (manually or via WebFetch if available); record whether the client appears, where, with what claim. Save as `day-1-ai-search-baseline.md` with a 5-row table: query | ChatGPT | Perplexity | AI Overview | notes.
3. GBP audit. Check categories, hours, services, photo count, Q&A count, post cadence, review count + last response. Save `day-1-gbp-audit.md` with a checklist of what's missing.
4. Schema audit. View-source the homepage and 2 key pages. Detect existing JSON-LD. List missing types: LocalBusiness, FAQPage, Restaurant/LodgingBusiness/Dentist (industry-dependent). Save `day-1-schema-audit.md`.
5. NAP-citation scan. Search for the business across: Apple Maps, Bing Places, Yelp (PB only), BBB, Chamber directory, FB. Note inconsistencies. Save `day-1-citations.md`.
6. Write `day-1-summary.md` — 1 page: 3 biggest gaps, what we'll fix Days 2–4, what the client needs to send (logins, photos, FAQ inputs).

### Day 2 — GBP optimization + schema
1. Read `day-1-gbp-audit.md` and `day-1-schema-audit.md`.
2. Produce `day-2-gbp-changes.md` — concrete edits: primary category set, secondary categories (max 9), services list, hours, attributes, 8 self-seeded Q&As written in owner voice (mine the intake for voice). 2 GBP posts written and dated.
3. Produce `day-2-schema.json` — actual JSON-LD blocks ready to drop into the site head. Include LocalBusiness with `areaServed`, Service entries with `offers.price`, FAQPage with 5–8 voice-query Q&As, Person entries for owners if applicable.
4. Produce `day-2-stub-faq.md` — 10 owner-voice answers based on a 30-min interview transcript or the intake notes. These become a new `/faq` page on the site.
5. Send the founder a 3-line midday update message draft for the client: "Today: GBP optimized + schema written. Tomorrow: citations + AI re-test. Anything to add to the FAQ?"

### Day 3 — NAP citations + AI search re-test
1. Read `day-1-citations.md`. Produce `day-3-citation-fixes.md` — for each platform, the exact NAP string + URL + category to set. Mark which need owner login (the founder does these together with the client over a 30-min call) vs which can be done by the founder alone.
2. Re-run the 5 AI-search queries from Day 1. Save as `day-3-ai-search-recheck.md` — same 5-row table, side-by-side with Day 1 baseline. Note any movement (usually too early; this is a baseline-2 not a result).
3. Schedule the schema deploy. Write `day-3-deploy-plan.md` — exact files to edit on the client site, exact JSON-LD blocks to insert, validation steps (Google Rich Results Test URLs).
4. Mid-sprint client check-in: 15-min call. Use the founder-facing prompt at the bottom of `day-3-citation-fixes.md` to walk through it.

### Day 4 — Dashboard build
1. Build a simple "Visibility Watch" dashboard as a single static HTML page or markdown file the client can bookmark. Pull together: GBP profile metrics (views/calls/direction-asks last 28 days), top 5 queries from Search Console if accessible, AI-search results table from Day 1 vs Day 3, citation status table.
2. Save `day-4-dashboard.md` (or `.html`) inside the sprint folder. Include a 1-line maintenance instruction.
3. Write `day-4-maintenance-checklist.md` — 1 page the owner keeps: monthly check (4 GBP posts, 1 photo, 2 review responses), quarterly check (re-run AI-search audit, check schema validity, refresh services list).

### Day 5 — Handoff + retainer offer
1. Compile `day-5-handoff.md` — the public-facing deliverable. Sections: what we did this week, before/after on each axis (AI search, GBP, schema, citations), the Visibility Watch dashboard URL/path, the maintenance checklist link, and the source files (a `source/` subfolder with the schema JSON, the GBP edits log, the FAQ page).
2. Write `day-5-retainer-offer.md` — the $250/mo Visibility Watch offer in plain language: what's included monthly (1 AI-search recheck, 4 GBP posts + 1 photo, schema/AI-surface delta review, quarterly maintenance call), what's not included (rebuilds, paid ads), how to say yes (Stripe link placeholder), how to say no ("totally fine; we won't follow up — the source files are yours").
3. Write `day-5-loom-script.md` — a 90-second handoff Loom script: 0–15s intro, 15–60s before/after walkthrough, 60–90s the maintenance checklist + retainer offer + thank-you.
4. Append to `clients/{name}/log.md`: `{date} — visibility sprint shipped. Retainer offer sent.`
5. Print the path to `day-5-handoff.md` and remind the founder to send the Stripe link for the retainer.

## Outputs
Inside `clients/{name}/sprint-visibility-{YYYY-MM-DD}/`:
- `day-1-ai-search-baseline.md`, `day-1-gbp-audit.md`, `day-1-schema-audit.md`, `day-1-citations.md`, `day-1-summary.md`
- `day-2-gbp-changes.md`, `day-2-schema.json`, `day-2-stub-faq.md`
- `day-3-citation-fixes.md`, `day-3-ai-search-recheck.md`, `day-3-deploy-plan.md`
- `day-4-dashboard.md` (or `.html`), `day-4-maintenance-checklist.md`
- `day-5-handoff.md`, `day-5-retainer-offer.md`, `day-5-loom-script.md`
- `source/` — all source files (schema JSON, FAQ markdown, citation log)

## Quality checklist
- [ ] Every Day's output is a concrete file the founder can hand the client without rewriting.
- [ ] AI-search audit was actually run (not faked) on real LLMs — if the run can't be done, the skill says so and pauses.
- [ ] Schema JSON validates against Google Rich Results Test before Day 5.
- [ ] GBP edits use the *owner's* voice — not generic marketing copy. Mine intake notes for verbatim phrases.
- [ ] FAQ page has exactly 10 Q&As, all in owner voice, all 60–120 words (the AI Overview pull format).
- [ ] No QR codes anywhere in the deliverables (Poconos clients especially).
- [ ] Day 5 retainer offer is $250/mo, public price, single tier — no Bronze/Silver/Gold.
- [ ] Maintenance checklist names the owner doing it, not "the team".

## Anti-patterns
- Don't claim AI-search ranking improvement on Day 5. The window is too short. Show baseline vs Day 3 movement and frame it honestly.
- Don't add services to GBP that the client doesn't actually offer. The category list isn't a marketing tool.
- Don't sneak in upsell language into the handoff doc. Retainer offer is its own document. Yes-or-no.
- Don't use a generic FAQ template. Every Q is from the owner's words; every A is in their voice. Otherwise the AI Overview citation play fails.
- Don't deploy schema without telling the client what changed and how to roll it back. The client owns the code.
- Don't run all 5 days in a single session. Each day's work is gated on the prior day's review and on real overnight indexing/owner feedback.

## Example invocation
> "Day 1 of Bistro Mizner visibility. GBP at maps.google.com/?cid=12345. Site at bistromizner.com. Targets: 'best Italian Boca Raton', 'Mizner Park dinner', 'Boca Italian reservations', 'Bistro Mizner menu', 'Italian Delray Boca'. Palm Beach. Restaurant."

Skill creates `clients/bistro-mizner/sprint-visibility-2026-05-12/`, runs the 4 audit tasks, writes the 5 Day-1 files, drafts the founder-to-client check-in message, and prints the summary path. Next morning the founder runs `/sprint-ai-visibility Day 2 of Bistro Mizner` and the next file set lands in the same folder.
