# Vocabulary Interface

Vocabulary is not this project's target, but vocabulary failures can corrupt a
flow score. Use the procedures below to separate the two.

## Five Links

| Link | Failure | Training response | Measured here |
|---|---|---|---|
| 1 | Word → concept: the learner cannot read a word | Contextual recognition | Yes, with term flags |
| 2a | Concept → known word: retrieval fails under load | Timed retrieval and novel cloze | Yes, with brackets |
| 2b | Concept → unknown word | Separate acquisition stream | Partly; brackets undercount it |
| 3 | Word → collocation: fit is uncertain | Check real corpus or dictionary examples | Yes, with brackets |
| 4 | Situation → register: meaning fits but channel does not | Genre and register work | No; do not claim to measure it |

Links 2a and 2b feel the same during writing. Only a later lookup separates them.

## Reception: Term Flags in Modes A and C

Before the learner's commitment:

1. The learner reads the item once and lists terms he is unsure of. `None` is a
   valid answer.
2. The drill partner glosses only those terms, one at a time.
3. A gloss must not state or imply that two terms share a referent.
4. If a term cannot be glossed without revealing the defect, do not score the item.

Log `terms flagged` for each item.

A flag alone does not classify a later miss. If a missed defect may depend on a
term, check the term afterwards:

| Evidence | Classification | Score handling |
|---|---|---|
| Term was flagged and glossed | Probable flow miss | Keep the flow score |
| Term was not flagged; learner did not know its definition | Confirmed reception miss, link 1 | Remove from flow score; log vocabulary signal |
| Learner knew each definition but did not know a relation between terms, such as shared reference | Off-page knowledge confound | Exclude the item from both scores |

Not flagging a term proves only that the learner believed he understood it. It does
not prove that he did.

The third row is an item-selection failure. A scored flow defect must be recoverable
from the paragraph and standalone glosses. See `AGENTS.md`.

## Production: Brackets in Mode E

When a word does not come during the cold draft, the learner writes:

```text
[ENG: intended meaning in your L1, a paraphrase, or a guess]
```

He then continues without searching. After the draft is locked, resolve each
bracket without changing the paragraph's structure:

| Lookup result | Category | Follow-up |
|---|---|---|
| “I knew that word” | 2a retrieval | Use it in a novel cloze sentence |
| “I did not know that word” | 2b acquisition | Add it to a separate acquisition stream |
| “I knew it but was unsure it fit” | 3 collocation | Check two or three real examples and record the boundary |

Also count `2b-avoided`: places where the learner deliberately simplified because
he did not know the expression he wanted.

### Measurement Bias

A bracket appears only when the learner reaches for a word and notices the miss.
An entirely unknown word often produces an unnoticed paraphrase instead. Therefore
2b is systematically undercounted, and a 2a-heavy result does not prove that the
productive lexicon is adequate.

Read a high 2a count against `2b-avoided`:

| Pattern | Working interpretation |
|---|---|
| Mostly 2a, low `2b-avoided` | Retrieval is the leading candidate |
| Mostly 2a, high `2b-avoided` | The apparent retrieval result is probably an acquisition gap |
| Mostly 2b | Acquisition is the leading candidate |
| Mostly 3 | Collocation confidence is the leading candidate |
| Even spread | Work on the largest category alone, then measure again |

Do not interpret this ratio below 30 total brackets. This is a bracket-count floor,
not a session-count floor.

## Optional Reverse-Retrieval Probe

Use this probe before changing the project because vocabulary appears to be the
bottleneck:

1. Select at least 50 words whose meanings the learner can recognize.
2. Separate long-known words from recently learned words.
3. Put the gloss on the front and the word on the back.
4. Test concept-to-word production once.
5. Compare production with recognition, using the long-known group as the main
   evidence.

If no suitable word list exists, the probe cannot run without first doing
acquisition work.

## Boundary of This Project

This project can identify where vocabulary interferes with flow and which semantic
areas recur. It does not provide enough input volume for vocabulary acquisition.
A large acquisition gap needs its own materials and schedule.

Brackets let a Mode E paragraph reach full length despite lexical holes, preserving
its information structure. Reception has no equivalent workaround: if the learner
cannot identify what a term refers to after a standalone gloss, the item is not a
valid flow measurement.
