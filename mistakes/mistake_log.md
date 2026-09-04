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
| 2026-09-03 | 2026-09-03-PM-R1 | Python | `dict.get()` and Key Existence | Does `record.get("crop_name") is None` prove that the key is absent? | — | — | Repeatedly treated a `None` return value as evidence that the key does not exist. | A present key may also have value `None`; use `"crop_name" in record` to test key existence. | 1 | No |
| 2026-09-03 | 2026-09-03-PM-R2 | SQL | Window Function output Grain | Does `SUM(amount) OVER (PARTITION BY customer_id)` return one row per customer? | — | — | Applied `GROUP BY` intuition to a Window Function and assumed the partition collapses rows. | A Window Function normally preserves the input grain and appends a value to each row; `GROUP BY` performs the aggregation. | 0 | Improved |
| 2026-09-03 | 2026-09-03-PM-R2 | SQL | `ROW_NUMBER()` Tie Behavior | Do tied values receive the same row number? | — | — | Confused `ROW_NUMBER()` with ranking functions that assign equal ranks to ties. | `ROW_NUMBER()` assigns a distinct sequential number to every row; add a deterministic secondary sort when needed. | 0 | Improved |
| 2026-09-03 | 2026-09-03-PM-R2 | SQL | `DENSE_RANK()` | Does `DENSE_RANK()` assign a different rank to every row? | — | — | Missed that tied values share a rank and that dense ranks do not leave gaps. | For `200, 200, 150`, `DENSE_RANK()` returns `1, 1, 2`. | 0 | Improved |
| 2026-09-03 | 2026-09-03-PM-R2/R3/R4 | SQL | `PARTITION BY` | Does `PARTITION BY customer_id` give all customers one global sequence? | — | — | Treated `PARTITION BY` as either a global ordering or a row-collapsing operation instead of a per-group calculation boundary. | Window calculations restart independently inside each partition while the original rows remain; each customer therefore starts at 1. | 3 | Improved |
| 2026-09-03 | 2026-09-03-PM-R2 | Database | ACID Durability | Which ACID property ensures committed data survives a later failure? | — | — | Confused persistence after `COMMIT` with the transaction's consistency constraints. | `Durability` means successfully committed data remains saved despite a later crash or power loss. | 0 | Improved |
| 2026-09-04 | 2026-09-04-R1 | SQL | Running Total | What does an ordered Window `SUM()` calculate? | — | — | Treated an ordered Window `SUM()` as the complete partition total even when a cumulative result was required. | With `ORDER BY` and an appropriate frame, ordered Window `SUM()` calculates a cumulative total; without ordering it can show the full partition total on each row. | 0 | Improved |
| 2026-09-04 | 2026-09-04-R1 | SQL | Running Total vs `GROUP BY` | How should cumulative customer spending be calculated while preserving order rows? | — | — | Used `GROUP BY` aggregation for a row-preserving cumulative requirement. | Use an ordered Window `SUM()` to preserve order-level rows; `GROUP BY` changes the output grain to the grouping keys. | 0 | Improved |
| 2026-09-04 | 2026-09-04-R1 | SQL | Window Frame / Peer Rows | How does `SUM(...) OVER (ORDER BY order_date)` behave when dates tie? | — | — | Initially assumed strict row-by-row accumulation despite peer rows sharing the same ordering value. | The default peer-aware frame can give tied dates the same cumulative result; use `ROWS` with a deterministic ordering for strict row-by-row accumulation. | 0 | Improved |
| 2026-09-04 | 2026-09-04-R1 | Data Engineering | Watermark Advancement / Failure Recovery | What is the safe order for target writing and watermark advancement? | — | — | Did not recognize that advancing the checkpoint before a successful target write can permanently skip records. | Write the target successfully before advancing the watermark, ideally in one transaction; roll back both states on failure. | 0 | Partial |
| 2026-09-04 | 2026-09-04-R2 | Database | Index Selectivity | Does having an index guarantee that PostgreSQL will use an Index Scan? | — | — | Treated index presence as sufficient regardless of how many rows the predicate returns. | The planner compares costs; highly selective predicates are more likely to use an index, while low-selectivity queries may reasonably use a Seq Scan. | 0 | Improved |
| 2026-09-04 | 2026-09-04-R3 | Data Engineering | Watermark Replay After Target Write | What happens if the target write succeeds but the watermark update fails? | — | — | Expected the watermark to advance automatically after the target write. | The watermark remains old, so the next run may replay the batch; idempotent business-key UPSERTs make that replay safe. | 0 | Partial |

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
- `Improved`: the concept was later answered correctly in targeted practice; delayed review may still be useful

Trivial slips do not need permanent logging unless repeated.
