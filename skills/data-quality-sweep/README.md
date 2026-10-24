# Data quality sweep

> Profiles a table and reports mixed types, text numbers, duplicates, category variants and blanks. Corrects nothing.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/data-quality-sweep.zip` from this repository, or copy this folder.
2. In Excel, open Copilot, select **Settings**, then **Manage plugins & skills**, then **Custom skills**, then **Create OneDrive folder** and **Open skills folder**. Place the `data-quality-sweep` folder inside, then select **Refresh**. Your Office display language must be set to English, or skills do not appear.
3. Type `@data-quality-sweep` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Check the quality of this dataset before I pivot it"
- "Why is my pivot splitting the same category in two?"
- "Profile these columns and tell me what is wrong"

## Complements, does not duplicate

Complements clean-data: reports and quantifies rather than cleaning.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live Excel tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
