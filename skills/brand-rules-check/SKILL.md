---
name: brand-rules-check
description: "Checks every slide of the open presentation against written brand rules (colours with hex codes, fonts, logo use, layouts, tone, banned visuals) kept in references/brand-rules.md, and returns a per-slide report of PASS, FIX PROPOSED and MANUAL CHECK items, applying fixes only after approval. Use when the user asks whether a deck is on brand, follows the corporate template, or meets design guidelines."
---

# Brand rules check

## Purpose

Give the deck owner an auditable answer to "is this on brand?". The rules live in a plain text file the organisation controls, so the check is the same every time and can be reviewed. The skill reports per slide, proposes fixes it can make, marks what only a person can verify, and changes nothing until approved.

## When to use

- The user asks to check a deck against brand guidelines, corporate identity, the template or a style guide.
- A deck is about to go to an external audience.
- Do not use to design a new deck; use it on a deck that exists.

## Inputs

1. The open presentation (required).
2. Brand rules: read references/brand-rules.md from this skill folder. If it is missing or still contains the bracketed placeholders from references/brand-rules-template.md, stop and ask the user to fill in the template or paste their rules into the conversation.
3. Scope (optional): all slides (default) or a range.

## Procedure

1. Load the brand rules. Restate them back to the user as a short checklist grouped by area: colours, fonts, logo, layouts, imagery, tone and wording, banned items.
2. For each slide in scope, check each rule area:
   - Colours: text, shapes and chart colours against the approved hex values.
   - Fonts: heading and body fonts and any size rules.
   - Logo: presence, position and clear space where the rules specify them.
   - Layouts: whether the slide uses an approved layout from the template.
   - Imagery: banned visual types (for example clip art, stock photos with visible watermarks).
   - Tone and wording: banned terms, required terms, capitalisation of product names.
3. Give each check a verdict: PASS, FIX PROPOSED (state exactly what you would change, from what to what), or MANUAL CHECK (anything you cannot read or set precisely, such as exact logo coordinates, colour inside images, or image licensing).
4. Never mark PASS on something you could not actually inspect; use MANUAL CHECK.
5. Summarise: slides fully compliant, slides with proposed fixes, slides needing manual checks.
6. Stop for approval.
7. After approval, apply only the approved fixes, one slide at a time, and confirm each change.

## Human approval checkpoint

Show the report and ask: "Apply all proposed fixes, apply fixes on specific slides, or none? Manual checks stay with you." Apply exactly what is approved.

## Output

Rules restated: short checklist.

Per-slide report:

| Slide | Area | Verdict | Detail (current value, proposed value) |
|---|---|---|---|

Summary: counts by verdict, then the manual checks as a to-do list for the deck owner.

After applying: list of changes made. If you cannot edit slides directly, return the report only.

## Fallbacks and edge cases

- Rules file uses colour names without hex values: check against names and note that hex values would make the check exact.
- Slide built on a non-template layout: mark FIX PROPOSED with the nearest approved layout, but do not rebuild the slide without approval.
- Text inside images: MANUAL CHECK.
- Rules conflict with each other: report the conflict instead of choosing.

## Rules

- The brand rules file is the only standard. Do not apply general design opinions as if they were rules.
- Never change content (wording, numbers) to fix a design rule, except banned terms the rules list, and only with approval.
- Never delete slides or images.
- Mark anything unverifiable as MANUAL CHECK.

## Self-check

- [ ] Rules were loaded from references/brand-rules.md or pasted by the user, and restated.
- [ ] Every slide in scope has a verdict for every rule area.
- [ ] No PASS was given for something not inspected.
- [ ] Only approved fixes were applied.
