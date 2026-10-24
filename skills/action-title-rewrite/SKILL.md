---
name: action-title-rewrite
description: "Reviews every slide title in the open presentation and proposes action titles that state each slide's message as a full sentence, flags slides with no clear point, and shows a before and after table for approval before changing anything. Use when the user asks to fix, sharpen or improve slide titles, make a deck tell a story, or apply a one message per slide rule."
---

# Action title rewrite

## Purpose

Make the deck readable from its titles alone. An action title states the slide's conclusion ("Support costs fell 18% after the portal launch") instead of its topic ("Support costs"). Reading the titles in order should tell the whole story. This skill proposes new titles, flags slides that have no single message, and changes nothing until the user approves.

## When to use

- The user asks to improve, sharpen, fix or rewrite slide titles.
- The user asks to make the deck tell a story, or to apply "one message per slide".
- The user asks for a storyline or titles-only read of the deck.
- Do not use for body text rewrites; this skill touches titles only.

## Inputs

1. The open presentation (required).
2. Scope (optional): all slides, a range, or a section. Default: all content slides; skip title, agenda, section divider and appendix slides unless asked.
3. Style constraints (optional): maximum title length, sentence case or title case, house terms. Defaults: a full sentence, 15 words or fewer, sentence case, no full stop at the end.

## Procedure

1. Read each in-scope slide's title, body and speaker notes.
2. Decide the slide's single main message from its content. Use only what is on the slide or in its notes.
3. Classify the current title:
   - KEEP: already states the message.
   - REWRITE: states a topic, or states a message the content does not support.
   - SPLIT: the slide carries two or more separate messages; recommend splitting rather than writing a title that hides one.
   - NO MESSAGE: the slide has no clear point (for example a list with no conclusion); ask the user what the slide should say.
4. For each REWRITE, draft an action title: a full sentence, the conclusion first, any number copied exactly from the slide.
5. Read the proposed titles in order as a storyline. Flag gaps (a jump in the argument) and repeats (two slides with the same message).
6. Stop for approval (see the checkpoint).
7. After approval, change only the titles the user approved. Do not alter fonts, sizes, positions or body text. If a new title is longer than the placeholder allows, tell the user rather than shrinking the font.

## Human approval checkpoint

Present the before and after table and the storyline check. Ask: "Which rewrites should I apply? Reply 'all', list slide numbers, or edit any title first." Apply exactly what is approved.

## Output

| Slide | Current title | Verdict | Proposed title | Reason |
|---|---|---|---|---|

Then:

- Storyline: the proposed titles in order, one per line.
- Gaps and repeats: numbered list, or "none found".
- After applying: a list of slides changed. If you cannot edit slides directly, return the table only; the user applies the titles.

## Fallbacks and edge cases

- The slide content contradicts the current title: mark REWRITE and say so in the Reason column.
- A number in the title differs from the number in the body: do not choose; flag it and ask.
- Charts without data labels: describe only what the chart visibly shows; do not estimate values.
- House style requires topic titles: offer to put the action message in the subtitle instead.

## Rules

- Titles state only what the slide supports. Never add a claim, number or comparison that is not on the slide.
- Never change body text, layout or formatting.
- Never apply a title the user has not approved.
- Keep the deck's language and spelling variant.

## Self-check

- [ ] Every in-scope slide has a verdict.
- [ ] Every proposed title is a sentence of 15 words or fewer, or the user's limit.
- [ ] Every number in a proposed title appears on that slide.
- [ ] The storyline check lists gaps and repeats or says none were found.
- [ ] Only approved titles were changed.
