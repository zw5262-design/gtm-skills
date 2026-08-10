---
name: gtm-score-leads
description: Applies a project's scoring rubric (points or tiers) to enriched leads — never improvises new criteria.
---

SKILL NAME: gtm-score-leads
Persistent, reusable skill — save it, do not run as a one-time task.

STEP 1: Read projects/{project}/00_ICP/scoring_rubric.md.

STEP 2: Apply it exactly, in whichever pattern it's written — weighted
points (produces score_tier: Hot/Warm/Cold) or tiered qualification
(produces tier: Tier 1/Tier 2a/Tier 2b/Remove). Missing data for a
criterion = not met, never assumed in the lead's favor.

Output scored_leads.csv, sorted best-fit first, every row with a
one-sentence reason citing the specific rubric line that applied.
Companies that don't qualify go to a separate removed_companies.csv
with a reason — never silently dropped.
