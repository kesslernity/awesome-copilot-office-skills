# Copilot in PowerPoint: personal skills

Sources, read 2026-10-24: Microsoft Support, [Use custom skills with Copilot in PowerPoint](https://support.microsoft.com/en-us/powerpoint/copilot/copilot-in-powerpoint-skills) and [Record a skill in Copilot in PowerPoint](https://support.microsoft.com/en-us/powerpoint/copilot/record-skill-copilot-powerpoint); Message Center [MC1434580](https://mc.merill.net/message/MC1434580), [MC1441645](https://mc.merill.net/message/MC1441645), [MC1441782](https://mc.merill.net/message/MC1441782) (July and August 2026), [MC1490903](https://mc.merill.net/message/MC1490903) (7 Oct 2026).

## Install

Option 1, upload: in the Copilot pane select **+ > Choose skills**, scroll to **Manage skills** (newer builds: **Manage plugins & skills**), select **Add skill** and upload `dist/personal/<skill>.zip` or drag in the files. The skill is saved to your OneDrive Skills folder.

Option 2, paste: **Add skill** also offers a form; paste the contents of `SKILL.md` and select **Add**.

Option 3, OneDrive folder: **Settings (...) > Manage skills > Custom skills > Create OneDrive folder**, then **Open skills folder**, copy the skill folder in (folder name exactly as shipped) and select **Refresh**.

Use: **+ > Choose skills**, or type `@<skill-name>` in your prompt.

## Record a Skill (October 2026)

**Manage plugins & skills > Custom skills > Add skill > Record Skill**. Perform the task, select **Stop**, review the drafted name, description and instructions, then **Upload**. Recordings must be under 10 minutes; voice and actions in other windows are not captured. Useful to capture a house formatting routine; the starter skills in this repo are written by hand.

## Limits and notes

- The folder name must equal the `name` in `SKILL.md`, or PowerPoint skips the folder.
- Personal skills are visible only to you.
- ZIP uploads: text types such as md, txt, csv, json, xml, html, svg, py and js are supported; PNG, PDF and nested zips are not.
- Turning a skill off in Manage skills stops automatic use and hides it from the menu.
- **Unconfirmed:** the exact OneDrive path (a community guide reports `Documents/Copilot/Microsoft PowerPoint/skills`; use **Open skills folder** instead), the zip shape PowerPoint expects (this repo's personal zips put the skill folder at the top level), whether files in `references/` are read, whether optional front matter fields are tolerated, and the maximum number of skills per user.
