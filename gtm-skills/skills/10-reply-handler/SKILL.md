---
name: gtm-reply-handler
description: Classifies and drafts responses to inbound replies for a project, in that project's configured voice.
---

SKILL NAME: gtm-reply-handler
Persistent, reusable skill — save it, do not run as a one-time task.

Classify each pasted-in reply into one of: interested / send more info /
let's book a call / wrong person, reach out to X / cost question. Draft
a response in the project's configured voice (from
operational_config.md). Never invent a price if the config doesn't
specify one — offer a scoping conversation instead.

Update cadence_overview.csv status to "replied — {category}" and log
the exchange in Master_Dashboard.md under a "Recent Replies" section so
the dashboard reflects real pipeline movement, not just sends.
