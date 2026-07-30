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
   `docs/05-worked-session.md`, then begin.

The order matters. Reading the defect taxonomy before the diagnostic contaminates
the sample — you would be testing whether you can apply rules you just read, not
what you produce by default.

---

## The arc after §0

Session counts below are conventional starting points, not findings. The log
overrides them.

### Sessions 1–2 — learn the instrument

Mode A on **one** item, then Mode E. The Mode A is not recognition training; it is
there so the annotation sheet and the defect codes become familiar enough to use on
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

## Vocabulary

Not this project's target, but it is the constraint that truncated the §0
paragraphs and it cost a defect in session 1. `docs/vocabulary-interface.md`
defines the boundary and carries two instruments:

- **Term flags** (Modes A and C) — you list terms you can't read *before*
  predicting, and the AI glosses those only. Separates a flow miss from a reading
  miss, which are different problems with different fixes
- **Brackets** (Mode E) — sort what you couldn't retrieve into 2a / 2b / 3. Read
  the ratio only past 30 brackets, and read it against the bias documented there:
  you cannot stall on a word you don't know exists, so acquisition gaps go
  systematically undercounted

**Acquisition does not come from this project.** Production gaps are a trickle. If
the acquisition gap turns out to be large, it needs its own input stream on its own
schedule, and this project supplies targeting for that — not volume.

---

## Files

| File | What it is |
|---|---|
| `AGENTS.md` | Instructions for the AI drill partner. Point it here at the start of every session |
| `docs/01-target.md` | The ability, its typing, its boundaries, what it excludes |
| `docs/02-patterns.md` | Six valid progression patterns, with examples |
| `docs/03-defects.md` | Nine defect codes, D1–D9 |
| `docs/05-worked-session.md` | One Mode A and one Mode E item, worked end to end. Read before your first real session |
| `docs/vocabulary-interface.md` | Where this project stops and vocabulary work starts. The five links, and how to measure which one is failing |
| `docs/04-annotation-format.md` | How you record an analysis. Quote-or-pick fields plus one rotating lens. Read before your first Mode A |
| `DRILLS.md` | The diagnostic plus four drill protocols |
| `corpus/starter-technical.md` | **Start here.** Support and infra writing — your own domain, so flow is the only unknown |
| `corpus/starter-general.md` | General expository prose. Worked after codes stabilise; four items carry off-page knowledge requirements and are marked |
| `corpus/KEYS.md` | Answers. Do not read early |
| `corpus/sources.md` | Real reading material and the two books that matter |
| `corpus/found/PROTOCOL.md` | How to build your own corpus of authentic paragraphs |
| `tests/verification-01.md` | Retention / near-transfer test, ~session 15–20 |
| `tests/verification-02.md` | Blind transfer test. Run a week after 01 |
| `LOG.md` | The only evidence this project generates. Fill it in |
| `baseline/` | Your untouched diagnostic paragraphs. Never edit these |
| `exercise/_template-mode-e.html` | The Mode E instrument. Click-to-answer, no install, no server |
| `exercise/_template-modes-abc.html` | Modes A, B, C. Same, plus locked predictions and a key gated behind your commitment |
| `exercise/` | One file per session — the generated sheet and the exported markdown record |

---

## Running a session

Open a session with the AI and say:

> Read `AGENTS.md` and everything in `docs/`. We're running Mode A then Mode E.
> Generate the exercise files first (R14). Hand me the pre-parsed sheet, not your
> analysis. Hand back your own filled sheet for comparison, not prose about my labels.

Two modes maximum per session.

**Commit before the answer is available.** That is the principle; the commitment
itself is different in every mode, and only Mode A's is a prediction:

| Mode | What you commit, before anything is revealed |
|---|---|
| **A** | The three-claim **prediction** — one named transition and its pattern, a `clean / defective / uncertain` verdict with confidence, one reader assumption. Locked once written |
| **B** | A stated **reason for every placement** — before the reference order opens |
| **C** | A **verdict** (`defective` / `clean` / `D8`), plus a code and a quoted span for each defect — before the key opens |
| **E** | **Nothing.** The draft is written cold |

Mode E has no prediction step, and asking for one is an error — you are the author,
so the honest forecast of your own defects is always "none." `DRILLS.md` §4 says why,
and what it costs.

The AI generates the exercise file before the drill starts (`AGENTS.md` R14). You
should never be laying out a sheet by hand.

**Every mode runs in the browser.** Two single-file instruments, no server and no
install — double-click to open. Both ship with a throwaway item for learning the
buttons; practise the mechanics there, never on a real one.

- `exercise/_template-mode-e.html` — Mode E. Times the draft, inserts brackets,
  splits sentences, and fills `Ties back by` and `Antecedent` by clicking words in
  your own text.
- `exercise/_template-modes-abc.html` — Modes A, B and C. Same click-to-quote
  fields, plus **the protocol as gates**: each mode's commitment must be made before
  the next step opens, Mode A's prediction locks and cannot be edited, and the key
  will not open until your commitment is in — the lock is the gate, not a debate.

The key is not a secret — it is sitting in `corpus/KEYS.md` and you can open that
whenever you like. It is gated because the *sequence* is the drill. Opening it early
cheats nobody; it just deletes the measurement.

Checks cover completeness only — **the page does not know whether your answers are
right.**

Export to markdown when you finish. **The markdown is the record**; the page is just
the instrument. End with the log block and paste it into `LOG.md`.

---

## Three rules that keep this honest

**The AI never writes your prose.** It points, names the defect, and explains what
a reader loses. You write every repair and every draft. The last batch of
documents was AI-drafted and approved — that produced documents and no
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
