# The Vocabulary Interface

Vocabulary is not this project's target. But it is the constraint that produced the
truncated §0 paragraphs, so the two need a defined boundary rather than mutual
avoidance.

## Five links, not three

An earlier version of this file collapsed 2a and 2b. That was wrong, and the
difference is the whole question.

| Link | What fails | Fix | Timescale |
|---|---|---|---|
| **1** | Word → concept. You meet a word and can't read it | Contextual recognition work — the morpheme deck | Long, accumulative |
| **2a** | Concept → word, **word is in your lexicon**, retrieval fails under load | Production drills: cloze into novel sentences, timed retrieval | Can move fast |
| **2b** | Concept → word, **word is not in your lexicon at all** | Acquisition. There is no shortcut | Long, accumulative |
| **3** | Word → collocation. You have the word, can't tell if it fits here | Collocation checks; corpus or dictionary examples | Medium |
| **4** | Situation → register. Word fits the meaning, not the channel | Genre reading with attention to register | Medium |

**2a and 2b feel identical from the inside.** Both present as "I don't know what to
write here." Only looking it up afterwards separates them, which is why the
bracket protocol below is a measurement instrument and not just a workaround.

## What the morpheme deck does and does not do

The deck is well built for what it does: front is a sentence with the word in
context, asking what it means *there*. That is **link 1**, trained as inference
rather than rote. Correct design for that purpose.

It trains link 1 **only**. Recognition and generation are different abilities —
a model that classifies an object when handed one cannot enumerate the extension
from the label. Knowing `electorate` on sight does not supply `electorate` when
you need it.

So: there is currently no targeted production-vocabulary practice anywhere in this
system. That is a real gap, correctly identified, and it needs its own track
rather than being treated as a by-product of reading more.

## The measurement problem

Right now nobody knows the 2a/2b ratio — not from self-report, which cannot audit
its own lexicon, and not from the drill, which hasn't run.

The ratio decides the strategy, so measure it before committing effort:

### Probe A — reverse the deck (one-off, ~20 minutes)

You have 91 notes with known glosses. Reverse them: **front = the gloss or
definition, back = the word.** Run through them once.

- Recognition score you already have from normal deck use
- Production score is what this probe gives you
- **The gap between them is your receptive-productive gap, measured on your own
  words**

Sample separately: words you learned *from* the deck (production failure expected)
versus words you knew long before it. The second group is the informative one.

The receptive-productive gap is robustly observed in language learners generally;
the size of yours is not knowable without running this. Exact conversion rates are
contested in the literature — don't take a number from anywhere but your own probe.

### Probe B — bracket ratio (ongoing)

Every Mode E session produces brackets. After ten sessions, count:

```
2a (knew it, couldn't retrieve)  : ___
2b (didn't know it)              : ___
3  (knew it, unsure it fit)      : ___
```

### Reading the ratio

| Result | Strategy |
|---|---|
| **Mostly 2a** | Your lexicon is adequate and inert. Activation drills, not acquisition. The deck matters less to your writing than you think |
| **Mostly 2b** | Genuine acquisition gap. Production-gap harvesting alone is far too slow — you'd acquire words only at the rate you happen to need them. **Run a separate input stream in parallel** |
| **Mostly 3** | You have the words and don't trust them. Collocation work, and the confidence issue is doing more damage than the lexical one |
| **Even spread** | Weight each track by its share and re-measure at session 20 |

## The parallel-track rule

If 2b is large, it does **not** get sourced from this project. Production gaps are
a trickle — you meet a word only when you happen to need it. Acquisition needs its
own input stream running independently, at its own pace, on its own schedule.

What this project supplies to that track is **targeting**: the brackets tell you
which semantic areas you keep falling into holes in. That's better than a
frequency list. It is not a substitute for volume.

## Why the cohesion drill still runs meanwhile

The bracket protocol decouples flow measurement from lexical availability. You
write `[ENG: ...]` and keep going, so the paragraph reaches full length with holes
in it — and a paragraph with holes still has an information structure that can be
annotated and scored.

That is the actual answer to "can I do both at once." Not that vocabulary is
secondary, but that brackets let the flow measurement survive the lexical gap
instead of being destroyed by it, the way truncation destroyed it in §0.
