# Starter Corpus — Tier 2: Support and Infrastructure Writing

**Start here.** This tier was originally marked "do not start here," on the
reasoning that domain vocabulary and genre convention stack on top of the flow
problem and confound the diagnosis. That reasoning is generically sound and
specifically backwards for this learner.

Tier 2 is connection pools, replication lag, rollback artifacts and runbooks —
vocabulary he **has**, in the genre he is actually targeting. Tier 1 is British
civic, charity-property and clinical-trial register — vocabulary he does not have
and has no reason to acquire. The confound the old note warned about is sitting in
Tier 1.

A diagnostic needs flow to be the only unknown. That condition holds here and not
there.

**Evidence:** session 1, item G3. The D5 turned on `council` / `local authority` /
`the borough` naming one body. The defect was missed for a reception reason and
scored as a flow miss. See `docs/vocabulary-interface.md`.

**Tier 1 is not retired.** Work it once defect codes are stable, using the
flag-unknowns step in `DRILLS.md` §1. Prose outside your domain is where transfer
gets tested — that is a later concern, not a first-session one.

Note the size difference: 6 items here, 12 in Tier 1. Generate fresh items per
`AGENTS.md` when this runs low.

Same rules: keys are in `KEYS.md`, the defective count is undisclosed, and some
items are clean.

Genres represented: customer escalation reply, incident writeup, runbook
section, docs page, internal status note.

---

### T1 — customer escalation reply

> Thanks for the detail — that helps. Your writes are failing because the
> connection pool on the primary is saturating during your nightly batch, not
> because of the schema change you mentioned. The pool is sized at 60 and your
> batch opens a connection per worker, so at 80 workers the last 20 queue until
> something frees up. Two options: cap the batch at 50 workers, which needs no
> change on our side, or move the batch to the read replica if it tolerates
> replication lag of a few seconds.

---

### T2 — incident writeup

> Between 02:14 and 02:31 UTC, requests to the ingest API returned 503 for
> approximately 40% of clients. The cause was a config push that disabled retry
> on the edge nodes. Rollback was initiated at 02:19 and completed at 02:31,
> because the previous artifact was not cached and had to be rebuilt from source.
> The rebuild path is now the primary action item: caching the last-known-good
> artifact would have reduced this incident to five minutes.

---

### T3

> The migration ran overnight. This caused the reporting dashboard to show stale
> figures. The data pipeline had been reading from the old table, and the ETL job
> was not updated until Wednesday, so the extract process continued pointing at
> the deprecated source.

---

### T4 — runbook section

> Check replication lag before failing over. The replica can be up to 30 seconds
> behind under normal load, and failing over during that window drops any writes
> that had not yet replicated. If lag exceeds 5 seconds, wait for it to clear
> rather than forcing the promotion.

---

### T5

> The p99 latency rose sharply after Tuesday's deploy. The deploy included a
> change to the retry policy. Therefore the retry policy change caused the latency
> regression, and reverting it will resolve the issue.

---

### T6

> A change to the way that timestamps are stored in the events table, which was
> made in order to support sub-millisecond resolution for the new market data
> feed, was deployed. Moreover, existing queries that compare timestamps to
> string literals now return no rows.
