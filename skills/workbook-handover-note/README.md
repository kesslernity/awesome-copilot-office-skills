# Workbook handover note

> Drafts the read me the file never had, with UNKNOWN left visible wherever the workbook does not say.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/workbook-handover-note.zip` from this repository, or copy this folder.
2. In Excel, open Copilot, select **Settings**, then **Manage plugins & skills**, then **Custom skills**, then **Create OneDrive folder** and **Open skills folder**. Place the `workbook-handover-note` folder inside, then select **Refresh**. Your Office display language must be set to English, or skills do not appear.
3. Type `@workbook-handover-note` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Write a handover note for this model"
- "I am leaving, document this workbook"
- "What would someone need to know to pick this up?"

## Complements, does not duplicate

Complements a documentation sheet: records what the file evidences and marks the gaps.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live Excel tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
