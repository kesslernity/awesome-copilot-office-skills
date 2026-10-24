---
name: reconciliation-check
description: "Re-adds every stated total in the open workbook against its components, checks that cross-sheet figures agree, and lists each line that does not tie with both values and their cell references. Never changes a number. Use when the user asks to tie out, reconcile, cross-check or verify that totals in a spreadsheet add up before it is sent or reported."
---

# Reconciliation check

## Purpose

Prove that a workbook agrees with itself before someone else finds out that it does not. The skill re-adds every stated total from its own components, compares figures that appear in more than one place, and reports each break with both values and where they live. It never edits a cell: the owner of the numbers resolves the break, the skill only makes it visible.

## When to use

- The user asks to reconcile, tie out, cross-check or verify totals in a workbook.
- A model, pack or report is about to go to finance, an auditor, a board or a client.
- Do not use to find the correct value. This skill reports differences, the user decides which side is right.

## Inputs

1. The open workbook (required).
2. Scope (optional): all sheets (default), or named sheets or ranges.
3. Tolerance (optional): an absolute or percentage threshold below which a difference is reported as WITHIN TOLERANCE rather than a break. Default is exact.

## Procedure

1. Identify every stated total: cells labelled Total, Sum, Subtotal, Net, Gross, Balance or similar, and the last row or column of any contiguous block of figures.
2. For each stated total, re-add its components from the cells it covers. Record the stated value, the re-added value and the difference.
3. Identify figures that appear more than once across sheets, matched on label and period rather than on cell position. Record each pair and whether they agree.
4. Check internal arithmetic relationships where both sides are present: opening plus movements equals closing, units times price equals value, parts expressed as percentages summing to one hundred.
5. Where a total is produced by a formula, record whether the formula range covers every component row, and flag ranges that stop short of the block or extend past it.
6. Classify every line: TIES, BREAK, WITHIN TOLERANCE, RANGE DOES NOT COVER BLOCK, or CANNOT CHECK.
7. Sort breaks by absolute size, largest first, and note which of them appear on a summary or reported sheet.
8. Stop for the checkpoint before writing anything into the workbook.

## Human approval checkpoint

Present the reconciliation table. Ask: "Would you like me to add a comment on each breaking cell recording the difference? I will not change any value or formula." Add comments only if the user agrees, and only comments.

## Output

Summary line: "N totals checked: X tie, Y break, Z cannot be checked. Largest break: <value> on <sheet>!<cell>."

Reconciliation table:

| # | Sheet | Cell | Label | Stated | Re-added | Difference | Status | Note |
|---|---|---|---|---|---|---|---|---|

Cross-sheet table, where the same figure appears in more than one place:

| Label | Period | Sheet A cell and value | Sheet B cell and value | Agrees |
|---|---|---|---|---|

Priority list: up to ten breaks to resolve first, each with the question the owner must answer.

Optional, after approval: a cell comment on each breaking cell beginning "RECONCILIATION:" followed by the stated value, the re-added value and the difference.

## Fallbacks and edge cases

- Values shown rounded in the cell but held at full precision: compare the underlying values and say so, because a difference that is only display rounding is not a break.
- Blocks broken by blank rows: treat each contiguous run as its own block and say which rows were grouped.
- A total that covers a range including itself: report as a circular reference rather than attempting the sum.
- Figures held as text: record CANNOT CHECK with the note "value stored as text", and never convert it.
- Very large workbooks: process sheet by sheet in tab order and say which sheets were covered if you stop early.

## Rules

- Never change, correct, round or delete a value or a formula.
- Never supply a value from memory or from outside the workbook.
- Quote cell references exactly, as sheet name then cell, for every figure reported.
- A difference of zero is a tie. Do not describe a tie as approximate.
- State the tolerance used in the summary line, including when it is exact.

## Self-check

- [ ] Every sheet in scope was read in tab order.
- [ ] Every stated total has a re-added value or a stated reason it could not be checked.
- [ ] Every BREAK row cites both values and the exact cells.
- [ ] No cell value or formula was changed.
- [ ] Comments were added only with approval.
