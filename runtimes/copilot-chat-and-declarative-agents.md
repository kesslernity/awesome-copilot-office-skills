# Microsoft 365 Copilot Chat, Cowork and declarative agents

These surfaces use the same folder-plus-`SKILL.md` shape but are separate from the PowerPoint skill picker.

## Copilot Chat and Cowork

Skills in Copilot Chat roll out from October 2026 to mid-November 2026: users create, upload, edit and share skills; admins deploy, install or block skills and plugins and review user-created skills under **Agents > Tools**. Skills created in Copilot Chat can also be used in Cowork. Source: [MC1493223](https://mc.merill.net/message/MC1493223), 9 Oct 2026.

Cowork custom skills live in OneDrive at `/Documents/Cowork/skills/<skill-name>/`. Cowork is billed in Copilot Credits on top of the Microsoft 365 Copilot licence. See the sibling repository [awesome-copilot-cowork-skills](https://github.com/kesslernity/awesome-copilot-cowork-skills) for details and sources.

In Chat or Cowork these skills cannot edit an open PowerPoint canvas the way Copilot in PowerPoint does; they fall back to returning slide content as Markdown, or to the file-creation capability of that surface. **Unconfirmed:** how each skill behaves there.

## Declarative agents (Agent Builder, Agents Toolkit)

Upload `dist/root/<skill>.zip` (SKILL.md at the zip root) under **Configure > Skills > Add** in Agent Builder, or add the folder with Agents Toolkit (`atk add skill --from <path>`, manifest version 1.9). Limits: 8 skills per agent, instructions under 20,000 characters, 350 files, directory depth 3, Agent Builder zip up to 50 MB. Agents with skills cannot also use embedded files yet, and tenants with Information Barriers are not supported.

Sources, read 2026-10-24: [Custom skills in declarative agents](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/declarative-agent-skills), [Agent Builder](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-add-skills), [Agents Toolkit](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/build-declarative-agents-add-custom-skills); [MC1476977](https://mc.merill.net/message/MC1476977) (general availability by end of September 2026, posted 22 Sep 2026; the Learn pages still say preview). The sibling repository [awesome-copilot-agent-skills](https://github.com/kesslernity/awesome-copilot-agent-skills) covers this surface in depth.
