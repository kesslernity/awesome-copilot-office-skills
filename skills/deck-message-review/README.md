# Deck message review

> Reads the whole deck and reports the message it actually makes, whether the slides build it in order, and whether it ends with a clear ask. Reports only.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes the presentation.

## Install in 60 seconds

1. Download `dist/personal/deck-message-review.zip` from this repository, or copy this folder.
2. In PowerPoint, open Copilot, select **+**, then **Choose skills**, then **Manage skills** (labelled **Manage plugins & skills** in newer builds), then **Add skill**, and upload the zip. Or place the `deck-message-review` folder in the Skills folder that **Custom skills > Open skills folder** opens in OneDrive, then select **Refresh**.
3. Type `@deck-message-review` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Does this deck land?"
- "What is the message a reader takes from this?"
- "Is this ready for the steering committee?"

## Complements, does not duplicate

Review this presentation: that comments slide by slide. This judges the deck as one argument and names the ask, or its absence.

## Status

Format-validated by `scripts/validate` on 2026-10-25. Tested in a live PowerPoint tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-25 | Initial version |
