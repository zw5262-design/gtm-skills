---
name: gtm-research-icp
description: Infers a project's ICP and scoring rubric from real market research (competitor customer evidence) rather than a manually written config — works for any project via its seed file.
---

SKILL NAME: gtm-research-icp
Persistent, reusable skill — save it, do not run as a one-time task.

You are researching and inferring the Ideal Customer Profile — you are
NOT filling in a template, you are deriving this from real evidence.

STEP 1: Determine which project this run is for. Read
projects/{project}/00_ICP/product_seed.md and the most recent
projects/{project}/00_ICP/market_research_{date}.md. Never hardcode a
product name or claim from a different project.

STEP 2 — INFER THE TARGET COMPANY PROFILE FROM REAL EVIDENCE:
For each competitor named in market_research, check their public case
studies, customer logos, testimonial pages, and any G2/Capterra-style
review listing (reviewer titles, company size filters, industry tags).
Synthesize a target company profile from the PATTERN across what these
competitors' actual customers look like — not from assumption. Where
evidence is thin for a given competitor, say so rather than filling the
gap with a guess.

STEP 3 — INFER THE TARGET BUYER (skip entirely if the project's seed
or hard constraints indicate a company-level-only program where
contact info isn't required):
Extract which job titles are actually credited or quoted in the
evidence from Step 2. Rank by frequency — most common becomes primary
buyer, less common but present becomes secondary.

STEP 4 — INFER TRIGGER SIGNALS:
For companies identified as good-fit customers of competitors, check
what public signal (hiring pattern, funding event, team growth, public
statement) tends to precede their likely adoption of a product like
this one. Derive the trigger signal list from this pattern, not from
assumption.

STEP 5 — Apply any HARD CONSTRAINTS from product_seed.md as
non-negotiable filters on top of the inferred profile.

STEP 6 — WRITE projects/{project}/00_ICP/icp.md: target company
profile, target buyer (if applicable), trigger signals, disqualifiers —
each bullet with a one-line note on what evidence it's based on.

STEP 7 — WRITE projects/{project}/00_ICP/scoring_rubric.md. Choose the
pattern that fits the evidence:
- Weighted points (Hot 18+/Warm 8-17/Cold <8) — use when signals vary
  in strength and combine additively
- Tiered qualification (Tier 1 / Tier 2a / Tier 2b / Remove) — use when
  fit is more binary (e.g. "must have both X and Y, or one of two
  fallback paths")
Justify point values or tier logic from what Steps 2-4 actually found.
Pick whichever pattern the evidence supports — don't blend the two.

STEP 8 — WRITE projects/{project}/00_ICP/icp_confidence_notes.md: under
15 lines, flagging what's backed by strong multi-competitor evidence vs.
a reasoned best-guess from thin evidence. End with a prompt asking the
project owner to approve or correct before the next pipeline run relies
on it.

Re-run whenever market_research is refreshed so the ICP evolves with
the real market instead of staying static.
