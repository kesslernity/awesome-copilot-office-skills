# Formula risk review

> Finds the formula faults that return a plausible wrong number instead of an error. Edits no formula.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/formula-risk-review.zip` from this repository, or copy this folder.
2. In Excel, open Copilot, select **Settings**, then **Manage plugins & skills**, then **Custom skills**, then **Create OneDrive folder** and **Open skills folder**. Place the `formula-risk-review` folder inside, then select **Refresh**. Your Office display language must be set to English, or skills do not appear.
3. Type `@formula-risk-review` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Review the formulas in this model before I send it"
- "Are there any hardcoded numbers inside these formulas?"
- "Check the sum ranges cover the whole block"

## Complements, and where it overlaps

Complements check-model: works on any workbook, reports only, never edits.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live Excel tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
