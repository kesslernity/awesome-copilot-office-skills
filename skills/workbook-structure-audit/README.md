# Workbook structure audit

> Maps every sheet including hidden ones, named ranges, external links, filters and protection. Changes nothing.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/workbook-structure-audit.zip` from this repository, or copy this folder.
2. In Excel, open Copilot, select **Settings**, then **Manage plugins & skills**, then **Custom skills**, then **Create OneDrive folder** and **Open skills folder**. Place the `workbook-structure-audit` folder inside, then select **Refresh**. Your Office display language must be set to English, or skills do not appear.
3. Type `@workbook-structure-audit` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "What is actually in this workbook?"
- "I inherited this file, map it for me"
- "Are there hidden sheets or external links in here?"

## Complements, and where it overlaps

None directly: describes the container rather than the calculations.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live Excel tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
