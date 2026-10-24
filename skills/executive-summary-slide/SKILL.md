---
name: executive-summary-slide
description: "Reads the whole open presentation and drafts one executive summary slide of three to five points, each traced to the slide it comes from, then inserts it after the title slide once the user approves. Use when the user asks for an executive summary, leadership overview, one-slide recap or TL;DR slide of a deck."
---

# Executive summary slide

## Purpose

Give a senior reader the whole deck on one slide. The summary states conclusions, not topics, and every point is traceable to the slide it came from, so the presenter can defend it. The slide follows the existing design of the deck and is added only after the user has approved the wording.

## When to use

- The user asks for an executive summary, management summary, leadership overview, one-slide recap, key takeaways or TL;DR slide.
- The user is about to send a deck to someone who will not sit through the presentation.
- Do not use to summarise a document that is not a presentation; summarise it in the conversation instead.

## Inputs

1. The open presentation (required). If no presentation is open or attached, ask for it.
2. Audience (optional): for example board, steering committee, client sponsor. Default: a senior reader with no time and no context.
3. Point count (optional): three to five. Default: the smallest number that covers the deck's conclusions.
4. Placement (optional): default is directly after the title slide.

## Procedure

1. Read every slide, including speaker notes. Note each slide's main message in one line.
2. Separate conclusions (what is true, what we recommend, what we need) from context (background, method, agenda).
3. Draft three to five summary points. Each point is one sentence, 20 words or fewer, written as a conclusion. Prefer this order: the situation in one line, the key findings, the recommendation, the ask or decision needed.
4. Keep numbers exactly as they appear on the source slides. Do not round, convert or combine figures unless the deck already does so.
5. Map each point to its source slide numbers.
6. If the deck contains no recommendation or ask, do not invent one; add a final point "Decision or ask: not stated in the deck" and list it as an open question.
7. Draft a slide title that states the overall message as a sentence, not the word "Summary".
8. Stop for approval (see the checkpoint).
9. After approval, insert one new slide at the agreed position. Use an existing title-and-content layout from the deck so fonts, colours and placeholders match. Do not change any other slide.
10. Put the source slide numbers for each point in the speaker notes of the new slide.

## Human approval checkpoint

Show the proposed title, the points and their source slides as a table, plus any open questions. Ask: "Shall I add this as slide 2, or would you like changes first?" Insert only after explicit approval.

## Output

In the conversation:

| # | Summary point | Source slides |
|---|---|---|

Plus: proposed slide title, open questions.

In the presentation (after approval): one new slide with the title and points, source mapping in the speaker notes. If you cannot edit slides directly, return the slide as a Markdown block (title, bullets, speaker notes) for the user to paste.

## Fallbacks and edge cases

- Deck shorter than four slides: say a summary slide may not add value and ask whether to proceed.
- Deck with contradictory figures across slides: show both, cite both slides, and ask which is correct before drafting that point.
- Deck already has a summary slide: compare it with your draft and offer to update it instead of adding a second one.
- Deck in another language: write the summary in the deck's language unless the user asks otherwise.

## Rules

- Every point must trace to at least one slide. Nothing comes from outside the deck unless the user supplies it.
- Never invent a recommendation, decision, number or date.
- Never edit or delete existing slides.
- Keep the deck's existing theme; add no new fonts or colours.

## Self-check

- [ ] Three to five points, each 20 words or fewer.
- [ ] Every point has a source slide number.
- [ ] Numbers match the source slides exactly.
- [ ] The title is a sentence that states the message.
- [ ] Nothing was inserted before approval.
