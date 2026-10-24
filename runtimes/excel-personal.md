# Copilot in Excel: personal custom skills

Sources, read 2026-10-24: Microsoft Support, [Use skills with Copilot in Excel to complete repeatable tasks](https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills) and [Use built-in skills and skills created by Microsoft with Copilot in Excel](https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-built-in-skills). Format: [Agent Skills specification](https://agentskills.io/specification).

## Before anything else

🔴 **Your Microsoft Office display language must be set to English.** Microsoft states that skills in Copilot in Excel are supported only in English. If the display language is anything else, custom skills do not appear at all, and nothing about the skill folder is at fault. This is the first thing to check when a correctly built skill is invisible.

## Install

1. Open a workbook and open the Copilot pane.
2. Select **Settings (...)**, then **Manage plugins & skills**, then **Custom skills**.
3. Select **Create OneDrive folder**, then **Open skills folder**.
4. Copy the skill folder in, keeping its name exactly as it is. Copilot skips any folder whose name does not match the `name` inside its `SKILL.md`.
5. Back in **Custom skills**, select **Refresh**.

## Use

Type `@` followed by the skill name in the Copilot prompt, for example `@reconciliation-check`, then your request. Copilot can also choose an enabled skill on its own when your request matches its description, which is why the `description` line in each file is written as a trigger rather than a summary.

Toggle skills on and off in **Manage plugins & skills**. A skill that is switched off can still be called explicitly with an at mention; switching it off only stops Copilot reaching for it unprompted.

## Do not collide with Microsoft's own skills

Excel ships managed skills that are enabled by default: `@brandkit`, `@chart-design`, `@clean-data`, `@skill-builder` and `@theme-design`. None of the skills in this repository uses those names, and `data-quality-sweep` is deliberately scoped to reporting and quantifying rather than cleaning, so it complements `@clean-data` instead of competing with it.

`@skill-builder` is the fastest way to turn one of your own recurring workflows into a skill. Use it alongside these files rather than instead of them.

## What Excel supports that this repository does not use

Microsoft documents that a custom skill may also contain `scripts`, `references` and `assets` subfolders, following the Agent Skills optional directories. **This repository ships text only and no scripts at all.** That is a deliberate choice, not a platform limit: one folder then drops safely into Excel, into PowerPoint and into every other runtime listed here, and nothing in this repository executes on your machine.

## Unconfirmed

- Whether Excel and PowerPoint read the same OneDrive Skills folder, or two separate ones. Install into each app's own folder until this is settled.
- The maximum number of custom skills per user in Excel. Cowork documents a limit of 50 for its own surface; no Excel page states one.
- Whether custom skills work on an account licensed as M365 Copilot (Basic), or only Premium.
- Whether running a skill consumes Copilot Credits. No Excel skills page mentions credits.

Report what you find with the tenant behaviour issue template.
