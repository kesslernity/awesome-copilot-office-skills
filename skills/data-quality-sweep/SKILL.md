---
name: data-quality-sweep
description: "Sweeps a data range in the open workbook for conditions that break reporting: mixed types in a column, numbers and dates stored as text, duplicates on the apparent key, inconsistent category spellings, out of range values, blanks that are meaningful, and inconsistent date formats. Corrects nothing. Use when the user asks to check data quality, find problems in a dataset, or audit a table before analysis."
---

# Data quality sweep

## Purpose

Report what is wrong with a table before anybody builds on it. The skill profiles each column, names the conditions that will distort a pivot, a chart or a total, and quantifies how much of the data each one affects. It corrects nothing, because the fix for a blank depends on what the blank means and only the owner knows that.

## When to use

- The user asks to check data quality, profile a dataset or audit a table before analysis.
- A pivot, chart or total has produced a result that looks wrong and the data is suspected.
- Do not use to clean the data. If the host offers a data-cleaning skill or tool, use that for fixes. This one reports and quantifies, and it stops there.

## Inputs

1. The open workbook (required), and the range or table to sweep.
2. Expected schema (optional): column names with their intended type and any valid value list. If supplied, check against it.
3. Key columns (optional): the columns that should identify a row uniquely.

## Procedure

1. Establish the range: header row, first and last data row, and column count. State what was taken as the header.
2. Profile every column: populated count, blank count, distinct count, inferred type, and the three most frequent values.
3. Flag mixed types within a column, reporting the minority type and its row count, because the minority is usually the fault.
4. Flag numbers and dates stored as text, with counts. These sum to zero in a total and sort alphabetically.
5. Flag inconsistent date representations within one column, including two digit years and ambiguous day and month ordering, and say which rows are ambiguous rather than resolving them.
6. On text categories, group values that differ only by case, trailing space, punctuation or a common misspelling, and report each group with its variants and counts. These split a category in a pivot without any error appearing.
7. On the key columns, report duplicate rows: fully identical rows, and rows sharing the key but differing elsewhere. The second kind is the one that corrupts a join.
8. Flag out of range values where a schema or an obvious bound exists: negative quantities, percentages above one hundred, dates in the future, and values far outside the rest of the column.
9. Distinguish blank, zero and a text placeholder such as a dash or the letters NA, and report each count separately, because they mean different things and only one is a number.
10. Score the table: the count of conditions found by severity, and the proportion of rows touched by at least one HIGH condition.
11. Stop for the checkpoint.

## Human approval checkpoint

Present the profile and findings. Ask: "Would you like me to write a Data quality sheet recording these findings, and add a flag column marking affected rows? I will not change any value in the data." Write only what the user approves, and only alongside the data, never over it.

## Output

Summary line: "R rows, C columns. N conditions found: H high, X medium, Y low. P per cent of rows touched by at least one high condition."

Column profile:

| Column | Populated | Blank | Distinct | Inferred type | Top values | Flags |
|---|---|---|---|---|---|---|

Findings:

| # | Severity | Column | Condition | Rows affected | Example rows | Why it matters |
|---|---|---|---|---|---|---|

Category variant groups: each group with its variants, counts and the row numbers of the minority spellings.

Duplicates: identical rows, and key collisions with differing detail, listed separately.

## Fallbacks and edge cases

- A column that is genuinely mixed by design, such as a notes field, is reported with the note "mixed type may be intentional".
- Where no header row can be established, say so and profile by column letter rather than guessing names.
- Regional date and decimal conventions: state the convention assumed, and report ambiguous values as ambiguous rather than converting them.
- Merged cells inside the range: report their presence and location, and treat the range as unsafe to profile below that point if structure is broken.
- Very large ranges: profile fully but cap example row lists at twenty, saying the list is capped.

## Rules

- Never correct, convert, trim, deduplicate, fill or delete a value.
- Never resolve an ambiguous date. Report both readings.
- Blank, zero and a text placeholder are three different findings and are never merged into one count.
- Quote example values exactly, and make trailing spaces visible by describing them.
- Where a bound is assumed rather than supplied, say that it was assumed.

## Self-check

- [ ] The header row and range used are stated.
- [ ] Every column has a profile row.
- [ ] Blank, zero and placeholder counts are reported separately.
- [ ] No value in the data was changed.
- [ ] A flag column or Data quality sheet was written only with approval, and never over the data.
