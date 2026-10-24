---
name: workbook-structure-audit
description: "Maps what the open workbook actually contains: every sheet including hidden and very hidden ones, named ranges, external links, data connections, protected areas, filtered or hidden rows and columns, and stale regions. Changes nothing. Use when the user asks what is in a workbook, inherits a file, or needs to understand a spreadsheet before trusting or editing it."
---

# Workbook structure audit

## Purpose

Tell someone what they have actually been sent. A spreadsheet hides most of itself: sheets set to hidden, rows filtered out of view, links reaching into files nobody can open, ranges named years ago. The skill produces one map of the whole file so a reader knows what exists before they trust a number on the front sheet.

## When to use

- The user has inherited, received or reopened a workbook and needs to know what is in it.
- Before editing, auditing or sending on a file that somebody else built.
- Do not use to judge whether the model is correct. This skill describes the container, not the calculations.

## Inputs

1. The open workbook (required).
2. Depth (optional): summary only, or full listing including every named range and link. Default is full.

## Procedure

1. List every sheet in tab order with its visibility state: visible, hidden, or very hidden. State the count of each.
2. For each sheet, record the used range, the approximate count of populated cells, whether it contains formulas, and whether it looks like input, calculation, output or documentation.
3. List every named range: name, what it refers to, its scope, and whether its reference resolves or is broken.
4. List every external link and data connection, with the target as written. Mark any target that is a local path, because those break for every other reader.
5. Record hidden or filtered rows and columns per sheet, and whether an autofilter is currently applied. A filtered sheet shows a subset, and a reader who does not notice will quote the wrong total.
6. Record protection: protected sheets, locked cells and whether the workbook structure is protected.
7. Flag regions that look stale: sheets with no formulas and dates older than the rest of the file, duplicated sheets whose names differ by a copy suffix, and ranges marked old, backup, v1 or do not use.
8. Report. This skill has no write step.

## Human approval checkpoint

This skill changes nothing, so there is no approval to give for a change. Before producing a full listing on a very large workbook, state the sheet count and ask: "Full listing of all N sheets, or summary only?" Then proceed as asked.

## Output

Summary line: "N sheets: V visible, H hidden, X very hidden. M named ranges, L external links, P protected sheets."

Sheet map:

| Tab | Sheet | Visibility | Used range | Formulas | Apparent role | Hidden rows or columns | Filter applied |
|---|---|---|---|---|---|---|---|

Named ranges:

| Name | Refers to | Scope | Resolves |
|---|---|---|---|

External links and connections:

| Sheet | Cell or connection | Target as written | Local path |
|---|---|---|---|

Attention list: hidden sheets holding formulas, broken names, local paths, and anything flagged stale, each with one line saying why a reader should look.

## Fallbacks and edge cases

- Very hidden sheets may not be listable in every environment. If the count cannot be established, say so rather than reporting zero, because zero and unknown are different answers.
- A sheet that is empty but present still gets a row, with the used range recorded as empty.
- Where a named range resolves to a deleted sheet, record the name and mark it broken rather than omitting it.
- Password-protected structure: record that it is protected and stop, rather than attempting to work around it.
- Charts and objects: count them per sheet without describing each one, unless the user asks for depth.

## Rules

- Never unhide, unfilter, unprotect or modify anything, including to see it better. Report what cannot be read instead.
- Never open or follow an external link.
- Report a local file path as written, and never guess what it points to.
- Unknown is a valid finding. Do not report zero where the answer could not be established.

## Self-check

- [ ] Every sheet in the workbook has a row, including hidden ones.
- [ ] Visibility counts in the summary line add up to the sheet count.
- [ ] Every named range was listed with whether it resolves.
- [ ] Nothing in the workbook was unhidden, unfiltered or changed.
- [ ] Anything that could not be read is reported as unknown, not as absent.
