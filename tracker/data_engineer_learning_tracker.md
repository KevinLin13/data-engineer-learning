# Data Engineer Learning Tracker

## Overall

- Total Questions: 206
- Correct: 183
- Accuracy: 88.8%
- Total Sessions: 4
- Current Streak: 3 days
- Best Streak: 3 days
- Last Session: 2026-09-05
- Current Phase: Foundation

> Session counting convention: one practice block is one learning session. Multiple same-day
> blocks are recorded in the same dated file. The 2026-09-03 file contains a morning block
> (3 rounds) and an afternoon block (4 rounds); the 2026-09-04 file contains one afternoon
> block with two completed rounds and one partial round; the 2026-09-05 file contains one
> completed round.

> The source result records round-level totals and conceptual mistakes, but not a per-question
> topic mapping. Topic-level `Questions` and `Accuracy` therefore remain `—` until that detail
> is captured in a future session.

## Mastery Scale

| Level | Meaning |
|---|---|
| 0 | Not assessed / not started |
| 1 | Recognizes the term but frequently misses questions |
| 2 | Can answer basic recognition questions |
| 3 | Can reason through common engineering scenarios |
| 4 | Can review and debug code/design reliably |
| 5 | Can solve the problem independently and explain trade-offs |

Mastery should not be based on raw accuracy alone. Consider recency, difficulty, code-review performance, and micro-practical performance.

## Skill Map

> Baseline states below are provisional and should be recalibrated through actual questions.

| Domain | Topic | Mastery | Questions | Accuracy | Last Practiced | Priority |
|---|---|---:|---:|---:|---|---|
| SQL | SELECT / WHERE / ORDER BY | 2.0 | — | — | 2026-09-03 | Medium |
| SQL | NULL / Three-valued Logic | 3.0 | — | — | 2026-09-03 | High |
| SQL | GROUP BY / Aggregation | 2.5 | — | — | 2026-09-03 | High |
| SQL | JOIN / Fanout | 3.0 | — | — | 2026-09-03 | High |
| SQL | Grain | 3.0 | — | — | 2026-09-04 | High |
| SQL | Subquery / EXISTS | 3.0 | — | — | 2026-09-03 | Medium |
| SQL | CTE | 1.5 | 0 | - | - | Medium |
| SQL | Window Functions | 2.5 | — | — | 2026-09-05 | High |
| SQL | Query Debugging | 1.5 | 0 | - | - | High |
| Python | Core Syntax / Data Structures | 2.25 | — | — | 2026-09-05 | Medium |
| Python | Functions / Parameters | 2.75 | — | — | 2026-09-05 | High |
| Python | Exceptions / Error Handling | 1.0 | 0 | - | - | Medium |
| Python | File / JSON Processing | 2.0 | 0 | - | - | Medium |
| Python | Type Hints | 1.5 | 0 | - | - | Low |
| Python | Testing / pytest | 1.5 | 0 | - | - | Medium |
| Database | PostgreSQL Basics | 2.5 | — | — | 2026-09-05 | High |
| Database | Constraints | 3.0 | — | — | 2026-09-03 | High |
| Database | Primary / Foreign / Business Keys | 3.0 | — | — | 2026-09-03 | High |
| Database | Indexes | 2.5 | — | — | 2026-09-05 | Medium |
| Database | Transactions / ACID | 2.0 | — | — | 2026-09-04 | High |
| Database | Normalization | 2.0 | — | — | 2026-09-03 | Medium |
| Data Engineering | ETL / ELT | 3.0 | — | — | 2026-09-03 | High |
| Data Engineering | Batch Pipelines | 2.0 | 0 | - | - | High |
| Data Engineering | Incremental Load | 3.0 | — | — | 2026-09-05 | High |
| Data Engineering | Idempotency | 3.0 | — | — | 2026-09-05 | High |
| Data Engineering | CDC | 2.0 | — | — | 2026-09-05 | High |
| Data Engineering | Backfill | 2.0 | — | — | 2026-09-05 | High |
| Data Engineering | Data Quality | 3.0 | — | — | 2026-09-03 | High |
| Data Engineering | Profiling vs Validation | 3.0 | — | — | 2026-09-03 | Medium |
| Data Engineering | Snapshot Diff | 2.25 | — | — | 2026-09-05 | High |
| Data Engineering | Schema Evolution / Migration | 1.0 | 0 | - | - | Medium |
| Data Engineering | Data Modeling | 1.0 | 0 | - | - | High |
| Data Engineering | Observability / Monitoring | 0.5 | 0 | - | - | Medium |
| API / Ingestion | REST APIs | 2.5 | — | — | 2026-09-03 | Medium |
| API / Ingestion | Pagination | 2.5 | — | — | 2026-09-03 | Medium |
| API / Ingestion | Retries / Rate Limits | 0.5 | 0 | - | - | Medium |
| Git | Git Fundamentals | 1.5 | 0 | - | - | Medium |
| Git | Branch / PR Workflow | 1.0 | 0 | - | - | Medium |
| CI/CD | GitHub Actions | 0.5 | 0 | - | - | Medium |
| Architecture | Bronze / Silver / Gold | 0.5 | 0 | - | - | Medium |
| Architecture | Warehouse vs Lake vs Lakehouse | 0.5 | 0 | - | - | Medium |
| Orchestration | DAG / Scheduling / Dependencies | 0.0 | 0 | - | - | Medium |
| Distributed Data | Spark / PySpark | 0.0 | 0 | - | - | Medium |
| Infrastructure | Docker Basics | 0.0 | 0 | - | - | Low |
| Cloud | Cloud Data Fundamentals | 0.0 | 0 | - | - | Low |

## Current Question Distribution

Initial default weighting:

| Area | Weight |
|---|---:|
| SQL | 35% |
| Data Engineering Concepts | 30% |
| Python | 15% |
| PostgreSQL / Database | 10% |
| API / Git / CI/CD / Architecture | 10% |

Weights should be adjusted automatically according to weak topics, recency, and unassessed skills.

## Practice Rules

- Default session length: 20 questions
- Ask exactly one question at a time
- Default answer format: A / B / C / D
- Give immediate correctness feedback
- Keep routine explanations concise
- Explain mistakes clearly enough to correct the underlying model
- Increase frequency of recently missed concepts
- Reduce frequency of consistently mastered concepts
- Include code-reading and AI code-review questions
- Include approximately one micro-practical per 20-question session
- Do not over-reward recognition-only performance
- Re-test mastered topics after a delay

## Weak Topics

- **Window Frame / Peer Rows** — highest priority. The delayed review on 2026-09-05 failed;
  continue `ROWS`, `RANGE`, peer rows, tied ordering values, and deterministic ordering.
- **Snapshot Diff** — `Changed` was initially confused with `Duplicate`, although the later
  comprehensive question was answered correctly. Continue delayed review of all three states.
- **Incremental Load advanced recovery** — the two basic failure orders were answered correctly;
  continue retries, transaction boundaries, replay safety, and checkpoint consistency.
- **Backfill advanced operation** — historical ranges and idempotent overlap handling are now
  established; continue its interaction with normal scheduled incremental loads.
- **CDC / delete reconciliation** — hard delete, soft delete, and tombstone basics are established;
  continue CDC edge cases and periodic Snapshot Diff reconciliation.
- **Python data-structure semantics** — mutable defaults and `dict.get()` versus key existence
  passed delayed re-test; retain lower-frequency checks to verify retention.

## Strong Topics

- SQL `COUNT(*)` vs `COUNT(column)`
- `NOT IN` / `NOT EXISTS` / `EXISTS`
- JOIN Fanout and Anti-Join patterns
- Window Function grain, ranking functions, `LAG()` / `LEAD()`, and `PARTITION BY` after targeted review
- PostgreSQL keys, constraints, and `ON CONFLICT`
- ETL / Canonicalization and Data Quality
- Business Key / Surrogate Key and Idempotency
- REST API Pagination
- Python keyword-only arguments
- Backfill basics and idempotent overlap handling
- Incremental Load failure-order reasoning and replay-safe writes
- CDC, soft delete, tombstone, and delete-event basics
- PostgreSQL selectivity, cardinality estimates, `EXPLAIN ANALYZE`, and `ANALYZE`
- Python mutable default arguments and `dict.get()` versus key existence after delayed re-test
- ACID properties and normalization anomalies after targeted review
- Composite indexes, equality / range, index-assisted ordering, `EXPLAIN`, and planner estimates
- Late-arriving data, Lookback Window, soft delete, and basic CDC concepts

## Next Session

Goal: stabilize Window Frame / Peer Rows and Snapshot Diff `Changed`, while extending Backfill,
Incremental Load, and CDC reasoning to more advanced scenarios.

Suggested focus:
- 25% Window Frame: `ROWS`, `RANGE`, peer rows, and deterministic ordering
- 20% Snapshot Diff and reconciliation: `Inserted`, `Changed`, and `Disappeared`
- 20% Incremental Load: advanced failure recovery, retries, and transaction boundaries
- 10% Backfill: production overlap and idempotent historical reruns
- 10% PostgreSQL: `EXPLAIN ANALYZE`, planner estimates, and `ANALYZE`
- 10% Python code review: mutable defaults and `dict.get()` versus key existence
- 5% Micro-practical task

## Session History

| Date / Block | Questions | Correct | Accuracy | Notes |
|---|---:|---:|---:|---|
| 2026-09-03 AM | 60 | 53 | 88.3% | 3 rounds; Grain improved but remains a priority |
| 2026-09-03 PM | 80 | 72 | 90.0% | 4 rounds; Window Functions improved, but `PARTITION BY` remains unstable |
| 2026-09-04 PM | 46 | 40 | 87.0% | 2 completed rounds + 1 partial round; Window Frame and incremental-load recovery were the main review areas |
| 2026-09-05 | 20 | 18 | 90.0% | 1 round; Backfill and failure recovery were strong, while Window Frame / Peer Rows and Snapshot Diff `Changed` remain review priorities |
| **Total** | **206** | **183** | **88.8%** | **4 practice blocks across 3 calendar days** |
