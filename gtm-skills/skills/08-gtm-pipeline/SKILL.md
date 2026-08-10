---
name: gtm-pipeline
description: Orchestrates gtm-list-builder through gtm-sequence-builder for a project's daily run, respecting its volume and send-cap settings.
---

SKILL NAME: gtm-pipeline
Persistent, reusable skill — save it, do not run as a one-time task.

Run in this exact order for the specified project:
gtm-list-builder → gtm-enrich-basic → gtm-score-leads →
gtm-sequence-builder.

Respect the project's configured volume-per-run and any send-cap
priority rules from operational_config.md (e.g. best tier sent first
when a daily cap would otherwise be exceeded). Stop and alert the
project owner if more than 30-40% of a run gets flagged for review or
removed — that signals the sourcing pass came back thin, not a normal
outcome to push through silently.

Write run_summary.md: totals by tier, flags and reasons, any touches
bumped due to a send cap, and the exact file paths ready to send today.
