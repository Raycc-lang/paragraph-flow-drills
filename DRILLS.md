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

| Finding | Verdict |
|---|---|
| Sentences are individually clear, but paragraphs lose their topic, shift direction unexplained, or leave relations implicit | **Target confirmed.** Proceed to §1. |
| Organization holds, but sentences are the struggle — wrong words, broken grammar, unclear meaning at the clause level | **Target wrong.** Stop this project; the bottleneck is sentence production. |
| Both are weak | Proceed, but expect slower returns, and run §4 more often than §1. |
| Both are strong | The gap is calibration, not skill. Go write the cover letter yourself and stop practicing. |

Record the verdict at the top of `LOG.md`. Re-run §0 after roughly 20 sessions
with fresh briefs, and compare.

---

## §1 — Mode A: Analyze known-good paragraphs

**Builds:** recognition. **Type:** fluency on re-used items, generality on fresh.

1. Take a paragraph from the corpus or from real published prose (`corpus/sources.md`).
2. Fill the annotator table yourself — role, departure point, link, new
   contribution, relation, pattern. **Before** the AI sees it.
3. Have the AI produce its own annotation under the full six-part protocol.
4. Compare. Disagreements are the lesson, and the AI is not automatically right —
   make it defend any difference against the text.
5. Name which progression pattern each transition uses. Where two patterns are
   defensible, say what would distinguish them.

**Do not** try to prove every paragraph follows one chain. Comparing *different*
patterns is the point of this drill.

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

Starting volume: one or two items, ~15 minutes.

---

## §4 — Mode E: Produce for a specified reader

**Builds:** generality. **The drill that actually moves production, and the one you
will be most tempted to skip.**

1. Take a situation brief — purpose, reader, what the reader already knows, what
   they need to be able to do afterward. Generate fresh briefs; never reuse.
2. Write one paragraph. **Time it.** No AI during writing.
3. Annotate your own information flow before showing anyone. Fill the table for
   your own paragraph.
4. Revise, based on your own annotation.
5. *Then* get AI feedback — pointing and naming only, no rewriting (R1).
6. Revise again yourself.

Step 3 is what converts this from "writing practice" into model construction.
Skipping it turns the drill into unpaired production, which builds fluency in your
current defects and nothing else.

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
