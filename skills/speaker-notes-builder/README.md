# Speaker notes builder

> Drafts a talk track per slide, marks where a note would need a fact the deck lacks, and flags notes that contradict their slide.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/speaker-notes-builder.zip` from this repository, or copy this folder.
2. In PowerPoint, open Copilot, select **+**, then **Choose skills**, then **Manage skills** (labelled **Manage plugins & skills** in newer builds), then **Add skill**, and upload the zip. Or place the `speaker-notes-builder` folder in the Skills folder that **Custom skills > Open skills folder** opens in OneDrive, then select **Refresh**.
3. Type `@speaker-notes-builder` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Write speaker notes for this deck"
- "Give me a talk track for a 20 minute slot"
- "Do my existing notes contradict the slides?"

## Complements, does not duplicate

Complements Prepare for Questions: writes the notes layer and refuses to invent facts.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live PowerPoint tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
