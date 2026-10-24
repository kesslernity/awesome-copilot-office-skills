---
name: steering-committee-status-deck
description: "Builds a short steering committee status deck (overall RAG status with reasons, milestones, risks and issues, budget if supplied, decisions and asks) from a status report, tracker export or notes, labels it DRAFT, and builds slides only after the user approves the status summary. Use when the user asks for a status update deck, steering committee pack, project board slides or monthly programme update."
---

# Steering committee status deck

## Purpose

Turn the material a project manager already has into a consistent five to seven slide status pack for a steering committee or project board. The status colours are proposed with their reasons, never decided by the skill. Everything is labelled DRAFT and traced to the source it came from.

## When to use

- The user asks for a status deck, steering committee pack, project board update, programme update or monthly report slides.
- Do not use for a one-off project kick-off deck or a business case; use outline-first-deck instead.

## Inputs

Ask for what is missing in one message.

1. Project or programme name and reporting period.
2. Source material: a status report, tracker or plan export, RAID log, previous status deck, or pasted notes.
3. RAG definitions the organisation uses. If none are given, use: GREEN on track; AMBER at risk but recoverable within tolerance; RED outside tolerance or needs steering committee action. State that these defaults were used.
4. Decisions or asks for the committee, if the user already knows them.
5. Template or previous deck to match, if any.

## Procedure

1. Read every source. List them back with their dates; flag any source older than the reporting period.
2. Extract into a working summary:
   - Milestones: name, baseline date, forecast date, status, from the sources only.
   - Risks and issues: top five by the source's own rating, with owner and next action.
   - Budget: planned, actual and forecast, only if the sources include them.
   - Achievements this period and plans for next period.
   - Decisions and asks for the committee.
3. Propose a RAG status for overall, schedule, scope, budget and resources. For each, give a one-line reason citing the evidence (for example "Milestone 3 forecast slipped 3 weeks past baseline"). If evidence is missing, propose GREY (not assessed) rather than guessing.
4. Compare with the previous period if a previous deck or report was supplied, and note changes in status.
5. Stop for approval of the working summary and the proposed RAG statuses.
6. After approval, build the deck in this order: title (with DRAFT and the reporting period); overall status and RAG summary with reasons; milestones; risks and issues; budget (only if data was supplied); decisions and asks; next period. Use existing layouts from the open deck or template. Put source references in the speaker notes of each slide.

## Human approval checkpoint

Present the working summary and the RAG proposals as tables, plus open questions. Ask: "Do you agree with these statuses and content? Change any colour or line, then tell me to build." The user, not the skill, sets the final RAG colours.

## Output

Stage 1 (in the conversation):

- RAG proposal: | Dimension | Proposed status | Reason and evidence |
- Milestones: | Milestone | Baseline | Forecast | Status | Source |
- Risks and issues: | Item | Rating (as in source) | Owner | Next action |
- Decisions and asks: numbered list.
- Open questions.

Stage 2 (after approval): five to seven slides as described. If you cannot edit slides directly, return each slide as a Markdown block for the user to paste.

## Fallbacks and edge cases

- No baseline dates in the sources: show forecast only and note that slippage cannot be assessed.
- Conflicting dates between sources: show both and ask.
- No budget data: omit the budget slide and say so in the build report.
- More than five risks: show five on the slide by the source's rating and list the rest in the speaker notes.

## Rules

- AI prepares, people decide: RAG colours are proposals until the user confirms them.
- Never invent milestones, dates, owners, ratings or figures.
- Copy risk ratings exactly as the source states them; do not re-score.
- Keep every slide traceable to a source via speaker notes, and keep DRAFT on the title slide.

## Self-check

- [ ] Every RAG proposal has a reason that cites evidence, or is GREY.
- [ ] Every milestone, risk and figure has a source.
- [ ] The user approved the summary before slides were built.
- [ ] The title slide shows DRAFT and the reporting period.
