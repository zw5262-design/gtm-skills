---
name: gtm-template-library
description: Writes the reusable, non-personalized outreach message shells for a project, following that project's voice and channel rules.
---

SKILL NAME: gtm-template-library
Persistent, reusable skill — save it, do not run as a one-time task.

STEP 1: Read the VOICE & MESSAGE RULES and CHANNELS sections of
projects/{project}/00_ICP/operational_config.md.

STEP 2: Write message shells (email and/or LinkedIn, per channels
active) that strictly follow the config's word/character limits, tone,
CTA style, and signature. Use {variable} placeholders for
personalization fields — e.g. {first_name}, {company}, {trigger_signal}.
Don't default to generic sales-copy conventions if the config specifies
something more specific.

Every message must implicitly answer: why should they care, why should
they believe this is real, does the sender know something specific
about them, is this a real person not spam, is this worth their time —
without stating any of that outright.

Save to projects/{project}/sequences/templates/.
