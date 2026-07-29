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
| Both are strong | The gap is calibration, not skill. Go write the cover letter yourself and stop practicing. |

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

## §1 — Mode A: Analyze known-good paragraphs

**Builds:** recognition. **Type:** fluency on re-used items, generality on fresh.

1. Take a paragraph from the corpus or from real published prose (`corpus/sources.md`).
2. **Predict first.** Commit three specific claims in writing before analyzing:
   1. **One named transition** — which sentence pair you expect to carry the
      paragraph's main move, and which pattern it uses
   2. **Verdict** — clean / defective / uncertain, plus confidence
   3. **One reader assumption** — something the writer is taking as already known

   Not "which pattern dominates." `02-patterns.md` says to name patterns *per
   transition* because mixed paragraphs are normal, so asking for a dominant
   pattern contradicts the project's own doctrine and invites a vague answer that
   cannot be scored as hit or miss.

   Three claims, under a minute. This is the highest-value step in the drill.
3. Fill the annotator table yourself — role, departure point, link, new
   contribution, relation, pattern. **Before** the AI sees it.
4. Have the AI produce its own annotation.
5. Compare. Disagreements are the lesson, and the AI is not automatically right —
   make it defend any difference against the text.
6. Where two patterns are defensible, say what would distinguish them.

**Do not** try to prove every paragraph follows one chain. Comparing *different*
patterns is the point of this drill.

### Scoring — Mode A

Record all three numbers. A single blended score hides which part is moving.

| Measure | How |
|---|---|
| **Pattern agreement** | transitions where your label matches the reference ÷ total transitions |
| **Defended disagreements** | count of differences where you argued your reading from the text and it held. These are *positive* — a high agreement rate with zero defended disagreements means you are deferring to the AI |
| **Prediction hit** | did step 2 match what you found? Y / partial / N |

The prediction hit rate is the number to watch. Agreement can rise from
familiarity with the corpus; prediction accuracy on *fresh* items cannot.

Starting volume: two paragraphs, ~10 minutes.

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
2. Diagnose: mark each problem with a code from `docs/03-defects.md`, and quote
   the span.
3. Repair, preserving the meaning. You write the repair. The AI does not.
4. Explain each change: what the reader could not do before, and can now.
5. Compare against the key — both the defect codes and the reference repair.

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

1. Take a situation brief — purpose, reader, what the reader already knows, what
   they need to be able to do afterward. Generate fresh briefs; never reuse.
2. Write one paragraph. **Time it.** No AI during writing.

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
> **On the translate app:** checking a single word you have already chosen is
> fine. Composing a sentence in your L1 and translating it is not — that trains a
> translation model, which is a different mapping and the one that produces
> L1-shaped English. If you reach for it mid-sentence, use the bracket protocol
> below instead.

### The bracket protocol

**While writing, when you stall on a word:** write `[ENG: what you mean, in any
form — Chinese, a paraphrase, a guess]` and keep going. Do not stop. Do not open
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
`docs/05-vocabulary-interface.md` for what each ratio implies. Ten sessions gives
you a number that no amount of introspection will.

### Grading order — four steps, not two passes

An earlier version said "score flow, ignore brackets entirely." That is not
possible. Rubric item 4 (references have unambiguous antecedents) and item 7
(transitions accurate and necessary) cannot be scored while the referring
expression or the connective is still `[ENG: …]`. Lexical choice *is* part of
reference, chain, and relation signalling.

But the reason for separating them still holds: if word choice is judged in the
same breath as flow, you simplify to protect the score — the behaviour that
produced four-sentence paragraphs in §0. So sequence rather than separate:

1. **Score what brackets cannot touch.** Proposition order, sentence roles,
   intended relations, whether the point is identifiable, whether the ordering
   serves the reader's task. Rubric items 1, 2, 3, 5, 6
2. **Mark items 4 and 7 provisional.** Do not guess them
3. **Resolve the brackets** — and **do not reorganize the paragraph while doing
   it.** This is the load-bearing constraint. If you restructure while filling
   gaps, the step-1 score becomes untraceable and you have measured nothing
4. **Finalize items 4 and 7** against the resolved text

Then route the brackets by type as above. Bracket routing is a separate activity
from grading and happens after all four steps.
3. Annotate your own information flow before showing anyone. Fill the table for
   your own paragraph.
4. Revise, based on your own annotation.
5. *Then* get AI feedback — pointing and naming only, no rewriting (R1).
6. Revise again yourself.

Step 3 is what converts this from "writing practice" into model construction.
Skipping it turns the drill into unpaired production, which builds fluency in your
current defects and nothing else.

### Scoring — Mode E

**Use the seven-item production rubric from `tests/verification-01.md` Part 3,
every time.** Not a different rubric, not an impression. Using the same instrument
for routine production and for the verification test is what makes the two
comparable — otherwise the test measures against a baseline that does not exist.

Carry to the log:

| Measure | Why |
|---|---|
| **First-draft rubric** | out of 7, scored on the draft *before* your own revision. **This is the primary measure** — the goal is producing good first drafts, not detecting bad ones |
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
