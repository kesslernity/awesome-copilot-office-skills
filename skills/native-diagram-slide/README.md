# Native diagram slide

> Builds diagram slides from native PowerPoint shapes in your theme, choosing from ten layouts. Editable afterwards, never a picture and never SmartArt.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes the presentation.

This skill reads [references/](references/) alongside `SKILL.md`. Keep the folder together when you copy or zip it.

## Install in 60 seconds

1. Download `dist/personal/native-diagram-slide.zip` from this repository, or copy this folder.
2. In PowerPoint, open Copilot, select **+**, then **Choose skills**, then **Manage skills** (labelled **Manage plugins & skills** in newer builds), then **Add skill**, and upload the zip. Or place the `native-diagram-slide` folder in the Skills folder that **Custom skills > Open skills folder** opens in OneDrive, then select **Refresh**.
3. Type `@native-diagram-slide` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Create me a deck that uses @native-diagram-slide using this information", then paste your content
- "Turn slide 4 into a process flow with swimlanes"
- "Make this list a 2x2"
- "Draw the roadmap as a timeline, and mark which dates are confirmed"

## Complements, does not duplicate

Narrative builder and Designer: those lay out text and pick images. This draws structure from your content as editable shapes.

## Status

Format-validated by `scripts/validate` on 2026-10-25. Tested in a live PowerPoint tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-25 | Initial version |
