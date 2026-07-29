# A Worked Session

The project tells you to commit a prediction and fill the annotator table. It
never shows one filled in. This is that — one Mode A item and one Mode E item,
start to finish.

The paragraph below is a **throwaway**, deliberately not from the corpus. Practice
the mechanics on scrap. Corpus items are non-renewable as novel material, and
burning one on a demonstration costs you a measurement later.

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

### Step 2 — fill the table

| # | Role | Departure point | Link to prior | New contribution | Relation | Pattern |
|---|---|---|---|---|---|---|
| 1 | Setup | `The village hall committee` — new, opening | Reader's situation only | Two years fundraising, for a roof | — | Opening |
| 2 | Development | Temporal frame `When the grant came through`; subject `it` = the grant | `grant` ← `raising money`; `roof` repeated verbatim | Surplus existed; it went on rewiring | Sequence, then consequence | Linear |
| 3 | Pivot / claim | `That` = the rewiring decision | Demonstrative, clausal antecedent | It mattered more than expected | Evaluation of 2 | Linear |
| 4 | Explanation | `The hall` | Lexical — superordinate for the whole enterprise | Losing bookings; the cited reason was never the roof | Cause — explains why 3 is true | Derived topic |

### Step 3 — the two components people skip

**Alternative analysis.** Sentence 3's `That` can be read two ways: the rewiring
decision, or the fact that the grant exceeded what was needed. The rewiring
reading wins on recency and salience, so the sentence is recoverable — but it is
a near-miss for D1, not a clean case. A writer with a less forgiving reader
should have written `The rewiring turned out to matter…`.

**Uncertainty.** Sentence 4 introduces two entities at once (the Saturday
bookings, the rival venue) and assumes the reader will accept that a village hall
competes for bookings at all. Whether that lands depends on a reader model I am
inferring, not reading. Flagged rather than scored.

### Step 4 — compare, and defend

Now the AI annotates. Suppose it marks sentence 4 as an unmotivated topic shift
(D2) because the departure point moves from the rewiring to the hall's bookings.

**Do not accept this.** The correct response:

> `The hall` is a superordinate for everything already discussed — the committee,
> the roof, the kitchen are all parts of it. Derived topics, not a shift. And
> sentence 4 is doing the work of explaining sentence 3's claim, which is the
> relation that licenses it.

That exchange is the session. A high agreement rate with zero defended
disagreements means you are deferring, and deference produces no model.

### Step 5 — score

| Measure | Result |
|---|---|
| Pattern agreement | 3/3 transitions |
| Defended disagreements | 1 (sentence 4) |
| Prediction hit | **Partial** — right about linear-with-pivot, right to watch `That`, but I predicted "clean" and it is borderline |

**Prediction gap:** I expected demonstratives to be either fine or broken. This one
is neither — it is recoverable but costs the reader a beat.

**Rule update:** D1 is not binary. There is a middle band where a reference
resolves on second pass, and whether that counts as a defect depends on the
reader and the stakes. Add "recoverable but expensive" as a thing to notice.

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

| # | Role | Departure | Link | New | Pattern |
|---|---|---|---|---|---|
| 1 | Answer | `Staging` — the thing they asked about | Their question | Cause: a restore | Opening, question–answer |
| 2 | Qualification | `This` = the restore | Demonstrative | It was legitimate | Linear |
| 3 | Concession | `The problem` | New framing | It wasn't announced | Linear |
| 4 | Remedy | `We` | Shift to actor | Heads-up in channel | Consequence |

**What I caught myself:**

- Sentence 2 `This was to test a runbook` — weak. `This` again, and `was to test`
  puts nothing in the stress position. **D4.**
- Sentence 3 `The problem was that it wasn't announced` — six words of throat-clearing
  before the content. The problem *is* the announcement gap; say it. **D4.**
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

1. Predict, in writing, before you look
2. Do the analysis yourself, completely, before the AI
3. Compare — and argue when you disagree
4. Record the **gap** and the **rule update**, not just the score
5. In Mode E: annotate your own draft before showing anyone, and count what you
   caught yourself

Steps 1 and 5 are the ones that convert this from reading practice into model
construction. They are also the two that quietly get dropped when you are tired.
