# Defect Taxonomy

Nine labelled failures. Drills name the defect by code; the log tracks which codes
recur. Recurring codes — not a textbook's chapter order — are your curriculum.

**Before assigning any code, decide the layer:** D1–D7 are cohesion failures, D8
is a coherence failure wearing cohesion's clothes, D9 is over-correction. Repairing
at the wrong layer hides the problem.

---

## D1 — Unresolvable reference

A pronoun, `this`, `that`, or `these X` whose antecedent is absent, ambiguous, or
too far back.

> The service retries failed writes and logs each attempt to the audit table.
> ~~**This** made the incident harder to diagnose.~~

Which one — the retrying, the logging, or both? Repair by naming the referent:
`This retry behaviour made…`

---

## D2 — Unmotivated topic shift

A new departure point the reader cannot connect to any active topic or
expectation.

> The connection pool was exhausted within four minutes. ~~Kubernetes schedules
> pods based on resource requests, not limits.~~

The second sentence may be true and even relevant, but nothing licenses the jump.
Repair by supplying the link, or by reordering so the link is visible.

**Not to be confused with pattern 5** (contrastive) or pattern 6 (question–answer),
where a shift is deliberate and licensed. The test is whether the reader can
recover *why* the shift happened.

---

## D3 — Buried relation

A contrast, cause, concession, or consequence left implicit where the ambiguity
costs the reader something.

> The cache reduced median latency. ~~Tail latency increased.~~

Is the second sentence an additional benefit, a cost, or a coincidence? Ordering
alone cannot carry this. `However, tail latency increased` is the right fix, and
this is exactly the case where a connective is doing real work rather than
decorating.

---

## D4 — Misplaced emphasis

The new or most important information sits in a weak position — mid-sentence, or
buried in a subordinate clause — while the stress position at the end holds
something the reader already knew.

> ~~A complete rebuild of the search index, which took six hours, was what the
> migration required.~~

Repair: `The migration required a complete rebuild of the search index — six
hours.` The number is the news; put it where the stress falls.

---

## D5 — Broken lexical chain

The same referent renamed on each mention, in a well-intentioned attempt to avoid
repetition. The reader has to keep proving that these are the same thing.

> The **ingestion pipeline** failed at 02:14. The **data intake system** had been
> reporting elevated queue depth since midnight. The **loader** was restarted.

Three names, one referent. In technical prose, repeat the term. Elegant variation
costs more than repetition does.

---

## D6 — Missing point of departure

A sentence opens with information the reader has no access to yet — a term, an
entity, or an assumption introduced as though already shared.

> ~~The quorum loss explains the write failures you saw on Tuesday.~~

If quorum loss has not been established, the sentence asks the reader to accept a
referent and an explanation simultaneously. Establish, then use.

---

## D7 — Inaccurate connective

A discourse marker that signals the wrong relation, or signals a relation that
isn't there. Includes the `moreover` / `furthermore` sprinkle.

> The rollback completed in eleven minutes. ~~**Therefore**, the artifact had to be
> rebuilt from source.~~

The relation runs the other way — the rebuild caused the duration. A wrong
connective is worse than none, because the reader trusts it.

**Repair rule:** for every connective, name the relation it claims and check that
the relation actually holds. For every relation you meant, check whether omitting
the marker would cost the reader anything. Neither "add transitions" nor "cut
transitions" is the target — **accurate and economical signaling** is.

---

## D8 — Coherence failure, not cohesion

Surface links are all fine. The content is broken: a missing premise, an
unexplained inference, an irrelevant sentence, or a conclusion the evidence does
not reach.

> The p99 latency rose after the deploy. The deploy changed the retry policy.
> Therefore the retry policy is the cause.

Every link resolves. The reasoning skips the possibility of a coincident change,
and `therefore` overstates what two facts support.

**This is the most important code in the list**, because polishing cohesion around
an incoherent argument makes the writing *more* persuasive and *less* correct.
When you assign D8, stop doing flow repair and fix the content.

---

## D9 — Over-correction

Introduced because this project's own drills can cause it. Flag when a "repair"
has damaged working prose:

- A connective added where the relation was already unambiguous
- A legitimate contrastive or question–answer opening rewritten into a chain
- Repetition introduced so aggressively the prose reads as robotic
- A paragraph reordered into strict linear progression that was correctly using
  derived or split progression

If your repairs start scoring D9, the drill is over-fitting and the rule needs
loosening, not more practice.

---

## Quick reference

| Code | Failure | Layer |
|---|---|---|
| D1 | Unresolvable reference | Cohesion |
| D2 | Unmotivated topic shift | Cohesion |
| D3 | Buried relation | Cohesion |
| D4 | Misplaced emphasis | Cohesion |
| D5 | Broken lexical chain | Cohesion |
| D6 | Missing point of departure | Cohesion |
| D7 | Inaccurate connective | Cohesion |
| D8 | Missing premise / irrelevance / overreach | **Coherence** |
| D9 | Damage caused by over-applying the rules | Meta |

---

## Structural preconditions — which defects a sentence can even have

Most of these defects are not available in every sentence. Clause structure decides
which ones are possible, which means **a clean score can mean "I avoided the defect"
or "the defect could not occur here", and those are different results.**

| Code | Needs | So it is scarce in |
|---|---|---|
| **D1** | two or more candidate antecedents, usually from 2+ independent clauses upstream | short simple sentences |
| **D2** | enough development for a topic to exist and be departed from | very short paragraphs |
| **D3** | two propositions placed adjacent without their relation marked — **most available when clauses are left unjoined**, or when a sentence is already carrying so much that the relation has nowhere to sit | almost nowhere; this is the one simple-sentence prose produces *more* of |
| **D4** | more than one position of prominence — subordination, a long predicate, a trailing coordinate clause | short simple sentences, which have essentially one |
| **D5** | three or more mentions of one referent | short paragraphs |
| **D6** | an opening that assumes shared ground | any |
| **D7** | an explicit connective, which needs joined clauses | prose with no connectives |

### The consequence for reading a score

A paragraph of six short simple sentences will tend to score clean on D1, D4 and D7
**by construction**. That is not evidence of skill at emphasis or at connective
accuracy; those abilities were not tested. It will simultaneously be *more* exposed to
D3, because unjoined clauses leave every relation to bare juxtaposition — the parataxis
habit `DRILLS.md` §4 warns the bracket protocol exists to prevent.

This is the same finding the §0 verdict recorded: *short simple sentences cannot carry
most flow defects, so drilling on them measures nothing.* Record the structure profile
alongside the score, and read one against the other.

### And the consequence for repair

**D3's textbook repair is to add a connective. That is often the wrong move**, because
a buried relation is frequently a symptom of a structural decision rather than a
missing word. If a sentence is already carrying four propositions, the relation you
want to signal has nowhere to sit, and adding a third connective makes a list of
caveats out of what should be a structured offer. In that case the repair is to
**split, or to re-subordinate so the relation occupies the main clause** — not to
decorate the existing structure.

Deciding when to join, when to split, and what to subordinate is not a separate
grammar skill sitting underneath flow. It is the same decision seen from the other
side. See the scope note in `01-target.md`.
