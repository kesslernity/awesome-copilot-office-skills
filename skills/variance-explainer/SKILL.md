---
name: variance-explainer
description: "Explains the movement between two periods or between plan and actual in the open workbook by splitting it into the drivers the data supports, reconciling the named drivers back to the total, and reporting the remainder as unexplained rather than attributing it. Invents no driver. Use when the user asks why a number moved, to bridge two periods, or to explain a variance."
---

# Variance explainer

## Purpose

Explain a movement without inventing a reason for it. The skill decomposes the change between two columns into the drivers the workbook can actually evidence, re-adds those drivers back to the total movement, and states the remainder as unexplained. A bridge that reconciles to the penny with no unexplained line is usually a bridge that has been forced.

## When to use

- The user asks why a figure moved, to bridge two periods, or to explain plan against actual.
- A variance needs a written explanation for a pack, a review or a meeting.
- Do not use to decide which driver matters most commercially. This skill decomposes, the user interprets.

## Inputs

1. The open workbook (required), and the two columns or ranges being compared, with which is the base and which is the comparison.
2. Driver data (optional): the dimensions available to split by, such as volume, price, mix, rate, currency, entity or product.
3. Materiality (optional): the threshold below which a driver is grouped into Other. Default is one per cent of the total movement.

## Procedure

1. State the comparison explicitly: base label and value, comparison label and value, absolute movement and percentage movement.
2. Confirm that both sides cover the same scope: same entities, same periods, same currency, same inclusion rules. Report any difference before decomposing, because a scope difference is not a driver.
3. Identify which drivers the data supports. A driver is available only where both sides carry the dimension. Where only one side carries it, say so and exclude it.
4. Decompose the movement one driver at a time, in a stated order, because volume and price effects depend on the order of calculation. State the convention used.
5. Re-add every quantified driver and compare the sum to the total movement. The difference is the unexplained remainder.
6. Report the remainder as its own line, with its value and its percentage of the total movement. Never distribute it across the named drivers.
7. Group drivers below the materiality threshold into Other, and say how many items it contains.
8. Flag any driver whose sign is opposite to the total movement, because those are the ones a reader will ask about.
9. Stop for the checkpoint before writing anything into the workbook.

## Human approval checkpoint

Present the bridge and the unexplained line. Ask: "Would you like me to write this bridge to a new sheet? I will not change any figure in the model, and the commentary will describe the movement without proposing a cause." Write only if the user agrees.

## Output

Summary line: "Movement from <base label> <value> to <comparison label> <value>: <absolute> (<percentage>). Explained <value> across N drivers. Unexplained <value> (<percentage>)."

Bridge:

| Step | Driver | Value | Direction | Per cent of movement | Basis |
|---|---|---|---|---|---|

Scope differences, if any: what differs between the two sides and whether it was excluded from the decomposition.

Questions the bridge raises: each driver with an opposite sign, and the unexplained remainder, each phrased as a question for the owner.

## Fallbacks and edge cases

- Where only a total is available on one side, no decomposition is possible. Report the movement and say what data would be needed.
- A movement of zero made of offsetting drivers is still decomposed, and the summary says the net is zero while the gross movement is not.
- Base of zero: report the absolute movement and say the percentage is not meaningful rather than printing a large or infinite figure.
- Currency: if both sides are not in one currency, stop and report it. Do not convert.
- Where the order convention materially changes the split, say so and state the alternative result for the largest driver.

## Rules

- Never invent a driver, a cause or a business explanation. The skill reports what the arithmetic supports.
- Never force the bridge to tie by adjusting a driver or by absorbing the remainder.
- Always print the unexplained line, including when it is zero.
- State the decomposition order and the materiality threshold in the output.
- Never change a figure in the model.

## Self-check

- [ ] Base and comparison are named with their values.
- [ ] Scope was compared before decomposition and differences are reported.
- [ ] The named drivers plus the unexplained remainder equal the total movement exactly.
- [ ] The unexplained line is present even when zero.
- [ ] No figure in the model was changed.
