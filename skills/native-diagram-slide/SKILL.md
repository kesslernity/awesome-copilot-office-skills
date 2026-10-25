---
name: native-diagram-slide
description: "Turns pasted content into diagram slides built from native PowerPoint shapes and connectors, in the deck's own theme. Offers a menu of ten layouts (process, timeline, cycle, hierarchy, matrix, funnel, hub and spoke, layered stack, comparison, grouped boxes), proposes one per slide, waits for approval, then draws editable shapes, never a picture and never SmartArt. Use when the user asks for a diagram, process flow, timeline, roadmap, cycle, org chart, 2x2, funnel, architecture or 'make this visual', or builds a deck from pasted content."
---

# Native diagram slide

## Purpose

Decks explain structures in paragraphs because drawing them by hand takes twenty minutes a slide.
This draws them: labelled shapes and connectors, on a grid, in the deck's own colours and fonts,
and **editable afterwards** because they are real shapes rather than a flat image.

One skill covers ten layouts on purpose. You should not have to know whether your content is a
"process" or a "cycle" before you paste it: say what you have, and the skill proposes the layout
and explains why.

## When to use

- The user asks for a diagram, process flow, workflow, swimlane, timeline, roadmap, milestone
  chart, cycle, loop, org chart, hierarchy, 2x2, matrix, funnel, pipeline, architecture, concept
  map, comparison or "make this look visual".
- The user pastes content into a blank or partial deck and asks for slides built from it.
- Do not use to make an existing picture prettier. This builds shapes; it cannot edit an image.
- Do not use for quantities that need a scale. A diagram that implies a size it cannot support is
  a chart that should have been a chart.

## The layout menu

| # | Layout | Use when the content is | Ceiling |
|---|---|---|---|
| 1 | Process flow | a sequence where order matters, optionally with actors in swimlanes | 9 steps |
| 2 | Timeline | milestones at stated points in time | 10 milestones |
| 3 | Cycle | a sequence that returns to its start | 7 stages |
| 4 | Hierarchy | a parent and child structure, org or decomposition | 4 levels, 15 nodes |
| 5 | Matrix (2x2) | items classified on two named dimensions | 2 axes, 12 items |
| 6 | Funnel | stages that narrow, each a subset of the one above | 6 stages |
| 7 | Hub and spoke | several things all relating to one centre | 1 hub, 8 spokes |
| 8 | Layered stack | things sitting in named tiers, one on another | 6 layers |
| 9 | Comparison | two or three options against the same criteria | 3 columns, 7 rows |
| 10 | Grouped boxes | things in named groups with few cross-links | 12 nodes |

Per-layout construction rules, including every ceiling above, are in
[references/layouts.md](references/layouts.md). Read the entry for the layout you choose before
drawing.

## Inputs

1. The content (required): pasted text, a list, a slide in the open deck, or an attached
   document. If none is supplied, ask what the diagram should show.
2. Layout (optional): a number or name from the menu. Default: proposed from the content's shape,
   and always stated with the reason so the user can overrule it.
3. Placement (optional): a new slide, or replacing an existing slide's body. Default: a new slide
   after the content it came from.
4. Slide count (optional), when building several slides from one paste. Default: one diagram per
   distinct structure found, each proposed separately.

## Procedure

1. Read the content and identify each distinct structure in it. One paste often contains several:
   a sequence, then a comparison, then a schedule. Each becomes its own slide.
2. For each structure, pick a layout by the shape of the content, not by taste:
   - ordered, and order matters: process flow
   - ordered, and it returns to the start: cycle
   - anchored to dates: timeline
   - parent and child: hierarchy
   - classified on two named dimensions: matrix
   - stages that narrow: funnel
   - everything meets at one centre: hub and spoke
   - named tiers: layered stack
   - options against shared criteria: comparison
   - otherwise: grouped boxes
3. Extract the elements. Each label is a noun or verb phrase, six words or fewer, **in the user's
   wording**. Keep their terms.
4. Extract the relationships: source, target, and a verb of three words or fewer. **A relationship
   with no verb in the source is drawn as a plain line, never an arrow.** An arrowhead asserts a
   direction the content did not state.
5. Check the ceiling for the layout in `references/layouts.md`. Over it, propose a split or a
   grouping. **Never shrink the type to fit.**
6. Lay out on a grid: equal widths within a row, equal gutters, nothing overlapping, nothing
   within one gutter of the slide edge, no connector crossing another if a reorder avoids it. Do
   not rotate text beyond 45 degrees, and prefer shortening the label.
7. Take every colour and font from the deck's theme. At most three theme colours per slide. Never
   introduce a colour or font the deck does not have.
8. If colour carries meaning, carry it a second way too, with a label or a position, and state it
   in a legend. Colour alone fails for a colour-blind reader and in a greyscale handout.
9. Draft the structure as text (see Output) and **stop for approval**.
10. After approval, draw with **native shapes and connectors**: rectangles, diamonds, ellipses,
    lines. Group each cluster so it moves as one. Never insert a picture of a diagram, and never
    use SmartArt: both resist editing, which is the whole point of drawing it here.
11. Put the element list, the relationship list and the source of each into the speaker notes.

## Human approval checkpoint

For each proposed slide, show the layout and why it was chosen, the element table, the
relationship table, anything dropped, and anything you could not place. Ask: "Shall I draw these,
change a layout, or fix the content first?" Draw only after explicit approval.

When building several slides from one paste, show **all** proposed slides before drawing any, so
the user approves the deck's shape rather than one slide at a time.

## Output

In the conversation, before drawing, per slide:

**Slide 3, proposed layout: funnel**, because the five stages each describe a subset of the one
above.

| # | Element | Group or stage | In the source? |
|---|---|---|---|

| From | Verb | To | Direction stated? |
|---|---|---|---|

Plus: proposed slide title, anything dropped and why, open questions.

In the presentation, after approval: native shapes in the deck's theme, grouped, with the element
and relationship lists in the speaker notes.

If you cannot draw shapes in this surface, return the layout as a text diagram plus a shape list
with positions, and **say plainly that you could not draw it**. Never return a bulleted list and
call it a diagram.

## Fallbacks and edge cases

- **Too few elements for the layout** (see each ceiling's floor in references): say a diagram adds
  nothing here and offer a sentence instead.
- **Over the ceiling:** propose a split or a collapse into named groups, with the detail in the
  speaker notes.
- **A relationship the source does not state:** leave it out and list it as an open question.
  Do not connect two boxes because they look like they belong together.
- **Content that is really a table:** say so. A comparison of eight options on nine criteria is a
  table, and forcing it into shapes makes it less readable.
- **No theme to inherit**, such as a blank deck: use the deck's default theme fonts and say that
  you did, then offer to restyle once a template is applied.
- **Mixed structures in one paste:** never merge them into one diagram. Propose one slide each.
- **The content contains dates:** prefer timeline, and apply the date-confidence rules in
  references, which are stricter than the other layouts'.

## Rules

- Every element and relationship comes from the source or the user. Invent neither.
- An arrowhead means a stated direction. A plain line means it was not stated.
- Native shapes only. Never a picture, never SmartArt.
- Only the deck's own fonts and colours, three colours at most.
- Readability beats completeness: drop an element and say so rather than shrink the type.
- Never draw before approval, and never edit a slide you were not asked to touch.

## Self-check

- [ ] Layout chosen from the menu, with the reason stated.
- [ ] Within the layout's ceiling.
- [ ] Every label six words or fewer, in the user's wording.
- [ ] Every arrowhead corresponds to a stated direction.
- [ ] Only theme colours and fonts, three at most.
- [ ] Any meaning carried by colour is carried a second way as well.
- [ ] Nothing overlaps; no avoidable crossing connectors.
- [ ] Shapes are native and grouped, not a picture and not SmartArt.
- [ ] Nothing was drawn before approval.
