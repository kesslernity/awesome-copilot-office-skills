# Scenario skeleton

> Builds a base, downside and upside scaffold wired to a case switch, and leaves every scenario value blank.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/scenario-skeleton.zip` from this repository, or copy this folder.
2. In Excel, open Copilot, select **Settings**, then **Manage plugins & skills**, then **Custom skills**, then **Create OneDrive folder** and **Open skills folder**. Place the `scenario-skeleton` folder inside, then select **Refresh**. Your Office display language must be set to English, or skills do not appear.
3. Type `@scenario-skeleton` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Add scenarios to this model"
- "Set up a downside and upside case"
- "Wire these inputs to a scenario switch"

## Complements, does not duplicate

Complements what-if analysis: builds the frame and refuses to invent the cases.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live Excel tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
