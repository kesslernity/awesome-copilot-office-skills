---
name: accessibility-pass
description: "Reviews the open presentation for accessibility issues (missing or duplicate slide titles, missing alt text, reading order, low contrast, small text, colour-only meaning, unexplained jargon and acronyms) and proposes fixes, including draft alt text, applied only after the user approves. Use when the user asks to make a deck accessible, check accessibility, add alt text or prepare slides for screen reader users."
---

# Accessibility pass

## Purpose

Help the deck owner make a presentation usable by people who rely on screen readers, magnification or high contrast, and by readers new to the subject. The skill finds issues, drafts fixes such as alt text, and applies only what the owner approves. It complements, and does not replace, the accessibility checker built into the application and a review by people who use assistive technology.

## When to use

- The user asks to check or improve accessibility, add alt text, or prepare a deck for screen reader users.
- A deck will be published, shared externally or used in training.
- Do not use as a compliance sign-off; the output is a draft review.

## Inputs

1. The open presentation (required).
2. Standard to follow (optional): the organisation's own guideline, if any. Default: common practice for presentations (every slide has a unique title, meaningful images have alt text, decorative images are marked decorative, text has sufficient contrast, meaning is not carried by colour alone).
3. Scope (optional): all slides (default) or a range.

## Procedure

1. For each slide, check:
   - Title: present, unique across the deck, and descriptive.
   - Images, icons, charts and SmartArt: alt text present and meaningful, or the item is decorative.
   - Reading order: the order a screen reader would follow matches the visual order, where you can inspect it.
   - Contrast: text against its background, where colours are readable. Flag likely low contrast; do not claim an exact ratio unless you can compute it from the colour values.
   - Text size: body text that looks smaller than 18 pt in a presentation intended for display.
   - Colour-only meaning: charts or status markers distinguished only by colour (for example red and green with no label).
   - Language: acronyms not expanded at first use, and jargon a newcomer would not understand.
   - Links: link text that says "click here" instead of describing the destination.
   - Tables: header row defined; no merged cells used for layout.
2. Draft alt text for each meaningful image without it: one or two sentences describing what the image conveys in context, not its appearance alone. For charts, state the chart type, what is measured and the main takeaway, using only values visible on the chart.
3. Give each finding a severity: HIGH (blocks understanding for a screen reader user), MEDIUM, LOW.
4. Stop for approval.
5. After approval, apply only the approved fixes: alt text, titles, decorative flags and acronym expansions. Report contrast, size and colour-only issues as recommendations unless the user explicitly asks you to change design.

## Human approval checkpoint

Present the findings table and the drafted alt text. Ask: "Which fixes should I apply? Reply 'all', list finding numbers, or edit any alt text first." Apply exactly what is approved.

## Output

| # | Slide | Issue | Severity | Proposed fix |
|---|---|---|---|---|

Drafted alt text: one block per image, with slide number and the image's position or name.

Summary: counts by severity, and a reminder to run the application's own accessibility checker and, where possible, a test with a screen reader.

If you cannot edit slides directly, return the table and alt text for the user to apply.

## Fallbacks and edge cases

- An image you cannot interpret: propose "Alt text needed: describe [what the image appears to show]" and mark it for the owner.
- A chart without readable values: describe the trend only and note that values were not readable.
- Slide titles hidden off-slide on purpose: treat them as present, but check they are descriptive.
- Decorative versus meaningful is unclear: ask the owner.

## Rules

- Alt text describes only what the image shows and what the slide says about it. Never invent data or names.
- Never change wording beyond titles and acronym expansions without approval.
- Do not present this review as a compliance certification.

## Self-check

- [ ] Every slide in scope was checked against every item in step 1.
- [ ] Every meaningful image has drafted alt text or a note explaining why not.
- [ ] Severity is assigned to every finding.
- [ ] Only approved fixes were applied.
