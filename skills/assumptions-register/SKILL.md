---
name: assumptions-register
description: "Finds every hardcoded input in the open workbook, separates genuine assumptions from calculated cells, and builds a register recording each one with its cell, value, unit, period and stated source, leaving the source blank where none is given. Never changes a value. Use when the user asks what a model assumes, where its inputs are, or to document or review assumptions before a review."
---

# Assumptions register

## Purpose

Make the inputs of a model visible as a list rather than scattered through its formulas. The skill separates what the workbook assumes from what it calculates, records every assumption with where it lives and where it came from, and leaves the source field blank when the workbook does not say. An assumption nobody can find is an assumption nobody can challenge.

## When to use

- The user asks what a model assumes, where the inputs are, or to build or review an assumptions list.
- A model is going into review, handover, audit or a decision meeting.
- Do not use to judge whether an assumption is reasonable. This skill records, the user judges.

## Inputs

1. The open workbook (required).
2. Scope (optional): all sheets (default), or named sheets.
3. An existing assumptions sheet (optional): if one exists, compare against it rather than starting from nothing.

## Procedure

1. Classify every populated cell as INPUT (a typed constant), CALCULATED (contains a formula), or LABEL.
2. From the INPUT cells, separate genuine assumptions from incidental constants. An assumption drives a result: it feeds at least one formula. A constant that nothing references is incidental, and is listed separately.
3. Find constants embedded inside formulas, for example a growth rate or a tax rate typed into the expression rather than held in its own cell. Record each with the formula it sits in. These are the assumptions most often missed.
4. For each assumption record: sheet and cell, label as written, value, unit, period or date basis, how many formulas depend on it, and the source as stated on the sheet, in a comment or in a notes column, or BLANK.
5. Flag assumptions that carry no unit, no period, or no source.
6. Flag any assumption whose value appears more than once as a separate typed constant in different cells, because those will drift apart.
7. If an assumptions sheet already exists, list what it holds that the model does not use, and what the model uses that it does not hold.
8. Stop for the checkpoint before writing anything into the workbook.

## Human approval checkpoint

Present the register. Ask: "Would you like me to write this register to a new sheet named Assumptions? I will not change any existing cell, and any value I write will be a copy, not a link." Write the sheet only if the user agrees.

## Output

Summary line: "N assumptions found across M sheets: X with a stated source, Y without, Z embedded in formulas."

Register:

| # | Sheet | Cell | Label | Value | Unit | Period | Dependants | Source stated | Flags |
|---|---|---|---|---|---|---|---|---|---|

Embedded constants:

| Sheet | Cell | Formula | Constant | What it appears to represent |
|---|---|---|---|---|

Duplicates: any value typed into more than one place, with every cell listed.

If an assumptions sheet exists: items in the sheet but unused, and items used but absent from the sheet.

## Fallbacks and edge cases

- A constant used once in a label or a footnote is not an assumption; list it under incidental constants.
- Dates typed as text: record the cell and note "date stored as text" rather than reinterpreting it.
- Named ranges: record the name alongside the cell reference, because reviewers look for the name.
- A cell that mixes a constant and a reference, such as a reference multiplied by a typed factor, counts as an embedded constant and the factor is recorded.
- Where the unit is not stated anywhere, leave the unit field blank. Do not infer it from the magnitude of the number.

## Rules

- Never change, move, relabel or delete an input.
- Never infer a source. If the workbook does not state one, the field is blank.
- Never judge whether a value is correct, conservative or aggressive.
- Record values exactly as held, not as displayed.
- A written Assumptions sheet contains copies, never formulas that overwrite or link back into the model.

## Self-check

- [ ] Every sheet in scope was classified.
- [ ] Every register row has a cell reference and a value.
- [ ] Constants embedded inside formulas were searched for, and the result is stated even when none were found.
- [ ] No existing cell was changed.
- [ ] The Assumptions sheet was written only with approval.
