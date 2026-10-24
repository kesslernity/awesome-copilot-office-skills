---
name: speaker-notes-builder
description: "Drafts speaker notes for each slide in the open presentation from what the slide actually shows, marks where a note would need a fact the slide does not contain, and flags any existing note that contradicts its slide. Adds nothing to the slides themselves. Use when the user asks for speaker notes, talk track, or help preparing to present a deck."
---

# Speaker notes builder

## Purpose

Write the words that go with the slide, not a second version of the slide. Good notes say what the presenter adds out loud: the transition, the point the visual is making, and the one sentence that lands it. The skill drafts those from the slide content, and refuses to supply facts the deck does not contain.

## When to use

- The user asks for speaker notes, a talk track, or help rehearsing a deck.
- A deck built by one person will be presented by another.
- Do not use to write the slides. This skill works on the notes layer only.

## Inputs

1. The open presentation (required).
2. Audience and time (optional): who is in the room and how long the slot is. If given, size the notes to the time available.
3. Tone (optional): the register to write in. Default is plain spoken English, short sentences.
4. Existing notes (optional behaviour): if notes already exist, review rather than replace.

## Procedure

1. Read every slide: title, body, tables, chart labels, and any existing notes.
2. Derive the single message of each slide from its title and content. Where a slide has no discernible single message, record that rather than inventing one.
3. For each slide draft a note with three parts: a one line transition from the previous slide, two to four sentences delivering the message, and a closing line that sets up the next slide.
4. Mark any sentence that would require a fact not present in the deck with a gap marker and the question it raises. Never fill it from memory.
5. Where existing notes are present, compare them to the slide. Report any note that states a figure, date or claim that the slide contradicts, quoting both.
6. Size to time if a slot was given: estimate at roughly one hundred and thirty spoken words per minute, report the total, and say which slides would need cutting to fit.
7. Flag slides that cannot be presented in under ninety seconds because they carry too many messages, and say which message appears to be primary.
8. Stop for the checkpoint before writing any note into the deck.

## Human approval checkpoint

Present the drafted notes as a table, with gaps and contradictions listed separately. Ask: "Would you like me to write these into the speaker notes? I will not change any slide, and existing notes will be preserved below a divider rather than replaced." Write only on approval.

## Output

Summary line: "N slides: notes drafted for M, G gaps needing a fact the deck does not contain, C contradictions with existing notes. Estimated speaking time: T minutes."

Notes:

| Slide | Message | Drafted note | Gaps | Estimated seconds |
|---|---|---|---|---|

Contradictions, where existing notes disagree with their slide:

| Slide | Slide says | Existing note says |
|---|---|---|

Timing: total estimate, and the slides to cut or shorten if a slot was given.

## Fallbacks and edge cases

- A slide that is purely a section divider gets a one line transition only, not a full note.
- A slide whose message cannot be established is reported with the note "no single message identified" and a question for the author, rather than a drafted note.
- Dense appendix slides: draft a note saying the slide is reference material and is not walked through, unless the user says otherwise.
- Where the deck's language is not English, draft in the deck's language and say which was used.
- Where existing notes are extensive, review and report rather than drafting over them.

## Rules

- Never add, change or remove anything on a slide. Notes only.
- Never supply a fact, figure, name or date that is not on the slide or supplied by the user.
- Never replace an existing note without preserving it below a divider.
- Do not restate the slide text as the note. A note that reads the slide aloud is a failed note, and is reported as such rather than delivered.
- Mark every gap visibly, so an unprepared presenter sees it before the room does.

## Self-check

- [ ] Every slide in the deck has a row, including dividers and appendix slides.
- [ ] Every gap is marked with the question it raises.
- [ ] No drafted note contains a fact absent from the deck.
- [ ] No slide was modified.
- [ ] Existing notes were preserved, not overwritten.
