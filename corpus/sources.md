# Sources — Real Material

The starter corpus is authored, which makes it controllable and makes it a weaker
standard than real prose. This is the counterweight: real writing, by people with
readers.

Use these for Mode A (analyze known-good). Two cautions that apply to all of them:

1. A published paragraph is an **observed output whose input is partly hidden**.
   You are seeing the ordering without seeing the purpose and reader the writer was
   working with. Reconstruct those explicitly before analyzing, and mark them as
   your inference.
2. Published does not mean well-written. Some of these will contain defects. Good.

---

## Read first — the theory, in worked-example form

**Gopen & Swan, "The Science of Scientific Writing"**, *American Scientist* 78
(1990). Roughly fifteen pages, almost entirely revision examples with commentary.
It is the compact statement of the reader-expectation approach — topic position,
stress position, and the cost of separating subject from verb.

Treat its worked revisions as **the authors' analysis, not laws of English**. Their
domain is scientific prose; some of what they present as general is specific to
it.

**Joseph Williams, *Style: Lessons in Clarity and Grace*.** The primary text for
this target. Chapters on cohesion, coherence, emphasis, and topics are the
relevant ones. Its exercises with answer keys are the closest thing available to
genuinely paired material — but note that editions differ and not every stylistic
exercise has a single correct answer. Where the key and your version differ,
decide whether you have a *different valid* answer before conceding.

**Zinsser, *On Writing Well*** — already in progress. Useful for taste and for
examples. It supplies no drills, so it cannot construct this model on its own.
Read it, don't budget training time against it.

---

## Tier 1 material — general expository prose

Look for writers who explain unfamiliar things to non-specialists. That constraint
forces visible information management.

- Long-form explanatory journalism — the pieces that explain a mechanism, not the
  ones that report an event
- Well-edited popular science and popular economics
- Essays by writers with a plain style. Paul Graham is a useful specimen: short
  sentences, heavy use of the previous sentence's content as the next one's
  departure point, and very few connectives — worth analyzing precisely because the
  flow is carried almost entirely by ordering
- Supreme Court dissents and good legal writing, if you want the extreme case of
  explicit relation-marking

## Tier 2 material — your target genres

- **Public postmortems** — Cloudflare, GitLab, AWS, Stripe. These are the single
  best genre match for incident writing: real constraints, expert readers, and
  published under reputational pressure so they are edited
- **Documentation** for tools you know — Supabase, PostgreSQL, systemd, Databento.
  Prefer conceptual and troubleshooting pages over API reference, which is
  templated and teaches little about flow
- **Mailing list and issue-tracker replies** from maintainers with a reputation for
  clear explanation. The genre closest to a support reply, written under time
  pressure, which is what you are training for
- **RFCs and design docs** published by engineering teams

---

## Building your own reference set

When a paragraph makes something clear that you expected to find hard, save it.
Note *what the reader had to already know* for it to work. A file of twenty such
paragraphs, annotated, is worth more than any published exercise set, because you
chose them against your own confusions.

Keep them in `corpus/found/`.
