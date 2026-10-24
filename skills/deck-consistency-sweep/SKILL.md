---
name: deck-consistency-sweep
description: "Sweeps the open presentation for the inconsistencies a reader notices and an author stops seeing: a term used two ways, acronyms never expanded, mixed date and number formats, product names spelled differently, and headings that change grammatical shape. Proposes fixes and applies none without approval. Use when the user asks to proofread, tidy or make a deck consistent before it goes out."
---

# Deck consistency sweep

## Purpose

Catch the small inconsistencies that make a deck look assembled rather than written. Nobody notices a consistent deck; everybody notices the slide where the product has a different name. The skill sweeps for those conditions across the whole deck, where a slide by slide read will always miss them, and proposes a single convention for each.

## When to use

- The user asks to proofread, tidy, polish or make a deck consistent.
- A deck has been written by more than one person, or assembled from older decks.
- Do not use for brand compliance against a written rules file. That is a different check.

## Inputs

1. The open presentation (required).
2. House conventions (optional): preferred spellings, date format, number format or terminology. If supplied, these decide every case rather than majority usage.
3. Scope (optional): all slides including notes and appendix (default), or body slides only.

## Procedure

1. Build a term index across every slide, table, chart label and note.
2. Find terms used in more than one form: differing capitalisation, singular and plural used for the same concept, hyphenated and unhyphenated variants, and British and American spellings in the same deck.
3. Find product, team and organisation names rendered differently, listing each variant with its slides. These matter most, because a reader reads a misnamed product as carelessness about the content.
4. Find acronyms: every acronym used, whether it is expanded on first use, and the slide of first use. Report any never expanded.
5. Check date formats across the deck and report every distinct format with its slides. Report ambiguous dates as ambiguous rather than normalising them.
6. Check number presentation: thousands separators, decimal places on comparable figures, currency symbol placement, and percentages written two ways.
7. Check heading grammar: titles that mix sentence case and title case, and titles that mix noun phrases with full sentences. Report the majority shape as the candidate convention.
8. For each condition propose one convention, chosen from the supplied house conventions where given, otherwise from the majority usage in the deck, and say which rule decided it.
9. Count the edits each proposal implies, by slide.
10. Stop for the checkpoint.

## Human approval checkpoint

Present the proposals with their edit counts. Ask: "Which of these conventions would you like me to apply? I will apply only the ones you name, one condition at a time, and report the slides changed after each." Apply nothing that was not named.

## Output

Summary line: "N slides swept. C conditions found affecting S slides. A acronyms never expanded."

Proposals:

| # | Condition | Variants found, with counts | Proposed convention | Decided by | Slides affected |
|---|---|---|---|---|---|

Names: every product, team or organisation name with each variant and its slides, listed separately because these carry the most risk.

Acronyms:

| Acronym | First used on slide | Expanded | Occurrences |
|---|---|---|---|

Ambiguous dates: each date, both readings, and its slide.

## Fallbacks and edge cases

- A quoted source must keep its original spelling. Where a variant sits inside quotation marks, report it and mark it "quoted, do not normalise".
- Deliberate variants, such as a legal entity name differing from a trading name, are reported with the note "may be intentional".
- Mixed language decks: sweep within each language and say which slides are in which.
- Where no majority exists, say there is no majority, propose nothing, and ask the user to choose.
- Text inside images cannot be swept. Report which slides contain image text so the user knows the sweep is incomplete there.

## Rules

- Never apply a convention that was not explicitly approved.
- Never normalise a quotation, a legal name or text inside an image.
- Never resolve an ambiguous date. Report both readings.
- Say which rule decided each proposal, house convention or majority usage, so the user can disagree with the basis rather than the outcome.
- Apply one condition at a time and report the slides changed after each.

## Self-check

- [ ] The sweep covered notes and appendix, or the output says which scope was used.
- [ ] Every proposal states the variants, the convention and what decided it.
- [ ] Quoted text and image text are reported as out of scope.
- [ ] Only approved conditions were applied.
- [ ] Slides changed were reported after each applied condition.
