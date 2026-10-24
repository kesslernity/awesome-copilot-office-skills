# Runtimes: the same SKILL.md in other tools

Every skill in this repository is one folder with a `SKILL.md` in the open Agent Skills format ([agentskills.io/specification](https://agentskills.io/specification)). The format is now hosted by the Agentic AI Foundation under the Linux Foundation ([Anthropic, 22 Oct 2026](https://www.anthropic.com/news/donating-agent-skills-to-the-agentic-ai-foundation); [Linux Foundation, 22 Oct 2026](https://www.linuxfoundation.org/press/agentic-ai-foundation-announces-four-new-projects-agent-skills-open-responses-openenv-and-opensandbox)). Prompts are the asset, models are commodities: the file stays the same, the runtime changes.

| Page | Runtime | Edits the open file directly? |
|---|---|---|
| [excel-personal.md](excel-personal.md) | Copilot in Excel, personal skills | Yes |
| [excel-organization.md](excel-organization.md) | Copilot in Excel, organization skills | Unconfirmed |
| [powerpoint-personal.md](powerpoint-personal.md) | Copilot in PowerPoint, personal skills | Yes |
| [powerpoint-organization.md](powerpoint-organization.md) | Copilot in PowerPoint, organization skills | Yes |
| [copilot-chat-and-declarative-agents.md](copilot-chat-and-declarative-agents.md) | Microsoft 365 Copilot Chat, Cowork, declarative agents | Not in the app canvas |
| [claude.md](claude.md) | Claude (claude.ai and Claude Code) | Depends on the surface |
| [chatgpt-codex.md](chatgpt-codex.md) | ChatGPT and Codex | Depends on the surface |
| [github-copilot-vscode.md](github-copilot-vscode.md) | GitHub Copilot and VS Code | No |
| [gemini-cli.md](gemini-cli.md) | Gemini CLI | No |
| [mistral-vibe.md](mistral-vibe.md) | Mistral Vibe | Depends on the surface |

Where a runtime cannot edit the open file, every skill here falls back to returning its output as Markdown for the user to paste. That fallback is written into each SKILL.md.

Status: format portability is by specification. Live behaviour outside Excel and PowerPoint is **not yet tested** for these skills; report results with the tenant behaviour issue template.
