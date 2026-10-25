# AI writing tells check

> Finds the patterns that make slide text read as machine-written and proposes a plain rewrite for each. Changes no number.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes the presentation.

This skill reads [references/](references/) alongside `SKILL.md`. Keep the folder together when you copy or zip it.

## Install in 60 seconds

1. Download `dist/personal/ai-writing-tells-check.zip` from this repository, or copy this folder.
2. In PowerPoint, open Copilot, select **+**, then **Choose skills**, then **Manage skills** (labelled **Manage plugins & skills** in newer builds), then **Add skill**, and upload the zip. Or place the `ai-writing-tells-check` folder in the Skills folder that **Custom skills > Open skills folder** opens in OneDrive, then select **Refresh**.
3. Type `@ai-writing-tells-check` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "This deck sounds like AI, fix the wording"
- "Run an AI tells check before this goes to the client"
- "Make slides 3 to 9 sound like a person wrote them"

## Complements, does not duplicate

Rewrite: that rewrites for tone on request. This names the specific tell on each slide and leaves every figure untouched.

## Status

Format-validated by `scripts/validate` on 2026-10-25. Tested in a live PowerPoint tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-25 | Initial version |
