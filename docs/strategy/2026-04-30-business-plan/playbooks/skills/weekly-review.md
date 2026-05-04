---
name: weekly-review
description: Friday afternoon review ritual that produces a 1-page Gap-and-Gain dashboard plus 3 Sullivan/Hardy reflection questions. Use when the user says "weekly review", "wrap the week", "Friday review", or every Friday by 4pm.
---

# Skill: Weekly Review

## When to use this skill
End of each week (Friday by 4pm). Produces the single artifact that locks the Sullivan/Hardy cadence in: a 1-page dashboard + 3 reflection questions written in Gain framing (what shipped vs where the week started), not Gap framing (what's still missing).

## Skip if
- A `weekly-reviews/{YYYY}-W{NN}.md` for the current week already exists and is < 24 hrs old (offer to revise rather than overwrite).
- It's not Friday or Saturday morning (the cadence matters; running this on Tuesday teaches the skill the wrong rhythm).
- Both founders are mid-sprint kickoff and review needs to wait until 5pm (offer to defer + pre-stage the file with empty metrics for fill-in later).

## Inputs
**Optional (skill auto-detects most):**
- Week number (default: current ISO week — derive from `date`)
- Year (default: current)
- Paths to metric sources: `clients/`, `outreach/`, `workshops/log.md`, `podcast/`, `newsletter/`. Skill scans these.
- A note from the founder: one paragraph of context about the week (energy level, surprises, blockers). Optional but high-value.

## Steps
1. **Determine the week.** `Bash` `date +%G-W%V` to get current ISO year-week. Confirm path: `weekly-reviews/{YYYY}-W{NN}.md`. If exists, abort or revise.
2. **Pull metrics.** Walk the repo and count:
   - **Calls booked.** Count Calendly events or files with `discovery-prep-` in the past 7 days under `clients/*/`.
   - **Sprints sold.** Count new `clients/{name}/proposal-*.md` files dated this week, plus any signed flag in their log.
   - **Sprints shipped.** Count `day-5-handoff.md` files completed this week.
   - **Retainers signed.** Grep for "retainer signed" / Stripe-link confirmation in client logs.
   - **Workshop attendees.** Read `workshops/log.md` for any workshop dated this week + actual count if recorded.
   - **Podcast listeners.** If a `podcast/metrics.md` exists, pull the latest weekly number; else mark "manual fill-in".
   - **Newsletter subscribers.** Same — read `newsletter/metrics.md` or mark manual.
   - **Direct mail sent.** Read `outreach/postcards/*/log.md` for waves dated this week.
   - **Cold-outreach drafts created.** Count files in `outreach/{this-week-dates}/`.
3. **Pull start-of-week baseline.** `Read` last week's review file (`{YYYY}-W{NN-1}.md`). If it exists, copy each metric's value into the "start of week" column. If not (first review), mark "—" and note this is the baseline week.
4. **Build the dashboard.** `Write` to `weekly-reviews/{YYYY}-W{NN}.md`:

   - **Header.** Week range (Mon date – Fri date), founders, geography rotation week (PB or Poconos).

   - **The Gain dashboard (table, 9 rows).** Columns: Metric | Start of week | End of week | Delta | Notes.
     - Calls booked
     - Sprints sold
     - Sprints shipped
     - MRR running (sum of active retainers × ARPU)
     - Retainers signed (this week)
     - Workshop attendees (this week)
     - Podcast listeners (latest ep avg)
     - Newsletter subscribers
     - Direct mail sent (this week)

   - **What shipped this week that wasn't shipping a year ago.** A bulleted list — the Gain question. The skill drafts 5 bullets from the metrics + recent file activity; founders edit. Examples: "Shipped first AI Front-Desk handoff at $1,800 + $200/mo (a year ago: not a product)." "Ran first Western Sullivan PL workshop, 22 attendees (a year ago: didn't exist)." Concrete, before/after, no abstractions.

   - **The 3 Sullivan/Hardy reflection questions.** Verbatim format every week:
     1. *What shipped this week that wasn't shipping a year ago?* (Gain — pre-filled from above; founders confirm or expand.)
     2. *What's in the A-column for next week?* (Unique-Ability work that energizes; only-I-can-do-this.)
     3. *What B/C work needs to move to a Who?* (Drains me / shouldn't be doing it. Every recurring B/C is a hiring signal.)

   - **Decision-trigger reminders (only on the right week).** If this week is M3 / M6 / M9 (count from project start in `docs/strategy/2026-04-30-business-plan/`), surface the relevant decision-trigger row from `23-business-plan-synthesis-v3.md` §10 (e.g., "M3: 4+ workshops run, 3+ sprints/workshop, 3+ retainers signed?"). Otherwise omit.

   - **Footer.** "Next review: {next Friday date}. — Matt & Mel."

5. **Append to the rolling index.** Add a row to `weekly-reviews/index.md` if it exists; create it if not. One line: week | sprints shipped | retainers active | MRR | one-line shipped.
6. **Print the file path** and the 3 reflection questions so the founders can do them out loud or together.

## Outputs
- `weekly-reviews/{YYYY}-W{NN}.md` — the 1-page review.
- `weekly-reviews/index.md` — appended one-line summary row.

## Quality checklist
- [ ] Dashboard is 9 rows, no more — single page printed.
- [ ] Every metric has a "start of week" value (or "—" if it's the first review).
- [ ] The Gain question is answered first, before the A-column / B-C-column questions. Order matters.
- [ ] The reflection questions are verbatim Sullivan/Hardy phrasing — not paraphrased.
- [ ] If it's a decision-trigger month (M3 / M6 / M9), the relevant trigger row appears.
- [ ] No "what's behind / what's missing" framing anywhere. Failure mode for two-founders-coming-off-W2 is comparing to imagined future. Skill refuses Gap framing.
- [ ] No screenshots, no charts. One page of text. Founders read it together over coffee or wine, ~10 min.
- [ ] Week is named in human terms ("Week of May 11–15") plus ISO ("2026-W20").

## Anti-patterns
- Don't import a 50-row metrics dashboard. Nine rows. The discipline is choosing what matters, not measuring everything.
- Don't grade the week ("B+", "rough week"). Show the deltas, ask the questions, no judgment.
- Don't auto-write the answers to the reflection questions in the founder's voice. Pre-draft the Gain bullets from data; leave Q2 and Q3 blank for the founders to fill.
- Don't cross-reference last quarter, last year, or "industry benchmark". Comparison is start-of-week → end-of-week. That's the Gain.
- Don't append a to-do list. Q3 ("B/C work that needs to move to a Who") IS the to-do list — and it's a hiring signal, not a personal-task signal.
- Don't run this without both founders present (or scheduled to read the same file within 24 hrs). It's a duo ritual.

## Example invocation
> "Weekly review."

Friday at 4pm. Skill computes ISO week is `2026-W20`, scans repo, counts: 5 calls booked (vs 3 last week), 2 sprints sold (vs 1), 1 sprint shipped, 1 retainer signed at $250/mo, 0 workshops this week, 22 podcast listeners avg (down from 28 — a Mel-only week), 14 newsletter subs (+3), 200 postcards sent. Pre-fills 5 Gain bullets ("first $1,800 AI Front-Desk shipped — a year ago we didn't have the offer", "first Wayne County BNI breakfast attended", etc.). Leaves Q2 and Q3 blank. Prints `weekly-reviews/2026-W20.md` and the 3 reflection questions. Mel and Matt walk through together over coffee.
