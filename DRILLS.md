# Drills

Run the diagnostic once before the training modes. After that, run no more than
two modes in one session. Session counts and volumes are starting points; adjust
them from `LOG.md`.

## §0 — Diagnostic

**Purpose:** test whether paragraph-level information flow is the learner's actual
bottleneck.

The learner must not read `docs/02-patterns.md` or `docs/03-defects.md` until this
diagnostic is scored and logged. The drill partner may read them.

### Tasks

1. **Two cold paragraphs.** The learner writes one paragraph for each brief without
   AI, a dictionary, or unusual revision. Time both.

   - **General explanation:** A non-technical friend asks why their home internet is
     fast for browsing but poor for video calls.
   - **Professional reply:** Another team reports stale numbers since your team
     shipped a related change last Tuesday. You confirmed the link and a fix ships
     tomorrow.

2. Save the untouched paragraphs as `baseline/diagnostic-original.md` before any
   annotation, revision, or discussion. Work only on a copy afterwards.
3. **Reorder:** reconstruct item G7 from `corpus/starter-general.md`. Give a reason
   for every placement before checking the key.
4. **Cold re-read:** wait at least one day, then mark what the learner would change
   in the two paragraphs.
5. Annotate all three artifacts under `AGENTS.md` and compare production with
   reordering before choosing a verdict.

### Decision rule

| Evidence | Verdict |
|---|---|
| Clear sentences, but topic, direction, or relations break across the paragraph | Target confirmed; proceed |
| Organization holds, but word choice, grammar, or clause-level meaning dominates | Stop; train sentence production instead |
| Reordering is strong and the produced paragraphs are very short | Target confirmed under production load; use the Mode E structural-opportunity floor from session one |
| Both are weak and the produced paragraphs have normal length | Proceed, but use Mode E more often than Mode A |
| Both are strong | Stop drilling; paragraph flow is not the bottleneck |

Record the verdict at the top of `LOG.md`. Re-run the diagnostic after roughly 20
sessions with fresh briefs and compare it with the untouched baseline.

## §1 — Mode A: Analyse Supplied Prose

**Builds:** recognition. Reused items build fluency; fresh items build generality.

1. Choose one Tier 2 technical paragraph by default. It may be clean or defective;
   do not tell the learner which.
2. Ask the learner to flag unknown terms. Gloss only flagged terms, one by one,
   without revealing that two terms share a referent.
3. Lock this three-part prediction, written in under a minute:
   - one sentence transition expected to carry the main move, with its pattern;
   - `clean`, `defective`, or `uncertain`, with confidence;
   - one reader-knowledge assumption.
4. Offer the annotation order from `AGENTS.md`: reference first, attempt first, or
   skip. Generate and use the Mode A instrument. The learner's prediction remains
   locked in every order.
5. Supply your completed reference sheet. If the learner also completed a sheet,
   compare the two field by field.
6. Reveal the key only after the prediction is locked and the learner's sheet is
   complete or skipped. Compare the learner's prediction, all completed sheets, and
   the key.
7. For every defect code, quote the span. When two patterns or orders are valid,
   state what reader question or emphasis would favour each.

Do not ask for a dominant paragraph pattern. Label patterns per transition. Do not
ask the learner to manufacture a disagreement.

### Mode A score

| Measure | How to record it |
|---|---|
| Pattern agreement | Matches with the reference ÷ scored transitions; void after reference-first or skip |
| Prediction hit | `Y`, `partial`, or `N`; valid in every annotation order |
| Lens | `R`, `S`, or `J`; tracked, not scored |

Start with one paragraph and about ten minutes.

## §2 — Mode B: Reorder Scrambled Propositions

**Builds:** ordering without sentence-production load.

1. Give one scrambled item without its key.
2. The learner chooses an order and locks a reason for every placement.
3. Reveal the reference order.
4. Compare the reasons. If the order differs, test whether it is also valid and
   state the trade-off instead of assuming the key is uniquely correct.

### Mode B score

| Measure | How to record it |
|---|---|
| Exact order match | `Y` or `N`; coarse, not the main signal |
| Reasoning hits | Placements whose reason matches the key's structural reason ÷ total placements |
| Valid alternative | If the order differs, `Y` or `N` after testing it |

Start with one item and about ten minutes.

## §3 — Mode C: Repair Diagnosed Disruptions

**Builds:** the bridge from recognition to production.

1. Give one item without saying whether it is defective.
2. Ask the learner to flag unknown terms and gloss only those terms, standalone.
3. The learner locks a verdict: `clean`, `defective`, or `D8`. For every claimed
   defect, he supplies a code and quoted span.
4. If repair is appropriate, the learner writes it and explains what the reader
   could not do before and can do now.
5. Reveal the key and compare the verdict, codes, spans, and repair.

Mode C has no annotation sheet, lens, or prediction. Some items are clean; marking
one defective is a false positive. For D8, stop flow repair and name the content
problem. Apply the connective rule and D9 check from `AGENTS.md`.

### Mode C score

Use the item score in `corpus/KEYS.md`. Log false positives separately. A rising
item score with rising false positives is D9, not improvement.

Start with one or two items and about fifteen minutes.

## §4 — Mode E: Produce for a Specified Reader

**Builds:** generation on new material.

### Sequence

1. Generate a fresh brief that states the purpose, reader, known facts, and what the
   reader must be able to do afterwards. Never reuse a brief.
2. The learner writes one cold, timed paragraph without AI. He uses brackets for
   missing words and keeps going. Lock this first draft.
3. Offer reference first, attempt first, or skip for the annotation sheet. Record
   the order and what the learner caught before seeing your sheet.
4. Resolve brackets without reorganizing the paragraph. The first draft remains
   frozen.
5. The learner revises from his own annotation, producing a separate second
   version.
6. Return your filled reference sheet and score both frozen versions with the same
   seven-item rubric from `tests/verification-01.md` Part 3. Quote evidence for each
   failed item. Do not write a replacement paragraph.
7. The learner may revise again.
8. After both rubric scores are final, give two or three complete alternative
   versions with different progression or emphasis choices. State the trade-off of
   each and label them as unvalidated comparisons, not answers.
9. Export the markdown record and log the session. Classify every bracket as 2a,
   2b, or 3 and count `2b-avoided` cases.

Mode E has no prediction or planning step. The target measure is cold first-draft
quality, so pre-writing planning would change the construct. After annotation,
record the **intent gap**: what the learner meant the paragraph to do versus what
the sheet shows it does.

### Annotation order

- **Reference first:** use while a field is still being learned. `Self-caught` is
  void.
- **Attempt first:** use after two consecutive agreements on that field.
  `Self-caught` is valid.
- **Skip:** the learner receives the reference sheet and score. `Self-caught` is
  void.

Both rubric scores remain valid in all three orders because they score drafts
written before any sheet was shown.

### Structural-opportunity variants

Alternate between these variants. Do not prescribe sentence length or syntax.

**E-Expand** is the early default. The brief must naturally require:

- at least five propositions;
- one entity mentioned at least three times;
- one non-additive relation such as cause, contrast, concession, or qualification.

**E-Concise** uses a realistic two-to-four-sentence constraint such as a chat reply,
commit message, or escalation. Run it about every third Mode E session.

These are properties of the brief, not quotas for the draft.

### Bracket protocol

When a word does not come during drafting, write:

```text
[ENG: intended meaning in your L1, a paraphrase, or a guess]
```

Do not stop to search. Resolve each bracket only after the draft is locked:

| Result after lookup | Category | Follow-up |
|---|---|---|
| The word was known but unavailable | 2a retrieval | Use it in a new cloze sentence |
| The word was not known | 2b acquisition | Send it to the separate acquisition stream |
| The word was known but its fit was uncertain | 3 collocation | Check two or three real collocations |

Also count places where the learner deliberately simplified because the wanted
word was unknown as `2b-avoided`. Do not interpret the category ratio below 30
total brackets; see `docs/vocabulary-interface.md`.

### Mode E score

Use the seven-item production rubric in `tests/verification-01.md` Part 3 for every
session.

| Measure | Meaning |
|---|---|
| First-draft rubric | Primary measure, out of 7, before learner revision |
| Structure profile | Counts of simple, compound, complex, and compound-complex sentences; coverage evidence, not a target |
| Self-revised rubric | Out of 7, after learner revision and before AI feedback |
| Self-caught | Defects found before the reference sheet; void after reference-first or skip |
| False positives | Working text changed as though defective |
| Time to first draft | Fluency signal |
| Bracket count | Lexical load |

Read a clean score against the structure profile. Mostly simple sentences provide
little evidence about antecedent ambiguity or connective accuracy; complex
sentences expose emphasis; a sentence carrying four or more propositions exposes
buried relations. Never turn the profile into a syntax quota.

Start with one paragraph and about twenty minutes including annotation.

## Session Shapes

| Shape | Modes | Use |
|---|---|---|
| Standard | A + E | Early recognition followed by production |
| Diagnostic-heavy | A + C | While defect codes are unfamiliar |
| Production-heavy | C + E | When recognition has plateaued |
| Light | B | Low-load session |

If three consecutive sessions contain no Mode E, shift the ratio toward Mode E.
