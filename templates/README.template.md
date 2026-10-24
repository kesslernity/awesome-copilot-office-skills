# Your skill name

> One sentence, the same promise as the catalog summary. Say what it never does.

## What it produces

See the Output section of [SKILL.md](SKILL.md). Every output is a draft: the skill stops at a human approval checkpoint before it changes anything.

## Install in 60 seconds

1. Download `dist/personal/your-skill-name.zip` from this repository, or copy this folder.
2. Excel: unzip, then **Settings > Manage plugins & skills > Custom skills > Open skills folder**, copy the folder in, then **Refresh**. Your Office display language must be English. PowerPoint: **+ > Choose skills > Manage skills > Add skill**, upload the zip, or use the OneDrive folder route.
3. Type `@your-skill-name` in the Copilot prompt, followed by your request.

Other tools: see [runtimes/](../../runtimes/).

## Example triggers

- "Something a user would actually type"
- "A second phrasing"
- "A third"

## Example

Illustrative example, invented data, not a tenant run.

Input: two lines describing the file this was run against.

| Column | Column | Column |
|---|---|---|
| Three to five abridged rows in the skill's exact Output format. | | |

## Complements, and where it overlaps

Name the built-in it sits beside, and state the concrete difference. If there is none, say "None directly" and why.

## Status

Format-validated by `scripts/validate` on YYYY-MM-DD. Tested in a live tenant: pending. See [STATUS.md](../../STATUS.md) and report results with the tenant behaviour issue template.

## Changelog

| Version | Date | Change |
|---|---|---|
| 1.0 | YYYY-MM-DD | Initial version |
