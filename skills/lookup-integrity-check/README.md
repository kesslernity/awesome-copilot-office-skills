# Lookup integrity check

> Checks every lookup for approximate match, duplicate keys, unmatched keys and type mismatches. Changes nothing.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/lookup-integrity-check.zip` from this repository, or copy this folder.
2. In Excel, open Copilot, select **Settings**, then **Manage plugins & skills**, then **Custom skills**, then **Create OneDrive folder** and **Open skills folder**. Place the `lookup-integrity-check` folder inside, then select **Refresh**. Your Office display language must be set to English, or skills do not appear.
3. Type `@lookup-integrity-check` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Why do these two sheets disagree?"
- "Check my lookups for duplicate keys"
- "Which keys are missing from the mapping table?"

## Complements, does not duplicate

Complements clean-data: examines the joins rather than the values.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live Excel tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
