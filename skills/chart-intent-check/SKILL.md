---
name: chart-intent-check
description: "Checks every chart in the open workbook against what its title and labels claim: truncated or inverted axes, inconsistent scales across a set, missing baselines, a series whose range does not match the data it claims, dual axes that imply a relationship, and colours carrying unexplained meaning. Changes nothing. Use when the user asks to review charts before a deck, a pack or a publication."
---

# Chart intent check

## Purpose

Check that each chart shows what its title says it shows. Most misleading charts are not fabricated: the numbers are real and the axis starts at eighty. The skill compares the visual construction of every chart against its stated claim and reports the gaps, so the author can decide whether the construction is justified.

## When to use

- The user asks to review, check or sanity-check charts before they go into a deck, pack or publication.
- A set of charts will be read side by side and should be comparable.
- Do not use to redesign charts. This skill reports, the author decides.

## Inputs

1. The open workbook (required).
2. Scope (optional): all charts (default), or charts on named sheets.
3. Intended audience (optional): if given, note where a construction is likely to be misread by that audience.

## Procedure

1. Inventory every chart: sheet, name or position, chart type, title as written, and the ranges each series points at.
2. For each chart, read the axis configuration: minimum, maximum, whether the value axis starts at zero, whether either axis is reversed, and whether a logarithmic scale is used.
3. Compare the title's claim to the construction. A title claiming growth on an axis starting at eighty is a finding. So is a title naming a period the data does not cover.
4. Check the series ranges against the data: a series that omits rows present in the table, includes blanks as zero, or covers a different period from its siblings.
5. Across a set of charts intended for comparison, check scale consistency. Two charts side by side with different maxima will be read as equal heights meaning equal values.
6. Flag dual axis charts, and say which series sits on which axis, because a dual axis invites a reader to see a relationship that the chart does not demonstrate.
7. Flag unexplained encoding: a colour, pattern or highlight used on some points and not others with no legend or note saying what it means.
8. Flag missing context: no units on the value axis, no period on the category axis, and no source note anywhere on the sheet.
9. Classify each finding as HIGH if it changes how a reader reads the magnitude or direction, MEDIUM if it impedes comparison, LOW if it is labelling.
10. Stop for the checkpoint.

## Human approval checkpoint

Present the findings. Ask: "Would you like me to write a Chart review sheet recording these findings? I will not change any chart, axis or series." Write only if the user agrees, and change no chart.

## Output

Summary line: "N charts checked: H high, X medium, Y low. Z charts in comparison sets with inconsistent scales."

Findings:

| # | Severity | Sheet | Chart | Type | Title as written | Finding | Why a reader could be misled |
|---|---|---|---|---|---|---|---|

Axis table:

| Chart | Value axis min | Value axis max | Starts at zero | Reversed | Log scale |
|---|---|---|---|---|---|

Comparison sets: charts intended to be read together, with their differing scales.

## Fallbacks and edge cases

- A truncated axis is sometimes correct, for example on an index that never approaches zero. Report it with the note "truncation may be justified" and let the author decide.
- Charts embedded as images: record that the chart is an image and cannot be inspected, rather than skipping it silently.
- A chart with no title: report the absence as a finding rather than inferring the intent from the data.
- Sparklines and conditional formatting bars: report them as present and note that scale behaviour differs, without treating them as charts.
- Where the source data range sits on a hidden sheet, say so, because the reader cannot check it.

## Rules

- Never change a chart, an axis, a series, a colour or a title.
- Never claim a chart is misleading. Report the construction and what a reader could conclude from it.
- Quote titles and axis bounds exactly as set.
- Where a construction is defensible, say so in the same row rather than in a separate note.
- A chart that cannot be inspected is reported as not inspected, never as passing.

## Self-check

- [ ] Every chart in scope has a row, including those that could not be inspected.
- [ ] Every HIGH finding states what a reader could wrongly conclude.
- [ ] Axis minimum and maximum are reported for every value axis read.
- [ ] No chart was modified.
- [ ] Comparison sets are identified, or the output says none were found.
