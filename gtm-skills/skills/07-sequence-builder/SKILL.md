---
name: gtm-sequence-builder
description: Personalizes outreach for each scored lead using the project's templates and cadence rules — never invents personalization details.
---

SKILL NAME: gtm-sequence-builder
Persistent, reusable skill — save it, do not run as a one-time task.

STEP 1: Read scored_leads.csv, sequences/templates/*, and the CADENCE
section of projects/{project}/00_ICP/operational_config.md.

STEP 2: For each lead, assign the cadence per its tier (from config),
select/fill the appropriate template, and populate every {variable}
with real data from the lead's row. If a variable can't be filled with
something real and specific, fall back to the simplest/safest template
variant and flag the lead for manual review — never fabricate a detail.

Output cadence_overview.csv (lead_id, company, tier, touch_number,
channel, send_day, status, flagged_for_review) and a personalized file
per lead at sequences/personalized/Lead_{n}_{company}.md, following
whatever channel-routing rules the config specifies (e.g. email to
auto-send queue, LinkedIn always manual).
