# Accessibility pass

> Finds accessibility issues, drafts alt text and fixes, and applies only what the owner approves.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes the presentation.

## Install in 60 seconds

1. Download `dist/personal/accessibility-pass.zip` from this repository, or copy this folder.
2. In PowerPoint, open Copilot, select **+**, then **Choose skills**, then **Manage skills** (labelled **Manage plugins & skills** in newer builds), then **Add skill**, and upload the zip. Or place the `accessibility-pass` folder in the Skills folder that **Custom skills > Open skills folder** opens in OneDrive, then select **Refresh**.
3. Type `@accessibility-pass` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Make this deck accessible"
- "Add alt text to every image"
- "Check this presentation for screen reader users"

## Complements, does not duplicate

The application's accessibility checker: adds drafted alt text, jargon and colour-only checks.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live PowerPoint tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
