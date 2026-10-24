# Brand rules check

> Checks each slide against a written brand rules file and reports PASS, FIX PROPOSED or MANUAL CHECK.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes the presentation.

## Install in 60 seconds

1. Download `dist/personal/brand-rules-check.zip` from this repository, or copy this folder.
2. In PowerPoint, open Copilot, select **+**, then **Choose skills**, then **Manage skills** (labelled **Manage plugins & skills** in newer builds), then **Add skill**, and upload the zip. Or place the `brand-rules-check` folder in the Skills folder that **Custom skills > Open skills folder** opens in OneDrive, then select **Refresh**.
3. Type `@brand-rules-check` in the Copilot prompt, followed by your request.

### Your brand rules: two routes

This skill needs your written rules. The zip ships `references/brand-rules-template.md`, never a filled-in `brand-rules.md`, because the rules are yours.

- **Fastest, and works everywhere.** Run `@brand-rules-check` and paste your rules into the chat when it asks. No file needed.
- **Persistent.** Copy `references/brand-rules-template.md` to `references/brand-rules.md` inside the skill folder in your OneDrive Skills folder, fill it in, then select **Refresh**. Note that whether PowerPoint reads files in `references/` is **Unconfirmed**, so test this route before relying on it.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Is this deck on brand?"
- "Check these slides against our brand guidelines"
- "Find anything off-template before this goes to the client"

## Complements, does not duplicate

Brand Kit: an auditable written report that also works where Brand Kit is not set up.

## Status

Format-validated by `scripts/validate` on 2026-10-24. Tested in a live PowerPoint tenant: pending. Report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-10-24 | Initial version |
