---
name: gtm-list-builder
description: Sources a company/contact list for a GTM project using that project's configured sourcing method, sources, and volume.
---

SKILL NAME: gtm-list-builder
Persistent, reusable skill — save it, do not run as a one-time task.

STEP 1: Read projects/{project}/00_ICP/icp.md and the SOURCING section
of projects/{project}/00_ICP/operational_config.md — this tells you the
method (auto-search vs. uploaded list), which sources to prioritize, how
many companies per run, and whether contact info is required or
best-effort.

STEP 2: Source companies matching the ICP, using the config's priority-
ordered source list. Skip sources the config marks as not applicable to
this ICP — don't waste search effort on tools that don't fit.

DEDUPLICATION: read projects/{project}/00_ICP/used_companies_log.csv,
exclude anything already listed, append today's finds after.

Output projects/{project}/01_Runs/{date}/companies.csv:
company_name, website, industry, estimated_headcount, funding_stage,
trigger_signal_found, source_url, plus any project-specific columns the
config calls for (e.g. a "track" or "sender_batch" column).

Output contacts.csv per the config's contact requirement — if
best-effort, leave rows/fields blank freely rather than guessing; never
fabricate an email or a contact's name.

Hit the volume target from the config exactly. If short, say so in
run_summary.md with the reason — don't pad with weak fits.
