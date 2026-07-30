# Drills

Five protocols. Run §0 first — it decides whether the rest of the project is
aimed at the right thing.

Volume guidance anywhere below is a **conventional starting point, not a finding**.
Adjust from `LOG.md` after roughly three weeks of real data.

---

## §0 — Diagnostic (run once, before anything else)

**Purpose:** confirm the target before committing to it. This project assumes your
bottleneck is paragraph-level flow. That assumption is untested.

**Do not read `docs/02-patterns.md` or `docs/03-defects.md` before this drill.**
Knowing the taxonomy contaminates the sample — you would be testing whether you
can apply rules you just read, not what you produce by default. (The AI reads
them; you shouldn't, until §0 is scored and logged.)

### Tasks

**0a. Two paragraphs from briefs.** Write one paragraph for each brief below. No
AI, no dictionary, no revision beyond what you would normally do. **Time each one
and record it.**

> **Save an untouched copy** as `baseline/diagnostic-original.md` before you
> annotate, revise, or discuss either paragraph. The session-20 comparison is the
> only hard evidence this project will produce, and it is destroyed the moment you
> improve the original. Work on a copy, always.

> **Brief 1 (explanation, general).** A friend who is not technical asks why their
> home internet is fast for browsing but bad for video calls. Write one paragraph
> that answers them.

> **Brief 2 (professional, consequential).** You are on a team that shipped a
> change last Tuesday. A colleague in another team reports that a report they rely
> on has been showing stale numbers since then. You have confirmed the two are
> related and a fix is going out tomorrow. Write one paragraph replying to them.

**0b. Reorder.** Take a scrambled paragraph from `corpus/starter-general.md`
(item G7 is reserved for this). Reconstruct it. Write down *why* you placed each
sentence before checking the key.

**0c. Read back cold.** Wait at least one day. Re-read your two paragraphs and
mark anything you would now change. This measures your revision judgment
independently of your production.

### Decision rule

Have the AI annotate all three under the protocol in `AGENTS.md`, then:

**Compare 0a against 0b before reading the table.** They measure different things:
0b tests ordering on someone else's sentences, with zero production load. 0a tests
ordering while you are also fighting for words. The gap between them is the
finding, and it is not visible from either one alone.

| Finding | Verdict |
|---|---|
| Sentences are individually clear, but paragraphs lose their topic, shift direction unexplained, or leave relations implicit | **Target confirmed.** Proceed to §1. |
| Organization holds, but sentences are the struggle — wrong words, broken grammar, unclear meaning at the clause level | **Target wrong.** Stop this project; the bottleneck is sentence production. |
| **0b strong, 0a paragraphs very short** | **Target confirmed, with a constraint.** The ordering model is better than your production shows — it is being suppressed by production load, not missing. Short simple sentences cannot carry most flow defects, so drilling on them measures nothing. Apply the minimum-complexity rule in §4 from session one. |
| Both are weak, and 0a paragraphs are of normal length | Proceed, but run §4 more often than §1. |
| Both are strong | The gap is calibration, not skill. Go write your high-stakes document yourself and stop practicing. |

**A note on why this drill exists if you already know the answer.** If you can
already say "both my sentences and my flow are weak," the *gate* above tells you
nothing you didn't know. Two things still make §0 worth doing: it produces the
untouched baseline for the session-20 comparison, and the **0a/0b contrast** is
not something self-report can generate. Self-assessment gives you a verdict on
each ability separately. It cannot tell you that one of them collapses only under
load — which is a different problem with a different fix.

Record the verdict at the top of `LOG.md`. Re-run §0 after roughly 20 sessions
with fresh briefs, and compare.

---

## §1 — Mode A: Analyze supplied prose

**Builds:** recognition. **Type:** fluency on re-used items, generality on fresh.

Called "analyze known-good" in an earlier version. That was wrong and it leaked:
the corpus contains defective items, the prediction step asks you for
`clean / defective / uncertain`, and being told in advance that the paragraph is
sound answers the question the drill is asking.

1. Take a paragraph from the corpus or from real published prose (`corpus/sources.md`).
   **Tier 2 (`starter-technical.md`) is the starting tier** — see its header for
   why.
2. **Flag unknown terms.** Read the item once, then list any term you are not sure
   of. The AI glosses those and only those, **each term standalone** — it must
   never tell you that two terms share a referent, which would hand you a D5.

   Do this before the prediction, not after. A defect you could not see because
   you could not read the words was never a flow measurement, and the flag is
   what separates the two. Carry `terms flagged` to `LOG.md`; see
   `docs/vocabulary-interface.md` for how the count is read.

   Flagging nothing is a legitimate answer. If you flag nothing and then miss a
   defect that turned on a term, **check the term afterwards** — not flagging it
   shows you believed you understood it, not that you did. Three outcomes, and
   only one of them is a vocabulary miss; see `docs/vocabulary-interface.md`.
3. **Predict.** Commit three specific claims in writing before analyzing:
   1. **One named transition** — which sentence pair you expect to carry the
      paragraph's main move, and which pattern it uses
   2. **Verdict** — clean / defective / uncertain, plus confidence
   3. **One reader assumption** — something the writer is taking as already known

   Not "which pattern dominates." `02-patterns.md` says to name patterns *per
   transition* because mixed paragraphs are normal, so asking for a dominant
   pattern contradicts the project's own doctrine and invites a vague answer that
   cannot be scored as hit or miss.

   Three claims, under a minute. This is the highest-value step in the drill.
4. Annotate it yourself, **before** the AI sees it, using
   `docs/04-annotation-format.md`. The AI hands you a pre-parsed sheet — subjects
   quoted but **never resolved**, clause boundaries marked, every clause quoted
   verbatim and lettered — and fills nothing else. You fill `Ties back by` and
   `Pattern`, plus `Antecedent` where a pronoun points back, **one rotating lens
   question**, and the two closing lines.

   If the AI hands you a paraphrase rather than a quote, or writes `= referent` in
   a subject bracket, reject the sheet — it has answered part of the drill.

   Per-sentence fields are quotes or picks. If you are composing prose into one,
   the field is wrong and it gets cut and logged. `Alternative reading` is free
   response by design; `Uncertainty` is a quoted term plus one clause.

   **Predictions are locked once written.** If your verdict changes during
   analysis, that change *is* the finding — record it as a revision underneath
   the original, never over it. A prediction edited after the fact cannot be
   scored as a hit or a miss, and the prediction hit rate is the only measure in
   Mode A that familiarity with the corpus cannot inflate.
5. **The AI hands over its own filled sheet and the key** (`AGENTS.md` R15). Your
   prediction is locked and your sheet is done, so nothing arriving now can inflate
   either. Compare all three readings: yours, the AI's, and the reference.
6. Where two patterns are defensible, say what would distinguish them.

**There is no contest step, and `Defended disagreements` is not scored.** An earlier
version made contesting a mandatory stop between the AI's reading and the key. It ran
three sessions and returned zero every time, twice while arguable points were named
explicitly — and this file already conceded why: *with no independent model yet, a
manufactured disagreement is noise.* A step whose honest output is silence is asking
you to perform a disagreement you do not have.

What protects you instead is an obligation on the AI: **every code it names is quoted
to a span.** No judgment without the words that carry it. If you do disagree, that is
worth more than the score was — record it in the session notes.

**Do not** try to prove every paragraph follows one chain. Comparing *different*
patterns is the point of this drill.

### Scoring — Mode A

Record all three numbers. A single blended score hides which part is moving.

| Measure | How |
|---|---|
| **Pattern agreement** | transitions where your label matches the reference ÷ total transitions |
| **Prediction hit** | did step 3 match what you found? Y / partial / N |
| **Lens** | which lens ran this item — R / S / J. Not scored; tracked so the rotation can be audited |

The prediction hit rate is the number to watch. Agreement can rise from
familiarity with the corpus; prediction accuracy on *fresh* items cannot.

**Disagreements are noted, not scored.** If you argued a reading from the text and it
held, write it in the session notes. It is not a column, and its absence is not
deference — see the note above.

Starting volume: **one paragraph**, ~10 minutes. README's arc says one Mode A item
in sessions 1–2, and this line previously said two — the arc wins. Two paragraphs
is a later volume, once the sheet is automatic.

---

## §2 — Mode B: Reorder scrambled propositions

**Builds:** ordering, independent of sentence production.

1. Take a scrambled item. Reconstruct the paragraph.
2. **Write your reasoning for each placement before revealing the key.**
3. Compare with the reference order.
4. Where you differ: decide whether your order is *also valid*. Often it is. Have
   the AI argue both sides under R4 rather than announcing a winner.

This drill isolates ordering from language production, which is why it is worth
doing even on days when writing feels impossible.

### Scoring — Mode B

| Measure | How |
|---|---|
| **Exact order match** | Y / N. Coarse, and not the main signal |
| **Reasoning hits** | placements where your stated reason matches the structural reason in the key ÷ total placements |
| **Valid alternative** | if you differed, did your order survive scrutiny? Y / N |

**Reasoning hits, not order match, is the score that matters.** Getting the right
order for the wrong reason is a guess that happened to land, and it will not
transfer. Getting a defensible different order for a stated structural reason is a
better outcome than matching the key by feel.

Starting volume: one item, ~10 minutes.

---

## §3 — Mode C: Repair diagnosed disruptions

**Builds:** the bridge from recognition to production.

1. Take a defective item. **Do not look at which defects it contains.**
2. **Flag unknown terms first**, exactly as in §1 step 2. The AI glosses them
   standalone and never states that two terms share a referent. Repair drills are
   more exposed to this than analysis drills: you cannot restore a lexical chain
   you cannot see, and you may "repair" a term you simply misread.
3. Diagnose: mark each problem with a code from `docs/03-defects.md`, and quote
   the span.
4. Repair, preserving the meaning. You write the repair. The AI does not.
5. Explain each change: what the reader could not do before, and can now.
6. Compare against the key — both the defect codes and the reference repair.

**Rules for this drill:**

- Do not automatically add or remove connectives. Justify each by relation (R3).
- Some items contain **no defect**. Marking a clean item as defective is a
  scored error, not a neutral outcome.
- Some items contain a **D8** (coherence). The correct response is to say the
  content is broken and refuse to fix it with flow repair.

### Scoring — Mode C

Per-item scoring is in `corpus/KEYS.md`. Carry two numbers to the log: the item
score, and the **false-positive count** (clean items marked defective) tracked
separately. A rising item score with a rising false-positive count is not
improvement, it is D9.

Starting volume: one or two items, ~15 minutes.

---

## §4 — Mode E: Produce for a specified reader

**Builds:** generality. **The drill that actually moves production, and the one you
will be most tempted to skip.**

### The sequence

**Nine steps, in order, with nothing interrupting them.** An earlier version of this
section put a four-step grading block in the middle of the numbered list, and then
resumed at 3 — so the file had two overlapping sequences and never said who scored
the first draft or when. That ambiguity cost a session.

1. **Take a fresh brief** — purpose, reader, what the reader already knows, what they
   need to be able to do afterwards. Never reuse a brief.
2. **Write one paragraph, cold and timed.** No AI. Bracket what you cannot retrieve
   (below) and keep going. **Then lock the draft**: it is the measured artifact, and
   editing it later makes every score untraceable.
3. **Annotate the locked draft** using `docs/04-annotation-format.md` — **or ask for the
   reference sheet first and study it, then annotate. Or skip the sheet entirely.**
   All three are legitimate; see the box below. Record what you caught yourself.
4. **Resolve the brackets, without reorganizing anything.** This is the load-bearing
   constraint in the whole drill. Fill the lexical gaps and change nothing else; if
   you restructure here, the first draft and its annotation stop describing the same
   paragraph.
5. **Revise, from your own annotation.** Yours, not the AI's — this is a second
   version, and the first one stays frozen.
6. **The AI hands back a filled reference sheet and scores both frozen versions** —
   pointing and naming only, never a rewrite (R1). The reference sheet is mandatory
   (`AGENTS.md` R15): same sheet, same material, every field, plus a field-by-field
   comparison. It scores the first draft on all seven rubric items and the self-revised
   draft on the same seven, so the two are comparable.
7. **Revise again if you want to.**
8. **The AI presents two or three complete alternative versions, with the trade-off of
   each** (`AGENTS.md` R1). This is the only point in the drill where it writes the
   paragraph, and it comes *after* both your rubric scores are final, so it cannot
   substitute for your production. **Never one version** — one reads as the answer,
   several read as a space to choose inside. They are unvalidated AI prose and any of
   them may be worse than yours.
9. **Export and log.** Route each bracket to 2a / 2b / 3, and count the `2b-avoided`
   cases that produced no bracket at all.

> ### The self-check steps are skippable, and there are two legitimate orders
>
> **Reference first** — the AI fills the sheet, you study it, then you annotate.
> **Attempt first** — you fill it, then the AI hands its version over.
> **Skip** — no sheet this session; go straight to the reference sheet and the score.
>
> You choose, per session and per field. None of the three is the disciplined option
> and none is the lazy one.
>
> **Why "attempt first" was the only order for three sessions, and why that was wrong.**
> The rule came from `prediction hit` in Mode A, where committing before you look is
> what makes the number scoreable. It got carried into the Mode E sheet, where nothing
> is scored except `self-caught` — so the measurement argument does not apply, and what
> remains is unguided problem-solving before any schema exists. That imposes search load
> which crowds out the learning the step is for. The **worked-example effect** says the
> efficient order for a novice is: study a correct example, then attempt with fading
> support. Session 3 is the demonstration — `Ties back by` answered wrong five times in
> one consistent direction, and the schema arrived from a prose explanation afterwards,
> not from the attempting.
>
> **The counter-argument, which is not worthless.** Attempting before seeing the answer
> improves retention even when the attempt fails — the generation effect, and productive
> failure. But that finding requires enough prior knowledge to produce *meaningful*
> attempts. Five identical wrong answers is not productive failure, it is floundering,
> which is what the **expertise-reversal effect** predicts at this stage.
>
> **So the order is a function of expertise, not of virtue.** Reference-first while a
> field is still being learned; attempt-first once you can fill it and agree with the
> reference. Flip when you agree on that field across two consecutive sessions — the
> same trigger shape as the scaffold fade in `AGENTS.md`.
>
> **What this costs, recorded honestly.** `Pattern agreement` and `self-caught` from a
> reference-first session are **not comparable** to an attempt-first session — you cannot
> be credited with catching what you were shown. Log which order ran, and never place
> the two side by side as though they measured the same thing. A run of reference-first
> sessions will make `self-caught` meaningless, and that is the price of building the
> schema first; the number becomes real again when you switch back.

**Who scores, and why the order is this way.** The AI scores, because `self-caught`
is defined as the defects you found *before* the AI and that number needs a
denominator that arrives afterwards. The brackets are resolved before scoring
because rubric items 4 and 7 — unambiguous antecedents, accurate transitions —
cannot be judged while the referring expression or the connective is still
`[ENG: …]`. Lexical choice *is* part of reference and relation signalling.

An earlier version scored items 1, 2, 3, 5, 6 first and marked 4 and 7 provisional,
resolving brackets in between. That dance is no longer needed: the draft is frozen
at step 2, so nothing about the scoring order can influence how you wrote it, and
by step 6 all seven items are directly scorable. The concern it was built to answer
— *if word choice is judged in the same breath as flow, you simplify to protect the
score* — is now handled by the freeze rather than by the sequence.

> ### No prediction step in Mode E
>
> Modes A, B and C each commit to something before the answer is available, and in
> Mode A that commitment is a prediction and the highest-value step in the drill.
> **Mode E commits to nothing, and asking it to is an error.**
>
> In Mode A the paragraph is fixed before you look at it, so `clean / defective` has
> an answer you can be right or wrong about. In Mode E you are the author.
> "Which defect will you produce?" asks you to forecast your own failure while
> trying to avoid it, and the honest answer is always *none* — if you could name the
> defect in advance you would not write it. An answer that can take only one value
> is not a measure. *Which rubric item will fail* has the same problem.
>
> **The reason for excluding the planning variants is narrower, and it is worth
> stating precisely.** Committing *the point in one line* or *the reader's active
> question* does **not** hand you rubric marks 1 and 6 — an earlier version of this
> file claimed that and overstated it. The brief already supplies the purpose and the
> `needs to be able to` line, so restating them grants nothing; and item 1 asks
> whether the *paragraph* makes the point identifiable, which a private note before
> writing does not settle. Choosing which of the supplied facts is the point would be
> a real planning act, and a defensible drill.
>
> It is excluded because **pre-writing planning changes the construct being
> measured.** The number this project watches is delayed *cold* first-draft quality,
> and §0 set that baseline cold. Add a planning step and you are measuring planned
> first-draft quality — plausibly a more useful ability, but a different one, with no
> baseline to compare against and no comparability with the session-20 re-run.
>
> **What replaces it: nothing.** The draft is written cold.
>
> **One cost, recorded honestly.** A pre-writing commitment would have separated *no
> point* from *a point lost while writing* — different problems with different fixes,
> and the annotation alone cannot tell them apart. The substitute is the **intent
> gap** note after the annotation: what you meant the paragraph to do versus what the
> sheet shows it does. Weaker, because it is reconstructed after the fact. If the log
> shows drift recurring and the intent gap failing to catch it, a pre-commitment
> earns its way back in — as a candidate, not a plan.
>
> `Pred. hit` is therefore blank on Mode E rows in `LOG.md`, the way
> `First-draft rubric` is blank on Mode A rows.

> ### Complexity floor — two Mode E variants
>
> An earlier version required "five sentences, two with subordinate clauses."
> That was the wrong lever: a syntax quota is satisfiable by writing one bad
> convoluted sentence, and it teaches that longer syntax is better — which
> contradicts everything else here.
>
> The requirement is **structural opportunity**, not sentence length. Alternate
> between two variants:
>
> **E-Expand** (default early; most sessions). The brief must yield:
>
> - at least **five propositions** — distinct things being asserted
> - at least **one entity referred to three or more times**, so a lexical chain
>   can exist to break
> - at least **one non-additive relation** — contrast, cause, concession,
>   qualification. Not a list
>
> These are checkable without judgment, and none of them rewards padding. Below
> this floor the drill returns a clean score that means nothing, and you conclude
> you have no flow problem.
>
> **E-Concise.** Two to four sentences under a realistic professional constraint —
> a Slack reply, a commit message, a one-line escalation. Run this roughly every
> third session.
>
> E-Concise exists because your target genre is often short, and because a project
> that only ever rewards expansion will teach you to pad. Different defects surface
> here: D4 dominates, because with three sentences every position is load-bearing.
>
> If word-choice anxiety pushes you to truncate inside E-Expand, note that
> avoidance **manufactures** D3: stripping sentences down forces every relation
> onto bare juxtaposition, which is the parataxis habit this project exists to
> correct.
>
> **On translation tools:** checking a single word you have already chosen is
> fine. Composing a sentence in your L1 and translating it is not — that trains a
> translation model, which is a different mapping and the one that produces
> L1-shaped English. If you reach for it mid-sentence, use the bracket protocol
> below instead.

### The bracket protocol

**While writing, when you stall on a word:** write `[ENG: what you mean, in any
form — your L1, a paraphrase, a guess]` and keep going. Do not stop. Do not open
anything.

> We confirmed the cause on Tuesday and the fix ships tomorrow. The report was
> `[ENG: 取数 from]` the old table until Wednesday.

This is not a workaround. It does two jobs:

1. **It protects the measurement.** The paragraph reaches full length with holes in
   it, and a paragraph with holes still has an information structure that can be
   annotated and scored. Truncating to words you're sure of — what happened in §0 —
   destroys the flow signal entirely
2. **It is the vocabulary diagnostic.** Each bracket, resolved afterwards, sorts
   into a category that self-report cannot distinguish from the inside

**Afterwards**, resolve each bracket and route it:

| On looking it up | Link | Action |
|---|---|---|
| "Right — I knew that word" | **2a** retrieval | Cloze it into a *novel* sentence. A production drill, not a recognition card |
| "I didn't know that word at all" | **2b** acquisition | Into the acquisition stream. Log it; do not expect this project to fix it |
| "I knew it, wasn't sure it fit here" | **3** collocation | Check two or three real collocations; note the boundary in one line |

Tally the three counts in `LOG.md`. The **ratio** is the point — see
`docs/vocabulary-interface.md` for what each ratio implies. Ten sessions gives
you a number that no amount of introspection will.

**Step 3 is what converts this from "writing practice" into model construction.**
Skipping it turns the drill into unpaired production, which builds fluency in your
current defects and nothing else.

**Step 4 is the one that quietly destroys a measurement.** Resolving a bracket is
filling a lexical gap. Reorganizing is a different act, it belongs in step 5, and
doing it during step 4 means the first draft and its annotation no longer describe
the same paragraph.

### Scoring — Mode E

**Use the seven-item production rubric from `tests/verification-01.md` Part 3,
every time.** Not a different rubric, not an impression. Using the same instrument
for routine production and for the verification test is what makes the two
comparable — otherwise the test measures against a baseline that does not exist.

### Structure profile — read the score against it, never prescribe it

Record the count of `simple / compound / complex / compound-complex` sentences in the
draft. The instrument does this automatically from the sheet.

**This is a coverage measure, not a target.** It says which defects were *available to
be made*, and therefore which parts of the rubric a clean score is evidence about.

| Profile | What a clean score does and does not tell you |
|---|---|
| Mostly **simple** | Items 4 and 7 were barely tested — D1 needs candidate antecedents and D7 needs connectives, and short simple sentences supply neither. Item 5 was tested *harder* than usual, because unjoined clauses leave every relation to juxtaposition |
| Mostly **complex** | D4 was live throughout: every subordinate clause is somewhere the news can hide |
| One sentence carrying 4+ propositions | Expect D3 there specifically. A sentence already holding four things has nowhere left to put a relation |

Session 3 is the worked case: four of seven sentences simple, no D4 produced, and the
one D3 sitting in the single 40-word compound-complex sentence. Reporting "no D4" from
that draft would have been reporting that the defect was unavailable.

**Do not turn this into a quota.** An earlier version of this file required "five
sentences, two with subordinate clauses", and that was wrong for reasons that still
hold: a syntax quota is satisfied by one bad convoluted sentence, and it teaches that
longer syntax is better. The complexity floor stays a property of the **brief** —
whether the structural opportunity exists. The profile is a property of the **draft**,
and it is read, not required.

Carry to the log:

| Measure | Why |
|---|---|
| **First-draft rubric** | out of 7, scored on the draft *before* your own revision. **This is the primary measure** — the goal is producing good first drafts, not detecting bad ones |
| **Structure profile** | counts by sentence type. Tells you which rubric items a clean score is evidence about, and which were untested |
| **Self-revised rubric** | out of 7, after your own revision, before the AI sees it |
| **Self-caught** | defects you found in your own annotation, before the AI |
| **False positives** | things you "fixed" that were not defects |
| **Time to first draft** | proceduralization shows up only here. Quality can be bought with time; fluency cannot |
| **Bracket count** | lexical load on this brief |

An earlier version called `self-caught ÷ total defects` the single most
informative ratio here. That was wrong twice over: its denominator is the AI's
defect count, which R10 says is unvalidated — so the headline metric rested on the
grader the project itself distrusts — and it can rise while first drafts stay flat,
which would mean you are getting better at spotting errors you keep making.

Read it as one of a panel. **Delayed first-draft quality is the evidence that
matches your goal**; self-caught is a supporting signal about your revision model.

Starting volume: one paragraph, ~20 minutes including annotation.

---

## Session shapes

Two modes maximum per session.

| Shape | Modes | When |
|---|---|---|
| Standard | A + E | Default. Recognition then production |
| Diagnostic-heavy | A + C | Early weeks, while the defect codes are still unfamiliar |
| Production-heavy | C + E | Once recognition scores plateau |
| Light | B alone | Low-energy days. Still counts |

If three consecutive sessions contain no Mode E, the ratio is wrong. `AGENTS.md`
instructs the AI to flag this.
