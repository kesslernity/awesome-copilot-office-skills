# Moving a skill from Cowork to Copilot in PowerPoint

The `SKILL.md` format is the same, so the file usually transfers unchanged. The **instructions**
usually do not, and that is the whole job.

Written from the structural differences between the two surfaces. The specifics of what you have
to change depend on what your skill does, so the useful thing here is the list of questions to ask
of your own file rather than a recipe.

---

## The one difference everything else follows from

**A Cowork skill goes and gets things. An in-app skill works on what is open in front of it.**

Cowork skills are written for an agent that can reach across your content: find the file, open the
thread, pull the data, then produce something. A skill running in the Copilot pane in PowerPoint
is working on **this deck**, now, with whatever the user attached.

Almost every change below is a consequence of that.

## Six things to check in your file

### 1. Where the input comes from

Cowork phrasing like "find the latest version of the deck" or "pull the figures from the finance
folder" has nothing to act on in PowerPoint.

**Change it to:** the open presentation, or an attached file, and **ask when neither is there**.
Every skill in this repo opens its Inputs section the same way: "The deck (required). If nothing
is open or attached, ask for it."

### 2. What it is allowed to change

Cowork produces an artefact. An in-app skill edits the thing the user is looking at, and that is a
much bigger deal: there is no draft copy, and undo is the only safety net.

**Change it to:** draft in the conversation, stop at an explicit approval checkpoint, then change
only what was approved. Every skill here carries a `## Human approval checkpoint` section for
exactly this reason, and it is the convention worth keeping even if your Cowork original did not
have one.

### 3. Output that assumed a document

If the skill ended by writing a report, a summary file or a document, that output has nowhere to
go in the PowerPoint pane.

**Change it to:** a table in the conversation plus, where it belongs on the slide, the speaker
notes. Speaker notes are the natural home for traceability: which slide a point came from, which
source a figure came from, what the skill could not place.

### 4. Anything that assumed it could run code or fetch a URL

In-app custom skills are instructions and text references. No scripts, no network calls.

**Change it to:** instructions that work from what is in the deck. If your skill genuinely needed
to fetch something, it cannot move, and that is a real answer rather than a problem to work
around.

### 5. Theme and formatting

A Cowork skill often specifies colours and fonts because it is generating something from nothing.
In PowerPoint that produces a slide that does not match the deck.

**Change it to:** inherit. "Take every colour and font from the deck's theme. Never introduce a
colour the deck does not have." If the deck is blank and has no theme, say so rather than picking.

### 6. Length and scope

Cowork skills can be long-running. An in-app skill shares a pane with a conversation, and a skill
that produces forty rows of proposals before its first checkpoint is one nobody reads.

**Change it to:** a ceiling, and a proposal when you hit it. The diagram skill in this repo caps
each layout and proposes a split rather than shrinking the type, which is the same instinct.

## What usually transfers unchanged

- The YAML front matter, though the `description` is worth rewriting: in PowerPoint it is what
  makes Copilot pick your skill, so it should name the triggers a user would actually type.
- The domain knowledge. The part of your skill that knows what a good diagram, a good summary or a
  good check looks like is the valuable part and it is surface-independent.
- `references/` files. They are just text.

## Then test it

Install it as a personal skill ([PowerPoint install](../README.md#powerpoint-personal-skill-no-admin)),
run it on a real deck, and watch for the two failures that always show up first: it tries to act
before asking, or it produces output with nowhere to go.

**If you move one, please tell us what you had to change.**
[Open an issue](https://github.com/kesslernity/awesome-copilot-office-skills/issues/new?template=tenant-behaviour-report.md).
This page is written from structure rather than from a pile of real migrations, and real ones
would make it much better.

## On credits

The common reason people ask about this move is cost. What Microsoft documents, and what it does
not, is set out in [Does running a skill here spend Copilot Credits?](../README.md#does-running-a-skill-here-spend-copilot-credits)
Short version: Cowork is billed in credits, the skills pages say nothing about credits either way,
and we are not going to tell you the move saves money when no published page says so.
