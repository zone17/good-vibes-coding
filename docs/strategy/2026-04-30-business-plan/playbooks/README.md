# GVC Playbooks

Operational books for running Good Vibes Coding day-to-day. Read in this order:

1. **[`01-recipe-book.md`](./01-recipe-book.md)** — what we sell and how to deliver it. Full step-by-step build plans for all 9 products (3 starter sprints + 2 backups + 1 bundle + 3 premium post-trust hospitality offers). Each recipe covers pitch, deliverables, day-by-day build, intake, stack, quality checklist, retainer onboarding, cold-pitch one-liner, geography fit, reproducibility score. Plus cross-cutting templates: intake form, contract structure, 3-email onboarding sequence, close-out + retainer pitch, case-study format.
2. **[`02-operations-playbook.md`](./02-operations-playbook.md)** — how the business runs. Hour-by-hour schedules for Matt and Mel across months 1, 4, 9. Standard 7-day week with daily outcomes + anti-patterns. Monthly themes M1–M9. Quarterly rhythm. 10 lifecycle workflows. Tooling stack (~$280/mo). 12-KPI dashboard. 32 anti-patterns.
3. **[`03-claude-code-skills-library.md`](./03-claude-code-skills-library.md)** — how to systematize the work in Claude Code. Catalog of 15 skills organized by category, build-order roadmap (M1 / M3 / M6+), conventions, install instructions. Plus 5 fully-built installable skill files in [`./skills/`](./skills/).

## Install the 5 starter skills

```bash
mkdir -p ~/.claude/skills && cp docs/strategy/2026-04-30-business-plan/playbooks/skills/*.md ~/.claude/skills/
```

The 5 skills:

| Skill | Purpose |
|---|---|
| [`intake.md`](./skills/intake.md) | On-demand client intake form generator |
| [`cold-batch.md`](./skills/cold-batch.md) | Batch cold-pitch outreach for an industry+city pair |
| [`sprint-ai-visibility.md`](./skills/sprint-ai-visibility.md) | Run the AI Visibility Tune-Up sprint end-to-end (5-day plan) |
| [`workshop-prep.md`](./skills/workshop-prep.md) | 75-min "AI for Small Business" workshop builder, venue+audience tailored |
| [`weekly-review.md`](./skills/weekly-review.md) | Friday review ritual with Sullivan/Hardy Gap-and-Gain framing |

## Upstream context

These playbooks operationalize the v3 strategy synthesis at [`../23-business-plan-synthesis-v3.md`](../23-business-plan-synthesis-v3.md). When the strategy changes, the playbooks need to follow. Cross-references at the top of each playbook tell you which upstream sections to update if anything in `23-...-v3.md` shifts materially.

## Voice & anti-patterns

Every artifact in this folder respects the same rules:

- Plain language. No SaaS-template vocabulary ("unlock," "supercharge," "leverage," "transform your business," "AI consulting" as a lead phrase).
- First-person plural "we." Named humans where credibility helps. Never "our team of experts."
- Anti-SaaS framing: every offering names the SaaS being replaced and the dollar amount being saved.
- Anti-bloat tooling: prefer markdown + minimal SaaS to "let's add Notion AI database for that."
- Geography-aware: Palm Beach motion ≠ Poconos motion. Pricing tiers differ by ~30%.
- Sullivan/Hardy aligned: founders operate primarily in Unique Ability; Whos hired before grind sets in.

## When you write a new playbook

Copy the structure of an existing book. Front-matter includes `title`, `date`, `type`. Cross-link to the strategy synthesis. Keep it under 6,000 words unless the depth genuinely earns it. Anti-pattern: writing playbooks that contradict each other — when in doubt, the recipe book wins on what we sell, the operations playbook wins on how we run, the skills library wins on automation surface.
