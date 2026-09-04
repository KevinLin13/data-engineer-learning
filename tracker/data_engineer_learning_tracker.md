# Data Engineer Learning Tracker

## Overall

- Total Questions: 186
- Correct: 165
- Accuracy: 88.7%
- Total Sessions: 3
- Current Streak: 2 days
- Best Streak: 2 days
- Last Session: 2026-09-04
- Current Phase: Foundation

> Session counting convention: one practice block is one learning session. Multiple same-day
> blocks are recorded in the same dated file. The 2026-09-03 file contains a morning block
> (3 rounds) and an afternoon block (4 rounds); the 2026-09-04 file contains one afternoon
> block with two completed rounds and one partial round.

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
| SQL | Window Functions | 2.5 | — | — | 2026-09-04 | Medium |
| SQL | Query Debugging | 1.5 | 0 | - | - | High |
| Python | Core Syntax / Data Structures | 2.0 | — | — | 2026-09-03 | Medium |
| Python | Functions / Parameters | 2.5 | — | — | 2026-09-03 | High |
| Python | Exceptions / Error Handling | 1.0 | 0 | - | - | Medium |
| Python | File / JSON Processing | 2.0 | 0 | - | - | Medium |
| Python | Type Hints | 1.5 | 0 | - | - | Low |
| Python | Testing / pytest | 1.5 | 0 | - | - | Medium |
| Database | PostgreSQL Basics | 2.5 | — | — | 2026-09-03 | High |
| Database | Constraints | 3.0 | — | — | 2026-09-03 | High |
| Database | Primary / Foreign / Business Keys | 3.0 | — | — | 2026-09-03 | High |
| Database | Indexes | 2.5 | — | — | 2026-09-04 | Medium |
| Database | Transactions / ACID | 2.0 | — | — | 2026-09-04 | High |
| Database | Normalization | 2.0 | — | — | 2026-09-03 | Medium |
| Data Engineering | ETL / ELT | 3.0 | — | — | 2026-09-03 | High |
| Data Engineering | Batch Pipelines | 2.0 | 0 | - | - | High |
| Data Engineering | Incremental Load | 2.5 | — | — | 2026-09-04 | High |
| Data Engineering | Idempotency | 2.75 | — | — | 2026-09-04 | High |
| Data Engineering | CDC | 1.0 | — | — | 2026-09-04 | High |
| Data Engineering | Backfill | 0.0 | 0 | - | 2026-09-04 | High |
| Data Engineering | Data Quality | 3.0 | — | — | 2026-09-03 | High |
| Data Engineering | Profiling vs Validation | 3.0 | — | — | 2026-09-03 | Medium |
| Data Engineering | Snapshot Diff | 2.0 | — | — | 2026-09-04 | High |
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

- **Incremental Load failure recovery** — distinguish duplicate/replay risk when the target write
  succeeds but the watermark update fails from data-loss risk when the watermark advances first.
- **Backfill** — introduced as the next question but unanswered; cover historical ranges,
  idempotency, and interaction with scheduled incremental loads.
- **CDC / delete handling** — continue connecting hard deletes, soft deletes, tombstones, CDC,
  and periodic Snapshot Diff reconciliation.
- **Window Frame** — `PARTITION BY`, ranking, and basic running totals improved, but retain a
  delayed review of `ROWS`, `RANGE`, and peer rows.
- **PostgreSQL planner behavior** — selectivity was corrected in-session; continue with realistic
  `EXPLAIN` / `EXPLAIN ANALYZE` and row-estimate scenarios.
- **Snapshot Diff** — reinforce the direction of `Inserted`, `Changed`, and `Disappeared`,
  especially `A 有、B 無 = Disappeared`.
- **Python data-structure semantics** — carry forward mutable default arguments and `dict.get()`
  versus key existence; this topic was not re-tested today.

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
- ACID properties and normalization anomalies after targeted review
- Composite indexes, equality / range, index-assisted ordering, `EXPLAIN`, and planner estimates
- Late-arriving data, Lookback Window, soft delete, and basic CDC concepts

## Next Session

Goal: extend incremental-load reasoning from basic recognition to failure-safe operation, while
retaining delayed verification of Window Frame behavior.

Suggested focus:
- 30% Incremental Load: failure recovery, retries, transaction boundaries, and the distinction
  between duplicate processing and data loss
- 20% CDC / deletes: hard deletes, soft delete, tombstones, and Snapshot Diff reconciliation
- 15% Backfill: historical ranges, idempotent writes, and interaction with normal schedules
- 15% PostgreSQL: `EXPLAIN ANALYZE`, selectivity, planner behavior, and bad row estimates
- 10% Delayed Window Frame review: `ROWS`, `RANGE`, peer rows, and tied ordering values
- 5% Python code review: mutable defaults and `dict.get()` versus key existence
- 5% Micro-practical task

## Session History

| Date / Block | Questions | Correct | Accuracy | Notes |
|---|---:|---:|---:|---|
| 2026-09-03 AM | 60 | 53 | 88.3% | 3 rounds; Grain improved but remains a priority |
| 2026-09-03 PM | 80 | 72 | 90.0% | 4 rounds; Window Functions improved, but `PARTITION BY` remains unstable |
| 2026-09-04 PM | 46 | 40 | 87.0% | 2 completed rounds + 1 partial round; Window Frame and incremental-load recovery were the main review areas |
| **Total** | **186** | **165** | **88.7%** | **3 practice blocks across 2 calendar days** |
