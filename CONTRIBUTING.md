# Contributing

Thanks for considering a contribution. This repository collects custom skills for Copilot in Excel and Copilot in PowerPoint, written in the open Agent Skills format so the same file runs in other tools. The bar is deliberately high: one skill that survives a real tenant is worth more than ten that look plausible.

Read this whole file before opening a pull request.

## The quality bar

1. **A repeatable presentation task with a visible finish line.** "Create one executive summary slide" qualifies; "make my deck better" does not. If the value fits in one chat message, it is a prompt and belongs in [awesome-microsoft-copilot-prompts](https://github.com/kesslernity/awesome-microsoft-copilot-prompts).
2. **Complement the built-ins, never duplicate them.** Copilot in Excel already ships @clean-data, @chart-design and @theme-design, and Copilot in PowerPoint ships Review this presentation, Visualize this slide, Prepare for Questions, Create interactive slide, and chat-based rewrite, translate and speaker notes. Say in your README which built-in your skill complements.
3. **A human approval checkpoint.** The skill shows what it would change and waits for explicit approval before it edits, inserts or deletes anything. AI prepares, people decide.
4. **Header is exactly `name` and `description`.** `name` is kebab-case, 1 to 64 characters, identical to the folder name. `description` is a single-line double-quoted string saying what the skill does and when to use it (40 to 1024 characters; aim for under 500).
5. **Host-neutral instructions.** Refer to "the open presentation", not to one product's buttons. Include the fallback: if the tool cannot edit slides, return slide content as Markdown.
6. **No scripts, no images, no PDFs.** Instructions plus text references only. Skill uploads do not support PNG, PDF or nested zips, and Microsoft does not document script execution in PowerPoint.
7. **Never invent facts.** Skills mark missing information UNKNOWN or ASSUMPTION and never fill gaps from general knowledge.
8. **British spelling, no em or en dashes, no hype words, no exclamation marks.** Microsoft product names keep their official spelling.
9. **Truthful status.** Your skill README says whether it has run in a real tenant, on which surface and date, or that it is format-validated only.

## Folder layout

```
skills/<skill-name>/
├── SKILL.md        # header + instructions (shipped)
├── README.md       # for humans on GitHub (never shipped)
└── references/     # optional, .md, .txt, .csv or .json only (shipped)
```

`skills/` is flat: no category subfolders. Both apps expect one folder per skill, and some loaders do not recurse.

## SKILL.md sections

All nine, in this order:

1. `## Purpose`
2. `## When to use`
3. `## Inputs`
4. `## Procedure` (numbered)
5. `## Human approval checkpoint`
6. `## Output` (exact format, plus the Markdown fallback)
7. `## Fallbacks and edge cases`
8. `## Rules`
9. `## Self-check` (checkbox list)

Instructions stay under 20,000 characters. No URLs and no brand names inside `SKILL.md`.

## README.md sections

H1 title, one-line blockquote, What it produces, Install in 60 seconds, Example triggers, Complements, does not duplicate, Status, Changelog.

## Before you open the pull request

```bash
pip install pyyaml
python3 scripts/validate
python3 scripts/build-dist
```

Add your skill to `scripts/catalog.json` and to the catalog table in `README.md`; `validate` fails if either is missing. Add a line to `CHANGELOG.md`.

## Sibling repositories

- Cowork skills: [awesome-copilot-cowork-skills](https://github.com/kesslernity/awesome-copilot-cowork-skills)
- Declarative-agent skills: [awesome-copilot-agent-skills](https://github.com/kesslernity/awesome-copilot-agent-skills)
- Mistral Vibe skills: [awesome-mistral-vibe-skills](https://github.com/kesslernity/awesome-mistral-vibe-skills)

A redirect to another repository is a routing decision, not a quality judgement.
