# Questions people actually ask

Every answer here is sourced, and anything Microsoft does not document is marked **Unconfirmed**
rather than guessed. Sources read 24 October 2026.

## How do I add a custom skill to Copilot in PowerPoint?

Three routes, all documented on [Use custom skills with Copilot in PowerPoint](https://support.microsoft.com/en-us/powerpoint/copilot/copilot-in-powerpoint-skills):
upload a zip or paste the skill in the Copilot pane under **+ > Choose skills > Manage skills >
Add skill**, or copy the folder into the Skills folder that **Custom skills > Open skills folder**
opens in OneDrive and select **Refresh**.

## How do I add one to Copilot in Excel?

The OneDrive folder route only: **Settings > Manage plugins & skills > Custom skills > Create
OneDrive folder > Open skills folder**, copy the folder in, select **Refresh**
([Use skills with Copilot in Excel](https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills)).
Excel has no Add skill upload, so unzip first. You can also build one from your own workflow with
`@skill-builder`.

## Why does my skill not appear?

In order of how often it is the cause:

1. **Excel: your Office display language is not English.** Microsoft states skills in Copilot in
   Excel are supported only in English. Nothing about the folder is wrong.
2. **The folder name does not match the `name` inside `SKILL.md`.** Both apps skip a folder whose
   name does not match. This is documented for both.
3. **You did not select Refresh** after editing in OneDrive.
4. **Zip shape.** Which shape PowerPoint's Add skill accepts is **Unconfirmed**, which is why this
   repository ships both `dist/personal/` (folder at the top) and `dist/root/` (SKILL.md at the root).

## Do custom skills need Microsoft 365 Copilot Premium?

**Unconfirmed.** What is documented: a *Copilot Chat (Basic)* account has no Copilot in Word, Excel,
PowerPoint or OneNote at all; *M365 Copilot (Basic)* has standard access in the apps; *M365 Copilot
(Premium)* has the add-on licence with priority access
([What Copilot license do I have](https://support.microsoft.com/en-us/microsoft-365-copilot/what-copilot-license-do-i-have),
updated April 2026). No page states the tier required for custom skills specifically.

## Do these consume Copilot Credits?

**Unconfirmed.** Neither the Excel nor the PowerPoint skills page mentions Copilot Credits. Cowork
is billed in credits, but that is a different surface and does not transfer.

## Can IT deploy skills to everyone?

For PowerPoint, yes, and it is documented: the admin centre takes a zip with a manifest and icons
under **Agents > All agents > Add agent**
([Deploy organization skills](https://support.microsoft.com/en-us/powerpoint/copilot/deploy-organization-skills-for-copilot-in-powerpoint)).
Whether the same package reaches Copilot in **Excel** is **Unconfirmed**: no Microsoft page
documents an Excel organisation path.

## Do these work in Claude, ChatGPT, Gemini CLI or Mistral Vibe?

The format does. Agent Skills is an open standard, donated by Anthropic to the Agentic AI Foundation
under the Linux Foundation on 22 October 2026, and Anthropic says more than 70 agent platforms had
adopted it. **Live behaviour of these 24 skills outside the Microsoft 365 apps is not tested.** See
[STATUS.md](STATUS.md) and [runtimes/](runtimes/).

## What is the difference between all these kinds of skill?

Same `SKILL.md` format, four different surfaces, four different install paths:

| Kind | Where it lives | Repository |
|---|---|---|
| App skills | OneDrive Skills folder, read by Copilot in Excel and PowerPoint | this one |
| Cowork skills | A Cowork skills folder in OneDrive | [awesome-copilot-cowork-skills](https://github.com/kesslernity/awesome-copilot-cowork-skills) |
| Declarative agent skills | Attached to an agent built in Agent Builder | [awesome-copilot-agent-skills](https://github.com/kesslernity/awesome-copilot-agent-skills) |
| Copilot Chat skills | Chat, governed by admin controls | see the runtimes page |

## Do these change my file without asking?

No. Every skill stops at a human approval checkpoint, states exactly what it would change, and
waits. The reporting skills never edit at all: `reconciliation-check` will not fix a break,
`assumptions-register` will not change an input, `numbers-and-claims-check` will not correct a
figure. That is the design, not a limitation.

## Can I use these commercially, or change them?

Yes, under CC BY-SA 4.0: attribute, and share adaptations under the same licence.
