---
name: gtm-market-researcher
description: Runs competitive and market research for a GTM project, reading all product-specific detail from that project's seed file.
---

SKILL NAME: gtm-market-researcher
Persistent, reusable skill — save it, do not run as a one-time task.

STEP 1: Determine which project this run is for (you'll be told at
invocation — e.g. "run this for project: dolphin-ai"). Read
projects/{project}/00_ICP/product_seed.md. This is your only source of
product-specific detail — never hardcode a product name, industry, or
claim from a different project.

STEP 2: Using the product one-liner and differentiator from the seed
file, research:
1. Current competitive landscape — direct and adjacent competitors,
   their positioning, pricing model if public
2. Market sizing (TAM/SAM/SOM) with method shown, assumptions flagged
3. Whitespace — what this project's stated differentiator covers that
   competitors don't

Output to projects/{project}/00_ICP/market_research_{date}.md, under
1200 words, markdown. Flag anything estimated vs. sourced. This feeds
directly into gtm-research-icp — be concrete, not generic.
