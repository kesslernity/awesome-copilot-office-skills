# Awesome Copilot Office Skills

> **24 custom skills for Copilot in Excel and Copilot in PowerPoint, in the open Agent Skills format.** Upload a zip, drop a folder in OneDrive, or have IT deploy them to the organisation. The same `SKILL.md` files run in Claude, ChatGPT and Codex, GitHub Copilot and VS Code, Gemini CLI and Mistral Vibe. Every skill drafts and then stops for your approval.

[![GitHub stars](https://img.shields.io/github/stars/kesslernity/awesome-copilot-office-skills?style=flat-square)](https://github.com/kesslernity/awesome-copilot-office-skills/stargazers)
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
[![Skills](https://img.shields.io/badge/skills-24-blue)](skills/)
[![Format: Agent Skills](https://img.shields.io/badge/format-Agent%20Skills-green)](https://agentskills.io/specification)

This is a community library, not affiliated with or endorsed by Microsoft. Every vendor claim below names its source and the date it was read (24 October 2026). Anything not documented is marked **Unconfirmed**.

---

## Two rules behind every file

- **Prompts are the asset, models are commodities.** A skill is a text file you own. It outlives the model and the vendor, so it is written once in an open format and run wherever you work.
- **AI prepares, people decide.** Each skill drafts, shows you what it would change, and waits. Nothing is applied, approved or decided until a person says so. Reconciliation breaks stay breaks until you resolve them, decision slides keep a blank outcome field, and scenario cases ship empty.

---

## What a Copilot skill is (60 seconds)

A skill is a folder containing one file, `SKILL.md`: a short header with a `name` and a `description` telling Copilot when to use it, then plain instructions. Both apps discover skills from a Skills folder in your OneDrive, and both skip any folder whose name does not match the `name` inside the file. You call one directly with `@skill-name`, or Copilot picks an enabled skill when your request matches its description.

| Surface | Where skills come from | Since | Source |
|---|---|---|---|
| Copilot in Excel, custom skills | You, via OneDrive or `@skill-builder` | June 2026, updated October 2026 | [Use skills with Copilot in Excel](https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills) |
| Copilot in Excel, Microsoft skills | Microsoft: `@brandkit`, `@chart-design`, `@clean-data`, `@skill-builder`, `@theme-design` | October 2026 | [Skills created by Microsoft](https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-built-in-skills) |
| Copilot in PowerPoint, personal skills | You, by upload, paste or OneDrive folder | July to August 2026 | [Use custom skills with Copilot in PowerPoint](https://support.microsoft.com/en-us/powerpoint/copilot/copilot-in-powerpoint-skills); [MC1434580](https://mc.merill.net/message/MC1434580), [MC1441645](https://mc.merill.net/message/MC1441645) |
| Copilot in PowerPoint, Record a Skill | You, by demonstration | October 2026 | [Record a skill](https://support.microsoft.com/en-us/powerpoint/copilot/record-skill-copilot-powerpoint); [MC1490903](https://mc.merill.net/message/MC1490903) |
| Organization skills | Your Microsoft 365 admin | Worldwide September 2026 | [Deploy organization skills](https://support.microsoft.com/en-us/powerpoint/copilot/deploy-organization-skills-for-copilot-in-powerpoint); [MC1463509](https://mc.merill.net/message/MC1463509) |

Both Microsoft pages say custom skills "must follow the industry standard format" and link the Agent Skills specification. That standard was donated by Anthropic to the Agentic AI Foundation under the Linux Foundation on 22 October 2026, after more than 70 agent platforms had adopted it ([Anthropic](https://www.anthropic.com/news/donating-agent-skills-to-the-agentic-ai-foundation), [Linux Foundation](https://www.linuxfoundation.org/press/agentic-ai-foundation-announces-four-new-projects-agent-skills-open-responses-openenv-and-opensandbox)). That is why one folder runs in Excel, in PowerPoint and in half a dozen tools that are not Microsoft's.

Not the same thing: skills attached to a declarative agent in Agent Builder, and skills in Copilot Chat and Cowork. Same file format, different surfaces, different install paths. See [runtimes/](runtimes/).

---

## Install

### Excel, personal skill (no admin)

1. Download a zip from `dist/personal/`, or download this repository (**Code > Download ZIP**) and extract it outside OneDrive.
2. In Excel, open Copilot, select **Settings (...) > Manage plugins & skills > Custom skills > Create OneDrive folder**, then **Open skills folder**.
3. Copy the skill folder in with its name unchanged, then select **Refresh**.
4. Type `@reconciliation-check` (or any skill name) followed by your request.

🔴 **Your Microsoft Office display language must be set to English**, or skills do not appear in Excel at all. This is the most common reason a correctly built skill is invisible ([Use skills with Copilot in Excel](https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills)).

### PowerPoint, personal skill (no admin)

1. Download a zip from `dist/personal/`, or download this repository and extract it outside OneDrive.
2. In PowerPoint, open Copilot, select **+ > Choose skills**, scroll to **Manage skills** (labelled **Manage plugins & skills** in newer builds) and select **Add skill**. Upload the zip, or paste the contents of `SKILL.md` into the form.
3. Or use the folder route: **Settings (...) > Manage skills > Custom skills > Create OneDrive folder > Open skills folder**, copy the folder in, then select **Refresh**.
4. Type `@outline-first-deck` followed by your request.

Personal skills are visible only to you.

### Record a Skill (PowerPoint, your own routine)

For a formatting routine you repeat, Copilot can draft a skill from what you do: **Manage plugins & skills > Custom skills > Add skill > Record Skill**, perform the task, select **Stop**, review the drafted instructions, then **Upload**. In Excel the equivalent is `@skill-builder`, which drafts a skill from your instructions, previous prompts or a completed workflow.

### Organisation-wide (admin)

Your admin builds packages with `python3 scripts/build-dist` (manifest version 1.30 with an `agentSkills` array, plus two icons) and uploads them in the Microsoft 365 admin center under **Agents > All agents > Add agent**, targeting all users or chosen groups. Full guide: [org-deploy/README.md](org-deploy/README.md).

---

## Excel skill catalog (12)

| Skill | What it does | Complements | Download |
|---|---|---|---|
| [workbook-structure-audit](skills/workbook-structure-audit/) | Maps every sheet including hidden ones, named ranges, external links, filters and protection. Changes nothing | Complements the built-in analysis skills | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/workbook-structure-audit.zip) |
| [formula-risk-review](skills/formula-risk-review/) | Finds the formula faults that return a plausible wrong number instead of an error. Edits no formula | Complements error checking | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/formula-risk-review.zip) |
| [lookup-integrity-check](skills/lookup-integrity-check/) | Checks every lookup for approximate match, duplicate keys, unmatched keys and type mismatches. Changes nothing | Complements clean-data | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/lookup-integrity-check.zip) |
| [data-quality-sweep](skills/data-quality-sweep/) | Profiles a table and reports mixed types, text numbers, duplicates, category variants and blanks. Corrects nothing | Complements clean-data | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/data-quality-sweep.zip) |
| [reconciliation-check](skills/reconciliation-check/) | Re-adds every stated total from its components and reports each line that does not tie, with both values. Never edits a number | Complements the built-in analysis skills | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/reconciliation-check.zip) |
| [units-and-rounding-check](skills/units-and-rounding-check/) | Finds thousands mixed with millions, multiple currencies summed together and display rounding that hides a real break | Complements number formatting | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/units-and-rounding-check.zip) |
| [assumptions-register](skills/assumptions-register/) | Lists every input with its cell, value, unit, period and stated source, including constants buried inside formulas | Complements a documentation sheet | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/assumptions-register.zip) |
| [model-map](skills/model-map/) | Traces the calculation chain behind one output cell back to its inputs, and flags typed overrides in the middle | Complements trace precedents | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/model-map.zip) |
| [variance-explainer](skills/variance-explainer/) | Splits a movement into the drivers the data supports and reports the remainder as unexplained. Invents no driver | Complements the built-in analysis skills | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/variance-explainer.zip) |
| [chart-intent-check](skills/chart-intent-check/) | Checks each chart against what its title claims: truncated axes, inconsistent scales, dual axes and unexplained colour | Complements chart-design | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/chart-intent-check.zip) |
| [scenario-skeleton](skills/scenario-skeleton/) | Builds a base, downside and upside scaffold wired to a case switch, and leaves every scenario value blank | Complements what-if analysis | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/scenario-skeleton.zip) |
| [workbook-handover-note](skills/workbook-handover-note/) | Drafts the read me the file never had, with UNKNOWN left visible wherever the workbook does not say | Complements a documentation sheet | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/workbook-handover-note.zip) |

## PowerPoint skill catalog (12)

| Skill | What it does | Complements | Download |
|---|---|---|---|
| [outline-first-deck](skills/outline-first-deck/) | Drafts a sourced slide outline, waits for approval, then builds the deck | Create a presentation from a file (Narrative builder) | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/outline-first-deck.zip) |
| [executive-summary-slide](skills/executive-summary-slide/) | Adds one approved summary slide of three to five conclusions, each traced to its source slide | Review this presentation | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/executive-summary-slide.zip) |
| [action-title-rewrite](skills/action-title-rewrite/) | Proposes full-sentence action titles and a storyline check, applied only after approval | Rewrite | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/action-title-rewrite.zip) |
| [numbers-and-claims-check](skills/numbers-and-claims-check/) | Registers every figure and claim with its source and flags unsourced or inconsistent items. Never edits a figure | Review this presentation and Prepare for Questions | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/numbers-and-claims-check.zip) |
| [brand-rules-check](skills/brand-rules-check/) | Checks each slide against a written brand rules file and reports PASS, FIX PROPOSED or MANUAL CHECK | Brand Kit | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/brand-rules-check.zip) |
| [decision-slide](skills/decision-slide/) | Builds a DRAFT options, criteria and recommendation slide with a named decision owner and a blank outcome | Prepare for Questions | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/decision-slide.zip) |
| [accessibility-pass](skills/accessibility-pass/) | Finds accessibility issues, drafts alt text and fixes, and applies only what the owner approves | The application's accessibility checker | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/accessibility-pass.zip) |
| [steering-committee-status-deck](skills/steering-committee-status-deck/) | Builds a DRAFT five to seven slide status pack with proposed RAG statuses the user confirms | None directly | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/steering-committee-status-deck.zip) |
| [speaker-notes-builder](skills/speaker-notes-builder/) | Drafts a talk track per slide, marks where a note would need a fact the deck lacks, and flags notes that contradict their slide | Complements Prepare for Questions | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/speaker-notes-builder.zip) |
| [deck-trim-proposal](skills/deck-trim-proposal/) | Proposes what to cut, merge or move so a deck fits its slot, naming what is lost in each case. Deletes nothing | Complements Review this presentation | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/deck-trim-proposal.zip) |
| [deck-consistency-sweep](skills/deck-consistency-sweep/) | Finds terms used two ways, unexpanded acronyms, mixed date and number formats and renamed products across the whole deck | Complements Rewrite | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/deck-consistency-sweep.zip) |
| [appendix-split](skills/appendix-split/) | Separates the presented argument from its supporting detail, leaving a pointer on every slide that lost support | Complements deck-trim-proposal | [zip](https://github.com/kesslernity/awesome-copilot-office-skills/raw/main/dist/personal/appendix-split.zip) |

None of these duplicates a built-in. Rewrite, translate and speaker notes already run through Copilot chat in PowerPoint ([MC1243550](https://mc.merill.net/message/MC1243550), March 2026), and Excel ships its own cleaning, charting and theming skills, so nothing here competes with `@clean-data`, `@chart-design` or `@theme-design`. `data-quality-sweep` reports and quantifies rather than cleaning, which is the difference.

**Status, 24 October 2026:** all 24 are format-validated by `scripts/validate`. Live tenant tests are pending; each skill's README carries its own tested-with line.

---

## Same file, other tools

The skills are written host-neutral. Where a tool can edit the open file, the skill edits it after approval; where it cannot, the skill returns its output as Markdown to paste.

| Tool | Where the folder goes | Page |
|---|---|---|
| Claude (claude.ai, Claude Code) | Upload `dist/personal/<skill>.zip`; or `~/.claude/skills/` | [runtimes/claude.md](runtimes/claude.md) |
| ChatGPT and Codex | ChatGPT Skills upload; Codex `.agents/skills/` | [runtimes/chatgpt-codex.md](runtimes/chatgpt-codex.md) |
| GitHub Copilot and VS Code | `.github/skills/`, `.agents/skills/` or `~/.copilot/skills/` | [runtimes/github-copilot-vscode.md](runtimes/github-copilot-vscode.md) |
| Gemini CLI | `.gemini/skills/` or `.agents/skills/` | [runtimes/gemini-cli.md](runtimes/gemini-cli.md) |
| Mistral Vibe | `.agents/skills/` or `~/.vibe/skills/`; web Context > Skills | [runtimes/mistral-vibe.md](runtimes/mistral-vibe.md) |
| Copilot Chat, Cowork, declarative agents | See page | [runtimes/copilot-chat-and-declarative-agents.md](runtimes/copilot-chat-and-declarative-agents.md) |

Each folder is kept to `name` and `description` in the header, instructions under 20,000 characters (the strictest documented Microsoft limit) and text-only references, so one file passes every runtime's loader. Live behaviour outside the Microsoft 365 apps is not yet tested.

---

## Licensing and cost

- **You need Copilot in the app.** Microsoft's licence page: a *Copilot Chat (Basic)* account has no Copilot in Word, Excel, PowerPoint or OneNote; *M365 Copilot (Basic)* has standard access in the apps; *M365 Copilot (Premium)* has the add-on licence with priority access ([What Copilot license do I have](https://support.microsoft.com/en-us/microsoft-365-copilot/what-copilot-license-do-i-have), updated April 2026).
- **Unconfirmed: whether custom skills work on M365 Copilot (Basic)**, in either app. No page states the tier for custom skills.
- **Unconfirmed: Copilot Credits.** Neither the Excel nor the PowerPoint skills page mentions Copilot Credits. Cowork is billed in credits; that is a different surface.
- Organization skills need a Microsoft 365 admin who can publish in the admin center.

## Known limits

- Folder name must equal `name`, or the skill is skipped. This is documented for both apps.
- **Excel is English only.** Your Office display language must be English.
- ZIP uploads: PNG, PDF and nested zips are not supported. This repo ships text only.
- Excel's documentation permits `scripts`, `references` and `assets` subfolders. **This repository deliberately ships no scripts**, so that one folder is safe to drop into either app and into every runtime above, and so nothing here executes on your machine.
- Edit files in OneDrive, then select **Refresh** in Custom skills.
- **Unconfirmed:** whether Excel and PowerPoint read the same OneDrive Skills folder or two separate ones, whether PowerPoint reads files in `references/`, whether optional header fields such as `license` are tolerated, the zip shape PowerPoint expects, and the maximum number of skills per user in either app.

---

## Contributing

Read [CONTRIBUTING.md](CONTRIBUTING.md). In short: one folder per skill directly under `skills/`, a `surface` entry in `scripts/catalog.json`, a header with exactly `name` and `description` (quoted), the nine required sections including a human approval checkpoint, no scripts or images, British spelling, no em dashes, and `python3 scripts/validate` must pass. Tenant reports, including things that worked, are the most useful contribution: use the issue template.

## Sibling repositories

- [awesome-copilot-cowork-skills](https://github.com/kesslernity/awesome-copilot-cowork-skills): folder-drop skills for Copilot Cowork.
- [awesome-copilot-agent-skills](https://github.com/kesslernity/awesome-copilot-agent-skills): skills for declarative agents in Agent Builder.
- [awesome-microsoft-copilot-prompts](https://github.com/kesslernity/awesome-microsoft-copilot-prompts): single-message prompts.
- [awesome-mistral-vibe-skills](https://github.com/kesslernity/awesome-mistral-vibe-skills): Agent Skills for Mistral Vibe.

## From the same author

- [The Real Cost of Copilot, sample](https://store.kesslernity.com/l/mgyzb?utm_source=github&utm_medium=readme&utm_campaign=office-skills)
- [Copilot Deployment Kit](https://store.kesslernity.com/l/kpfpi?utm_source=github&utm_medium=readme&utm_campaign=office-skills)

Store pages carry their own terms, separate from this repository's licence.

<sub>Content licensed CC BY-SA 4.0. Not affiliated with, or endorsed by, Microsoft, Anthropic, OpenAI, GitHub, Google or Mistral AI.</sub>
