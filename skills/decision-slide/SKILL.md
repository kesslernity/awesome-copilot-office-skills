---
name: decision-slide
description: "Builds one decision slide that sets out the question, the options, the criteria, a comparison, the recommended option with its risks, and the decision required from a named owner by a date, labelled DRAFT and built only after the user approves the content. Use when the user asks for a decision slide, options slide, recommendation slide or a slide asking a committee or sponsor to decide."
---

# Decision slide

## Purpose

Make the decision on a slide explicit: what is being decided, between which options, against which criteria, what is recommended and who decides by when. The skill prepares the case; the named owner decides. The slide stays labelled DRAFT and the decision cell stays blank until a person fills it in.

## When to use

- The user asks for a decision slide, options slide, options appraisal, recommendation slide or "ask" slide.
- A deck goes to a steering committee, board or sponsor and needs a decision.
- Do not use to make the decision; the skill never records a decision as taken.

## Inputs

Ask for what is missing, in one message.

1. The decision question in one sentence.
2. The options: two to four, including "do nothing" or "defer" where relevant.
3. Criteria: what matters (for example cost, time, risk, benefit, fit). Ask the user to confirm or weight them.
4. Evidence for each option against each criterion: from the open deck, attached files, or the user.
5. Decision owner (role or name) and the date the decision is needed by.
6. The preferred option, if the user already has one.

## Procedure

1. Restate the decision question and confirm it with the user if it was inferred.
2. Build an options-by-criteria table. Fill each cell only from the evidence supplied; write UNKNOWN where there is none.
3. If the user has a preferred option, check it against the table and state any criterion where another option scores better. If there is no preferred option, propose one only if the evidence clearly supports it; otherwise write "Recommendation: to be agreed" and say why.
4. List the top three risks of the recommended option, each with a mitigation if the sources give one.
5. Write the decision request: "Decision required from [owner] by [date]: [question]". Leave the outcome blank.
6. Draft the slide title as the recommendation in one sentence, or as the question if there is no recommendation.
7. Stop for approval.
8. After approval, build one slide using an existing layout from the deck: title, compact comparison table, recommendation with risks, and the decision request in a visible box. Add DRAFT to the title or a corner label. Put the full evidence references in the speaker notes.

## Human approval checkpoint

Show the full slide content as text: title, table, recommendation, risks and decision request, plus every UNKNOWN cell. Ask: "Approve this content for the slide, or tell me what to change." Build only after approval. Never fill in the decision outcome, even if asked to "mark it approved"; say that the owner records the decision.

## Output

In the conversation: the slide content as Markdown:

- Title
- Options table: | Criterion | Option A | Option B | Option C |
- Recommendation and rationale (two lines)
- Risks and mitigations (up to three)
- Decision required from [owner] by [date]: [question]. Outcome: ________
- Open questions and UNKNOWN cells

In the presentation (after approval): one DRAFT slide as described, evidence in speaker notes. If you cannot edit slides directly, return the Markdown for the user to paste.

## Fallbacks and edge cases

- Only one option given: ask for at least one alternative, including "do nothing", before building.
- More than four options: suggest shortlisting and show the long list in the speaker notes.
- Criteria weights not given: present the table unweighted and say so.
- Evidence missing for most cells: build the slide only if the user accepts the UNKNOWN cells; otherwise list what is needed.

## Rules

- AI prepares, people decide: never record, imply or pre-fill a decision outcome.
- Never invent costs, dates, benefits or risks.
- Keep the slide labelled DRAFT.
- Do not change other slides.

## Self-check

- [ ] The decision question, owner and date are on the slide.
- [ ] Every table cell has evidence or UNKNOWN.
- [ ] The recommendation is supported by the table or marked "to be agreed".
- [ ] The outcome field is blank.
- [ ] The slide carries DRAFT.
