# Defect Taxonomy

Assign a code only after deciding the layer. D1–D7 are cohesion failures, D8 is a
coherence failure, and D9 is damage caused by over-correction. Quote the span that
supports every code.

## D1 — Unresolvable Reference

A pronoun, demonstrative, or `this X` has no antecedent, several live antecedents,
or an antecedent too far back for the target reader.

> The service retries failed writes and logs each attempt. **This** made the
> incident harder to diagnose.

`This` may mean retrying, logging, or both. Repair by naming the referent.

## D2 — Unmotivated Topic Shift

A new departure point has no recoverable link to the active topic or reader
expectation.

> The connection pool was exhausted within four minutes. **Kubernetes schedules
> pods based on resource requests, not limits.**

The second fact may be relevant, but the paragraph does not license the jump. Do
not confuse D2 with a valid contrastive or question-answer progression.

## D3 — Buried Relation

A cause, result, contrast, concession, or other relation is left unclear where the
ambiguity costs the reader.

> The cache reduced median latency. **Tail latency increased.**

The second sentence could be an added benefit, cost, or coincidence. Repair the
structure or signal the intended relation. Adding a connective is not always the
right repair; a crowded sentence may need splitting or re-subordination.

## D4 — Misplaced Emphasis

The most important new information is buried in a weak position while the final
stress position holds less useful material.

> A complete rebuild of the search index, **which took six hours**, was what the
> migration required.

If the duration is the news, give it a stronger position.

## D5 — Broken Lexical Chain

One referent is repeatedly renamed, forcing the reader to prove that the names
refer to the same thing.

> The **ingestion pipeline** failed. The **data intake system** had reported a deep
> queue. The **loader** was restarted.

In technical prose, stable repetition often costs less than elegant variation.

## D6 — Missing Point of Departure

A sentence opens with an entity, term, or assumption presented as shared even
though the prior text has not made it available.

> **The quorum loss** explains the write failures you saw on Tuesday.

If quorum loss has not been established, introduce the fact before using it as the
explanation.

## D7 — Inaccurate Connective

A discourse marker signals the wrong relation or a relation that does not exist.

> The rollback completed in eleven minutes. **Therefore**, the artifact had to be
> rebuilt from source.

The causal direction runs the other way. For every connective, name the relation
it claims and test whether that relation holds and needs explicit signalling.

## D8 — Coherence Failure

The links resolve, but the content has a missing premise, irrelevant sentence,
unexplained inference, or unsupported conclusion.

> The p99 latency rose after the deploy. The deploy changed the retry policy.
> Therefore the retry policy caused the increase.

The conclusion excludes other possible causes without evidence. Stop flow repair
and fix the reasoning or information gap.

## D9 — Over-Correction

A repair damages working prose. Examples include:

- adding a connective where the relation was already clear;
- flattening a valid contrastive or question-answer opening into a chain;
- introducing mechanical repetition;
- forcing derived or split progression into linear order.

Repeated D9 means the drill rules need loosening.

## Quick Reference

| Code | Failure | Layer |
|---|---|---|
| D1 | Unresolvable reference | Cohesion |
| D2 | Unmotivated topic shift | Cohesion |
| D3 | Buried relation | Cohesion |
| D4 | Misplaced emphasis | Cohesion |
| D5 | Broken lexical chain | Cohesion |
| D6 | Missing point of departure | Cohesion |
| D7 | Inaccurate connective | Cohesion |
| D8 | Missing premise, irrelevance, or overreach | Coherence |
| D9 | Damage caused by applying the rules | Meta |

## Structural Preconditions

A clean score is evidence only for defects the paragraph made possible.

| Code | Usually requires | Scarce in |
|---|---|---|
| D1 | Two or more candidate antecedents upstream | Short simple sentences |
| D2 | Enough development for an active topic | Very short paragraphs |
| D3 | Adjacent propositions with an unclear relation | Rarely scarce; bare juxtaposition creates it |
| D4 | More than one position of prominence | Short simple sentences |
| D5 | At least three mentions of one referent | Short paragraphs |
| D6 | An opening that assumes shared ground | No common structural limit |
| D7 | An explicit connective | Prose with no connectives |

A paragraph made mostly of short simple sentences may avoid D1, D4, and D7 by
construction while becoming more exposed to D3. Record the structure profile with
the score. Use it to state which abilities were tested, not to prescribe a syntax
shape.
