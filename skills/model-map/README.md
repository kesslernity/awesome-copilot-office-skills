# Model map

> Traces the calculation chain behind one output cell back to its inputs, and flags typed overrides in the middle.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/model-map.zip` from this repository, or copy this folder.
2. In Excel, open Copilot, select **Settings**, then **Manage plugins & skills**, then **Custom skills**, then **Create OneDrive folder** and **Open skills folder**. Place the `model-map` folder inside, then select **Refresh**. Your Office display language must be set to English, or skills do not appear.
3. Type `@model-map` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "How is this number calculated?"
- "Trace this total back to its inputs"
- "What would change if I moved this assumption?"

## Complements, and where it overlaps

Complements check-model: traces one output cell on any workbook, reports only.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live Excel tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
