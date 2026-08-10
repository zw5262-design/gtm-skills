---
name: gtm-enrich-basic
description: Adds free public signals (funding, hiring, tech stack, news) to a sourced list, using the trigger signals defined in that project's ICP.
---

SKILL NAME: gtm-enrich-basic
Persistent, reusable skill — save it, do not run as a one-time task.

STEP 1: Read the Trigger Signals section of
projects/{project}/00_ICP/icp.md.

STEP 2: For each row in companies.csv/contacts.csv, check for each
listed trigger signal specifically — hiring posts, funding, tech stack,
public statements, whatever the ICP names. Add a trigger_type column
identifying which signal is strongest per lead, since scoring and
messaging both key off this.

Output projects/{project}/01_Runs/{date}/enriched_leads.csv with all
prior columns plus per-signal columns and trigger_type. Only include a
signal you can source — blank is a valid, expected result, never guess.
