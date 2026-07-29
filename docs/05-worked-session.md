# A Worked Session

The project tells you to commit a prediction and annotate. It never shows one
filled in. This is that — one Mode A item and one Mode E item, start to finish.

**The format is defined in `docs/04-annotation-format.md`. Read that first.** The
AI hands you a pre-parsed sheet — subjects bracketed, clauses split, assertions
numbered. You fill `Ties back by` and `Pattern`, plus `Antecedent` where a pronoun
points back, plus the two closing lines. Everything you write is a quote off the
page or a pick off a list.

The Mode A paragraph below is a **throwaway**, deliberately not from the corpus.
Practise the mechanics on scrap — corpus items are non-renewable as fresh
measurements, and burning one on a demonstration costs you a score later.

---

## Mode A, worked

### Step 1 — read once, commit a prediction

> The village hall committee spent two years raising money for a new roof. When
> the grant finally came through, it covered rather more than the roof needed, and
> the surplus went on rewiring the kitchen. That turned out to matter more than
> anyone expected. The hall had been losing its Saturday bookings to a newer venue
> eight miles away, and the thing people cited was never the roof.

**Prediction, written before analyzing:**

> Mostly linear, with a pivot at sentence 3. Expect it to be clean. Watch `That` in
> sentence 3 — possible D1.

One line. Thirty seconds. Committed before anything else, because a prediction you
form *while* analyzing is not a prediction.

**It is then locked.** If the verdict changes while you work, write the revision
underneath — never over the top. An edited prediction cannot be scored, and the
prediction hit rate is the only Mode A measure that familiarity with the corpus
cannot inflate.

### Step 2 — annotate the sheet

The AI supplies the bracketed lines. Everything after them is mine.

```
SENTENCE 1  [subject: "The village hall committee" | nothing precedes | 2 assertions]
   a. spent two years raising money
   b. the money was for a new roof

Ties back by:  nothing - this is the opening
Pattern:       opening


SENTENCE 2  [subject: "it" (= the grant) | preceded by "When the grant finally
             came through," | 2 assertions]
   a. the grant exceeded what the roof needed
   b. the surplus went on rewiring the kitchen

Ties back by:  "the grant" - points back to "raising money"
               "the roof" - repeated verbatim
Pattern:       2 linear


SENTENCE 3  [subject: "That" | nothing precedes | 1 assertion]
   a. it mattered more than anyone expected

Ties back by:  "That" - demonstrative, present and resolving, but only just
Antecedent:    2b, the rewiring - wins on recency over 2a
Pattern:       2 linear


SENTENCE 4  [subject: "The hall" | nothing precedes | 3 assertions]
   a. the hall had been losing its Saturday bookings
   b. the rival venue is eight miles away
   c. the reason people gave was never the roof

Ties back by:  "The hall" - superordinate covering the committee, the roof and
               the kitchen, all already established
Pattern:       3 derived topics


Alternative reading:  sentence 3's "That" can point at 2b, the rewiring, or at
                      the whole fact that the grant overshot. The rewiring wins
                      on recency and salience, so it resolves - but it is a
                      near-miss for D1, not a clean case. What would settle it:
                      how forgiving this reader is.
Uncertainty:          sentence 4 assumes a reader who accepts that a village hall
                      competes for bookings at all. That is a reader model I am
                      inferring, not reading.
```

**Notice sentence 2's bracket.** The temporal clause and the grammatical subject
are recorded separately, because they are different things and the difference is
frequently where a defect lives. Sentence 2 is fine here — but you cannot know
that without the split, which is why the AI supplies it every time.

**Notice sentence 3's `Antecedent` line.** It fires because the subject is a
demonstrative. Nowhere else in this paragraph does it appear. It is not a field
you fill four times; it is a field that switches on when something points back.

### Step 3 — contest the AI's reading, before either of you opens the key

The AI annotates now, and hands its version over **without the key**. This step
exists so that a disagreement is possible at all — if the answer arrives in the
same message as the analysis, there is nothing to argue with.

Suppose it marks sentence 4 as an unmotivated topic shift (D2), because the
departure point moves from the rewiring to the hall's bookings.

**Do not accept this.** The correct response:

> `The hall` is a superordinate for everything already discussed — the committee,
> the roof, the kitchen are all parts of it. Derived topics, not a shift. And
> sentence 4 explains sentence 3's claim, which is the relation that licenses it.

You do not need expertise to run this step. **The move that is always available is
to make the AI point at the span.** Ask which words carry the defect. A judgment
that cannot be attached to specific words on the page is a judgment you should not
accept, and you can apply that test on session one.

Only after this exchange does the key come out.

### Step 4 — score

| Measure | Result |
|---|---|
| Pattern agreement | 3/3 transitions |
| Defended disagreements | 1 (sentence 4) |
| Prediction hit | **Partial** — right about linear-with-pivot, right to watch `That`, but I predicted "clean" and it is borderline |

**Prediction gap:** I expected demonstratives to be either fine or broken. This one
is neither — it is recoverable but costs the reader a beat.

**Rule update:** D1 is not binary. There is a middle band where a reference
resolves on second pass, and whether that counts as a defect depends on the reader
and the stakes. Add "recoverable but expensive" as a thing to notice.

That rule update is worth more than the 3/3.

---

## Mode E, worked

### The brief

> A colleague asks why the staging environment was down all Tuesday afternoon.
> The cause: someone ran a database restore against it to test a runbook, which is
> a legitimate use, but nobody announced it. **Reader:** a peer, mildly annoyed,
> not on your team. **Needs to be able to:** know whether to plan around this
> happening again.

### Draft, written cold, timed — 6 minutes

> Staging was down on Tuesday afternoon because someone was running a database
> restore against it. This was to test a runbook, which is a legitimate use of
> staging. The problem was that it wasn't announced anywhere. We're going to add a
> heads-up to the team channel for anything that takes staging down, so you should
> get warning next time.

### Self-annotation, before any AI sees it

Same sheet. On your own draft you parse it yourself, because splitting your own
sentences is part of seeing what you wrote.

```
SENTENCE 1  [subject: "Staging" | nothing precedes | 2 assertions]
   a. staging was down Tuesday afternoon
   b. the cause was a database restore

Ties back by:  "Staging" - the thing they asked about. No explicit word links to
               prior text because the prior text is their question
Pattern:       opening


SENTENCE 2  [subject: "This" | nothing precedes | 2 assertions]
   a. the restore was to test a runbook
   b. that is a legitimate use of staging

Ties back by:  "This" - demonstrative, present and resolving
Antecedent:    1b, the restore
Pattern:       2 linear


SENTENCE 3  [subject: "The problem" | nothing precedes | 1 assertion]
   a. the restore was not announced anywhere

Ties back by:  no explicit word, reader infers it - "the problem" reframes what
               has just been described
Pattern:       2 linear


SENTENCE 4  [subject: "We" | nothing precedes | 3 assertions]
   a. a heads-up goes in the team channel
   b. it covers anything that takes staging down
   c. you will have warning next time

Ties back by:  no explicit word, reader infers it - "we" are the team behind the
               unannounced restore
Pattern:       6 question-answer - it answers the reader's live question,
               "do I have to plan around this again?"


Alternative reading:  sentence 4 could be read as 3 derived topics, with "we" as
                      part of the staging-owners frame. Question-answer wins
                      because the brief says the reader needs to know whether to
                      plan around it, so that question is genuinely live.
Uncertainty:          I am assuming this reader knows who "we" refers to. They
                      are on another team.
```

**Sentence 4 shows a mistake worth naming.** An earlier version of this document
put `Consequence` in the pattern field. That is a **relation**, not a pattern. A
sentence can stand in a causal relation to the one before while departing from a
completely different point — and only the pattern field records the second. If a
relation word ends up in the pattern field, the two have been collapsed.

**What I caught myself:**

- Sentence 2 `This was to test a runbook` — weak. `This` again, and `was to test`
  puts nothing in the stress position. **D4.**
- Sentence 3 `The problem was that it wasn't announced` — six words of
  throat-clearing before the content. The problem *is* the announcement gap; say
  it. **D4.**
- The reader `needs to know whether to plan around this happening again`. My last
  clause gestures at it (`you should get warning next time`) but hedges with
  `should`. Rubric item 6 fails.

### Revision — mine, not the AI's

> Staging was down on Tuesday afternoon because someone ran a database restore
> against it to test a runbook. That's a legitimate use of staging; the problem
> was that nobody announced it. From now on anything that takes staging down gets
> a heads-up in the team channel, so you'll have warning.

### Score

| Measure | Result |
|---|---|
| Rubric | 7/7 after revision, 5/7 on the draft |
| **Self-caught** | 3 of 3 — the AI added nothing I hadn't found |
| Time to first draft | 6 min |

Self-caught 3/3 is the result worth having. A 7/7 rubric score reached by
following AI corrections would be a worse session with a better-looking number.

---

## The shape, stripped down

1. Predict, in writing, before you look. Then lock it
2. Annotate the sheet yourself, completely, before the AI
3. Take the AI's reading **without the key**, and make it point at spans
4. Open the key
5. Record the **gap** and the **rule update**, not just the score
6. In Mode E: annotate your own draft before showing anyone, and count what you
   caught yourself

Steps 1 and 6 are what convert this from reading practice into model construction.
Step 3 is the one the AI will collapse into step 4 if nobody stops it, and a
collapsed step 3 makes disagreement impossible rather than merely unlikely.
