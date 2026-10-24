# Changelog

All notable changes to this repository. Dates are ISO 8601.

## 2.0.0 | 2026-10-24

- Repository covers two surfaces: Copilot in Excel and Copilot in PowerPoint. Renamed to awesome-copilot-office-skills.
- Twelve Excel skills added: workbook-structure-audit, formula-risk-review, lookup-integrity-check, data-quality-sweep, reconciliation-check, units-and-rounding-check, assumptions-register, model-map, variance-explainer, chart-intent-check, scenario-skeleton, workbook-handover-note.
- Four PowerPoint skills added: speaker-notes-builder, deck-trim-proposal, deck-consistency-sweep, appendix-split. Twenty four skills in total.
- `scripts/catalog.json` gains a required `surface` field per skill, enforced by `scripts/validate`. A skill with no surface cannot be routed to the right install instructions.
- `scripts/build-dist` now produces three organisation packs: `excel-skills-pack.zip`, `powerpoint-skills-pack.zip` and `office-skills-pack.zip`, so an admin can deploy one app's set without the other.
- `runtimes/excel-personal.md` and `runtimes/excel-organization.md` added. The Excel organisation path is marked Unconfirmed: Microsoft documents admin deployment on the PowerPoint page only.
- Documented that Excel skills require the Office display language to be set to English, and that Excel permits `scripts`, `references` and `assets` subfolders which this repository deliberately does not use.

## 1.0.0 | 2026-10-24

- Initial release: eight skills (outline-first-deck, executive-summary-slide, action-title-rewrite, numbers-and-claims-check, brand-rules-check, decision-slide, accessibility-pass, steering-committee-status-deck).
- `scripts/validate` and `scripts/build-dist`: personal zips (skill folder at the top level), root zips (SKILL.md at the root, for Agent Builder), and optional organization packages (manifest 1.30 with `agentSkills`).
- `org-deploy/` manifest template and admin guide; `runtimes/` pages for nine runtimes.
- Status: format-validated; live tenant tests pending.
