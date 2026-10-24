# Chart intent check

> Checks each chart against what its title claims: truncated axes, inconsistent scales, dual axes and unexplained colour.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/chart-intent-check.zip` from this repository, or copy this folder.
2. In Excel, open Copilot, select **Settings**, then **Manage plugins & skills**, then **Custom skills**, then **Create OneDrive folder** and **Open skills folder**. Place the `chart-intent-check` folder inside, then select **Refresh**. Your Office display language must be set to English, or skills do not appear.
3. Type `@chart-intent-check` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Check these charts before they go in the pack"
- "Is this axis misleading?"
- "Are these two charts comparable?"

## Complements, does not duplicate

Complements chart-design: reviews what a reader could wrongly conclude.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live Excel tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
