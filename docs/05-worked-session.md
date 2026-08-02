# Worked Session

Read `docs/04-annotation-format.md` first. This file shows one Mode A item and one
Mode E item using the current protocol. Both examples use attempt-first; reference-
first and skip remain valid choices under `AGENTS.md`.

## Mode A

### 1. Read Once and Lock a Prediction

> The village hall committee spent two years raising money for a new roof. When
> the grant finally came through, it covered rather more than the roof needed, and
> the surplus went on rewiring the kitchen. That turned out to matter more than
> anyone expected. The hall had been losing its Saturday bookings to a newer venue
> eight miles away, and the thing people cited was never the roof.

```text
Main transition: sentence 2 → 3, pattern 2 linear
Verdict: clean, medium confidence
Reader assumption: the reader will take "That" to mean the rewiring
```

The prediction is now locked. A later change is written separately and scored as a
prediction gap.

### 2. Complete the Sheet

The Mode A instrument supplies the verbatim sentences, subjects, preceding
material, and clause spans. The learner fills the fields below.

```text
SENTENCE 1
Starts from: "The village hall committee"
Ties back by: opening
Pattern: opening

SENTENCE 2
Starts from: "When the grant finally came through"; subject "it"
Ties back by: "the grant" and "the roof"
Antecedent: "it" → "the grant"
Pattern: 2 linear

SENTENCE 3
Starts from: "That"
Ties back by: "That"
Antecedent: the rewiring; recoverable by recency, but uncertain
Pattern: 2 linear

SENTENCE 4
Starts from: "The hall"
Ties back by: "The hall"
Pattern: 3 derived topics

LENS R
Relation: cause
Signalled by: none
Costs the reader: no

Alternative reading: "That" may refer to the whole grant surplus rather than only
                     the rewiring; a more specific noun would settle it.
Uncertainty: "The hall" — I assumed the reader keeps the building, committee,
             roof, and kitchen in one active frame.
```

The pre-parse must show `subject: "it"`, not `"it" = the grant`. Resolving the
pronoun is the learner's task.

### 3. Compare the Reference Sheet and Key

After the learner's sheet is complete, the drill partner returns the same filled
sheet and the key opens. Every defect code is attached to a quoted span. A plausible
reference judgment is that `That` is recoverable but costly rather than a clear D1.

```text
Pattern agreement: 3/3
Prediction hit: partial
Lens: R
```

**Prediction gap:** The learner expected `That` to be either clean or defective;
it occupies a reader-dependent middle case.

**Rule update:** A reference can resolve and still cost enough to deserve attention.

## Mode E

### 1. Use a Fresh Brief

```text
Purpose: explain an outage and set the expectation for next time
Reader: a mildly annoyed peer on another team
Known facts: staging was down Tuesday afternoon; a database restore caused it; the
             restore was a valid runbook test; nobody announced it
Needs to be able to: decide whether to plan around another unannounced outage
Variant: E-Expand
```

### 2. Write Cold and Lock the Draft

```text
Staging was down on Tuesday afternoon because someone was running a database
restore against it. This was to test a runbook, which is a legitimate use of
staging. The problem was that it wasn't announced anywhere. We're going to add a
heads-up to the team channel for anything that takes staging down, so you should
get warning next time.
```

The draft is timed and frozen before annotation.

### 3. Complete the Mode E Sheet

The instrument splits the draft into sentences. The learner corrects any bad split
and fills `Sentence type` and `Parts`; no clause lettering is used.

```text
SENTENCE 1
Starts from: "Staging"
Ties back by: opening
Pattern: opening
Sentence type: complex
Parts: 1

SENTENCE 2
Starts from: "This"
Ties back by: "This"
Antecedent: "a database restore"
Pattern: 2 linear
Sentence type: complex
Parts: 1

SENTENCE 3
Starts from: "The problem"
Ties back by: no explicit word, reader infers it
Pattern: 2 linear
Sentence type: complex
Parts: 1

SENTENCE 4
Starts from: "We"
Ties back by: no explicit word, reader infers it
Pattern: 6 question-answer
Sentence type: compound-complex
Parts: 2

LENS S
S1 final constituent: "a database restore against it" → news
S2 final constituent: "a legitimate use of staging" → news
S3 final constituent: "wasn't announced anywhere" → news
S4 final constituent: "you should get warning next time" → news

Alternative reading: Sentence 4 can be read as derived topics if "We" is part of
                     the established staging-owner frame; question-answer is more
                     useful because the brief makes recurrence the active question.
Uncertainty: "We" — I assumed the other team knows which group owns staging.

Intent gap: I meant to guarantee advance notice; "should get warning" only predicts
            it.
```

### 4. Resolve Brackets Without Reorganizing

This draft has no brackets. If it did, lexical replacements would be made in a
copy without changing sentence order or structure. Reorganization belongs in the
next step.

### 5. Make a Separate Self-Revision

```text
Staging was down on Tuesday afternoon because someone ran a database restore
against it to test a runbook. That's a legitimate use of staging; the problem was
that nobody announced it. From now on, anything that takes staging down gets a
heads-up in the team channel, so you'll have warning.
```

The first draft remains unchanged.

### 6. Receive the Reference and Scores

The drill partner returns a filled sheet, compares it field by field, and scores
both frozen versions with `tests/verification-01.md` Part 3.

```text
First-draft rubric: 5/7
Self-revised rubric: 7/7
Self-caught: 2/2
Reference order: attempt first
Voided measures: none
Time to first draft: 6 minutes
```

The denominator for `Self-caught` comes from the later reference analysis, so it
must not be treated as a validated ground truth.

### 7. Compare Alternatives Only After Scoring

The drill partner now gives two or three full alternatives with different
progression or emphasis choices and states the trade-off of each. These are
unvalidated comparisons, not a standard answer. They arrive only after both scores
are final.

## Minimal Sequence

1. Generate the exercise file.
2. In Mode A, flag terms and lock the three-part prediction. In Mode E, write and
   lock the cold draft.
3. Choose reference-first, attempt-first, or skip for the annotation sheet.
4. Keep the key behind the mode-specific commitment gate.
5. Preserve frozen drafts and revisions as separate artifacts.
6. Return the completed reference sheet and evidence-based scores.
7. In Mode E, show multiple full alternatives only after both scores are final.
8. Export markdown and log the valid and void measures.
