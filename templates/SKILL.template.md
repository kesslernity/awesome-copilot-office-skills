---
name: your-skill-name
description: "One line that tells Copilot WHEN to reach for this skill, not what it is. Name the trigger words a user would actually type. State what the skill refuses to do. Add a Not for clause pointing at the sibling skill it could be confused with. Between 40 and 1024 characters, on one line, in double quotes."
---

# Your skill name

## Purpose

What this exists to do, and the failure it prevents. Two to four sentences. Say what it never does.

## When to use

- The trigger, in the words a user would say.
- A second situation.
- Do not use for X. This skill reports, the user decides.

## Inputs

1. The open workbook or presentation (required).
2. A second named input, and what happens if it is absent.
3. Scope or threshold (optional), with the default stated.

## Procedure

1. Numbered steps the model follows in order.
2. Keep each step checkable, so a reader can tell whether it was done.
3. Say what to record at each step, not only what to look at.
4. Stop for the checkpoint before changing anything.

## Human approval checkpoint

What is presented, and the exact question asked. State plainly what will and will not change if the user agrees.

## Output

Summary line: the one sentence with the counts in it.

The table, with named columns:

| Column | Column | Column |
|---|---|---|

Anything written only after approval.

## Fallbacks and edge cases

- The case where the input is ambiguous: report both readings, never resolve.
- The case where something cannot be read: report it as unknown, never as absent.
- Very large inputs: say what was covered if you stop early.

## Rules

- Never change the thing the skill is reporting on.
- Never supply a value from memory or from outside the file.
- Never name a vendor: these files run in several runtimes, and the validator rejects it.
- Quote exactly, including references, so a reader can find what you mean.

## Self-check

- [ ] Every item in scope was covered, or the gap is named.
- [ ] Every row has its reference and its status.
- [ ] Nothing was changed without approval.
- [ ] Anything unreadable is reported as unknown.
