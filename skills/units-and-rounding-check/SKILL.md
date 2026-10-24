---
name: units-and-rounding-check
description: "Checks the open workbook for unit and rounding faults: thousands mixed with millions, more than one currency added together, percentages stored inconsistently, displayed rounding that makes totals appear not to add, and hardcoded conversion factors. Changes no value. Use when the user asks to check units, scaling, currency consistency, or why a total looks one out. Not for re-adding totals against their components; use reconciliation-check for that."
---

# Units and rounding check

## Purpose

Catch the arithmetic that is correct and still wrong. Adding a figure in thousands to one in millions produces a number with no error attached to it, and a total that appears not to add because of display rounding produces a question in a board meeting. The skill reports both conditions and never edits a value.

## When to use

- The user asks to check units, scaling, currency or rounding in a workbook.
- A total looks one or two out and the formulas have already been checked.
- Before a pack where figures from several sources are combined.
- Do not use to convert, rescale or restate anything.

## Inputs

1. The open workbook (required).
2. Scope (optional): all sheets (default), or named sheets.
3. Reporting basis (optional): the intended unit and currency for the pack, if there is one.

## Procedure

1. Read the unit signals for every block of figures: column and row headers, the number format applied, any scaling note such as a figures in thousands caption, and the unit recorded on any assumptions sheet.
2. Record the stated unit per block, or UNSTATED where no signal exists. Unstated is a finding, not a blank.
3. Find aggregations that combine blocks with different stated units, and report each with both units and the cell doing the combining. This is the highest severity finding the skill produces.
4. Find aggregations combining more than one currency, including any sum crossing a currency labelled column.
5. Check percentage storage: values held as a fraction and values held as a whole number both appear as a percentage once formatted. Report any column mixing the two, and any formula multiplying by one hundred where the source is already a whole number.
6. Find hardcoded conversion and scaling factors inside formulas, such as a division by one thousand or a fixed exchange rate, and record each with its cell.
7. Check displayed versus underlying rounding: where a column of displayed values does not sum to the displayed total, report it as a display rounding difference and state both the displayed and the underlying difference, because only one of them is a real break.
8. Check that the reporting basis, if supplied, matches the figures presented on the output sheets.
9. Assign severity: HIGH for mixed units or currencies inside one aggregation, MEDIUM for unstated units and hardcoded factors, LOW for display rounding that is cosmetic.
10. Stop for the checkpoint.

## Human approval checkpoint

Present the findings. Ask: "Would you like me to add a comment on each HIGH finding, and a units column on the assumptions sheet if one exists? I will not change any value, format or formula." Add only what the user approves.

## Output

Summary line: "N blocks read: U with a stated unit, V unstated. H high findings, X medium, Y low."

Unit map:

| Sheet | Block or range | Stated unit | Currency | Source of the signal |
|---|---|---|---|---|

Findings:

| # | Severity | Sheet | Cell | Condition | Units or currencies involved | Why it matters |
|---|---|---|---|---|---|---|

Hardcoded factors: each cell, formula and the factor, with what it appears to convert.

Display rounding: each total with its displayed difference and its underlying difference.

## Fallbacks and edge cases

- A block with no header and no format signal is reported UNSTATED rather than assumed to match its neighbours.
- A currency symbol in a number format is a signal, but a symbol typed into a label is a stronger one. Report both and say which was used.
- Where a conversion factor is correct and intentional, it is still reported, marked "may be intentional", because a correct factor typed into a formula still breaks when the rate moves.
- Percentages stored as text: report under storage, not under units.
- Where the reporting basis is not supplied, say that basis consistency could not be checked rather than assuming one.

## Rules

- Never convert, rescale, reformat or restate any value.
- Never assume a unit from the magnitude of a number. A figure of 1,250 could be either.
- Always report the displayed and the underlying difference separately for a rounding finding.
- Unstated is a finding and is always reported with its count.
- Quote number formats exactly where they carry the unit signal.

## Self-check

- [ ] Every block of figures in scope has a unit row, including unstated ones.
- [ ] Every HIGH finding names both units or both currencies and the combining cell.
- [ ] Display rounding findings report both differences.
- [ ] No value, format or formula was changed.
- [ ] Comments were added only with approval.
