---
name: deck-trim-proposal
description: "Proposes which slides to cut, merge or move to an appendix so a deck fits its slot and its argument, using repetition, slides carrying no message, and slides that do not support the stated conclusion as the criteria. Deletes nothing. Use when the user says a deck is too long, needs to fit a time slot, or asks what can be cut."
---

# Deck trim proposal

## Purpose

Decide what leaves the room with you. A deck that is too long is rarely too long by a little, and the slides that should go are usually not the ones the author is tired of. The skill proposes a cut list against stated criteria, keeps every proposal reversible, and deletes nothing.

## When to use

- The user says a deck is too long, must fit a slot, or asks what can be cut.
- A deck has grown through several reviews and now repeats itself.
- Do not use to shorten individual slides. This skill works at the slide level.

## Inputs

1. The open presentation (required).
2. Target (optional): a slide count, a time slot, or both. If neither is given, propose against the argument rather than a number.
3. The conclusion (optional): the one thing the deck must land. If the user does not give it, derive a candidate from the closing or summary slide and confirm it before proposing cuts.

## Procedure

1. Build the slide inventory: number, title, single message, and whether the slide carries data, argument, context or navigation.
2. Establish the conclusion, from the user or from the deck, and state it. Every later judgement depends on it, so it is confirmed before anything is proposed.
3. Map each slide to the conclusion: DIRECTLY SUPPORTS, PROVIDES CONTEXT, NAVIGATION, or DOES NOT SUPPORT.
4. Find repetition: slides making the same point, the same figure presented twice in different forms, and context repeated after it was established.
5. Find slides with no single message, and slides whose message is already stated in a neighbouring slide's title.
6. Propose an action per slide: KEEP, MERGE WITH <slide>, MOVE TO APPENDIX, or CUT. Every proposal carries a one line reason tied to the criteria above, never to taste.
7. Where the target is a slide count or a time, order the proposals so the target is met by taking them in order, and say exactly where the line falls.
8. Identify what the deck would lose: for each CUT, the single fact or argument that disappears with it, so the author can overrule.
9. Stop for the checkpoint. This skill never deletes.

## Human approval checkpoint

Present the proposal. Ask: "Would you like me to apply the approved actions? Slides marked for appendix will be moved to the end behind a divider, and slides marked cut will be moved there too rather than deleted, so nothing is lost." Apply only the actions the user names, one at a time.

## Output

Summary line: "N slides. Proposed: K keep, M merge, A appendix, C cut. Taking the proposals in order reaches <target> at slide <position>."

Proposal:

| Slide | Title | Message | Supports conclusion | Proposed action | Reason | What is lost |
|---|---|---|---|---|---|---|

Repetition map: each repeated point with every slide that makes it.

Order of cuts: the sequence to apply to reach the target, with the running count or time after each.

## Fallbacks and edge cases

- A slide that does not support the conclusion may still be required, for example a mandatory disclaimer. Propose KEEP with the reason "required regardless of argument" where the slide looks obligatory.
- Where the conclusion cannot be established, stop and ask. Proposing cuts against a guessed conclusion is worse than proposing none.
- Backup and appendix slides already at the end are reported but not re-proposed unless the user asks.
- Animated or build slides: treat the build as one slide and say so.
- Where the target cannot be reached without cutting slides that directly support the conclusion, say so plainly and stop at the last safe cut.

## Rules

- Never delete a slide. Cut means moved behind a divider at the end.
- Never propose a cut without naming what the deck loses.
- Never propose against taste, polish or density. The criteria are repetition, absence of a message, and failure to support the stated conclusion.
- The conclusion is confirmed with the user before any proposal is made.
- Apply approved actions one at a time, reporting the new slide count after each.

## Self-check

- [ ] The conclusion is stated and was confirmed before proposing.
- [ ] Every slide has a proposed action and a reason.
- [ ] Every CUT names what is lost.
- [ ] No slide was deleted; cut slides are behind a divider at the end.
- [ ] If a target was given, the output says where the line falls.
