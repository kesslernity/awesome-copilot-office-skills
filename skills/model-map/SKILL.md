---
name: model-map
description: "Traces the calculation chain behind a chosen output cell in the open workbook, back through every intermediate step to the inputs it ultimately depends on, and reports the path, the sheets crossed, and anything that breaks the chain such as hardcoded overrides or external references. Changes nothing. Use when the user asks how a number is calculated, what drives it, or what would change if an input moved. Not for reviewing every formula in the workbook; use formula-risk-review for that."
---

# Model map

## Purpose

Answer the question every reviewer eventually asks: where does this number actually come from. The skill walks the dependency chain backwards from one output cell to the inputs underneath it, names every step on the way, and flags the places where the chain stops being a calculation and becomes a typed value.

## When to use

- The user asks how a figure is calculated, what drives it, or what feeds a reported total.
- Before changing an input, to see what it touches.
- Do not use to judge whether the logic is right. This skill traces, the reviewer judges.

## Inputs

1. The open workbook (required).
2. The target cell (required): the output to trace back from.
3. Direction (optional): backwards to inputs (default), or forwards to everything the target affects.
4. Depth limit (optional): maximum levels to walk. Default is the full chain.

## Procedure

1. Confirm the target: sheet, cell, current value, and its formula or a note that it is a typed constant.
2. Walk backwards one level at a time. At each level record the cell, its formula, its value, and which cells it references.
3. Continue until each branch terminates at an input, an external reference, or the depth limit.
4. Classify every terminal: TYPED INPUT, EXTERNAL REFERENCE, NAMED CONSTANT, or DEPTH LIMIT REACHED.
5. Flag overrides: a cell in the middle of the chain that holds a typed value where its neighbours hold formulas. An override is a deliberate or forgotten manual change and it stops the model responding to its inputs.
6. Record every sheet boundary the chain crosses, and the count of crossings. A chain that crosses six sheets is harder to review than one that crosses one, and that is worth saying.
7. Record the breadth: how many distinct inputs the target ultimately depends on, and which inputs have the most paths to it.
8. If direction is forwards, do the same walk outward and report everything the target feeds, with the reported outputs it reaches.
9. Report. This skill has no write step.

## Human approval checkpoint

This skill changes nothing, so there is no change to approve. Before tracing a chain that exceeds roughly two hundred cells, report the size and ask: "Full trace, a summary of the first three levels, or only the terminal inputs?" Then proceed as asked.

## Output

Summary line: "<sheet>!<cell> depends on N distinct inputs through M intermediate cells, crossing S sheets. O overrides found."

Chain, deepest level last:

| Level | Sheet | Cell | Value | Formula or terminal type | Feeds |
|---|---|---|---|---|---|

Terminal inputs:

| Sheet | Cell | Label | Value | Paths to target |
|---|---|---|---|---|

Attention list: overrides, external references, and any branch stopped by the depth limit.

## Fallbacks and edge cases

- Circular references: report the cycle with every cell in it and stop walking that branch, rather than looping.
- Very wide chains: cap the per level listing at fifty cells, say it is capped, and always report the terminal inputs in full.
- Whole column references: record the reference as written and treat it as one edge rather than expanding it cell by cell.
- Indirect or dynamically built references: record them as UNRESOLVED REFERENCE with the formula, because the target cannot be established statically.
- External workbooks: record the path as written and stop. Do not open the file.

## Rules

- Never change, replace or remove an override, even when it is obviously stale. Report it.
- Never follow an external reference out of the workbook.
- Report an unresolved reference as unresolved rather than guessing its target.
- Quote formulas and cell references exactly, including sheet qualifiers.
- A typed value sitting in a formula block is always reported, even where it matches what the formula would have produced.

## Self-check

- [ ] The target cell, its value and its formula are stated.
- [ ] Every branch ends in a classified terminal or a stated limit.
- [ ] Every override is listed with its cell and value.
- [ ] Sheet crossings are counted and reported.
- [ ] Nothing in the workbook was changed.
