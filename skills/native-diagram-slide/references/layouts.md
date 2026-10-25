# Layout reference

Construction rules for each of the ten layouts in `native-diagram-slide`. Read the entry for the
layout you have chosen before drawing. The shared rules in `SKILL.md` apply to all ten: native
shapes, theme colours only, approval before drawing, never invent an element.

Each entry gives a floor and a ceiling. Below the floor, say a diagram adds nothing. Above the
ceiling, propose a split or a grouping, never a smaller type size.

---

## 1. Process flow

**Floor 4 steps. Ceiling 9 steps**, or 7 if swimlanes are used.

- Each step is a verb phrase, five words or fewer, numbered in order.
- **Never assign an actor the source does not name.** A step with no stated actor goes in an
  "unassigned" lane and is listed as an open question. A wrongly assigned step on a slide
  reassigns work in the room, and nobody re-reads a picture to check it.
- A decision is a question with two or more named outcomes, drawn as a diamond. If the source
  gives the question but not the outcomes, keep the question and list the outcomes as open.
- A handoff is any step whose actor differs from the previous step's. Label what passes across it
  if the source says so; leave it blank if not.
- Rectangles for steps, diamonds for decisions, rounded ends for start and stop.
- Flow runs one direction. A loop or rework path is a labelled return arrow **underneath** the
  main flow, never a line crossing through it.
- Swimlanes are full-width rows, actor named on the left, bands in a single tint rather than six
  colours.
- If there is no decision and no handoff, it is a list. Say so and offer a numbered list.

## 2. Timeline

**Floor 3 milestones. Ceiling 10.** The strictest layout, because people plan against it.

- **Classify every date CONFIRMED, TARGET or UNDATED**, from the source. Wording like "around",
  "mid", "by end of" or "expected" makes it a TARGET.
- **Never invent or narrow a date.** "Q2" stays a band across the quarter, never a dot on 1 May.
  An UNDATED milestone is listed under the axis as unplaced: never dropped, never guessed into
  position.
- **Equal time gets equal width.** Evenly spacing milestones for tidiness is a lie about the
  schedule and it is the most common defect in roadmap slides.
- If one gap dominates, propose a visibly marked axis break or a different unit. Never silently
  compress.
- Alternate labels above and below the axis to avoid collisions.
- CONFIRMED and TARGET must differ by **shape or fill**, not only colour: filled versus hollow or
  dashed. Put it in a legend.
- Put an **as-at date** on the slide. A timeline without one cannot be read later.
- A milestone in the past that has not happened gets marked and raised, never quietly moved.
- If every date is a target, draw it and say so in the legend: a clean axis must not imply
  confirmation the content does not have.

## 3. Cycle

**Floor 3 stages. Ceiling 7.**

- Stages are equal arcs or equal boxes around a loop. Equal size, because a cycle makes no claim
  about duration unless the source does.
- Direction must be stated in the source. If it is not, draw the ring without arrowheads and ask.
- Put the cycle's name in the centre only if the source names it. An empty centre is better than
  an invented label.
- If the sequence does not actually return to its start, it is a process flow. Switch.

## 4. Hierarchy

**Floor 3 nodes. Ceiling 4 levels and 15 nodes.**

- One parent per child. If the content has a child with two parents, it is not a hierarchy: use
  grouped boxes or a matrix and say why.
- Siblings sit at the same level with equal widths.
- Never infer a reporting line, an owner or a level the source does not state. An org chart that
  invents a reporting line is a political document.
- Collapse a branch into one node with a count ("Operations, 6 teams") and name its contents in
  the speaker notes rather than exceed the ceiling.

## 5. Matrix (2x2)

**Floor 4 items. Ceiling 12 items.**

- Both axes need a name and both ends of each axis need a label, all from the source. An unlabelled
  axis is unreadable and an invented one is worse.
- Place an item only where the source supports both of its coordinates. An item positioned on one
  known and one guessed dimension goes in a list beside the matrix instead.
- Quadrants get names only if the source names them.
- Do not imply a scale. A 2x2 is a classification, not a measurement, and the position within a
  quadrant carries no meaning unless the source gives values.

## 6. Funnel

**Floor 3 stages. Ceiling 6.**

- Each stage must be a genuine subset of the one above. If it is not, this is a process flow.
- **Width is a claim.** Only vary stage widths proportionally if the source gives quantities. With
  no numbers, use equal widths and say the shape shows sequence, not volume.
- Label the drop between stages only where the source states it.

## 7. Hub and spoke

**Floor 3 spokes. Ceiling 8.**

- The hub must be named in the source. Do not invent a centre to make the content fit.
- Spokes at equal radius and even angles.
- Only draw a spoke-to-spoke link if the source states that relationship; they clutter fast.
- If more than one node looks like a centre, it is grouped boxes or a layered stack.

## 8. Layered stack

**Floor 3 layers. Ceiling 6.**

- Layers must be named tiers in the source, drawn bottom-up unless the source orders them
  otherwise. State which way you drew it.
- Equal heights unless the source gives a reason to differ.
- Items within a layer sit side by side with equal widths.
- A stack implies each layer rests on the one below. If that is not true of the content, use
  grouped boxes.

## 9. Comparison

**Floor 2 columns. Ceiling 3 columns and 7 rows.**

- Criteria are rows, options are columns, and every cell comes from the source. A blank cell stays
  blank and is listed as an open question: a blank cell reads as "no" and that may be wrong.
- Use the same unit and wording down a row.
- Do not add a verdict row, a score or a recommendation unless the source states one. The skill
  presents the comparison; the human makes the call.
- Above 3 columns or 7 rows this is a table. Say so.

## 10. Grouped boxes

**Floor 3 nodes. Ceiling 12.**

- Groups need names from the source. An unnamed grouping is an assertion about what belongs
  together.
- Few cross-group links. If most nodes link across groups, the grouping is wrong: try hub and
  spoke or a layered stack.
- Equal box widths within a group, equal gutters between groups.
- Collapse a group into one node and name its contents in the speaker notes rather than exceed the
  ceiling.
