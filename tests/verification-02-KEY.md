# Verification Test 02 — Key

**Do not open until all three parts are written down.**

---

## How to read these keys

Every finding below is tagged. This exists because the earlier keys stated
judgments flatly while `AGENTS.md` R4, R5, and R10 require the opposite — never
declare one reading uniquely correct, mark reader assumptions as assumptions, and
state unreliability. A categorical key trains false confidence, which is worse
than a missed defect.

| Tag | Meaning | Scoring |
|---|---|---|
| **[REQUIRED]** | Holds under any plausible reader or purpose. Missing it is an error | Full |
| **[CONDITIONAL]** | Depends on an inferred purpose, reader, or domain fact. The key states which | Full credit for either verdict **if you state the condition** |
| **[ALTERNATIVE]** | A defensible different reading, with the evidence that would decide | No penalty |

If you disagree with a [CONDITIONAL] and can name the reader or purpose under
which your reading holds, you were right. Score it that way.

---

## Part 1

### X1 — SOUND
The longest item in the project, and it contains nothing to fix. That is the test.

Patterns, in order: opening context → contrastive (`nonetheless`, accurately
marked) → derived topic shift to the company's finances, licensed by the canal
enterprise as superordinate → constant topic across `The company` / `Its
shareholders` → a cleft (`What they had wanted was…`) placing the explanation in
the stress position → a cold closing sentence that returns to the canal.

Two things worth noticing rather than flagging:

- Sentence 3 shifts from freight rates to dividends with no connective. It is
  licensed because both are properties of one enterprise — derived topics, not an
  unmotivated shift
- The final sentence is deliberately unmarked. Its force comes from the bare fact
  in the stress position (`less than the cost of its final three miles`). Adding
  `Ultimately` or `In the end` would weaken it

If you found a defect here, ask whether you found it because it was there or
because you expected a test to contain one.

### X2 — DEFECTIVE: D4 **[CONDITIONAL]**
One defect type, no others. If you assigned three codes, you over-called.

**The condition:** a thirty-word subject is unambiguously a *processing cost*. Whether
it is a *defect* depends on the reader. In a design document read slowly by someone
who needs the full qualification before the verb, it may be acceptable. In a status
update skimmed by a manager, it is not. The key scores it defective on the
assumption this is a decision record read once, at speed.

**[ALTERNATIVE]** — call it sound, *if* you state that the reader is reading
deliberately and needs the criterion fully specified before its effect. Evidence
that would decide: whether the document has a summary elsewhere, and whether
readers act on it or file it.

The passive close (`was adopted in March`) is **[REQUIRED]** — that one holds under
any reading, since the stress position carries a date nobody needs.

- The decisive sentence has a **thirty-word subject** with an appositive wedged
  between subject and verb (`A requirement that had not been written down… is what
  eliminated two of them`). The reader holds an unresolved subject across the
  entire criterion before learning what it does
- `The remaining option was adopted in March` — agentless passive holding the
  paragraph's outcome, with `in March` in the stress position. The date is the
  least important thing in the sentence

*One repair:* `Two were eliminated by a requirement nobody had written down until
late: the backend had to support point-in-time recovery without a separate tooling
stack. The team adopted the remaining option in March.`

**Not a defect:** the paragraph announces three criteria and then introduces a
fourth. That is the *point being made* — the late requirement is the story. Coding
this as a split-progression violation is a content/flow confusion.

### X3 — DEFECTIVE: D1 — with a legitimate override that must NOT be flagged
Co-occurrence item.

- **Override, correct:** `Do not merge this until…` leads because acting before
  finishing the paragraph is costly. Same class as G11, T4, V4. Flagging it scores −1
- **D1, genuine:** `This was discovered on Thursday.` Three candidate antecedents —
  the importer still running, the belief that it was decommissioned being wrong, or
  the column conflict. The sentence also adds little; `Thursday` earns its place
  only if the reader needs the timeline

Getting *both* judgments right is the item. Catching the D1 while also flagging
the imperative scores worse than missing the D1 entirely, because it means the
override is not learned.

### X4 — DEFECTIVE: D8 (irrelevance), D2, D4 — **[CONDITIONAL] on genre**
The far-transfer form of D8. Not correlation-mistaken-for-causation this time —
this is a sentence that does not belong and a paragraph with no thread.

**The condition, and it is decisive:** as an **executive summary**, all three codes
hold. As **meeting minutes**, they mostly dissolve — minutes are chronological by
convention, the office move genuinely was raised, and `Nobody objected` is a
material fact worth recording. Under that genre the paragraph is doing its job.

The key scores it defective because the surrounding items are summaries and the
paragraph reads as one. If you called it sound *and named minutes as the genre*,
score yourself full marks — that is a better answer than the key's, because it
identifies that the flow verdict was never decidable without the genre.

**Evidence that would decide:** whether the document has an owner and an action
list, and whether anyone reads it who was not in the room.

- **D8** — `The office move is scheduled for August` connects to nothing. Not a
  flow problem: no reordering saves it. It should be cut or given a thread
- **D2** — the opening attendance remark also leads nowhere. Either it explains
  something later (it doesn't) or it goes
- **D4** — the paragraph's actual news is that the shortfall moved forward a
  quarter. It sits mid-paragraph in a relative clause, and the closing stress
  position holds `Nobody objected`

The correct top-level verdict: *this is a minutes-dump, not a summary.* Repairing
the flow without deciding what the paragraph is for would produce a smoother
minutes-dump.

### X5 — SOUND (trap)
Question–answer opening, then a colon-introduced mechanism, then two derived
consequences marked `This is why` and `It is also why`.

The near-miss you may have flagged: `This is why batch size matters` — a
demonstrative with a clausal antecedent. That is **not** D1. D1 requires genuine
ambiguity, and here exactly one proposition precedes it. Demonstratives pointing
at a whole preceding clause are ordinary English; treating every `This` as a
defect is the over-correction this project can teach.

`Not, for the most part, the arithmetic.` — a fragment, and correct. It answers
the question before the mechanism arrives, which is what lets the reader hold the
rest.

### X6 — DEFECTIVE: D5, D6
The disguised chain. Harder than G3 or V7, where the synonyms were obviously
co-referential.

- **D5 [CONDITIONAL]** — `the intake form` / `the submission` / `validated
  applications` / `Records` / `a partially completed form`. In many real systems
  these *are* genuinely distinct objects: a form is what the user fills, a
  submission is the event, an application is the resulting entity, a record is its
  row. If the domain distinguishes them, the varied naming is precise rather than
  broken.
  It is still scored defective here, for a reason that survives either reading:
  **the paragraph never establishes the distinctions it relies on.** A reader
  outside the system cannot tell whether five names mean five things or one.
  Precise naming without a stated mapping is indistinguishable from elegant
  variation.
  **[ALTERNATIVE]** — sound, *if* you state that the reader already knows the
  domain object model. Evidence that would decide: whether this paragraph appears
  in onboarding docs or in an internal design note
- **D6** — `The rejection notice` arrives definite and unestablished. Nothing said
  a notice is sent

Note the interaction: because the chain is broken, the reader cannot resolve
whether `a partially completed form` at the end is the original intake form. One
defect is manufacturing another.

### X7 — DEFECTIVE: D7, D3 — and the D7 is a timeline error
The hardest item.

- **D7** — `Consequently` asserts that the exemption applications follow from the
  cost rise, which follows from the limits. But the limits took effect **in April**
  and the costs rose **in the first quarter** — before them. The connective claims
  a causal chain the paragraph's own dates contradict. A wrong connective is worse
  than none, and this one is wrong in a way that survives a careless read
- **D3** — the final sentence's relation is unmarked. Is the unchanged particulate
  reading evidence the limits are failing, or a caveat that it is too early? The
  paragraph's meaning changes completely depending on which, and nothing tells you

Full credit requires catching the date contradiction, not just calling
`Consequently` clunky. If you flagged D7 for the right reason, that is the
strongest single signal in this test.

---

## Score

Part 1 is out of 14. Two items are sound (X1, X5); five are defective.

| Signal | Reading |
|---|---|
| −1 on X1 or X5 | Defect-hunting under test conditions, or over-flagging demonstratives. Both are D9 |
| Flagged the imperative in X3 | The override is not learned. This matters more than any missed defect |
| Over-coded X2 | You are assigning codes by quantity. One defect is a complete answer |
| Caught X7's date contradiction | Genuine coherence-layer attention. The best outcome available here |
| Missed all of X4's D8 | Cohesion/coherence line still not held |

---

## Part 3 notes

**Q1** — the hidden requirement is that the reader `needs to decide whether to keep
escalating`. A paragraph that apologises well and never gives them the basis for
that decision fails item 6 no matter how it reads. Check whether you: stated the
actual cause plainly, said what you got wrong without burying it in a subordinate
clause, and gave them something concrete enough to act on.

A specific trap: the natural instinct is to open with the apology. Consider
whether the correction or the remedy should lead — the reader has already had one
wrong answer from you, and what they want first is the right one.

**Q2** — three sentences means you cannot establish, explain, and conclude in the
usual order. Something must carry two jobs. Check whether your first sentence
does real work or spends itself on setup.

---

## Recording

Log both test scores side by side, with the gap:

```
V01 Part1: __/14   V01 Part3: __/7    Date:
V02 Part1: __/14   V02 Part3: __/7    Date:
Gap:
```

A large 01→02 drop means templates, not models. The fix is sourcing authentic
material against your recurring codes — `corpus/found/PROTOCOL.md` — not more
repetitions of the starter corpus.
