# Mistake Log

Record conceptual mistakes rather than every wrong option.

| Date | Session | Domain | Topic | Question | Chosen | Correct | Root Cause | Correct Concept | Review Count | Resolved |
|---|---|---|---|---|---|---|---|---|---:|---|
| 2026-09-03 | 2026-09-03-R1 | SQL | JOIN output Grain | After joining `customers` to `orders`, what does one row represent? | — | — | Looked only at the left-table grain and did not trace the one-to-many relationship. | When one customer has multiple orders, the joined result is usually at order grain. | 0 | Partial |
| 2026-09-03 | 2026-09-03-R1 | SQL | GROUP BY and Grain | Does `GROUP BY` change the grain? | — | — | Confused row filtering with aggregation. | `WHERE` changes row population; `GROUP BY` aggregates and commonly changes the grain to its grouping keys. | 0 | Partial |
| 2026-09-03 | 2026-09-03-R1 | Python | Mutable Default Argument | What happens when a function uses `items=[]` as a default? | — | — | Assumed the default list is recreated when the function ends or is called again. | Default expressions are evaluated once at function definition; use `None` and create a new list inside the function. | 0 | Partial |
| 2026-09-03 | 2026-09-03-R2 | SQL | LEFT JOIN Anti-Join | What does `LEFT JOIN ... WHERE right_col IS NULL` find? | — | — | Did not recognize the unmatched-left-row pattern. | It finds left-table rows with no matching right-table row and is a common Anti-Join pattern. | 0 | Improved |
| 2026-09-03 | 2026-09-03-R2 | SQL | DISTINCT and Grain | Does `DISTINCT` always change the grain? | — | — | Judged from the presence of `DISTINCT` instead of the selected column combination. | The output grain depends on the full set of selected columns; `DISTINCT customer_id` is customer grain, while a unique `(customer_id, order_id)` remains order-level. | 0 | Improved |
| 2026-09-03 | 2026-09-03-R3 | Data Engineering | Snapshot Diff | How should an A-only key be classified? | — | — | Reversed the direction of the snapshot comparison. | A has the key and B does not: `Disappeared`; A does not and B does: `Inserted`; both have it but values change: `Changed`. | 0 | No |
| 2026-09-03 | 2026-09-03-R3 | Python | `dict.get()` and Key Existence | How can you tell whether `"volume"` exists when its value may be `None`? | — | — | Used `get()` or truthiness to infer key existence, which cannot distinguish a missing key from a present `None` value. | Use `"volume" in record`; `record.get("volume") is None` is not a key-existence test. | 0 | No |

## Rules

A mistake should be logged when it reveals a reusable misconception, for example:

- NULL / three-valued logic misunderstanding
- JOIN fanout miscount
- Wrong output grain
- Confusing business key and primary key
- Treating an anomaly as a hard Data Quality failure without evidence
- Misunderstanding idempotency
- Incorrect transaction or index reasoning

`Resolved` uses the following provisional statuses:

- `No`: no confirming correct re-test was recorded
- `Partial`: the concept was corrected during explanation but remains a review priority
- `Improved`: the concept was later answered correctly in the same day's targeted practice

Trivial slips do not need permanent logging unless repeated.
