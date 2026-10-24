# Deploy these skills to your organisation

Copilot in PowerPoint supports **organization skills**: an admin uploads a package in the Microsoft 365 admin center and chooses who gets it. Users then see the skill under **+ > Choose skills** in PowerPoint for the web, Windows and Mac.

Sources, read 2026-10-24: Microsoft Support, [Deploy organization skills for Copilot in PowerPoint](https://support.microsoft.com/en-us/powerpoint/copilot/deploy-organization-skills-for-copilot-in-powerpoint); Message Center [MC1463509](https://mc.merill.net/message/MC1463509) (Frontier, 28 Aug 2026) and [MC1478961](https://mc.merill.net/message/MC1478961) (Windows general availability, rollout September 2026, posted 24 Sep 2026).

## What a package contains

```
<package>.zip
├── manifest.json        # Microsoft 365 app manifest, manifestVersion 1.30, with an agentSkills array
├── color.png            # colour icon
├── outline.png          # outline icon
└── skills/
    └── <skill-name>/
        ├── SKILL.md
        └── references/  # optional, text files only
```

The part of `manifest.json` that makes it a skill package:

```json
"agentSkills": [
  { "folder": "./skills/executive-summary-slide" }
]
```

`id` must be a unique GUID. Each `folder` path must match a folder in the zip. The template is [manifest.template.json](manifest.template.json).

## Build the packages

1. Copy `org-config.example.json` to `org-config.json` and fill in your organisation's name and https URLs (website, privacy, terms). This file is in `.gitignore`.
2. Add `icons/color.png` and `icons/outline.png` (see [icons/ICONS.md](icons/ICONS.md)). Also ignored by git.
3. Run `python3 scripts/build-dist` from the repository root.

You get one package per skill in `dist/org/<skill>.zip`, matching Microsoft's single-skill example, plus `dist/org/office-skills-pack.zip` with all eight. Each package gets a stable GUID derived from your website URL and the skill name, so rebuilding does not create a new app.

**Unconfirmed:** Microsoft's example lists one skill. Whether the admin center accepts several skills in one `agentSkills` array is not documented. Test the pack in a test group before relying on it; the per-skill packages are the safe path.

## Upload and deploy

1. Sign in to the Microsoft 365 admin center.
2. Go to **Agents > All agents**, open the **More actions (...)** menu, then select **Add agent**.
3. On **Upload agent to publish**, select **Choose file** and upload the package zip.
4. Review the validation results. If validation fails, fix the package or manifest and upload again.
5. Choose who can use the skill: all users, or specific users and groups. Complete the publishing flow.
6. Check the deployment under **Agents > Tools**: details, users, version and status.
7. As a user included in the deployment, open PowerPoint, open Copilot, select **+ > Choose skills** and find the skill.

Start with a small pilot group. AI prepares, people decide: these skills draft and stop for approval, but your own review of each skill's text before deployment is still the control that matters.

## Governance notes

- Personal skills (uploaded by users to their own OneDrive Skills folder) need no admin action and are visible only to that user (Message Center MC1434580).
- For Copilot Chat, admins can deploy, install or block skills and review user-created skills under **Agents > Tools** (Message Center [MC1493223](https://mc.merill.net/message/MC1493223), 9 Oct 2026). **Unconfirmed:** whether the same block and review controls cover personal PowerPoint skills.
- The Microsoft Support page also mentions the Agent 365 CLI as another way to prepare and publish packages.
