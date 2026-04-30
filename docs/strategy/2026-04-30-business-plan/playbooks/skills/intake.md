---
name: intake
description: Generate a tailored client intake form after a proposal is signed. Use when starting kickoff for a new sprint, when the user says "create intake for {name}" or "send {name} the intake form", or when a clients/{name}/proposal-*.md file exists but no intake.md does.
---

# Skill: Intake

## When to use this skill
A new sprint has been sold (proposal signed, deposit invoice sent or paid) and the founder needs to send the client a tailored intake document before kickoff. Trigger on phrases like "create intake for {name}", "send {name} the intake", "draft kickoff form for {name}".

## Skip if
- No signed proposal exists for the client (route to `/proposal` first).
- An `intake.md` already exists in the client folder and is < 7 days old (offer to revise instead of overwrite).
- The engagement is a retainer-only (no sprint) — use the lighter `/onboarding` flow if that exists, or write a 1-page version manually.

## Inputs
**Required:**
- Client name (e.g., "Bistro Mizner", "Lake Wallenpaupack Inn")
- Sprint type: one of `visibility` ($750), `menu-reviews` ($1,500), `front-desk` ($1,800 + $200/mo), `bundle-restaurant` ($3,500 + $500/mo), `bundle-bnb` ($3,300 + $300/mo)

**Optional:**
- Geography: `palm-beach` or `poconos` (infer from existing client folder if not provided)
- Industry tag (restaurant / B&B / HVAC / dental / salon / contractor / inn / cafe)
- Path to discovery-call notes (if exists, mine for stated pains)

## Steps
1. **Locate the client folder.** Use `Bash` to check `clients/{name}/` exists. If not, create it with `mkdir -p clients/{name-slug}`. Slug = lowercased + hyphenated (e.g., "Bistro Mizner" → `bistro-mizner`).
2. **Mine prior context.** `Read` any of these that exist: `clients/{name}/discovery-prep-*.md`, `clients/{name}/proposal-*.md`, `clients/{name}/log.md`. Extract verbatim: stated SaaS in use + monthly $, named pains, owner's first name, communication preference (phone vs email vs text), the geography, and which sprint was sold.
3. **Resolve sprint defaults.** Map sprint type to scope + price + retainer:
   - `visibility` → 5 days, $750, $250/mo Visibility Watch
   - `menu-reviews` → 1 week, $1,500, $300/mo Hospitality Ops Lite
   - `front-desk` → 2 weeks, $1,800 + $200/mo built-in retainer
   - `bundle-restaurant` → 3 weeks, $3,500 + $500/mo (only after 5+ standalone deals exist)
   - `bundle-bnb` → 3 weeks, $3,300 + $300/mo (Poconos only)
4. **Build the intake doc.** `Write` to `clients/{name}/intake.md` with these sections in order:
   - **Header.** Client name, sprint type + price, retainer offer (where applicable), kickoff date placeholder, primary contact (Mel or Matt — the one who took the discovery call).
   - **1. Business basics.** Legal name, DBA, owner first names, address, phone, website, GBP URL, hours, locations served, # employees, year founded.
   - **2. Current SaaS stack (named line items).** A table prompting for: tool name, monthly cost, what it's for, how long they've used it, how often they actually use it (1–5). Pre-fill 3–5 likely items based on industry — restaurants: OpenMenu / Bloom / Birdeye / Yext / Toast; B&Bs: Lodgify / Hostfully / Airbnb-take / Hostfully Guidebook; HVAC: ServiceTitan / Housecall Pro / Goodcall; dental: Numa / Rosie / DentaPoint; salon: Mindbody / SimplePractice. The pre-fill is a starting point — owner edits.
   - **3. Pain points.** 5 prompts: what costs you the most monthly that you barely use; where do you redo the same work twice; what calls/messages do you keep missing; what's broken on the website right now; what would you do with 4 extra hours/week. Exact wording — these are calibrated.
   - **4. Access credentials needed for this sprint.** Tailor to sprint type — visibility needs GBP owner access + website CMS login + DNS for schema; menu-reviews adds review platform logins (Google + Yelp + TripAdvisor) + Squarespace/WordPress admin; front-desk adds Twilio account access (or willingness to set one up) + Cal.com + the existing phone number to port or forward. Never request payroll/POS/payment-processor access (out of scope every time).
   - **5. Success criteria.** 3 outcome-shaped questions: what does "this worked" look like in 30 days; what number gets better; who else needs to agree this worked.
   - **6. Communication preferences.** Channel (text/email/Slack), best hours, decision-maker if not the contact, weekly check-in time.
   - **7. What we will NOT do during this sprint.** Pull verbatim from the relevant sprint scope doc — for visibility: "we won't rebuild your website, run paid ads, or write blog content"; for menu-reviews: "we won't manage your social, take payments, or rebuild your booking system"; for front-desk: "we won't replace your live front-desk staff, handle complex multi-step bookings, or take credit-card data over the phone".
5. **Add the kickoff CTA at the bottom.** "Reply with this filled in by {kickoff date − 2}. We start {kickoff date}. Questions: text Matt at {phone}." For Poconos clients: phone is primary, not email.
6. **Append to log.** `Edit` `clients/{name}/log.md` adding a line: `{date} — intake.md drafted, sent to client.`
7. **Print the file path** so the founder knows where to grab it, and remind them to send it through the client's preferred channel (text for Poconos B&B owners, email for PB restaurateurs).

## Outputs
- `clients/{name}/intake.md` — the intake document, ready to copy into email or send as a Notion link.
- One-line append to `clients/{name}/log.md`.

## Industry pre-fill quick reference
The skill pre-fills section 2 (SaaS stack) based on the industry tag. Use these as the starting set; owner edits to reality.

| Industry | Pre-fill items + likely $/mo |
|---|---|
| Restaurant | OpenMenu $30, Bloom $99, Birdeye $300, Yext $199, Toast $69+ |
| B&B / cabin | Lodgify $16–45, Hostfully $119, Airbnb take 14–18%, Hostfully Guidebook $79 |
| HVAC | ServiceTitan $349, Housecall Pro $65–199, Goodcall $59 |
| Dental | Numa $49, Rosie $49–149, generic PMS varies |
| Salon / spa | Mindbody $169–729, SimplePractice $69, Goodcall $59 |
| Inn / small hotel | Lodgify, Hostfully, plus PMS like Cloudbeds $125+ |
| Cafe / bakery | Square $60+, Toast, OpenMenu, Bloom |

## Quality checklist
- [ ] Every SaaS line item in section 2 names the tool the prospect *actually* uses (not generic "your CRM").
- [ ] Section 4 credentials list is sprint-specific. Visibility intake should not ask for Twilio.
- [ ] Public sprint price appears in the header — no quote-on-call language.
- [ ] Section 7 ("what we will NOT do") is present. This is a Playbook B signature.
- [ ] No mention of "AI consulting", "digital transformation", or "platform". Use "we build the thing that replaces {SaaS}."
- [ ] Both founder names appear once if either is mentioned.
- [ ] File ends with a concrete date, not "TBD".

## Anti-patterns
- Don't ask for everything "just in case." If the sprint is visibility, don't request payroll system access.
- Don't ask the client to fill in their own pain points in marketing language. The pain prompts are concrete ("what calls do you miss"), not abstract ("what are your goals").
- Don't include a Bronze/Silver/Gold upsell ladder. Retainer offer happens at sprint completion, not at intake.
- Don't promise outcomes the sprint scope doesn't deliver.
- Don't use a generic intake template — tailor the SaaS-stack prompts to the industry. Generic intake = generic pain inventory = bad sprint.

## Example invocation
> "Create intake for Bistro Mizner. Visibility sprint. Boca Raton, indie restaurant."

The skill reads `clients/bistro-mizner/proposal-visibility-2026-05-08.md`, finds Mel's discovery notes mentioning Yext at $199/mo and a manually-edited PDF menu, generates `clients/bistro-mizner/intake.md` with restaurant-tuned SaaS prompts (Yext, Bloom, Birdeye, OpenMenu pre-listed), credentials specific to GBP + Squarespace + DNS, and a kickoff date 5 business days out. Appends to log. Prints the path.
