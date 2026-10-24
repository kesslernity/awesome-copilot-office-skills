# Assumptions register

> Lists every input with its cell, value, unit, period and stated source, including constants buried inside formulas.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/assumptions-register.zip` from this repository, or copy this folder.
2. In Excel, open Copilot, select **Settings**, then **Manage plugins & skills**, then **Custom skills**, then **Create OneDrive folder** and **Open skills folder**. Place the `assumptions-register` folder inside, then select **Refresh**. Your Office display language must be set to English, or skills do not appear.
3. Type `@assumptions-register` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "What does this model assume?"
- "Build me an assumptions list from this workbook"
- "Find the rates hardcoded inside the formulas"

## Complements, does not duplicate

Complements a documentation sheet: built from the model rather than maintained beside it.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live Excel tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
