---
name: ai-writing-tells-check
description: "Finds the patterns that make slide text read as machine-written (filler openers, inflated verbs, groups of three, em dashes, hedge stacks, symmetrical sentences) and proposes a plain rewrite for each, slide by slide. Changes no figure, name, date or claim, and applies nothing until the user approves. Use when the user says a deck sounds like AI, sounds generic, needs a human voice, or asks for an AI-tells, slop or tone check."
---

# AI writing tells check

## Purpose

A deck drafted with AI help is usually factually fine and tonally obvious. The tells are
structural, not vocabulary: openers that clear the throat, triples that pad, hedges stacked two
deep, every sentence the same length. Readers notice before they can name it, and in a client or
board deck the cost is credibility.

This finds the tells and proposes plain replacements. It never touches a number.

## When to use

- The user says a deck sounds like AI, sounds generic, sounds corporate, needs a human voice,
  or asks for a slop, tone or AI-tells check.
- A deck was drafted with AI help and is going to a client, a board or a public audience.
- Run it **last**, after the content is settled. Rewriting prose that is about to be cut wastes
  the user's attention.
- Do not use to change meaning, shorten a deck or fix consistency. Those are `deck-trim-proposal`
  and `deck-consistency-sweep`.

## Inputs

1. The deck (required). If nothing is open or attached, ask for it.
2. Scope (optional): all slides, a range, titles only, or speaker notes too. Default: all slide
   text and titles, excluding speaker notes.
3. Voice (optional): a sample of the user's own writing, or a house style note. Default: plain,
   specific and direct.
4. Strictness (optional): `flag-all`, or `high-confidence` which reports only tells with a clear
   fix. Default: `high-confidence`.

## Procedure

1. Read every slide. Work slide by slide, keeping each slide's text together, because a tell is
   often only visible against its neighbours.
2. Check each tell in [references/tells.md](references/tells.md). That file is the list; do not
   invent additional tells from taste, and do not skip ones you find unfashionable.
3. For each hit, record: slide number, the exact span, which tell, and one proposed replacement.
4. **Carry every figure, name, date, product and claim through unchanged.** Copy them, never
   retype them. If a rewrite cannot keep a number in place, do not propose it.
5. If a sentence's only problem is that it is long, leave it. Length is not a tell; uniformity is.
6. Where a tell is load-bearing, say so and leave it. A triple that lists three real things is a
   list, not padding. An em dash inside a quotation stays, because it is someone else's words.
7. Rank by how visible each tell is to a reader who is not looking for it. Openers and inflated
   verbs top; rhythm last.
8. Draft the table (see Output) and **stop for approval**.
9. After approval, apply only the accepted rewrites, one slide at a time, leaving every other
   character untouched.
10. Report what you changed and what you left.

## Human approval checkpoint

Show the table of proposed rewrites with the tell named for each, plus the count by tell type and
anything you deliberately left. Ask: "Shall I apply all of these, a subset, or would you like to
edit the wording first?" Change nothing before explicit approval.

## Output

In the conversation:

| Slide | Tell | Current text | Proposed | Numbers touched |
|---|---|---|---|---|

Every row's last column must read "none". If a row says otherwise, the rewrite is wrong.

Plus: count by tell type, a list of tells deliberately left and why, and any slide where the text
reads as human already (say so; the absence of a finding is a finding).

After approval: the applied changes, slide by slide, and anything the user declined.

## Fallbacks and edge cases

- **A quotation:** never rewrite. Someone else's words, including their em dashes, stay.
- **A legal, regulatory or safety line:** never rewrite. Flag it and say it needs its owner.
- **A deck in another language:** apply the structural tells (openers, triples, hedge stacks,
  rhythm) and skip the English vocabulary list, saying you did.
- **Technical terms that look inflated:** "leverage" as a finance term is not a tell. Judge by the
  domain, not the word.
- **Nothing found:** say so plainly. A clean deck is a valid result and inventing three weak
  findings to look useful is the failure mode here.
- **The user's own voice sample contradicts a tell:** their voice wins. Say which tell you
  skipped and why.

## Rules

- Never change a number, name, date, product or claim. Copy them through.
- Never change meaning. A rewrite that says something different is a rejected rewrite.
- Never rewrite inside a quotation, or a legal, regulatory or safety line.
- Work from `references/tells.md`. Do not add tells from personal taste mid-run.
- Propose, do not apply. Nothing changes before approval.
- Report tells left in place as well as tells fixed.

## Self-check

- [ ] Every row's "Numbers touched" column reads "none".
- [ ] No quotation, legal or safety line was rewritten.
- [ ] Every proposed rewrite means the same as the original.
- [ ] Every tell named maps to an entry in `references/tells.md`.
- [ ] Load-bearing tells are listed as deliberately left.
- [ ] Nothing was applied before approval.
