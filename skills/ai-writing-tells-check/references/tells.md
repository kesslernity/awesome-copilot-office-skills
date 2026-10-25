# The tells

The list `ai-writing-tells-check` works from. Each entry gives what to look for, why a reader
notices, and what to do instead. Order is roughly how visible each one is to a reader who is not
looking for it.

A tell is a **signal, not a verdict**. Every one of these appears in good human writing. What marks
text as machine-drafted is several of them together, at an even density, across every slide.

---

## 1. Filler openers

Sentences that clear the throat before saying anything.

> "It is important to note that", "It is worth mentioning", "In today's fast-paced world",
> "As we navigate", "When it comes to", "At the end of the day", "Let's dive in"

**Why it shows:** the first four words carry no information, and a reader skimming a slide reads
exactly those four words.

**Instead:** delete the opener and start at the subject. "It is important to note that margins
fell" becomes "Margins fell".

## 2. Inflated verbs and nouns

A plain word swapped for a longer one.

> delve, leverage, utilise, facilitate, spearhead, harness, unlock, empower, elevate, foster,
> streamline, robust, seamless, holistic, synergy, paradigm, landscape, realm, tapestry, journey,
> game-changer, best-in-class, cutting-edge, state-of-the-art

**Why it shows:** these cluster. One is nothing; three on a slide is a signature.

**Instead:** the plain verb. Use, not utilise. Help, not facilitate. Start, not spearhead.

**Exception:** domain terms. "Leverage" in a finance deck means debt. Judge by the domain.

## 3. The group of three

Three items where the content supports one or two, often three adjectives in a row.

> "fast, reliable and scalable", "people, process and technology", "clear, concise and compelling"

**Why it shows:** the rhythm is satisfying and the third item is usually filler, so the sentence
reads confident and says less than it appears to.

**Instead:** keep the items the source supports. Two real things beat three with one invented.

**Exception:** a genuine list of three things. Three named workstreams are a list, not a tell.

## 4. Em dashes

> "The result was clear — margins fell."

**Why it shows:** the em dash is the default connector in machine-drafted prose, and most business
writers reach for a comma, a colon or a full stop. A deck with em dashes on five slides reads
machine-written even when every fact is right.

**Instead:** a comma for an aside, a colon before an explanation, a full stop for two thoughts.

**Exception:** inside a quotation. Someone else's punctuation stays.

## 5. Hedge stacks

Two or more hedges in one clause.

> "may potentially", "could possibly", "might arguably suggest", "it seems likely that perhaps"

**Why it shows:** one hedge is honest caution. Two is the writing avoiding commitment, and on a
decision slide it reads as nobody being willing to say what they think.

**Instead:** one hedge, or a stated confidence. "May fall" or "likely to fall, on the Q3 run rate".

## 6. Symmetrical rhythm

Every sentence roughly the same length, every bullet the same shape, every slide the same count.

**Why it shows:** human writing is uneven. Perfect evenness across a whole deck is the strongest
structural tell and the hardest to spot on one slide, which is why this runs deck-wide.

**Instead:** vary deliberately. A three-word sentence after a long one. Four bullets on one slide
and two on the next.

## 7. The restated conclusion

A closing sentence that repeats the slide's title or first line in different words.

> Title: "Margins fell in Q3." Final bullet: "In summary, Q3 saw a decline in margins."

**Why it shows:** it pads to a shape rather than ending when the point is made.

**Instead:** delete it, or replace it with the consequence: what should happen now.

## 8. Vague intensifiers

> very, really, quite, significantly, substantially, dramatically, considerably

Used without a figure anywhere on the slide.

**Why it shows:** "significantly" with no number is a feeling. A reader who wants the number
notices the absence immediately.

**Instead:** the number if the deck has it. If it does not, cut the intensifier: "margins fell"
is stronger than "margins fell significantly" with nothing behind it.

## 9. Abstract subjects

Sentences whose subject is a concept rather than an actor.

> "The implementation of the framework enables improved outcomes."

**Why it shows:** nobody does anything, so nobody is accountable, which is the opposite of what a
business slide is for.

**Instead:** name the actor. "The finance team will use the framework to close two days faster."

## 10. Negative parallelism

> "It's not about cost, it's about value." "This isn't a tool, it's a platform."

**Why it shows:** a template that sounds profound and asserts a contrast the content has not
earned.

**Instead:** state the positive claim and support it.

---

## Not tells

Do not flag these. Flagging them trains the user to ignore the whole report.

- **Long sentences.** Length is not a tell; uniformity is.
- **Passive voice.** Often correct, especially where the actor is unknown or irrelevant.
- **Technical jargon the audience shares.** Precision, not padding.
- **Repetition of a key term.** Decks should use one word for one thing, which is what
  `deck-consistency-sweep` enforces.
- **A bulleted list.** It is a slide.
