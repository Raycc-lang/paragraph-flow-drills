# Starter Corpus — Tier 2: Support and Infrastructure Writing

**Tier 2. Do not start here.** Work Tier 1 (`starter-general.md`) until your
defect codes stabilise. This tier adds domain vocabulary and genre convention on
top of the flow problem, which confounds the diagnosis early on.

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
