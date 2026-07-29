# The Vocabulary Interface

Vocabulary is not this project's target. But it is the constraint that produced
the truncated §0 paragraphs, and in session 1 it produced a missed defect. The two
need a defined boundary rather than mutual avoidance.

## Five links

| Link | What fails | Fix | Timescale | Instrumented here? |
|---|---|---|---|---|
| **1** | Word → concept. You meet a word and can't read it | Contextual recognition work | Long, accumulative | **Yes — term flags, below** |
| **2a** | Concept → word, **word is in your lexicon**, retrieval fails under load | Production drills: cloze into novel sentences, timed retrieval | Can move fast | Yes — brackets |
| **2b** | Concept → word, **word is not in your lexicon at all** | Acquisition. There is no shortcut | Long, accumulative | Partly — brackets, and they undercount |
| **3** | Word → collocation. You have the word, can't tell if it fits here | Collocation checks; corpus or dictionary examples | Medium | Yes — brackets |
| **4** | Situation → register. Word fits the meaning, not the channel | Genre reading with attention to register | Medium | **No instrument. Do not claim to measure it** |

**2a and 2b feel identical from the inside.** Both present as "I don't know what
to write here." Only looking it up afterwards separates them, which is why the
bracket protocol is a measurement instrument and not just a workaround.

---

## Two directions, two instruments

An earlier version of this file routed everything one way — production only, Mode E
only. Session 1 failed in the other direction and had nowhere to record it.

| Direction | Where it bites | Instrument |
|---|---|---|
| **Production** (links 2a, 2b, 3) | Mode E — you cannot reach a word | Brackets, `DRILLS.md` §4 |
| **Reception** (link 1) | Modes A and C — you cannot read a word, so you cannot see what the text is doing with it | **Term flags**, below |

A link-1 failure inside an analysis drill is invisible without the second
instrument. It does not look like a vocabulary problem. It looks like a missed
defect.

---

## Term flags — the reception instrument

**In Mode A and Mode C, before committing your prediction:** read the item once and
list any term you are not sure of. The AI glosses those terms and only those.

Two things this produces:

1. **An uncorrupted flow score.** A defect you could not see because you could not
   read the words was never a flow measurement.
2. **Link-1 data**, logged per item, on real material rather than a deck.

**Scoring splits cleanly on the flag:**

| You flagged the term | You missed the defect | Diagnosis |
|---|---|---|
| Yes | Yes | **Flow miss.** You had the meaning and did not see the structure |
| No | Yes | **Link-1 miss.** You did not know the word was doing anything |
| Yes | No | Clean — the gloss did its job |

Carry `terms flagged` to `LOG.md`. A count that stays high across sessions on
Tier 2 material — your own domain — would be a strong signal that the target is
wrong and reading is the bottleneck.

### Session 1 example

G3 renames one body three times: `The council`, `The local authority`, `the
borough`. The D5 is undetectable without knowing those can be the same referent.
No term was flagged, the defect was missed, and the sheet recorded "no explicit
word" — a reception failure that presented as a flow judgment.

---

## Brackets — the production instrument, and its bias

Every Mode E session produces brackets. After enough of them, count:

```
2a (knew it, couldn't retrieve)  : ___
2b (didn't know it)              : ___
3  (knew it, unsure it fit)      : ___
```

### The bias, stated plainly

**A bracket is only generated when you reach for a word and miss. You cannot stall
on a word you do not know exists.** When the word is entirely absent from your
lexicon, you route around it with a paraphrase and never notice you did — so no
bracket appears.

The consequence: **2b is systematically undercounted, and "mostly 2a" is the
result this instrument tends to produce regardless of the truth.**

This is a validity problem, not a volume problem. Do not read a 2a-heavy ratio as
evidence that your lexicon is adequate. Read it as *consistent with* an adequate
lexicon and equally consistent with a large invisible acquisition gap.

The partial correction: when resolving brackets, also note any place where you
**deliberately simplified** — chose a phrase you were sure of over the meaning you
wanted. Those are 2b events that produced no bracket. Count them separately as
`2b-avoided`.

### Sample floor

**Do not read the ratio below 30 total brackets.** Ten sessions producing eight
brackets is noise. The floor is a bracket count, not a session count.

### Reading the ratio

| Result | Strategy |
|---|---|
| **Mostly 2a**, low `2b-avoided` | Lexicon is adequate and inert. Activation drills, not acquisition |
| **Mostly 2a**, high `2b-avoided` | The 2a reading is an artifact. Treat as 2b |
| **Mostly 2b** | Genuine acquisition gap. Production-gap harvesting alone is far too slow — you would acquire words only at the rate you happen to need them |
| **Mostly 3** | You have the words and don't trust them. Collocation work, and the confidence issue is doing more damage than the lexical one |
| **Even spread** | Do not "weight each track by share" — that is not an instruction anyone can follow. Pick the largest category, work it alone until it stops being largest, re-measure |

---

## The reverse-retrieval probe

The receptive-productive gap is robustly observed in language learners generally.
The size of yours is not knowable without measuring it, and exact conversion rates
in the literature are contested — take a number from your own probe or from
nowhere.

**The probe:** take any list of words whose meanings you know, put the **gloss on
the front and the word on the back**, and run it once. Recognition you already
have; this gives production. The gap between them is your receptive-productive gap
measured on your own vocabulary.

Two conditions for it to mean anything:

- Sample **words you have known for a long time** separately from words you learned
  recently. The long-known group is the informative one; recently-learned words
  fail production for a trivial reason.
- At least ~50 items, or the number is noise.

This is a one-off, roughly twenty minutes, and it answers "is vocabulary my
bottleneck" faster than any other measurement in this project. **Run it before
deciding to switch tracks, not after.**

If no such word list exists yet, the probe cannot run — and building one is
acquisition work, which is the next section's problem, not this one's.

---

## Acquisition does not come from this project

If the acquisition gap is large, it does **not** get sourced here. Production gaps
are a trickle: you meet a word only when you happen to need it, and — per the bias
above — often not even then.

Acquisition needs its own input stream, running independently, at its own pace, on
its own schedule. This project does not supply one and should not pretend to.

What this project can supply is **targeting**: term flags and resolved brackets
tell you which semantic areas you keep falling into holes in. That is better
information than a frequency list. It is not a substitute for volume.

---

## Why the cohesion drill still runs meanwhile

The bracket protocol decouples flow measurement from lexical availability. You
write `[ENG: ...]` and keep going, so the paragraph reaches full length with holes
in it — and a paragraph with holes still has an information structure that can be
annotated and scored.

That is the actual answer to "can I do both at once." Not that vocabulary is
secondary, but that brackets let the flow measurement survive the lexical gap
instead of being destroyed by it, the way truncation destroyed it in §0.

**The reception side has no such trick.** A gloss is not a workaround you can write
around; you either know what the words refer to or the analysis is not measuring
flow. That is why term flags are mandatory in Modes A and C rather than optional,
and why corpus items are chosen from material whose vocabulary you already hold.
