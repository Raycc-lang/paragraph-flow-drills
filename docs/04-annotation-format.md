# The Annotation Format

How you record an analysis. Used in `DRILLS.md` §1 step 3 (Mode A) and §4 step 3
(Mode E).

This file is written from measured failures, not from theory. Every rule below
replaced something that cost real session time. See the changes table in `LOG.md`
for which evidence produced which rule.

---

## The principle

> **An annotation format must ask you to point at the text, not to describe it.**

Pointing is recognition, which §0 confirmed is intact. Describing is production,
which §0 confirmed collapses under simultaneous load. A format that asks you to
compose English metalanguage while analyzing imposes the exact constraint the
project exists to relieve, and then measures its own overhead.

Every per-sentence field is answered with **a quote** or **a pick off a closed
list**. If such a field cannot be answered that way, it is the wrong field — say
so, and it gets cut and logged.

**Two fields are deliberate exceptions**, and they are marked as such below:
`Alternative reading` and `Uncertainty`. They are one line each, at the end of the
paragraph, and they are the only place in the sheet where a judgment is expressed
in your own words. An earlier version of this file claimed "nothing is composed,"
which was false and risked the AI rejecting valid answers.

---

## Division of labour

> **The AI transcribes. You interpret.**

The AI's preprocessing is restricted to **mechanically quoted material**. It may:

- quote the grammatical subject, **without resolving it**
- quote any material preceding the subject
- mark clause boundaries and number the clauses
- quote each clause span verbatim

It may **not**:

- write `= referent` or otherwise resolve a pronoun — that answers `Antecedent`
- paraphrase a clause into an "assertion" — paraphrase normalizes ambiguity,
  invents implicit propositions, and silently picks one reading
- flip a passive, unpack a nominalization, or regularize word order — those
  destroy the stress placement that D4 lives in
- name a relation, a role, or a pattern

An earlier version of this file asked the AI to number *assertions*. That was
semantic analysis wearing parsing's clothes: `This was welcomed by residents'
groups` rendered as `residents' groups welcomed it` deletes the emphasis evidence,
and `subject: "it" (= the grant)` hands over an antecedent the learner was
supposed to retrieve.

**Quoted clauses, not paraphrased propositions.** If the AI cannot supply a line
by copying characters off the page, it does not supply that line.

**The AI must not fill `Ties back by`, `Antecedent`, or `Pattern`.** Those are the
drill.

---

## The sheet

**No mode uses the version below by hand any more.** Mode E runs in
`exercise/_template-mode-e.html`; Modes A, B and C run in
`exercise/_template-modes-abc.html`. The fields are identical in both; only the
transcription is gone. The block below remains the definition of what the fields
*mean*, and it is what the instruments were built from.

The instruments implement this file's principle more literally than a paper sheet
could: clicking a word **is** pointing at the text. Nothing is described, and no
quote can be mistyped.

In Modes A and C the AI still supplies the pre-parse — verbatim sentence, quoted
subject, lettered clause quotes — and the page renders it read-only, because there you
are reading prose you did not write. In Mode E there is **no clause-boundary step**: the
page splits sentences, and you answer `Sentence type` and `Parts` instead. See the
section below on why the lettering was dropped.

The sheet as written out:

```
SENTENCE n  [subject: "..." | precedes subject: "..." or none | n clauses]
   a. "...verbatim clause..."
   b. "...verbatim clause..."

Ties back by:  ......... pick one of four:
                 quote the linking word            - a device is present and works
                 no explicit word, reader infers it - legitimate, common
                 there is a word but it fails       - D1 ambiguous / D5 renamed
                 nothing connects it                - D2 / D6

Antecedent:    ......... only when the line above is a pronoun or demonstrative.
                         Which lettered clause does it point at? "cannot pick"
                         is an answer, and it means D1

Pattern:       ......... 1 constant topic / 2 linear / 3 derived topics /
                         4 split / 5 contrastive / 6 question-answer / opening


[ one lens question - see below ]


Alternative reading:  ......... FREE RESPONSE, one line. Another way the
                                structure could be read, and what would settle it
Uncertainty:          ......... quote the term or assumption, then one clause on
                                what you took the reader to already know.
                                "None" is almost always wrong
```

Two fields per sentence, one conditional field, one lens, two closing lines.

---

## The four answers to `Ties back by`

This is the field that does the work, and its options are not interchangeable.

| Answer | Means | Verdict |
|---|---|---|
| *quote the word* | A cohesive device is present and resolves | Clean |
| `no explicit word, reader infers it` | Nothing carries the link, but the reader recovers it | Legitimate |
| `there is a word but it fails` | A device is present and does not do its job | **D1** if ambiguous, **D5** if the referent has been renamed |
| `nothing connects it` | No route from prior context exists | **D2**, or **D6** for an entity arriving as though shared |

**The third option is the one that gets missed, and missing it produces a
specific, repeatable error.** When a link is present but broken, the sentence
*feels* disconnected — so the natural entry is "no explicit word." That records
your reading experience accurately and misfiles the cause. Absence and failure
are different defects with different repairs.

The test: **look for the device before you conclude there isn't one.** A pronoun
that could point at three things is not an absent link. It is a present link that
has failed, and only the second description names a repairable defect.

---

## One lens per item

The core sheet catches **D1, D2, D5, D6** — reference, topic continuity, lexical
chains, missing departure points. It catches nothing else, and the gap is not
theoretical: session 1's minor D4 was missed with no field through which it could
have been found.

The fix is not to restore the six-column table. It is **one closed-choice question
per item, rotating.** Answer exactly one lens each session and log which.

### Lens R — relation · catches D3, D7

```
For the transition you named as the paragraph's main move:

Relation:      pick one - cause / result / contrast / concession /
                          qualification / addition / sequence / unclear
Signalled by:  quote the connective, or write "none"
Costs the reader:  yes / no / uncertain
```

`unclear` is a finding, not a failure — an unnameable relation is **D3**. A
connective whose named relation does not match the one you picked is **D7**.

### Lens S — stress · catches D4

```
For each sentence, CLICK the final constituent - the last few words before
the full stop - then pick:

   S1: [click]   is that the news?  news / already known / uncertain
   S2: [click]   ...
```

Old information in the stress position is **D4**.

**Clicked, never typed.** Session 3 ran this lens on 1 of 7 sentences and left the
rest blank, because the field asked for text to be copied out by hand — for every
sentence. A lens that costs seven manual transcriptions does not get run, and a lens
that does not get run catches nothing. It is now a click plus a three-way pick, which
is what "costs almost nothing" was always meant to describe.

### Lens J — job · catches structure and D8

```
Job per sentence: pick one -
   claim / context / evidence / qualification / consequence /
   contrast / definition / instruction / transition / closing
```

Two sentences doing the same job, or a paragraph with no `claim` anywhere, is
usually a structure problem rather than a flow one — see **D8**.

### Rotation

`R → S → J → R → …`, one per item. Log the lens in `LOG.md`. If a defect code
keeps being missed, run its lens twice in a row rather than adding a second lens
to one item.

---

## What `Antecedent` is for

It fires only when `Ties back by` is a pronoun or a demonstrative. Then: **point at
what it refers to, in the earlier text.**

If you cannot pick, that *is* the finding. A demonstrative with two live candidates
is **D1** — you have not failed to answer, you have answered.

**Where the antecedent can live.** In earlier sentences — all of them, not only the
immediately previous one. `03-defects.md` defines D1 as an antecedent that is
absent, ambiguous, **or too far back**, so the field has to be able to reach back
several sentences or that third case cannot be recorded. G3's sentence 3 renames a
noun from sentence 1, two sentences back.

It cannot live in the sentence doing the pointing. `Ties back by` asks what links
this sentence *to prior text*; if the referent is inside the same sentence, that is
intra-sentential and not what this field measures.

**The instrument enforces both scopes.** `Ties back by` offers only the current
sentence to click, because the linking word is by definition in it. `Antecedent`
offers only the preceding sentences. Nothing else is clickable, so the two fields
cannot be confused by pointing in the wrong direction.

## Sentence type, and why clause lettering was dropped

Earlier versions of this file lettered each clause `a.`, `b.` so `Antecedent` could
answer "1a, 1b, or the pair." Once `Antecedent` is answered by **clicking the words
themselves**, the letters address nothing — the click is more precise than the label
ever was. They were doing no work and they are gone.

What replaced them earns its place differently: **sentence type predicts which
defect is available.**

```
Sentence type:  simple / compound / complex / compound-complex
Parts:          1 / 2 / 3+        (independent clauses; only if not simple)
```

| Answer | What it tells you to look for |
|---|---|
| `compound`, 2+ parts | The next sentence has that many candidate antecedents. This is the **D1** condition, visible before the pronoun arrives |
| `compound` joined by `and` | If the parts stand in contrast, cause or concession, `and` is flattening it — **D3**, and often **D7** |
| `complex` | The news may be sitting in the subordinate clause instead of the stress position — **D4** |
| `simple` at 20+ words | Suspect a missed second clause. A long simple sentence is unusual |

**This is grammar used as an instrument, not adopted as a target.**
`01-target.md` excludes grammatical *accuracy* — whether the sentence is correct.
It does not exclude structure: component 3 of the target is "sentence topics and
grammatical subjects", component 4 is reference, component 6 is emphasis placement,
and all three depend on how many clauses there are and how they are joined. The list
of legitimate overrides in that file already includes "grammatical constraints on
what can occupy the subject slot."

Two closed picks, no prose, and each one narrows the search before you start looking.

---

## `None` on the closing lines

`Uncertainty: none` is almost always wrong, and it is wrong in a specific place —
whenever the paragraph names one thing more than one way, or assumes a reader
knows two terms are the same. That is a claim about reader knowledge, which R5
says is inference rather than fact.

If you write `none` twice in a row, check whether you skipped the line rather than
answered it.

---

## Worked example

A throwaway paragraph. Never practise the mechanics on a corpus item — they are
non-renewable as fresh measurements.

> **[1]** The bakery on Mill Street closes for three weeks every January.
> **[2]** The owner uses the time to service the ovens, which run continuously for
> the rest of the year. **[3]** Regulars grumble, but the alternative is a
> breakdown in the middle of a Saturday morning.

```
SENTENCE 1  [subject: "The bakery on Mill Street" | precedes subject: none | 1 clause]
   a. "The bakery on Mill Street closes for three weeks every January"

Ties back by:  nothing - this is the opening
Pattern:       opening


SENTENCE 2  [subject: "The owner" | precedes subject: none | 2 clauses]
   a. "The owner uses the time to service the ovens"
   b. "which run continuously for the rest of the year"

Ties back by:  "The owner" - part of the bakery, already established
               "the time" - points back to "three weeks every January"
Pattern:       3 derived topics


SENTENCE 3  [subject: "Regulars" | precedes subject: none | 2 clauses]
   a. "Regulars grumble"
   b. "but the alternative is a breakdown in the middle of a Saturday morning"

Ties back by:  "Regulars" - the bakery's customers, same frame
               "the alternative" - points back to the January closure
Pattern:       3 derived topics


LENS R (relation, this item)
Relation:          contrast - between 3a and 3b
Signalled by:      "but"
Costs the reader:  no


Alternative reading:  sentence 2 is linear if "the time" is taken as the link.
                      It reads as derived because the departure point is "The
                      owner" and "the time" sits in the object, not the opening.
                      What settles it: whether the reader's attention after
                      sentence 1 rests on the closure or on the bakery.
Uncertainty:          "the alternative" - I assumed the reader agrees a
                      mid-Saturday breakdown is worse than a January closure.
```

**Note what the AI supplied and what it did not.** Every lettered line is
characters copied off the page. It did not write `a. customers object` for
`Regulars grumble`, because `grumble` and `object` are not the same word and the
choice between them is a reading. It did not tell you that `the time` refers to
the January closure. That is `Ties back by`, and it is yours.

**Sentence 2 is the teaching case.** The naive move is to hunt for a repeated
word, find `the time` echoing `three weeks`, and call it linear. But a repeated
word in the object position sets no departure point. Cohesion is about **where**
information sits, not merely **whether** it recurs.

**Sentence 3 is the second one.** It contains `but`, yet its pattern is derived,
not contrastive. Contrastive progression means the contrast occupies the departure
point. Here the departure point is `Regulars` and the contrast arrives later.
Within-sentence contrast is not pattern 5.

---

## Second worked example — a defective paragraph

Corpus item **G3**, worked in session 1 and therefore already burned as a fresh
measurement. Reused here at no cost, because it shows the two things the bakery
example cannot: the `Antecedent` line firing, and the *there is a word but it
fails* option in use.

> **[1]** The council extended the consultation period and published the full set
> of objections online. **[2]** This was welcomed by residents' groups.
> **[3]** The local authority had previously released only a summary, and the
> borough's decision to change course followed three months of pressure.

```
SENTENCE 1  [subject: "The council" | precedes subject: none | 2 clauses]
   a. "The council extended the consultation period"
   b. "published the full set of objections online"

Ties back by:  nothing - this is the opening
Pattern:       opening


SENTENCE 2  [subject: "This" | precedes subject: none | 1 clause]
   a. "This was welcomed by residents' groups"

Ties back by:  there is a word but it fails - "This" is present and points, but
               does not say at what
Antecedent:    cannot pick. 1a, 1b, or the pair are all live -> D1
Pattern:       2 linear


SENTENCE 3  [subject: "The local authority" | precedes subject: none | 2 clauses]
   a. "The local authority had previously released only a summary"
   b. "the borough's decision to change course followed three months of pressure"

Ties back by:  there is a word but it fails - "The local authority" is the
               council renamed, and "the borough" renames it again -> D5
Pattern:       1 constant topic, obscured. The departure point is the same body
               throughout; only the name changes


LENS S (stress, this item)
   S1: "published the full set of objections online"  -> news
   S2: "welcomed by residents' groups"                -> news
   S3: "followed three months of pressure"            -> news, but competing
       - the causal fact is trailing a compound sentence, so it shares the
         stress position with 3a's summary point  -> minor D4


Alternative reading:  sentence 3 looks like 5 contrastive, because "The local
                      authority" reads as a new entity arriving in first
                      position. It only resolves to constant topic once you
                      accept that council, local authority and borough are one
                      body - which is exactly the acceptance D5 makes expensive.
Uncertainty:          "The local authority" / "the borough" - I assumed this
                      reader treats those and "The council" as one referent. A
                      reader who does not will read sentence 3 as a topic shift.
```

**Lens S is what would have caught the minor D4 in session 1.** The core sheet has
no field for emphasis, so the defect had nowhere to surface. Quoting the final
constituent and asking whether it is the news costs one line and finds it.

**Note the clause quotes on sentence 2.** The passive is preserved. An earlier
version rendered it `residents' groups welcomed it`, which deletes exactly the
evidence Lens S runs on.

**Key:** D1, D5, and a minor D4 — the causal fact (three months of pressure)
trails a compound sentence where it competes for the stress position.

**The error this example exists to prevent.** In session 1, sentences 2 and 3 were
both entered as `no explicit word`. Both were wrong in the same direction. `This`
is an explicit device; `The local authority` is an explicit device. Both were
present, and both failed. The sentences *felt* disconnected, and "no explicit word"
recorded that feeling accurately while naming the wrong cause.

Absence and failure need different repairs. An absent link is supplied. A failed
link is *replaced* — the demonstrative gets a noun, the renamed entity gets its
original name back. Filing one as the other sends you to the wrong repair.

**And note where the pattern field went wrong.** Sentence 3 was labelled
`5 contrastive`, which is what a broken lexical chain looks like from the inside:
the transition becomes hard to label, because you cannot tell whether the opening
noun is old or new. **An unlabelable transition is itself evidence.** When the
pattern will not resolve, check the lexical chain before reaching for pattern 5.

---

## When to change this file

Cut any field still being answered with composed prose after three sessions. If a
paragraph takes more than five minutes to annotate, cut to `Ties back by` alone
and record it in `LOG.md`.

The format serves the drill. When it starts consuming the session, it has become
the thing being practised, and that is not the target.

**This warning now applies to the instrument as well.** A browser tool is a bigger
apparatus than a markdown file, and the same failure is available to it: time spent
maintaining the page is time not spent writing paragraphs. The test is unchanged —
if the tool consumes the session, the tool is what is being practised. Keep it a
single file with no dependencies and no build step, so that abandoning it costs
nothing and editing it needs no toolchain.
