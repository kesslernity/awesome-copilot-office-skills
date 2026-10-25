---
name: deck-message-review
description: "Reads a whole deck and reports whether it carries one message, whether the slides support it in order, and whether it ends with a clear ask. Names the message the deck actually makes, which is often not the one the author intended, and lists every slide that does not serve it. Reports only; changes nothing. Use when the user asks whether a deck lands, hangs together, has a storyline, makes its point, or is ready to present."
---

# Deck message review

## Purpose

A deck can have strong slides and no argument. Each slide is defensible, the order is roughly
chronological, and the audience leaves without knowing what was being asked of them.

This reads the deck as one piece and answers three questions: what is the message, do the slides
build it, and what is the ask. It reports; it rewrites nothing.

## When to use

- The user asks whether a deck lands, hangs together, tells a story, makes its point, flows, or is
  ready to present.
- Before a deck goes to a board, a steering committee, a client or an executive.
- Run it **before** `action-title-rewrite`. The titles should serve the storyline, so settle the
  storyline first.
- Do not use to check facts: that is `numbers-and-claims-check`.
- Do not use to shorten: that is `deck-trim-proposal`.

## Inputs

1. The deck (required). If nothing is open or attached, ask for it.
2. The intended message (optional): one sentence of what the author wants the audience to
   conclude. **Ask for it if not given, but do not require it:** the comparison between intended
   and delivered is the most useful output, and when it is absent the delivered message alone is
   still worth having.
3. Audience and decision (optional): who sees it and what they must decide.
4. Slot (optional): how long the author has.

## Procedure

1. Read every slide including speaker notes. Write each slide's claim in one line, in the deck's
   own words. A slide whose claim you cannot state in one line is itself a finding.
2. **Derive the delivered message** from the claims alone, before looking at any intended message
   the user supplied. Write it as one sentence a listener could repeat.
3. If the user supplied an intended message, compare. State plainly whether they match, partly
   match, or differ, and if they differ, which slides pull toward each.
4. Test the order. For each slide, ask what the audience must already accept for it to land. Flag
   any slide that depends on something established later.
5. Classify every slide: **CARRIES** the message, **SUPPORTS** it, **CONTEXT** that could be cut
   or appended, or **OFF-MESSAGE**. Give one reason each.
6. Find the ask. The ask is a named thing a named person is expected to do or decide. Record the
   slide it is on and its wording. **If there is no ask, say so as the headline finding**, because
   a deck with no ask is the single most common reason a meeting ends without a decision.
7. Check the ask is supported: every claim it rests on should appear earlier in the deck. List any
   that does not.
8. Check the opening. State whether the first two slides tell the audience what this is about and
   what is wanted, or whether they are agenda and background.
9. Identify the weakest link: the one slide whose removal or failure would break the argument.
10. Report. Change nothing.

## Human approval checkpoint

None. This skill only reports, so there is nothing to approve. Offer next steps at the end:
`action-title-rewrite` to make the titles carry the storyline, `executive-summary-slide` to state
the message up front, `deck-trim-proposal` if slides are OFF-MESSAGE.

## Output

In the conversation:

**Delivered message:** one sentence, derived from the slides.
**Intended message:** as supplied, or "not supplied".
**Match:** yes, partly or no, with the slides that pull each way.

| Slide | Claim in one line | Role | Note |
|---|---|---|---|

Role is CARRIES, SUPPORTS, CONTEXT or OFF-MESSAGE.

**The ask:** the wording, the slide, the named owner, or "none found".
**Unsupported claims behind the ask:** list, or none.
**Order problems:** slides that depend on something established later.
**Opening:** what the first two slides actually do.
**Weakest link:** the slide the argument cannot lose.

## Fallbacks and edge cases

- **No single message:** say the deck carries two or three and name them. Do not pick one and call
  it the message. Offer to split the deck.
- **Pure status or information deck with no ask:** say an ask is not expected here, and check
  instead that the audience knows what needs no action and what does.
- **An ask with no named owner:** flag it. "The business should decide" is not an owner.
- **Fewer than five slides:** run the same checks and say the sample is small.
- **An appendix:** exclude it from the storyline and say that you did. Flag any load-bearing
  claim that lives only in the appendix.
- **Speaker notes carry the argument and the slides do not:** say so. It is a finding about the
  deck's ability to travel without its presenter.

## Rules

- Derive the delivered message from the slides before reading any intended message.
- Quote the deck's own wording for each claim; do not improve it while summarising.
- Never rewrite, reorder, add or delete a slide. This skill reports.
- Never invent an ask. If there is none, that is the finding.
- Judge a slide against the message, not against taste. OFF-MESSAGE is not the same as bad.

## Self-check

- [ ] Delivered message written before the intended one was read.
- [ ] Every slide classified with a reason.
- [ ] The ask quoted with its slide and owner, or reported as absent.
- [ ] Order problems named with the slide they depend on.
- [ ] Weakest link identified.
- [ ] Nothing in the deck was changed.
