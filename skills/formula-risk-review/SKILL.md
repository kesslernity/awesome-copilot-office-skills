---
name: formula-risk-review
description: "Reviews the formulas in the open workbook for the faults that silently produce wrong answers: constants typed inside expressions, ranges that stop short of their block, inconsistent formulas across a row, volatile and fragile functions, and error values hidden behind IFERROR. Changes no formula. Use when the user asks to review, audit or sanity-check the formulas or the build quality of a spreadsheet."
---

# Formula risk review

## Purpose

Find the formula faults that do not announce themselves. A broken formula shows an error and gets fixed. A formula whose range stops one row short returns a plausible number and gets presented. The skill looks for the second kind, reports each with its cell and why it matters, and never edits the workbook.

## When to use

- The user asks to review, audit or quality-check the formulas or construction of a workbook.
- Before a model is relied on for a decision, or handed to someone else.
- Do not use to rebuild or optimise formulas. This skill reports risk, the builder decides what to change.

## Inputs

1. The open workbook (required).
2. Scope (optional): all sheets with formulas (default), or named sheets or ranges.
3. Severity floor (optional): report everything (default), or only HIGH findings.

## Procedure

1. Inventory every formula cell by sheet, and group formulas that should be identical across a row or column block.
2. Within each block, find cells whose formula differs from its neighbours. An inconsistent cell in an otherwise uniform row is the single most common cause of a wrong total.
3. Find constants typed inside formulas, excluding the obvious structural ones such as a multiplier of twelve for months. Record the cell, the formula and the constant.
4. Check aggregate ranges against the block they appear to cover: a sum that starts one row below the first data row, or stops above the last, or includes the header or the total itself.
5. Flag fragile constructions: nested conditionals more than three deep, references to entire columns inside large calculations, hardcoded cell references where a named range exists, and references that cross sheets without a label nearby.
6. Flag volatile functions that recalculate on every change, and say where they are concentrated.
7. Flag error suppression: any wrapper that replaces an error with a blank or a zero. Record what the underlying error would have been where it can be established, because a suppressed error becomes a silent zero in a total.
8. Assign each finding a severity: HIGH if it can change a reported number without showing an error, MEDIUM if it will break under edit, LOW if it is style.
9. Stop for the checkpoint. This skill proposes, it does not edit.

## Human approval checkpoint

Present the findings table. Ask: "Would you like me to add a comment on each HIGH finding describing the risk? I will not change any formula." Add comments only if the user agrees, and only comments.

## Output

Summary line: "N formula cells reviewed across M sheets: H high, X medium, Y low."

Findings:

| # | Severity | Sheet | Cell | Formula as written | Finding | Why it matters |
|---|---|---|---|---|---|---|

Inconsistent blocks: each block with its expected pattern, the cells that differ, and both formulas.

Range coverage: each aggregate whose range does not match its block, with the range used and the block it appears to cover.

## Fallbacks and edge cases

- A deliberate exception inside a uniform row, such as a first period with no prior balance, is still reported, with the note "may be intentional". The reviewer decides.
- Array and spill formulas: report the anchor cell and treat the spill range as one finding, not one per cell.
- Where a formula is too long to quote in full, quote the first eighty characters and say it is truncated.
- Protected or very large sheets: say which sheets were not reviewed and why.
- External references: report them as a finding only when they also carry one of the faults above; the structure audit covers their existence.

## Rules

- Never change, simplify, repair or reformat a formula.
- Never state what a formula should be unless the pattern is established by its own neighbours in the same block.
- Quote formulas exactly as written, including sheet qualifiers.
- Severity describes consequence, not effort. A one-character range error that moves a reported total is HIGH.
- Do not report a finding as a defect when the only evidence is that it is unusual. Say it is unusual.

## Self-check

- [ ] Every sheet in scope was inventoried, and sheets skipped are named with a reason.
- [ ] Every finding has a sheet, a cell and the formula as written.
- [ ] Every HIGH finding states the number it could change.
- [ ] No formula was edited.
- [ ] Comments were added only with approval.
