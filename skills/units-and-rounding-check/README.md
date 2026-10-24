# Units and rounding check

> Finds thousands mixed with millions, multiple currencies summed together and display rounding that hides a real break.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/units-and-rounding-check.zip` from this repository, or copy this folder.
2. In Excel, open Copilot, select **Settings**, then **Manage plugins & skills**, then **Custom skills**, then **Create OneDrive folder** and **Open skills folder**. Place the `units-and-rounding-check` folder inside, then select **Refresh**. Your Office display language must be set to English, or skills do not appear.
3. Type `@units-and-rounding-check` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Why is this total one out?"
- "Check the units are consistent across these sheets"
- "Are we mixing currencies anywhere in this model?"

## Complements, does not duplicate

Complements number formatting: reads units as meaning, not as formatting.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live Excel tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
