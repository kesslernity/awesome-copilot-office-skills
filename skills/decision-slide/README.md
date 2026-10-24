# Decision slide

> Builds a DRAFT options, criteria and recommendation slide with a named decision owner and a blank outcome.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes the presentation.

## Install in 60 seconds

1. Download `dist/personal/decision-slide.zip` from this repository, or copy this folder.
2. In PowerPoint, open Copilot, select **+**, then **Choose skills**, then **Manage skills** (labelled **Manage plugins & skills** in newer builds), then **Add skill**, and upload the zip. Or place the `decision-slide` folder in the Skills folder that **Custom skills > Open skills folder** opens in OneDrive, then select **Refresh**.
3. Type `@decision-slide` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Make a decision slide for the vendor choice"
- "I need the steering committee to choose between these three options"
- "Add a recommendation slide with the ask"

## Complements, does not duplicate

Prepare for Questions: turns the debate into an explicit decision request.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live PowerPoint tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
