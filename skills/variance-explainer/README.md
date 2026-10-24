# Variance explainer

> Splits a movement into the drivers the data supports and reports the remainder as unexplained. Invents no driver.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/variance-explainer.zip` from this repository, or copy this folder.
2. In Excel, open Copilot, select **Settings**, then **Manage plugins & skills**, then **Custom skills**, then **Create OneDrive folder** and **Open skills folder**. Place the `variance-explainer` folder inside, then select **Refresh**. Your Office display language must be set to English, or skills do not appear.
3. Type `@variance-explainer` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Why did this move between the two periods?"
- "Bridge plan to actual for me"
- "Explain this variance and show what is unexplained"

## Complements, and where it overlaps

None directly: refuses to force the bridge to tie.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live Excel tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
