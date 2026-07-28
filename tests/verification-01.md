# Verification Test 01

Run after roughly 15–20 drill sessions, or whenever you want to know whether
anything has actually changed. **Every item is novel** — none appears in the
starter corpus.

## Rules

- **The number of defective items is not disclosed and is not 50/50.** Do not
  count, do not balance your answers.
- Some items are clean. Some are clean but look defective under a naive chain
  rule. At least one is a coherence failure that must be refused, not repaired.
- No AI assistance during the test. The AI grades afterward, under `AGENTS.md`.
- Time each section.

---

## Part 1 — Recognition (diagnose)

For each item: state whether it is sound. If not, give defect codes and quote the
spans. If it is sound, name the progression pattern that makes it work.

### V1
> The department published its spending figures a month late. The figures showed
> a twelve per cent overrun on consultancy. The overrun was concentrated in two
> contracts, both awarded without competitive tender.

### V2
> Attendance at the evening sessions held up better than anyone expected. The
> morning sessions collapsed. Both had been advertised in the same newsletter and
> both were free, so the difference is unlikely to be either cost or awareness.

### V3
> Rainfall in the catchment was the highest on record for March. Reservoir levels
> remain below the seasonal average. Moreover, the restrictions announced in
> February stay in force.

### V4
> Before you disconnect the sensor, note its serial number. The replacement
> procedure requires it, and the label is on the underside of the housing where it
> cannot be read once the unit is mounted.

### V5
> Schools that adopted the reading programme improved their results. The programme
> increases time spent reading aloud. Therefore reading aloud is what raised the
> results.

### V6
> The committee's remit covers three areas. Procurement was reviewed first,
> because the outstanding complaints concerned it. Staffing is scheduled for the
> autumn. The estate will not be examined until the following year.

### V7
> The tenancy agreement was signed in June. The lease sets out a six-month break
> clause. This has been disputed by the landlord's agent, who maintains the
> contract was varied in writing before the document took effect.

---

## Part 2 — Repair

Revise **V3** and **V7**, preserving the meaning. Then, for each change: state what
the reader could not do before and can now.

Do not repair V5. Instead, write two sentences explaining why flow repair is the
wrong tool for it.

---

## Part 3 — Production

Two briefs. One paragraph each. Time both.

> **P1.** A colleague two teams away has asked why their weekly export has been
> arriving four hours later than it used to. The cause is that their job was moved
> onto a shared scheduler in a batch of migrations last month, and it now queues
> behind two larger jobs. It can be moved back to a dedicated slot, but that
> requires their manager to request capacity. Write the reply. **Reader:** technical
> enough to understand scheduling, not familiar with your infrastructure. **Needs
> to be able to:** decide whether to escalate to their manager.

> **P2.** Write one paragraph for a general audience explaining why a photograph
> taken on a phone in a dim room looks noisy, while the same phone produces a
> clean image outdoors. **Reader:** no technical background. **Needs to be able
> to:** explain it to someone else afterwards.

---

## Grading

### Part 1 — per item

| Outcome | Score |
|---|---|
| Correct verdict, correct codes and spans | 2 |
| Correct verdict, imprecise codes | 1 |
| Missed a defect | 0 |
| Called a clean item defective | −1 |

### Part 3 — production rubric

Score each paragraph on seven items. These are the criteria; **none of them is
"every sentence begins with old information."** A paragraph can score full marks
while opening sentences with new information throughout.

| # | Criterion | Pass? |
|---|---|---|
| 1 | The intended point is identifiable — a reader could state it in one line |  |
| 2 | Every sentence has a clear role in the paragraph |  |
| 3 | Each departure point is accessible from context or prior text |  |
| 4 | Every reference has an unambiguous antecedent |  |
| 5 | The logical relations are recoverable |  |
| 6 | The ordering supports what the reader has to *do* next |  |
| 7 | Explicit transitions are accurate, and each is necessary |  |

### Reading the result

- **Part 1 strong, Part 3 weak** — recognition is running ahead of generation.
  Expected, and the fix is a higher Mode E ratio, not more analysis.
- **Negative scores on clean items** — over-correction (D9). Loosen the rules
  before drilling more.
- **Part 3 item 1 failing** — the problem is above flow. Point, not ordering.
- **Sentence-level errors dominate the grader's notes** — the target was wrong.
  Revise the project.

Record the full result in `LOG.md`, including the section times.
