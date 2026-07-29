# Verification Test 02 — Blind Transfer

Run **after** `verification-01.md`, ideally a week later so the two don't
contaminate each other.

This is **farther transfer across longer, mixed structures** — not a template-free
test. An earlier version claimed no item reused a starter-corpus shape. That was
false: X3 uses the instruction-first class from G11/T4/V4, X5 uses the
question–answer pattern from G9, X6 revisits lexical-chain failure from G3/V7/T3.

That is not a flaw to remove. A transfer test must preserve the construct — strip
out every taught pattern and you are testing patterns you never taught, which
measures nothing. What actually differs from `verification-01.md`:

- Paragraphs are longer — five to seven sentences, so defects sit inside
  structure instead of standing alone in a three-sentence frame
- Patterns are **mixed within a paragraph** rather than one per item
- Two items combine a **legitimate override with a genuine defect** in the same
  paragraph, which no starter-corpus or v01 item does. "This breaks the chain
  rule" is useless as a heuristic in both directions
- Defect count is undisclosed and unbalanced
- Genres are new: narrative, meeting summary, pipeline description, argument

So: a large 01→02 gap still means templates rather than models. A small gap is
weaker evidence of generalization than the earlier framing implied.

**No AI during the test.** Time each part.

---

## Part 1 — Recognition

For each: sound or not. If not, defect codes and spans. If sound, name what makes
it work — including any override in play.

### X1
> The canal reached the town nine years later than its promoters had promised, and
> by then the first railway survey had already been completed. Freight rates
> nonetheless fell by roughly a third within two years of opening, which was enough
> to keep the coal trade moving by water until the 1860s. The company never paid
> the dividend its prospectus had implied. Its shareholders, most of them local
> merchants who had subscribed partly to secure cheaper carriage for their own
> goods, seem not to have minded a great deal. What they had wanted was the rate
> reduction, and they had it whether or not the shares performed. The canal was
> sold to the railway in 1871 for less than the cost of its final three miles.

### X2
> The team reviewed four candidate storage backends over six weeks. Cost,
> operational familiarity, and expected write throughput were the criteria agreed
> at the outset. Three of the four cleared the throughput bar comfortably. A
> requirement that had not been written down until late in the process, namely that
> the backend support point-in-time recovery without a separate tooling stack, is
> what eliminated two of them. The remaining option was adopted in March.

### X3
> Do not merge this until the migration has run in staging. Two of the columns it
> touches are still being written by the legacy importer, which we had believed was
> decommissioned in January but which is evidently still running somewhere. This
> was discovered on Thursday. The staging run will tell us whether the importer's
> writes conflict with the new constraint, and if they do we will need a
> coordination window rather than a straight deploy.

### X4
> Attendance at the quarterly review was lower than usual. The finance lead
> presented the revised forecast, which brings the shortfall forward by one
> quarter. The office move is scheduled for August. Two teams asked for more
> detail on how the shortfall interacts with the hiring freeze, and it was agreed
> that a written note would follow within the week. Nobody objected to the revised
> figures themselves.

### X5
> What actually limits how fast a language model can answer? Not, for the most
> part, the arithmetic. The bottleneck on current hardware is memory bandwidth:
> the weights have to be moved from memory to the compute units for every token
> generated, and moving them takes longer than multiplying them. This is why batch
> size matters so much — a larger batch amortises one movement of the weights
> across many simultaneous requests. It is also why quantisation buys more speed
> than its arithmetic savings alone would suggest.

### X6
> The intake form is validated when the applicant submits it. The submission
> handler checks required fields and rejects anything malformed. Validated
> applications are then queued for review, and the review queue is worked in order
> of receipt. Records that fail the intake check are held for seven days before
> deletion, which gives the applicant time to resubmit. The rejection notice
> includes a link back to a partially completed form.

### X7
> The revised limits took effect in April. Compliance costs for the smaller
> operators rose by an estimated eight per cent in the first quarter. Consequently,
> three of them have applied for the hardship exemption. The measured particulate
> levels at the four monitoring stations have not yet changed.

---

## Part 2 — Repair

Repair the two items you scored as most seriously defective. For each change,
name what the reader could not do before.

Then: for any item where you identified a **coherence** problem rather than a flow
problem, write two sentences on why flow repair is the wrong tool — and say what
you would ask the writer for instead.

---

## Part 3 — Production under constraint

Both briefs are structurally unlike P1 and P2 in `verification-01.md`.

> **Q1 — hostile reader, and you were wrong.** Three weeks ago you told a customer
> their timeout errors were caused by their own client configuration. They pushed
> back; you re-checked; they were right and you were not — the cause was a
> connection limit on your side that you had misread. They have since escalated to
> your account manager. Write one paragraph to the customer. **Reader:** technically
> competent, currently annoyed, and has already been told one wrong thing by you.
> **Needs to be able to:** decide whether to keep escalating.

> **Q2 — hard constraint.** Explain to a new colleague why the team writes database
> migrations as two deploys — schema change first, code change second — rather than
> one. **Maximum three sentences.** The constraint is the point: with only three
> sentences, ordering and emphasis carry the entire load, and there is no room to
> repair a bad opening later.

---

## Grading

Part 1 scoring as in `verification-01.md`. Part 3 uses the same seven-item rubric
— that is deliberate, so the three production measurements (routine Mode E,
test 01, test 02) sit on one scale.

### The comparison that matters

| Pattern | Reading |
|---|---|
| 01 and 02 scores close | Generalization is real. The distinctions transfer to unfamiliar shapes |
| **01 strong, 02 much weaker** | You learned the templates, not the models. Fix by sourcing material *against* your recurring codes (see `corpus/found/PROTOCOL.md`) rather than re-running corpus items |
| Both weak, but Part 3 fine | The analytic vocabulary is not sticking, but production is working anyway. Consider whether the annotation apparatus is earning its cost |
| False positives concentrated in X1, X5 | Length and unfamiliarity are triggering defect-hunting. You are finding problems because you expect a test to contain them |

Log both scores side by side. The gap is the number, not either score alone.
