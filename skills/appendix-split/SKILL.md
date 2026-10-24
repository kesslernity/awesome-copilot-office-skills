---
name: appendix-split
description: "Separates the deck that gets presented from the detail that answers questions, by proposing which slides move to an appendix, leaving a pointer on the slide that needed them, and building a navigable appendix index. Moves nothing without approval. Use when the user says a deck is too dense, carries too much back-up detail, or needs a shorter main story. Not for deciding what to cut entirely; use deck-trim-proposal for that."
---

# Appendix split

## Purpose

Let the main deck make an argument and the appendix answer the questions. Most overlong decks are not carrying the wrong content, they are carrying all of it in one sequence. The skill proposes the split, keeps every moved slide reachable from the point it supported, and moves nothing until the user agrees.

## When to use

- The user says a deck is dense, detailed or too long for the audience.
- A deck must work both as a walkthrough and as a document read afterwards.
- Do not use to decide what to cut entirely. Cutting is a different decision; this skill relocates.

## Inputs

1. The open presentation (required).
2. The main line (optional): the argument the presented deck must carry. If not supplied, derive it from the title, summary and closing slides and confirm it before proposing.
3. Audience (optional): who sees the main deck, which affects how much detail stays.

## Procedure

1. Inventory every slide with its title, single message and content type: argument, evidence, method, data table, background or navigation.
2. Confirm the main line with the user before proposing anything.
3. Classify each slide: MAIN if it advances the argument, APPENDIX if it supports or evidences a main slide without advancing it, UNDECIDED if it does both.
4. For each APPENDIX candidate, identify the main slide it supports. A slide with no main slide to support is reported separately, because it may belong in neither.
5. Draft the pointer for each main slide that loses support, in the form of one line naming what moved and where it went. The pointer is what makes the split safe.
6. Build the appendix order: grouped by the main slide each item supports, in main deck order, so a reader can find things under pressure.
7. Draft the appendix index slide listing each group and its slides.
8. Report the resulting shape: main slide count, appendix slide count, and the estimated change in presented length.
9. Resolve UNDECIDED slides with the user rather than deciding alone.
10. Stop for the checkpoint.

## Human approval checkpoint

Present the proposed split, the pointers and the appendix order. Ask: "Would you like me to apply this split? Slides will be moved behind an appendix divider, in the order shown, with an index slide added and a pointer line added to each main slide that lost support. Nothing is deleted." Apply only on approval, and report the new structure.

## Output

Summary line: "N slides: M proposed main, A proposed appendix, U undecided. Main deck would fall from N to M slides."

Split:

| Slide | Title | Type | Proposed | Supports which main slide | Pointer to add |
|---|---|---|---|---|---|

Orphans: appendix candidates supporting no main slide, each with the question of whether it belongs in the deck at all.

Appendix order: the groups, in main deck order, with the slides under each.

Index slide: the drafted content of the appendix index.

## Fallbacks and edge cases

- A slide required for compliance or legal reasons stays in the main deck regardless of argument, and is marked "required in main".
- Where the main line cannot be established, stop and ask. A split proposed against a guessed argument moves the wrong slides.
- A data table referenced from two main slides gets one pointer on each, and sits once in the appendix.
- Animated builds move as one slide and the output says so.
- If the appendix would exceed the main deck by more than three to one, say so, because that usually means the deck is carrying material that belongs in a document rather than a presentation.

## Rules

- Never delete a slide. Appendix means moved behind a divider, never removed.
- Never move a slide without adding its pointer to the main slide it supported.
- Never resolve an UNDECIDED slide without the user.
- The main line is confirmed before any proposal is made.
- Preserve original slide order within each appendix group, so a returning reader finds what they remember.

## Self-check

- [ ] The main line is stated and was confirmed.
- [ ] Every proposed appendix slide names the main slide it supports, or is listed as an orphan.
- [ ] Every main slide losing support has a drafted pointer.
- [ ] No slide was deleted.
- [ ] The appendix index covers every moved slide.
