---
name: outline-first-deck
description: "Drafts a numbered slide outline from a brief or source document, waits for the user to approve or edit it, and only then builds the slides. Use when the user asks to create, draft or start a presentation or deck from notes, a brief, a document or a topic, and the content matters more than speed."
---

# Outline-first deck

## Purpose

Turn a brief or a source document into a presentation in two gated stages: first an outline the user can read in under a minute, then the slides. The outline is the cheapest place to fix the storyline, so nothing is built until a person has approved it. Every slide in the outline names the source it draws on, so the user can see where each point came from.

## When to use

- The user asks for a new deck, presentation or slides from a brief, notes, a document, a spreadsheet summary or a topic.
- The user asks to rebuild an existing deck around a new storyline.
- Do not use for a single slide (build it directly) or when the user explicitly says "skip the outline".

## Inputs

Gather these in one message where possible. Ask only for what is missing.

1. Purpose of the deck in one sentence: what should the audience know, decide or do afterwards.
2. Audience: who they are and what they already know.
3. Target length: number of slides or minutes. Default to 10 slides if the user does not say, and state that default.
4. Source material: the open presentation, attached or referenced files, or pasted text. If there is no source material, say that every point will be marked ASSUMPTION until the user supplies a source.
5. Constraints: template or theme to follow, mandatory slides (agenda, disclaimer, contact), language.

## Procedure

1. Read every source the user provided. List the sources back by name before drafting, so the user can spot a missing file.
2. Write a one-sentence storyline: the single message the deck must land.
3. Draft the outline as a numbered table, one row per slide, with these columns: slide number, slide type (title, agenda, section, content, data, decision, summary, appendix), working title written as a full-sentence message, two to four key points, and source (file name and section, or ASSUMPTION).
4. Check the outline against the target length. If the content needs more slides than the target, propose what moves to an appendix rather than silently exceeding it.
5. List open questions: facts the sources do not contain, numbers that need confirming, and any point marked ASSUMPTION.
6. Stop and present the outline (see the checkpoint below).
7. After approval, build the slides in outline order. Follow the existing theme or template if one is open; do not introduce new fonts or colours. Keep each slide to its approved points.
8. Put the word DRAFT in the subtitle of the title slide.
9. Add a speaker note to any slide whose content rests on an ASSUMPTION, naming the assumption.
10. After building, report what was created and anything that differs from the approved outline.

## Human approval checkpoint

Present the storyline sentence, the outline table and the open questions, then ask: "Approve this outline, or tell me what to change. I will not build slides until you approve." Apply edits to the outline and show it again if the changes are substantial. Proceed only on an explicit approval such as "approved", "go ahead" or "build it".

## Output

Stage 1 (in the conversation):

- Storyline: one sentence.
- Outline table: | # | Type | Working title | Key points | Source |
- Open questions: numbered list.

Stage 2 (after approval):

- The slides, built in the open presentation if you can edit it. If you cannot edit slides directly, return each slide as a Markdown block with title, bullet points and suggested layout, ready to paste.
- A short build report: slides created, deviations from the outline, assumptions flagged in speaker notes.

## Fallbacks and edge cases

- No source material: build the outline from the user's description, mark every content point ASSUMPTION, and say so at the top of the outline.
- Conflicting sources: show both values in the outline row and add an open question; do not choose one.
- The user approves only part of the outline: build only the approved slides and list the rest as pending.
- Very long source documents: summarise each source into its main points first, then outline from that summary, and say which sections you used.

## Rules

- Never build slides before explicit approval of the outline.
- Never invent figures, quotes, names or dates. Missing facts are marked UNKNOWN or ASSUMPTION.
- Never overwrite or delete existing slides without asking; add new slides instead.
- The deck stays labelled DRAFT until the user removes the label.

## Self-check

Before presenting the outline and again before the build report, confirm:

- [ ] Every outline row has a source or is marked ASSUMPTION.
- [ ] The slide count matches the target or the difference is explained.
- [ ] Open questions are listed, or the outline states there are none.
- [ ] No slide was built before approval.
- [ ] The title slide carries DRAFT.
