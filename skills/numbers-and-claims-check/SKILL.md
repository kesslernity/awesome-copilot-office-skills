---
name: numbers-and-claims-check
description: "Audits the open presentation for every number, date, percentage, quote and factual claim, records where each appears and whether a source is given, and lists unsourced or inconsistent items for the presenter to resolve. Never changes a figure. Use when the user asks to fact-check, verify numbers, check sources or audit claims in a deck before it is presented or sent."
---

# Numbers and claims check

## Purpose

Find every figure and factual claim in a deck before an audience does. The skill builds a register of what the deck asserts, where, and on what source, and flags anything unsourced, inconsistent or arithmetically wrong. It never corrects a number itself: the presenter owns the facts, the skill only makes the gaps visible.

## When to use

- The user asks to fact-check, verify, audit or sanity-check numbers, claims or sources in a presentation.
- A deck is about to go to a board, client, regulator or the press.
- Do not use to research the correct values; this skill reports, the user resolves.

## Inputs

1. The open presentation (required).
2. Source documents (optional): reports, spreadsheets or links the figures should come from. If supplied, compare against them.
3. Scope (optional): all slides (default), or a range.

## Procedure

1. Read every slide, including tables, chart labels, footnotes and speaker notes.
2. Extract each item into the register:
   - Numbers: amounts, counts, percentages, ratios, rankings.
   - Dates and time periods.
   - Direct quotes and attributed statements.
   - Factual claims: comparisons ("largest", "first", "fastest growing"), causal claims ("led to", "because of"), and market or benchmark statements.
3. For each item, record the slide number, the exact text, and the source as stated on the slide or in its notes (or NONE).
4. Check consistency: the same metric reported with different values on different slides, totals that do not equal their parts, percentages that do not match their numerators and denominators, and periods that do not line up (for example Q3 on one slide, Q2 on another for the same figure).
5. If source documents were supplied, compare each item against them and record MATCH, MISMATCH (with both values) or NOT FOUND IN SOURCE.
6. Assign a status to every item: SOURCED, UNSOURCED, INCONSISTENT, ARITHMETIC CHECK FAILED, MISMATCH WITH SOURCE, or SUPERLATIVE NEEDS EVIDENCE.
7. Summarise counts by status and list the items that most need attention first: anything on the title, summary or decision slides, then mismatches, then unsourced items.
8. Stop for the checkpoint before touching the deck.

## Human approval checkpoint

Present the register and summary. Ask: "Would you like me to add a speaker note on each flagged slide listing its open items? I will not change any figure on the slides." Add notes only if the user agrees, and only notes.

## Output

Summary line: "N items checked: X sourced, Y unsourced, Z inconsistent, ..."

Register:

| # | Slide | Item (exact text) | Type | Source stated | Status | Note |
|---|---|---|---|---|---|---|

Priority list: up to ten items to resolve first, with the question the presenter must answer for each.

Optional, after approval: a speaker note on each flagged slide beginning "OPEN CHECKS:" followed by its items.

## Fallbacks and edge cases

- Charts without data labels: record "value not readable from chart" rather than estimating.
- Rounded figures that differ only by rounding (for example 18% and 18.4%): mark as INCONSISTENT with the note "possible rounding", and let the user decide.
- Very large decks: process in slide order and say which slides are covered if you stop early.
- Figures in images: record that the slide contains a figure inside an image that could not be checked.

## Rules

- Never change, round, correct or remove a figure or claim on a slide.
- Never supply a "correct" value from memory or general knowledge; only compare against sources the user provided.
- Quote every item exactly as it appears.
- Treat speaker notes as part of the deck.

## Self-check

- [ ] Every slide in scope was read, including notes and footnotes.
- [ ] Every register row has a slide number, exact text and status.
- [ ] Every INCONSISTENT row cites both slides and both values.
- [ ] No figure on any slide was changed.
- [ ] Speaker notes were added only with approval.
