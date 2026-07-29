# Building Your Own Corpus

The starter corpus is 18 authored items. That is enough to introduce the
distinctions and nowhere near enough to proceduralize them. Generated items keep
the supply going but share the generator's blind spots — an AI producing practice
material for a defect it does not reliably detect will quietly under-represent it.

Authentic prose has neither problem. This file makes collecting it a protocol
rather than an intention.

**Target: 20–30 annotated paragraphs.** At two or three a week that is a couple of
months, which is fine — this corpus is a byproduct of reading you are doing
anyway, not a separate project.

---

## The selection criterion

**Save a paragraph only if it resolved a real confusion.** Not because it is
well-written — most published prose is adequately written and teaches nothing.

Concretely, one of:

- It made something clear that you expected to find hard, and you want to know how
- You initially read it as defective and were wrong. **These are the most valuable
  items you will ever collect**, because they mark the exact boundary your model
  currently gets wrong
- It does something your own writing never does
- It is genuinely defective, published, by a competent writer — proof the defect
  is real and not a rule you invented
- It uses a progression pattern you under-use. Check your log: if your Mode E
  paragraphs are all constant-topic, go find derived and split ones

If you cannot name which confusion it resolved, don't save it. A corpus of
paragraphs you merely admired is a scrapbook.

---

## Sourcing against your own gaps

Once the log has a few sessions in it, source *against the recurring defect codes*
rather than reading at random.

| Recurring code | Go find |
|---|---|
| D1, D5 | Long technical explanations tracking several entities at once — postmortems with multiple systems involved |
| D3, D7 | Argumentative prose: legal writing, policy analysis, critical reviews. Relation-marking is the whole game there |
| D4 | Journalism. Professional editors are relentless about what lands at the end of a sentence |
| D2, D6 | Writing for readers outside the author's field — good popular science, onboarding docs |
| D8 | Anything where the reasoning is contested, so the gaps are visible |

---

## The annotation template

One file per paragraph in this directory, named `NN-short-slug.md`.

```markdown
# NN — <short description>

**Source:** <publication, author, URL, date accessed>
**Genre:** <postmortem / docs / essay / journalism / mailing list / …>
**Why saved:** <the confusion it resolved — one sentence, required>

## The paragraph

> <verbatim, one paragraph, no more>

## Reconstructed input

These are inferences, not facts. The published paragraph is an observed output
whose input is hidden — write down what you think it was before analyzing.

- **Purpose:**
- **Reader:**
- **What the reader already knew:**
- **What the reader had to be able to do afterwards:**

## Analysis

| # | Role | Departure point | Link | New contribution | Relation | Pattern |
|---|---|---|---|---|---|---|

## What I'd have done instead

<Your default version of the same content — one or two sentences is enough.
The delta between this and the original is the actual lesson.>

## Boundary note

<If this is a legitimate override — contrastive opening, instruction-first,
conclusion-first — say which, and say what made it correct here.>
```

The **"What I'd have done instead"** field is the one that does the work. An
analysis of someone else's paragraph is recognition; contrasting it against your
own default is the only part that touches production.

---

## Using the corpus

- Mode A items, but with a difference: you already annotated these, so re-running
  one is **fluency**, not generality. Label it that way in the log
- Re-read your "What I'd have done instead" fields every ten sessions. If your
  defaults have changed, that is transfer, and it is better evidence than any
  score in this project
- Once you have twenty, the collection itself is a diagnostic: which patterns and
  codes are missing tells you what you have not been noticing

---

## What this corpus cannot do

Published paragraphs come without their brief. You are reconstructing the purpose
and reader, and you may reconstruct them wrongly — in which case an ordering that
was correct for the real reader looks defective to you, or vice versa.

Practical consequence: when your analysis of an authentic paragraph says the
author erred, the more likely explanation is that you have the wrong model of
their reader. Treat that verdict as a hypothesis about your own assumptions first.
