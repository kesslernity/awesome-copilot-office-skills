# Copilot in Excel: organization skills

Sources, read 2026-10-24: Microsoft Support, [Deploy organization skills for Copilot in PowerPoint](https://support.microsoft.com/en-us/powerpoint/copilot/deploy-organization-skills-for-copilot-in-powerpoint) and [Use skills with Copilot in Excel](https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills).

## State of the documentation

🔴 **Microsoft documents the admin centre deployment path on the PowerPoint page. There is no equivalent Excel page as of 24 October 2026.** The package shape described there, a zip holding `manifest.json`, `color.png`, `outline.png` and one or more skill folders, is what `scripts/build-dist` produces, and the admin centre validates the package on upload.

Whether a package deployed that way reaches Copilot in Excel as well as Copilot in PowerPoint is **Unconfirmed**. Treat the Excel organisation path as untested until an admin has tried it in a real tenant.

## Build the packages

```
cp org-deploy/org-config.example.json org-deploy/org-config.json   # fill in your details
# add org-deploy/icons/color.png and org-deploy/icons/outline.png
python3 scripts/build-dist
```

This produces, under `dist/org/`:

- one package per skill, matching Microsoft's single-skill worked example, which is the shape most likely to validate;
- `excel-skills-pack.zip`, the twelve Excel skills in one package;
- `powerpoint-skills-pack.zip`, the twelve PowerPoint skills;
- `office-skills-pack.zip`, all twenty four.

`dist/org/` is git-ignored, because the packages carry your organisation's own developer URLs and icons.

## Deploy

1. In the Microsoft 365 admin center, go to **Agents > All agents**.
2. Select **More actions (...)**, then **Add agent**.
3. On **Upload agent to publish**, choose the zip. The admin centre validates the package and reports what it found.
4. Choose who can use the skill: everyone, or named users and groups.
5. Publish, then open the app with an account inside the deployment and confirm the skill appears in the skills list.

## Order of attempts

Start with a single-skill package. It matches Microsoft's documented example exactly, so a failure there is a real failure rather than an untested shape. Only then try a multi-skill pack, because **whether the admin centre accepts more than one entry in `agentSkills` is Unconfirmed**. The manifest schema allows a list; no Microsoft page shows one deployed.

## Unconfirmed

- Whether an organisation package deployed through this path appears in Copilot in Excel.
- Whether the admin centre accepts a package with more than one `agentSkills` entry.
- Whether the Copilot Chat skill block and review controls ([MC1493223](https://mc.merill.net/message/MC1493223)) also govern skills in the Microsoft 365 apps.
- Whether the English display language requirement applies to organisation skills in Excel as it does to personal ones.

Report what you find with the tenant behaviour issue template.
