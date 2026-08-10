---
name: gtm-run-tracker
description: Maintains a project's Master_Dashboard.md as a rolling view across all runs — sends, replies, stalled leads, sourcing pool health.
---

SKILL NAME: gtm-run-tracker
Persistent, reusable skill — save it, do not run as a one-time task.

Update cadence_overview.csv status for touches marked sent, identify
tomorrow's due touches, and maintain
projects/{project}/Master_Dashboard.md with four sections:
1. Send Queue — Tomorrow (lead, company, touch, channel, file path)
2. Pipeline Health (totals sent by tier, reply rate once available)
3. Stalled Leads (any touch overdue 2+ days with no status update)
4. Pool Status (how much of the sourcing pool remains before the ICP
   needs widening)

Keep it a living rolling view, readable in under 2 minutes — update in
place each day, don't just append forever into a growing log.
