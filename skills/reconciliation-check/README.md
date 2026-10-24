# Reconciliation check

> Re-adds every stated total from its components and reports each line that does not tie, with both values. Never edits a number.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/reconciliation-check.zip` from this repository, or copy this folder.
2. In Excel, open Copilot, select **Settings**, then **Manage plugins & skills**, then **Custom skills**, then **Create OneDrive folder** and **Open skills folder**. Place the `reconciliation-check` folder inside, then select **Refresh**. Your Office display language must be set to English, or skills do not appear.
3. Type `@reconciliation-check` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Does this pack tie out?"
- "Re-add these totals and show me what breaks"
- "Check the summary agrees with the detail sheets"

## Complements, does not duplicate

Complements the built-in analysis skills: proves the workbook agrees with itself.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live Excel tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
