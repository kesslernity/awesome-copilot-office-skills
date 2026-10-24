# Mistral Vibe

Vibe CLI reads skill folders from `.agents/skills/` in a project or `~/.vibe/skills/`. The Vibe web interface takes the same folder under **Context > Skills > Import** (upload a skill file or folder) or **New skill** (paste the body). Vibe CLI discovery does not recurse, which is one reason this repository keeps `skills/` flat.

Source: the sibling repository [awesome-mistral-vibe-skills](https://github.com/kesslernity/awesome-mistral-vibe-skills), which cites Mistral's documentation and ships its own checker.

Vibe cannot edit an open PowerPoint deck; the skills return slide content as Markdown. **Unconfirmed:** live behaviour of these eight skills in Vibe.
