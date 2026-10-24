---
name: scenario-skeleton
description: "Builds a base, downside and upside scenario scaffold wired to the workbook's existing input cells, with a single switch driving which case is live, and leaves every scenario value blank for the user to populate. Invents no assumption. Use when the user asks to add scenarios, sensitivities or cases to a model that currently holds one set of numbers."
---

# Scenario skeleton

## Purpose

Give a single point model the structure to hold more than one future, without inventing what those futures are. The skill finds the inputs worth flexing, builds a scenario block and a switch, and wires the model to read from the live case. Every scenario cell is left blank, because the numbers in a downside case are a judgement and the skill does not have one.

## When to use

- The user asks to add scenarios, cases or sensitivities to a model.
- A model produces one answer and a reviewer has asked what happens if an input moves.
- Do not use to decide what the downside is. The skill builds the frame, the user fills it.

## Inputs

1. The open workbook (required).
2. The inputs to flex (optional): if the user names them, use exactly those. If not, propose a list from the assumptions in the model and ask before building.
3. Case names (optional): default is Base, Downside, Upside.
4. Target sheet (optional): where the scenario block should live. Default is a new sheet named Scenarios.

## Procedure

1. Identify candidate inputs: typed constants that feed at least one formula and carry a label. Rank them by how many formulas depend on each.
2. Propose the list to flex, with the dependant count for each, and stop for approval of the list before building anything.
3. On approval, build the scenario block: one row per input, one column per case, plus a column recording the current live value so nothing is lost.
4. Copy the existing value into the Base column only. Leave Downside and Upside blank. Blank is the honest state until the user decides.
5. Build the switch: one cell holding the active case name, with validation limited to the case names, and a visible label stating which case is live.
6. Build the selector row that reads the active case for each input.
7. Prepare, but do not apply, the rewire: for each flexed input, the formula that would replace the typed constant with a reference to the selector. Present these as a list of proposed changes with the cell and both versions.
8. Stop for the checkpoint. The model is not rewired until the user approves.
9. On approval, apply the rewire one input at a time, and after each one confirm the model still produces the original result while the switch is on Base. If any output moves, stop and report.

## Human approval checkpoint

Two checkpoints, both required. First: the list of inputs to flex, before anything is built. Second: the rewire, presented as a before and after list, before any existing formula is touched. Say plainly: "Applying the rewire changes existing cells in the model. With the switch on Base every output should be unchanged, and I will verify that after each input."

## Output

Proposed inputs:

| Input | Sheet | Cell | Label | Current value | Dependants |
|---|---|---|---|---|---|

Scenario block, as built:

| Input | Current live value | Base | Downside | Upside |
|---|---|---|---|---|

Proposed rewire:

| Sheet | Cell | Before | After |
|---|---|---|---|

Verification after each applied rewire: the output cells checked and whether each is unchanged on Base.

## Fallbacks and edge cases

- An input used in only one formula may not be worth flexing. Report the dependant count and let the user choose.
- Where an input is already a reference rather than a constant, it does not need rewiring. Say so and exclude it.
- Protected sheets: report that the rewire cannot be applied and leave the scenario block built but unwired.
- If an output moves while the switch is on Base, stop immediately, report the cell and both values, and do not continue with the remaining inputs.
- Existing scenario structures: report them and ask whether to extend rather than building a second one.

## Rules

- Never populate a Downside or Upside value. Blank is the deliverable.
- Never apply the rewire without the second approval.
- Never rewire more than one input without verifying the Base result in between.
- Preserve the original typed value in the block before replacing the cell, so the change is reversible by hand.
- Never delete or overwrite an existing scenario mechanism.

## Self-check

- [ ] The input list was approved before anything was built.
- [ ] Base holds the original values and the other cases are blank.
- [ ] The switch is validated to the case names only.
- [ ] The rewire was approved separately, and every applied input was verified on Base.
- [ ] Original values are recorded in the block before any cell was changed.
