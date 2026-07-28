# Thematic Progression Patterns

Six ways a well-formed English paragraph moves from sentence to sentence. **All
six are correct.** The purpose of knowing them is to stop yourself — and stop an
AI reviewer — from marking a paragraph defective merely because it isn't using
the linear pattern.

The single most common error in learning this material is treating pattern 2 as
the rule and patterns 1, 3, 4, 5, 6 as violations of it.

---

## 1. Constant topic

Several consecutive sentences depart from the same established topic. The topic
holds; the comment changes.

> **The reconciliation script has three known limitations.** *It* cannot process
> records older than the retention window. *It* silently skips rows whose
> checksums are missing. *It* also assumes the source clock is accurate to within
> a second.

Departure point stays `the script` throughout. Nothing here is "new information
from the previous sentence," and nothing is wrong.

**Use when:** enumerating properties of one thing.
**Fails when:** the repeated topic becomes monotonous, or when the reader has
lost track of what `it` refers to after several sentences.

---

## 2. Linear progression

The new information at the end of one sentence becomes the departure point of the
next. Chain-like.

> The deploy stalled at **the health check**. *The health check* waits for **a
> readiness endpoint** to return 200. *That endpoint* depends on a cache warm-up
> that had not finished.

**Use when:** tracing a causal or diagnostic chain — each step licenses the next.
**Fails when:** the chain runs so long the reader forgets the original subject, or
when the links are actually parallel rather than sequential.

---

## 3. Derived topics

Several sentences develop different aspects of one superordinate topic
established earlier. Each opening is new, but each is recognizably *part of* the
established whole.

> **A good incident report has three parts.** *The timeline* records what happened
> and when. *The analysis* explains why the system behaved that way. *The action
> list* names who will change what, and by when.

Sentence openings here are not the previous sentence's closing information. They
are accessible because the superordinate topic licenses them.

**Use when:** decomposing a whole into parts, a process into stages, a system into
components.
**Fails when:** the superordinate topic was never established, so the reader has
no frame to hang the parts on.

---

## 4. Split progression

Two or more elements are introduced together, then developed one at a time in
order.

> Two things went wrong: **a bad config push** and **a slow rollback**. *The config
> push* disabled request retries on every edge node. *The rollback* then took
> eleven minutes, because the previous artifact had to be rebuilt from source.

**Use when:** you have announced a count. The announcement creates an expectation
that the development satisfies.
**Fails when:** the development order doesn't match the announcement order, or
when you announce two and develop three.

---

## 5. Contrastive progression

A new or contrasting topic is placed first, deliberately, because the contrast is
the point.

> Most of the queries improved after the index was added. **A handful got
> dramatically worse.** Those were the ones relying on a sequential scan to dodge
> a bad row estimate.

Sentence 2 opens with something new. That is the intended effect — the reversal
is the information. Marking this as a "topic shift error" is a miscalibration.

**Use when:** the exception, reversal, or counter-case is what the reader needs.
**Fails when:** the contrast isn't signalled at all and reads as a non-sequitur.

---

## 6. Question–answer progression

An explicit or implicit question governs what comes next. The reader's active
question, not the previous sentence's content, sets the departure point.

> So why keep the old endpoint alive at all? **Three customers still call it**, and
> two have contracts guaranteeing twelve months' notice.

**Use when:** you can predict the objection or question the reader is forming.
**Fails when:** the question was never actually raised in the reader's mind, so the
answer arrives as an interruption.

---

## Mixed paragraphs are normal

Real paragraphs switch patterns. A paragraph that opens with split progression,
develops one branch linearly, and closes with a contrast is not confused — it is
ordinary competent prose.

When analyzing, name the pattern **per transition**, not per paragraph.

---

## The practical principle

Rather than "old information first," use:

> Put information where the reader can connect it to an **active topic or
> expectation**. Use sentence openings to establish a recognizable point of
> departure. Use later positions for development and emphasis.

Less mechanically satisfying than a chain rule. More accurate, and it does not
generate false positives on five of the six patterns above.
