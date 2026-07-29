# Reader-Oriented Information Flow — Drill Project

A training project for one specific English writing ability: ordering and
expressing propositions so a reader can follow them.

Not vocabulary. Not grammar. Not naturalness. Not argument quality. Those are
real targets and this project deliberately excludes them, because a project that
targets everything measures nothing.

---

## Start here

1. Read `docs/01-target.md`. Ten minutes. It defines what is and isn't in scope.
2. **Run `DRILLS.md` §0, the diagnostic, before reading anything else in `docs/`.**
   Two paragraphs from briefs, one reorder, one cold re-read a day later. This
   decides whether the project is aimed at the right thing.
3. Record the verdict in `LOG.md`.
4. If confirmed, read `docs/02-patterns.md`, `docs/03-defects.md`, and
   `docs/04-worked-session.md`, then begin.

The order matters. Reading the defect taxonomy before the diagnostic contaminates
the sample — you would be testing whether you can apply rules you just read, not
what you produce by default.

---

## The arc after §0

Session counts below are conventional starting points, not findings. The log
overrides them.

### Sessions 1–2 — learn the instrument

Mode A on **one** item, then Mode E. The Mode A is not recognition training; it is
there so the annotation table and the defect codes become familiar enough to use on
your own draft. Drop it as soon as it is.

Mode E from session one, under the minimum-complexity rule, with brackets.

### Sessions 3–8 — the working shape

**Mode C + Mode E.** C gives you defect codes on material where defects are known
to exist, which is faster than waiting for them to appear in your own writing. E is
the target.

If your §0 showed strong ordering on 0b and compressed production on 0a, weight
harder toward E than the default `A + E` shape suggests — analysis of other
people's paragraphs is the thing you already demonstrated you can do.

### Sessions 9–10 — first review

Answer the four review questions in `LOG.md`. Look for pairs, not single columns:
prediction hit rising while self-caught stays flat means analysis is improving and
production isn't. Change the plan here; that is what the review is for.

### Sessions 11–20 — adjust and continue

Whatever the review said. If the same defect code keeps recurring, start sourcing
authentic paragraphs against it (`corpus/found/PROTOCOL.md`) instead of working
starter-corpus items you have already seen.

### Session ~15–20 — test

`tests/verification-01.md` (retention), then `verification-02.md` (blind transfer)
about a week later. The **gap between the two scores** is the finding, not either
score.

### Session ~20 — re-run §0

Fresh briefs, cold, timed. Compare against `baseline/diagnostic-original.md`. This
is the only hard evidence the project produces.

---

## When to stop

The project has falsification conditions in `AGENTS.md`. It also needs a success
condition, or it runs forever:

> **Mode E rubric consistently 6–7 of 7 on the FIRST draft** — not after revision —
> with a high self-caught ratio, and a small gap between verification 01 and 02.

At that point flow is no longer your bottleneck. Stop, and pick the next target
from the exclusion list in `docs/01-target.md`.

---

## The vocabulary track runs beside this, not inside it

`vocab/lexical-landscape-prompt.md` is a separate instrument on a separate goal.
Run it on real scenarios, roughly weekly. Do **not** wire its output into this
project's drills or into interview prep — different goal types, different
verification.

The only thing crossing the boundary is the bracket tally in `LOG.md`. On your
first landscape session, count how many of its 5–8 items you already knew. That
number decides whether targeting is worth any coordination at all.

---

## Files

| File | What it is |
|---|---|
| `AGENTS.md` | Instructions for the AI drill partner. Point it here at the start of every session |
| `docs/01-target.md` | The ability, its typing, its boundaries, what it excludes |
| `docs/02-patterns.md` | Six valid progression patterns, with examples |
| `docs/03-defects.md` | Nine defect codes, D1–D9 |
| `docs/04-worked-session.md` | One Mode A and one Mode E item, worked end to end. Read before your first real session |
| `docs/05-vocabulary-interface.md` | Where this project stops and vocabulary work starts. The five links, and how to measure which one is failing |
| `DRILLS.md` | The diagnostic plus four drill protocols |
| `corpus/starter-general.md` | Tier 1 items — general expository prose |
| `corpus/starter-technical.md` | Tier 2 items — support and infra writing |
| `corpus/KEYS.md` | Answers. Do not read early |
| `corpus/sources.md` | Real reading material and the two books that matter |
| `corpus/found/PROTOCOL.md` | How to build your own corpus of authentic paragraphs |
| `tests/verification-01.md` | Retention / near-transfer test, ~session 15–20 |
| `tests/verification-02.md` | Blind transfer test. Run a week after 01 |
| `LOG.md` | The only evidence this project generates. Fill it in |
| `baseline/` | Your untouched diagnostic paragraphs. Never edit these |

---

## Running a session

Open a session with the AI and say:

> Read `AGENTS.md` and the three files in `docs/`. We're running Mode A then Mode
> E. Don't read `corpus/KEYS.md` until I've answered.

Two modes maximum per session. **Commit a prediction before each item** — which
pattern you expect, whether you expect a defect. Thirty seconds, and it converts
the drill from reading into retrieval. End with the log block and paste it into
`LOG.md`.

---

## Three rules that keep this honest

**The AI never writes your prose.** It points, names the defect, and explains what
a reader loses. You write every repair and every draft. The last batch of
application documents was AI-drafted and approved — that produced documents and no
ability, and `AGENTS.md` R1 exists to stop it recurring.

**Recognition and generation are different abilities.** Analyzing paragraphs is
comfortable; producing them is not. Mode E is the one that moves production and
the one that will get skipped. Watch the ratio.

**Clean items count.** An undisclosed number of corpus items are sound, some of
them deliberately looking wrong under a naive rule, and marking a clean item
defective scores *negative*. Over-correction is the failure mode this project
creates, and it is worse than the defects it fixes.

---

## What this project does not claim

- **No timelines.** How long any of this takes is not asserted anywhere in these
  files. `LOG.md` will answer it in a few weeks; nothing else can.
- **No grader reliability.** AI annotation of information flow is unvalidated. It
  runs under a protocol that forces it to show its work, give alternatives, and
  mark uncertainty — treat every judgment as a hypothesis and check it against
  keys and published prose.
- **No claim the target is correct.** §0 tests that. If the diagnostic says the
  bottleneck is sentence-level production, this project is wrong for you and
  should be abandoned rather than pushed.

---

## Cover letters

Use them as the **test**, not the training set. They are low-volume, high-stakes,
and formulaic — three properties that work against learning, plus one specific
trap: because you want the letter to be good, you will let the AI fix it, and the
correction never becomes yours.

Train on low-stakes volume. Verify on the letter.
