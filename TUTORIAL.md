# Build a deck from pasted content, start to finish

One worked session. Blank deck, a pile of raw content, and four skills in order. About twenty
minutes, most of it spent reading what the skills propose rather than typing.

This is the workflow a user described to us, and it is a better starting point than the
skill-by-skill reference because it shows the part that is hard to guess: **what order to run
things in, and what to do with each checkpoint.**

Install first if you have not: [Try one in 60 seconds](README.md#try-one-in-60-seconds).

---

## The short version

```
Blank deck
  @outline-first-deck         paste content, approve the outline
  @native-diagram-slide       approve a layout per slide, it draws
  @ai-writing-tells-check     approve the rewrites
  @deck-message-review        read the report, fix what it names
```

Four skills, four approval points, and you never hand over the decision.

---

## Step 1: start from a blank deck and paste

Open a blank presentation. Apply your template now if you have one, because every skill here
inherits the deck's theme and a blank deck has nothing to inherit.

In the Copilot pane:

```
@outline-first-deck Draft a deck from this. Audience is the steering committee,
15 minutes, they need to approve the budget.

[paste your notes, the email thread, the meeting transcript, whatever you have]
```

It comes back with an outline and stops. **Read the outline, not the slides.** This is the
cheapest moment in the whole process to change your mind: reordering a line costs nothing and
reordering ten built slides costs ten minutes.

Approve, and it builds.

> **Skipping this step:** if you already have the deck, go straight to step 2.

## Step 2: turn the walls of text into diagrams

This is the step most people do not know is available, and it is the one that changes how the
deck looks.

```
@native-diagram-slide Look at slides 3, 5 and 8 and draw what they describe.
```

Or, from a standing start, the way the user we learned this from does it:

```
@native-diagram-slide Create me a deck that uses this information

[paste the content]
```

It reads the content, finds each distinct structure in it, and **proposes a layout per slide with
the reason**: a process flow here because order matters, a 2x2 there because the content
classifies things on two named dimensions, a timeline for the dated part. Ten layouts are
available and you can overrule any choice by name.

**At the checkpoint you get a table per slide** listing every element and every relationship, and
which of them the source actually stated. Read the "Direction stated?" column: an arrow it cannot
justify is drawn as a plain line rather than guessed, and that is usually where you find out your
own notes were vague.

Approve, and it draws with **native shapes and connectors in your theme colours**, grouped so you
can nudge them afterwards. Not a picture, and not SmartArt: both of those resist editing, which
defeats the point.

> **If your deck has no template**, it will say so and use the default theme. Apply your template
> and ask it to restyle.

## Step 3: take the AI tone out

Run this **after** the content is settled. Rewriting prose that is about to be cut wastes your
attention.

```
@ai-writing-tells-check Check the whole deck before it goes out.
```

It works from a published list of tells: filler openers, inflated verbs, groups of three, em
dashes, hedge stacks, and the one most people cannot see on a single slide, every sentence being
the same length. For each it proposes a plain replacement.

**Check the last column of its table. Every row must read "Numbers touched: none".** A rewrite
that moves a figure is a rejected rewrite, and the skill is built so you can verify that at a
glance rather than trusting it.

It will also tell you when a deck reads fine already. That is a real result, not a failure to find
anything.

## Step 4: find out whether it lands

```
@deck-message-review Does this deck land? The ask is sign-off on the budget.
```

This one changes nothing. It reads the whole deck and reports the message the slides **actually**
make, which is often not the one you intended, then classifies every slide as carrying,
supporting, context or off-message.

The finding worth waiting for is the ask. If the report says **"the ask: none found"**, you have
just avoided the most common reason a meeting ends without a decision.

Then loop back: `@action-title-rewrite` if the titles do not carry the storyline,
`@deck-trim-proposal` if slides are off-message and the slot is tight.

---

## Moving a skill you already have in Cowork

If you built a skill in Cowork and want it in PowerPoint, the file mostly transfers and the
instructions mostly do not. See
[runtimes/cowork-to-powerpoint.md](runtimes/cowork-to-powerpoint.md) for what changes and why.

The short version: Cowork skills tend to assume they can go and fetch things, and an in-app skill
works on what is open in front of it. Rewriting for that is usually the whole job.

---

## What this does not do for you

- **It does not decide anything.** Every skill stops before it changes the deck, by design.
- **It does not check your facts.** `numbers-and-claims-check` flags unsourced figures; it cannot
  tell you a sourced figure is wrong.
- **It does not know your audience.** Tell it, every time. "Steering committee, 15 minutes, budget
  sign-off" produces a different deck from "internal update".

## If something does not work

Skills are new and the surfaces differ. [STATUS.md](STATUS.md) records what has actually been run
by a named person, and "Not tested" is the honest default rather than a defect. If a skill
misbehaves, or works,
[report it](https://github.com/kesslernity/awesome-copilot-office-skills/issues/new?template=tenant-behaviour-report.md).
A confirmed working result is as useful as a bug.
