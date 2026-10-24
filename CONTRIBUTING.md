# Contributing

Thanks for considering a contribution. Start from [templates/SKILL.template.md](templates/SKILL.template.md) and [templates/README.template.md](templates/README.template.md): they carry the nine required headings in order and the rules below as guidance under each. This repository collects custom skills for Copilot in Excel and Copilot in PowerPoint, written in the open Agent Skills format so the same file runs in other tools. The bar is deliberately high: one skill that survives a real tenant is worth more than ten that look plausible.

Read this whole file before opening a pull request.

## The quality bar

1. **A repeatable Excel or PowerPoint task with a visible finish line.** "Create one executive summary slide" qualifies, and so does "reconcile every stated total in a pack against its components". "Make my deck better" and "tidy this model" do not. If you cannot say what the finished deck or workbook looks like, it is not ready to be a skill.
2. **Complement the built-ins, and overlap one only on purpose.** Copilot in Excel ships `@clean-data`, `@chart-design`, `@theme-design`, `@brandkit`, `@skill-builder` and built-in finance skills such as `check-model`; Copilot in PowerPoint ships Review this presentation, Prepare for Questions and Agent mode rewriting, translation and speaker notes. A skill here may cover the same ground, but only if its README names the built-in and states the concrete difference, as `formula-risk-review` and `speaker-notes-builder` do.
3. **A human approval checkpoint.** The skill shows what it would change and waits for explicit approval before it edits, inserts or deletes anything. AI prepares, people decide.
4. **Header is exactly `name` and `description`.** `name` is kebab-case, 1 to 64 characters, identical to the folder name. `description` is a single-line double-quoted string saying what the skill does and when to use it (40 to 1024 characters; aim for under 500).
5. **Host-neutral instructions.** Refer to "the open presentation" or "the open workbook", never to one product's buttons, and never name a vendor inside a SKILL.md: `scripts/validate` rejects it, because these files also run in Claude, ChatGPT, Gemini CLI and Mistral Vibe. Include the fallback for both: if the tool cannot edit the open file, return the output as Markdown to paste.
6. **No scripts, no images, no PDFs.** Instructions plus text references only. Skill uploads do not support PNG, PDF or nested zips. Excel's documentation does permit `scripts`, `references` and `assets` subfolders, and this repository ships no scripts by choice, so one folder stays safe to drop into either app and into every other runtime.
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
python3 -m venv .venv && . .venv/bin/activate   # a venv, because a system pip install fails under PEP 668 on current macOS and Linux
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
