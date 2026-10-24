# Claude

## claude.ai

Upload `dist/personal/<skill>.zip`. Claude expects the skill folder as the top level of the zip (`<skill>/SKILL.md`), which is the shape this repo builds. In claude.ai go to **Customize > Skills**, select **+**, then **Create skill > Upload a skill**. Custom skills need code execution and file creation enabled.

Sources, read 2026-10-24: [Create custom skills](https://claude.com/docs/skills/how-to), [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

## Claude Code

Copy the skill folder to `~/.claude/skills/<skill>/` (personal) or `.claude/skills/<skill>/` in a repository (project). Source: [Claude Code skills](https://code.claude.com/docs/en/skills).

## Notes

Claude ships its own PowerPoint file skill for creating and editing .pptx files on claude.ai. The skills here describe the presentation method; when Claude cannot edit a deck in place they return slide content as Markdown. **Unconfirmed:** live behaviour of these eight skills in Claude.
