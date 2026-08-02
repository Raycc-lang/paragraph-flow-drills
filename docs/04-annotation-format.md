# Annotation Format

This format is used in Mode A and Mode E. Mode C does not use an annotation sheet
or lens.

The learner points at text or chooses from a list. He does not compose English
metalanguage in per-sentence fields. The only free-response fields are
`Alternative reading` and `Uncertainty`.

## Division of Work

For Mode A, the drill partner may pre-parse only material that can be copied from
the paragraph:

- the sentence verbatim;
- its grammatical subject, quoted but not resolved;
- material before the subject;
- clause boundaries and verbatim clause spans.

The drill partner must not:

- resolve a pronoun or demonstrative;
- paraphrase a clause;
- change passive voice, nominalization, or word order;
- name the relation, role, pattern, or defect in a learner field.

If a line cannot be made by copying characters from the paragraph, it does not
belong in the Mode A pre-parse.

In Mode E, the page splits the learner's own draft into sentences. The learner can
correct sentence boundaries and records `Sentence type` and `Parts`; there is no
clause-lettering task.

## Per-Sentence Fields

### Starts from

Record the grammatical subject and any material before it separately. In Mode A,
these are read-only quotes supplied by the drill partner. In Mode E, the learner
selects them from the draft.

### Ties back by

Choose one answer for each transition:

| Answer | Meaning | Typical verdict |
|---|---|---|
| Quote the linking word | A device is present and works | Clean |
| `no explicit word, reader infers it` | No word carries the link, but the relation is recoverable | Clean |
| `there is a word but it fails` | A device is present but does not resolve | D1 or D5 |
| `nothing connects it` | No route from prior context is available | D2 or D6 |
| `opening` | First sentence | Not scored as a transition |

Look for a device before choosing `no explicit word`. A pronoun with several live
referents is a present device that fails, not an absent device.

### Antecedent

Use this field only when `Ties back by` identifies a pronoun or demonstrative.
Select its referent from an earlier sentence. `cannot pick` is a valid answer and
usually indicates D1.

The antecedent may be several sentences back. It cannot be inside the sentence
that contains the pointing expression, because this field measures links to prior
text.

### Pattern

Choose one pattern for each transition, or `opening`:

1. constant topic;
2. linear progression;
3. derived topics;
4. split progression;
5. contrastive progression;
6. question-answer progression.

Name the pattern per transition. A paragraph may mix patterns.

### Sentence Type and Parts

Mode E also records:

```text
Sentence type: simple / compound / complex / compound-complex
Parts: 1 / 2 / 3+ independent clauses
```

Use these as coverage evidence, not as targets:

| Observation | Defect made more available |
|---|---|
| Compound sentence with several candidate antecedents | D1 in the following sentence |
| Clauses joined by `and` despite cause, contrast, or concession | D3 or D7 |
| Complex sentence | D4 if the news is buried in subordination |
| One sentence carrying many propositions | D3 |

Do not prescribe a sentence-type quota.

## One Rotating Lens

Use one lens per item, rotating `R → S → J`. If a defect is repeatedly missed, run
its lens again on the next item instead of adding a second lens.

### Lens R: Relation

Use for D3 and D7 on the paragraph's main transition.

```text
Relation: cause / result / contrast / concession / qualification /
          addition / sequence / unclear
Signalled by: quote the connective, or `none`
Costs the reader: yes / no / uncertain
```

`unclear` indicates D3. A connective that signals a different relation from the
one selected indicates D7.

### Lens S: Stress

Use for D4. For each sentence, select the final constituent and choose:

```text
news / already known / uncertain
```

Already-known material in the stress position may indicate D4. The field is a
click and a closed choice; do not require transcription.

### Lens J: Job

Use for structure and D8. Choose one role per sentence:

```text
claim / context / evidence / qualification / consequence /
contrast / definition / instruction / transition / closing
```

Repeated roles or no identifiable claim may indicate a structure or coherence
problem. Confirm against the paragraph before assigning D8.

## Closing Fields

```text
Alternative reading: one line describing another plausible structure and what
                     would distinguish it
Uncertainty: quote a term or assumption, then state in one clause what the reader
             was assumed to know
```

These are the only free-response fields. `Uncertainty: none` is unusual whenever
the paragraph renames an entity or assumes shared knowledge; treat claims about
reader knowledge as inferences.

## Reference Sheet

When returning a reference sheet, the drill partner fills the same fields on the
same paragraph. If the learner also filled a sheet, compare every field. Quote the
text behind each defect code and mark judgment calls.

A reference sheet is required even when the learner uses reference-first or skips
his own sheet. What changes is the validity of the agreement or self-caught
measure; see `AGENTS.md`.

## Compact Example

> **[1]** The bakery on Mill Street closes for three weeks every January.
> **[2]** The owner uses the time to service the ovens, which run continuously for
> the rest of the year. **[3]** Regulars grumble, but the alternative is a
> breakdown in the middle of a Saturday morning.

```text
SENTENCE 1
Starts from: "The bakery on Mill Street"
Ties back by: opening
Pattern: opening

SENTENCE 2
Starts from: "The owner"
Ties back by: "The owner" and "the time"
Pattern: 3 derived topics

SENTENCE 3
Starts from: "Regulars"
Ties back by: "Regulars" and "the alternative"
Pattern: 3 derived topics

LENS R
Relation: contrast
Signalled by: "but"
Costs the reader: no

Alternative reading: Sentence 2 can be read as linear if attention rests on
                     "three weeks" and "the time" rather than on the bakery.
Uncertainty: "the alternative" — I assumed the reader sees a Saturday breakdown
             as worse than a planned January closure.
```

The example does not make `but` a contrastive-progression label. The contrast is
inside sentence 3; its departure point is still the derived topic `Regulars`.

## Change Test

Change this format only when session evidence shows that a field is failing. If a
per-sentence field still requires composed prose after three sessions, replace it
with a quote or closed choice. If annotation takes more than five minutes for one
paragraph, reduce it to `Ties back by` and record the change in `LOG.md`.

Keep the instruments dependency-free and single-file. Time spent maintaining the
tool is not drill time.
