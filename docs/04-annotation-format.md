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

Every field is answered with **a quote** or **a pick off a closed list**. Nothing
is composed. If a field cannot be answered that way, it is the wrong field — say
so, and it gets cut and logged.

---

## Division of labour

> **The AI parses. You point.**

Finding a grammatical subject, splitting clauses, and counting assertions is
syntax. Your sentence-level English is functional, so parsing measures an ability
you already have. The AI does it and hands you a pre-parsed sheet.

Deciding what a sentence ties back to, whether that tie works, and which pattern
is operating — that is the ability under training. That stays yours, always.

**The AI must not fill `Ties back by` or `Pattern`.** Those are the drill.

---

## The sheet

The AI produces the bracketed header lines. You fill the dotted lines.

```
SENTENCE n  [subject: "..." | what precedes it | how many assertions]
   a. ...
   b. ...

Ties back by:  ......... pick one of four:
                 quote the linking word            - a device is present and works
                 no explicit word, reader infers it - legitimate, common
                 there is a word but it fails       - D1 ambiguous / D5 renamed
                 nothing connects it                - D2 / D6

Antecedent:    ......... only when the line above is a pronoun or demonstrative.
                         Which of the numbered assertions does it point at?

Pattern:       ......... 1 constant topic / 2 linear / 3 derived topics /
                         4 split / 5 contrastive / 6 question-answer / opening


Alternative reading:  ......... one line. Another way the structure could be
                                read, and what would settle it
Uncertainty:          ......... one line. What you assumed the reader already
                                knows. "None" is almost always wrong
```

That is the whole format. Two fields per sentence, one conditional field, two
closing lines. It is not a first stage to be graduated from.

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

## What `Antecedent` is for

It fires only when `Ties back by` is a pronoun or a demonstrative. Then: which of
the pre-parsed assertions does it point at?

If you cannot pick one, that *is* the finding. A demonstrative with two live
candidates is **D1** — you have not failed to answer, you have answered.

An earlier version of this file made you list every proposition in every sentence.
That was transcription. The count is what matters, the AI supplies it, and the
list only matters where something points back at it.

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
SENTENCE 1  [subject: "The bakery on Mill Street" | nothing precedes | 1 assertion]
   a. closes for three weeks every January

Ties back by:  nothing - this is the opening
Pattern:       opening


SENTENCE 2  [subject: "The owner" | nothing precedes | 2 assertions]
   a. uses the closure to service the ovens
   b. the ovens run continuously the rest of the year

Ties back by:  "The owner" - part of the bakery, already established
               "the time" - points back to "three weeks every January"
Pattern:       3 derived topics


SENTENCE 3  [subject: "Regulars" | nothing precedes | 2 assertions]
   a. customers object
   b. the alternative is a breakdown mid-Saturday

Ties back by:  "Regulars" - the bakery's customers, same frame
               "the alternative" - points back to the January closure
Pattern:       3 derived topics


Alternative reading:  sentence 2 is linear if "the time" is taken as the link.
                      It reads as derived because the departure point is "The
                      owner" and "the time" sits in the object, not the opening.
                      What settles it: whether the reader's attention after
                      sentence 1 rests on the closure or on the bakery.
Uncertainty:          sentence 3 assumes the reader agrees a mid-Saturday
                      breakdown is worse than a January closure.
```

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
SENTENCE 1  [subject: "The council" | nothing precedes | 2 assertions]
   a. extended the consultation period
   b. published the full set of objections online

Ties back by:  nothing - this is the opening
Pattern:       opening


SENTENCE 2  [subject: "This" | nothing precedes | 1 assertion]
   a. residents' groups welcomed it

Ties back by:  there is a word but it fails - "This" is present and points, but
               does not say at what
Antecedent:    cannot pick. 1a, 1b, or the pair are all live -> D1
Pattern:       2 linear


SENTENCE 3  [two clauses]
   clause 1 subject: "The local authority" | nothing precedes | 1 assertion
      a. it had previously released only a summary
   clause 2 subject: "the borough's decision to change course" | 1 assertion
      b. the change followed three months of pressure

Ties back by:  there is a word but it fails - "The local authority" is the
               council renamed, and "the borough" renames it again -> D5
Pattern:       1 constant topic, obscured. The departure point is the same body
               throughout; only the name changes


Alternative reading:  sentence 3 looks like 5 contrastive, because "The local
                      authority" reads as a new entity arriving in first
                      position. It only resolves to constant topic once you
                      accept that council, local authority and borough are one
                      body - which is exactly the acceptance D5 makes expensive.
Uncertainty:          whether this reader treats those three names as one
                      referent. A reader who does not will read sentence 3 as a
                      topic shift.
```

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
