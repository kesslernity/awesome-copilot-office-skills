# Status: tested in a tenant

Every skill here is **format-validated** by `scripts/validate`. That proves the file shape, not the
behaviour. This page records what has actually been run, by anyone, on a real tenant or runtime.

Nothing on this page is marked Works until somebody reports it. "Not tested" is the honest default
and it is not a defect.

**[Report a result](https://github.com/kesslernity/awesome-copilot-office-skills/issues/new?template=tenant-behaviour-report.md)** including things that worked. A confirmed Works is as useful as a bug.

## Legend

| Mark | Meaning |
|---|---|
| Works | Ran as described, by a named reporter, on that surface |
| Partial | Ran but deviated; link the issue |
| Fails | Did not run or produced the wrong thing; link the issue |
| Not tested | Nobody has reported this combination |

## Matrix

| Skill | Surface | Excel web | Excel Win | Excel Mac | PPT web | PPT Win | PPT Mac | PPT iPad | Org package | Claude | ChatGPT | GH Copilot | Gemini CLI | Mistral Vibe |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| [assumptions-register](skills/assumptions-register/) | excel | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [chart-intent-check](skills/chart-intent-check/) | excel | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [data-quality-sweep](skills/data-quality-sweep/) | excel | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [formula-risk-review](skills/formula-risk-review/) | excel | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [lookup-integrity-check](skills/lookup-integrity-check/) | excel | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [model-map](skills/model-map/) | excel | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [reconciliation-check](skills/reconciliation-check/) | excel | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [scenario-skeleton](skills/scenario-skeleton/) | excel | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [units-and-rounding-check](skills/units-and-rounding-check/) | excel | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [variance-explainer](skills/variance-explainer/) | excel | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [workbook-handover-note](skills/workbook-handover-note/) | excel | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [workbook-structure-audit](skills/workbook-structure-audit/) | excel | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [accessibility-pass](skills/accessibility-pass/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [action-title-rewrite](skills/action-title-rewrite/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [appendix-split](skills/appendix-split/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [brand-rules-check](skills/brand-rules-check/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [decision-slide](skills/decision-slide/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [deck-consistency-sweep](skills/deck-consistency-sweep/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [deck-trim-proposal](skills/deck-trim-proposal/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [native-diagram-slide](skills/native-diagram-slide/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [ai-writing-tells-check](skills/ai-writing-tells-check/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [deck-message-review](skills/deck-message-review/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [executive-summary-slide](skills/executive-summary-slide/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [numbers-and-claims-check](skills/numbers-and-claims-check/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [outline-first-deck](skills/outline-first-deck/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [speaker-notes-builder](skills/speaker-notes-builder/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |
| [steering-committee-status-deck](skills/steering-committee-status-deck/) | powerpoint | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested | Not tested |

## Open questions to test

These are the repository's Unconfirmed items, gathered in one place. Each is a thing Microsoft does
not document, left unresolved rather than answered by inference. Closing any one of them improves
the install instructions for everybody.

1. **Do Excel and PowerPoint read the same OneDrive Skills folder, or two separate ones?** Every
   install instruction depends on the answer. Highest value.
2. The exact OneDrive Skills folder path. A community guide reports one; Microsoft documents none.
3. The maximum number of custom skills per user, in either app. Cowork documents 50 for its own
   surface.
4. Do custom skills work on an account licensed M365 Copilot (Basic), or Premium only?
5. Does running a skill consume Copilot Credits? Neither skills page mentions them.
6. Does an organisation package deployed from the admin centre reach Copilot in **Excel**?
   Microsoft documents that path on the PowerPoint page only.
7. Will the admin centre accept a package with more than one `agentSkills` entry?
8. Do the Copilot Chat skill block and review controls ([MC1493223](https://mc.merill.net/message/MC1493223))
   govern skills in the Microsoft 365 apps?
9. Does Excel's English display language requirement apply to organisation skills as well as
   personal ones?
10. Does PowerPoint read files in `references/`? Only `brand-rules-check` uses one, and it has a
    paste route precisely because this is unknown.
11. Are optional front matter fields such as `license` or `metadata` tolerated, or do they break
    discovery?
12. Which zip shape does PowerPoint's Add skill accept: `dist/personal` (folder at the top) or
    `dist/root` (SKILL.md at the root)? The repository ships both rather than guessing.

Live behaviour in Claude, ChatGPT, GitHub Copilot, Gemini CLI and Mistral Vibe is untested for all
24 skills. The format is portable by specification; that is not the same as verified.
