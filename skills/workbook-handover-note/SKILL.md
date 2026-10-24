---
name: workbook-handover-note
description: "Writes the note that should have been in the file: what the workbook is for, which sheet to start on, where the inputs are, what is calculated, what must be refreshed and on what cadence, what is known to be fragile, and who to ask. Records only what the workbook evidences. Use when a model is being handed over, archived, or picked up by somebody new."
---

# Workbook handover note

## Purpose

Write down what the builder knew and never recorded. Most models are inherited rather than introduced, and the cost of that is paid in weeks of reverse engineering. The skill drafts a handover note from what the workbook itself evidences, and leaves an explicit gap wherever the file does not say, so the person handing over fills in the parts only they know.

## When to use

- A workbook is being handed to another person, team or successor.
- A model is being archived and should be understandable later.
- The user has just inherited a file and wants a note to build on as they learn it.
- Do not use to document what the model should do. The note records what it does.

## Inputs

1. The open workbook (required).
2. Known context (optional): purpose, owner, cadence and audience, if the user supplies them.
3. Prior audits (optional): output from a structure audit, assumptions register or formula review, which this skill summarises rather than repeating.

## Procedure

1. Establish the shape: sheet count, which sheets are inputs, calculations, outputs and documentation, and which are hidden. Where a prior structure audit exists, use it rather than re-deriving.
2. Identify the start sheet: the one a reader should open first, chosen by where the outputs are presented, and say why it was chosen.
3. Identify the inputs: where typed assumptions live, and whether they are gathered or scattered. Where they are scattered, say so plainly, because that is the thing that costs the successor time.
4. Identify refresh points: external links, data connections, dated labels and any cell holding a period or as at date. For each, record what must be updated and anything the workbook states about frequency. Where frequency is not stated, record UNKNOWN.
5. Identify fragility: overrides, hardcoded factors, sheets without formulas feeding reported numbers, and anything a prior audit flagged HIGH. Summarise, with pointers to the detail rather than reproducing it.
6. Record the open questions the workbook cannot answer: owner, approver, source systems, why a given assumption is set where it is. Each becomes a labelled gap in the note.
7. Draft the note using only what has been established. Every claim traces to a sheet, a cell or a supplied input.
8. Stop for the checkpoint before writing anything into the workbook.

## Human approval checkpoint

Present the drafted note and the list of gaps. Ask: "Would you like me to write this as a new sheet named Read me first, placed as the first tab? I will not change any other sheet, and the gaps will stay marked as gaps." Write only if the user agrees.

## Output

The note, in this order:

1. What this workbook produces, in two sentences.
2. Start here: the sheet to open, and why.
3. Inputs: where they are, how many, and whether gathered or scattered.
4. Calculation path: the main chain in plain words, naming the sheets in order.
5. Refresh: what to update, where, and how often, with UNKNOWN where the file does not say.
6. Known fragility: the shortlist, each with a cell reference.
7. Gaps: what the workbook cannot tell you, as labelled questions.
8. Provenance: the date the note was drafted and that it was drafted from the file itself.

Gap list, kept separate so it is easy to fill:

| Gap | Question for the outgoing owner |
|---|---|

## Fallbacks and edge cases

- Where the purpose cannot be established from the file, say so in section one rather than inferring it from the sheet names. An invented purpose is worse than a blank one.
- Where no clear output sheet exists, name the candidates and say the start sheet is uncertain.
- Very large workbooks: keep the calculation path to the main chain and say that secondary chains are not covered.
- Where a prior audit is supplied, cite it rather than repeating its tables.
- If the workbook already has a documentation sheet, read it, note where it disagrees with the file, and never overwrite it.

## Rules

- Never invent a purpose, an owner, a cadence or a source system.
- UNKNOWN is a valid and expected entry. Do not replace it with a guess to make the note look complete.
- Every statement in the note points at a sheet or a cell, or is labelled as supplied by the user.
- Never overwrite an existing documentation sheet. Write alongside it and report the disagreement.
- Never change any other sheet.

## Self-check

- [ ] Every section is present, including those that are mostly unknown.
- [ ] Every factual statement traces to a sheet, a cell, or a user supplied input.
- [ ] The gap list is populated and is not empty by assumption.
- [ ] No existing sheet was changed or overwritten.
- [ ] The Read me first sheet was written only with approval.
