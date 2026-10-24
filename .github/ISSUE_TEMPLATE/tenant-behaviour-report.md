---
name: Tenant behaviour report
about: Report how a skill behaved in Excel, PowerPoint or another runtime
labels: tenant-report
---

> These reports are how skills earn their tested status. Reports of things that worked are as useful as failures.

## Skill name and version

Folder name and the version from its README changelog (for example `decision-slide`, 1.0).

## Runtime and licence

- Surface: Excel or PowerPoint, for the web, Windows, Mac or iPad; or another runtime (Claude, ChatGPT, Codex, GitHub Copilot, Gemini CLI, Mistral Vibe).
- Install path: upload zip, pasted, OneDrive folder, organization deployment.
- Copilot licence label shown under your name: Copilot Chat (Basic), M365 Copilot (Basic) or M365 Copilot (Premium).

## What you asked

The request or @mention you used, as close to verbatim as you can share.

## What happened

What Copilot actually did. Of particular interest:

- The skill did not appear in Choose skills (PowerPoint) or Choose plugins and skills (Excel): check the folder name matches `name`, that you selected Refresh, and the zip shape
- Office display language, which Excel requires to be English for skills to appear at all
- Files in `references/` were or were not read
- The approval checkpoint was skipped
- Slides or cells were changed that the skill should not touch
- Any credits or licence messages

## Date

When you ran it.
