---
name: lookup-integrity-check
description: "Checks every lookup in the open workbook for the faults that return a wrong row rather than an error: approximate match left on by default, duplicate keys on the lookup side, keys that exist in one table and not the other, mismatched types, and ranges that shift when rows are inserted. Changes nothing. Use when the user asks to check lookups, joins, references between tables, or why two sheets disagree."
---

# Lookup integrity check

## Purpose

A lookup that fails loudly returns an error and gets fixed. A lookup that matches the wrong row returns a real value from a real record, and that value goes into a report. The skill examines every lookup in the workbook for the faults that produce a confident wrong answer, and reports them with the keys involved.

## When to use

- The user asks to check lookups, joins, mappings or references between tables.
- Two sheets that should agree do not, and the cause is not yet known.
- Do not use to repair or rewrite lookups. This skill reports, the builder decides.

## Inputs

1. The open workbook (required).
2. Scope (optional): all lookups (default), or named sheets.
3. Key columns (optional): if the user names the columns that should act as keys, use them; otherwise infer and say what was inferred.

## Procedure

1. Find every lookup, in whatever form the workbook uses: direct lookup functions, index and match pairs, and conditional aggregations acting as lookups.
2. For each, record the lookup value, the table or range searched, the column or index returned, and the match mode as written.
3. Flag approximate match wherever it is used without an explicit reason nearby. Where the match mode argument is omitted and the function defaults to approximate, flag it, because an omitted argument is the most common form of this fault.
4. On the lookup table, test the key column for duplicates. A duplicate key means the lookup returns the first match and silently ignores the rest. Record the duplicated keys and how many times each appears.
5. Compare key sets in both directions: keys present in the source but missing from the lookup table, and keys in the table never used. Report counts and up to twenty examples each way.
6. Check type consistency on the key: numbers stored as text on one side and as numbers on the other, trailing spaces, and differing case where the function is case sensitive.
7. Flag index arguments given as a fixed column number rather than a matched header, because inserting a column silently redirects the result.
8. Flag lookup ranges that are not absolute or named, where copying the formula shifts the table.
9. Assign severity: HIGH if the fault can return a wrong row, MEDIUM if it breaks on edit, LOW if it is style.
10. Stop for the checkpoint.

## Human approval checkpoint

Present the findings. Ask: "Would you like me to add a comment on each HIGH lookup describing the fault, and a sheet listing the unmatched keys? I will not change any formula." Add only what the user approves.

## Output

Summary line: "N lookups checked: H high, X medium, Y low. D duplicate keys, U unmatched keys."

Lookups:

| # | Severity | Sheet | Cell | Lookup value | Table searched | Returns | Match mode | Finding |
|---|---|---|---|---|---|---|---|---|

Duplicate keys: each key, the sheet and column, and the number of occurrences.

Unmatched keys: present in source but not in table, and present in table but never used, each as a list with counts.

Type mismatches: the key, both representations, and the sheets.

## Fallbacks and edge cases

- Where approximate match is correct, as in a banded rate table, still report it, marked "approximate match may be intentional on a banded table".
- Keys that differ only by trailing space: report them as a type or whitespace mismatch, not as unmatched, because the fix is different.
- Very large key sets: report full counts and cap the examples at twenty each way, saying the list is capped.
- A lookup pointing at another workbook: record it and mark the key comparison as CANNOT CHECK rather than opening the file.
- Case sensitivity differs by function. State the assumption used for each finding.

## Rules

- Never change a formula, a key, a table or a cell type.
- Never deduplicate, trim or convert a key, even to test a theory. Report the condition instead.
- Quote keys exactly, including spaces, and say where a space is present.
- Do not report unmatched keys without stating the direction. Missing from the table and unused in the table are different problems.

## Self-check

- [ ] Every lookup in scope has a row, including those inside conditional aggregations.
- [ ] Every row states the match mode, including when the argument was omitted.
- [ ] Key comparison was run in both directions and both counts are reported.
- [ ] Nothing in the workbook was changed.
- [ ] Capped lists say they are capped.
