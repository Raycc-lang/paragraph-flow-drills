# Keys — Tier 1 and Tier 2

**Stop.** Do not read this before committing an answer. `AGENTS.md` R7 forbids the
AI from reading this file into a drill session before you have answered.

Keys give the defect codes and the reasoning. Where a repair is shown it is *one*
valid repair, not the answer — if yours differs and preserves the meaning, argue
for it.

---

## Tier 1

### G1 — CLEAN
Constant topic. Departure point stays `the fine policy` (`It`, `It`, `it`)
across three sentences; each comment is new. Not linear progression, and correctly
so. Marking this defective for "not chaining" is a naive-rule false positive.

### G2 — CLEAN
Derived topics. `three parts` establishes a superordinate topic; `The
acknowledgement`, `The account`, `The commitment` are each new as sentence
openings but accessible because the whole licenses the parts. Count matches
development (three announced, three delivered).

### G3 — DEFECTIVE: D1, D5
- **D1** — `This was welcomed` has three candidate antecedents: the extension, the
  publication, or the pair. The sentence forces a guess.
- **D5** — `The council` / `The local authority` / `the borough` are one referent
  under three names. Elegant variation; in this register, repeat `the council`.
- Minor D4: the causal fact (three months of pressure) is trailing a compound
  sentence where it competes for the stress position.

*One repair:* `The council extended the consultation period and published the full
set of objections online. Residents' groups welcomed the extension. The council
had previously released only a summary, and changed course after three months of
pressure.`

### G4 — DEFECTIVE: D3 ×2
Every relation is left implicit. Sentence 2 is a *cost* set against sentence 1's
benefit — nothing marks it. Sentence 3 is a *concession or counterweight* — also
unmarked. The reader cannot tell whether this paragraph is arguing for the
timetable, against it, or neither.

This is the case where connectives do real work. `but`, `however`, `even so`, or a
restructure that makes the contrast structural — any is defensible. Adding nothing
is not.

### G5 — CLEAN (trap item)
Contrastive progression. Sentence 2 opens with entirely new information (`Four
left`), which a chain rule flags as a topic shift error. It is not: the reversal
is the information, and `Most … / Four …` makes the contrast structural without
needing `however`. Sentence 3 then uses constant topic on `All four`.

If you marked this defective, that is a boundary error, and it is worth more
attention than any of the genuine defects in this set.

### G6 — DEFECTIVE: D2, D6
- **D2** — nothing licenses the jump from trial results to measurement difficulty
  to a committee meeting. Three unrelated departure points.
- **D6** — `The steering committee` arrives as though established; it hasn't been.
- Note: this may *also* be D8. If the writer had no argument connecting these
  facts, no reordering will help. Deciding between "badly ordered" and "no
  argument" is the useful judgment here.

### G7 — reorder key
Reference order: **2 → 4 → 3 → 1**

> Most people assume that the hardest part of learning an instrument is the
> physical technique. In practice, the first real obstacle is usually attention:
> noticing the difference between what you played and what you intended. Teachers
> spend much of the early months not correcting fingers but describing sounds,
> because a student who cannot hear the error has no way to fix it. Technique
> improves quickly once the ear has something to aim at.

Structure: expectation (2) → correction of it (4) → evidence (3) → consequence (1).
`In practice` in sentence 4 is the tell that it answers a stated assumption, so it
cannot come first. Sentence 1 must be last: `the ear` refers back to material
established in 4 and 3.

**A defensible alternative:** 2 → 4 → 1 → 3, which puts the consequence before the
evidence. Weaker, because 3 explains *why* 1 is true and reads oddly as an
afterthought — but not wrong. If you produced this, you were reading the roles
correctly.

### G8 — DEFECTIVE: D8 (coherence, not cohesion)
Every link resolves cleanly. The reasoning does not: correlation is treated as
established causation, other changes in those cities are not considered, and
`Therefore` claims more than two facts support.

**Correct response: refuse to repair this with flow work.** Say the argument is
broken. Any smoothing here makes a bad inference read better, which is worse than
leaving it rough.

### G9 — CLEAN
Question–answer opening, then split progression. `Two reasons` announces a count;
two are delivered, in order. `neither is squeamishness` pre-empts the reader's
likely wrong guess — reader-modelling doing real work.

### G10 — DEFECTIVE: D4, D7
- **D4** — the news (forty pence, April, over-21s) is stuffed into a subject and a
  relative clause, and the stress position holds `was announced`, which carries no
  information. Passive with an empty verb at the end.
- **D7** — `Moreover` signals addition. The actual relation is contrast or
  concession: wages rose *and yet* employment didn't fall. Wrong marker is worse
  than no marker.

*One repair:* `The minimum wage rose by forty pence an hour in April, for workers
over twenty-one. Employment in the affected sectors has not fallen.` — the
contrast now sits in the bare juxtaposition, which is enough here; `Even so` would
also be defensible.

### G11 — CLEAN (trap item)
Instruction-first. The imperative leads because the cost of the reader acting
before finishing the paragraph is high. Given-before-new is correctly overridden
by hazard-first genre convention. Sentence 2 then supplies the justification, and
sentence 3 handles the exception case.

### G12 — DEFECTIVE: D5, D4
- **D5** — `The report` / `The document` / `The publication` / `the review` / `the
  text`: five names, one referent.
- **D4** — the most important content (`the most serious material`) is demoted into
  a relative clause, and the stress position of the final sentence holds `an
  annex`. If burial is the point being made, the sentence should say so directly.

---

## Tier 2

### T1 — CLEAN
Note the structure: it corrects the customer's wrong hypothesis explicitly
(`not because of the schema change you mentioned`) rather than ignoring it —
reader-modelling. Then linear progression through the mechanism, then split
progression for the two options. Each option carries its cost. This is the target
shape for an escalation reply.

### T2 — CLEAN
Chronological override at the opening (time window first, per incident-report
convention), then cause, then a `because` clause carrying the delay explanation,
then the action item in the stress position of the final sentence. The last
sentence is doing the most work and is correctly placed last.

### T3 — DEFECTIVE: D1, D5
- **D1** — `This caused` is ambiguous between the migration itself and its
  completion overnight.
- **D5** — `The data pipeline` / `the ETL job` / `the extract process` read as three
  systems. If they are one, name it once.
- Also worth noting: the paragraph never says whether it is fixed, which a reader
  in this genre needs. That gap is closer to D8 than to any flow defect.

### T4 — CLEAN
Instruction-first, same override as G11. `Check … before failing over` leads;
justification follows; threshold and exception close.

### T5 — DEFECTIVE: D8
Structurally identical to G8, in your target domain. Post hoc reasoning, a
`Therefore` the evidence does not support, and a remediation proposed on that
basis. Flow is fine. Refuse to repair with flow work.

### T6 — DEFECTIVE: D4, D7
Same shape as G10. The news is buried in a subject-plus-relative-clause and the
stress position holds `was deployed`; `Moreover` marks addition where the relation
is consequence — and a consequence the reader urgently needs flagged, since it
means their queries are silently returning nothing.

---

## Scoring

For Mode C, per item:

| Outcome | Score |
|---|---|
| Correct codes, correct spans | 2 |
| Right that it's defective, wrong code or span | 1 |
| Missed a defect | 0 |
| Marked a clean item defective | **−1** |
| Marked a D8 item and repaired it with flow work | **−1** |

The negative scores exist because false positives are the failure mode this
project creates. An over-corrector damages good prose, and that is worse than
leaving a defect in place.
