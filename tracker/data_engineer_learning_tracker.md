# Data Engineer Learning Tracker

## Overall

- Total Questions: 306
- Correct: 282
- Accuracy: 92.2%
- Total Sessions: 7
- Current Streak: 2 days
- Best Streak: 4 days
- Last Session: 2026-09-19
- Current Phase: Foundation

> Session counting convention: one practice block is one learning session. Multiple same-day
> blocks are recorded in the same dated file. The 2026-09-03 file contains a morning block
> (3 rounds) and an afternoon block (4 rounds); the 2026-09-04 file contains one afternoon
> block with two completed rounds and one partial round; the 2026-09-05 file contains one
> completed round; the 2026-09-06 file contains one block with three completed rounds; the
> 2026-09-18 file contains one completed round; the 2026-09-19 file contains one completed round.

> Earlier source result records do not always contain a per-question topic mapping. Lifetime
> topic-level `Questions` and `Accuracy` therefore remain `—` where historical totals cannot
> be reconstructed reliably; `0` is retained only for topics that remain unassessed.

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
| SQL | GROUP BY / Aggregation | 2.5 | — | — | 2026-09-18 | High |
| SQL | JOIN / Fanout | 3.25 | — | — | 2026-09-19 | Medium |
| SQL | Grain | 3.25 | — | — | 2026-09-19 | Medium |
| SQL | Subquery / EXISTS | 3.0 | — | — | 2026-09-18 | Medium |
| SQL | CTE | 1.5 | 0 | - | - | High |
| SQL | Window Functions | 3.25 | — | — | 2026-09-19 | Medium |
| SQL | Query Debugging | 1.5 | 0 | - | - | High |
| Python | Core Syntax / Data Structures | 2.25 | — | — | 2026-09-06 | Medium |
| Python | Functions / Parameters | 2.75 | — | — | 2026-09-06 | Medium |
| Python | Exceptions / Error Handling | 1.75 | — | — | 2026-09-19 | Medium |
| Python | File / JSON Processing | 2.0 | — | — | 2026-09-18 | Medium |
| Python | Type Hints | 1.5 | 0 | - | - | Low |
| Python | Testing / pytest | 1.5 | — | — | 2026-09-18 | Medium |
| Database | PostgreSQL Basics | 2.5 | — | — | 2026-09-06 | High |
| Database | Constraints | 3.0 | — | — | 2026-09-03 | High |
| Database | Primary / Foreign / Business Keys | 3.0 | — | — | 2026-09-06 | High |
| Database | Indexes | 2.5 | — | — | 2026-09-06 | Medium |
| Database | Transactions / ACID | 2.25 | — | — | 2026-09-19 | Medium |
| Database | Normalization | 2.0 | — | — | 2026-09-03 | Medium |
| Data Engineering | ETL / ELT | 3.0 | — | — | 2026-09-03 | High |
| Data Engineering | Batch Pipelines | 2.0 | 0 | - | - | High |
| Data Engineering | Incremental Load | 3.75 | — | — | 2026-09-19 | Medium |
| Data Engineering | Idempotency | 3.0 | — | — | 2026-09-19 | High |
| Data Engineering | CDC | 2.0 | — | — | 2026-09-06 | Medium |
| Data Engineering | Backfill | 2.0 | — | — | 2026-09-06 | Medium |
| Data Engineering | Data Quality | 3.0 | — | — | 2026-09-18 | High |
| Data Engineering | Profiling vs Validation | 3.0 | — | — | 2026-09-06 | Medium |
| Data Engineering | Snapshot Diff | 3.25 | — | — | 2026-09-19 | Low |
| Data Engineering | Schema Evolution / Migration | 2.5 | — | — | 2026-09-19 | Medium |
| Data Engineering | Data Modeling | 2.75 | — | — | 2026-09-19 | High |
| Data Engineering | Observability / Monitoring | 0.5 | 0 | - | - | High |
| API / Ingestion | REST APIs | 2.5 | — | — | 2026-09-03 | Medium |
| API / Ingestion | Pagination | 2.5 | — | — | 2026-09-03 | Medium |
| API / Ingestion | Retries / Rate Limits | 0.5 | 0 | - | - | High |
| Git | Git Fundamentals | 1.5 | 0 | - | - | High |
| Git | Branch / PR Workflow | 1.5 | — | — | 2026-09-06 | Medium |
| CI/CD | GitHub Actions | 2.5 | — | — | 2026-09-19 | Medium |
| Architecture | Bronze / Silver / Gold | 2.75 | — | — | 2026-09-19 | Medium |
| Architecture | Warehouse vs Lake vs Lakehouse | 0.5 | 0 | - | - | High |
| Orchestration | DAG / Scheduling / Dependencies | 0.0 | 0 | - | - | High |
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

- **SQL Query Debugging / CTE** — still unassessed in the tracker and should become a primary next-step area.
- **Observability / Monitoring** — essentially unassessed; introduce metrics, logs, alerts, SLIs/SLO-style reasoning, and pipeline-failure scenarios.
- **API Retries / Rate Limits** — unassessed; practice retryable errors, backoff, jitter, rate-limit handling, and idempotent ingestion.
- **Warehouse vs Lake vs Lakehouse** — unassessed; build architectural trade-off reasoning rather than definition-only recognition.
- **DAG / Scheduling / Dependencies** — not started; introduce dependency ordering, retries, scheduling, backfills, and failure propagation.
- **Git Fundamentals** — tracker still has no direct assessment; practice working tree / staging / commit / branch reasoning.
- **Schema Evolution / Migration** — rollout order, breaking-change detection, and transaction rollback were correct on 2026-09-19, but real migration implementation and backward-compatibility handling still need practice.
- **GitHub Actions / CI implementation** — workflow structure and dependency-debugging questions passed on 2026-09-19; retain implementation-oriented YAML debugging rather than basic definition questions.
- **Data Modeling** — grain, fanout, Fact vs Dimension, and order-item fact grain were strong; continue schema-design and dimensional-modeling micro-practicals before raising mastery further.
- **Bronze / Silver / Gold architecture** — layer responsibilities and Bronze replayability are stable, but an end-to-end architecture-design micro-practical is still needed.

## Strong Topics

- SQL `COUNT(*)` vs `COUNT(column)`
- `NOT IN` / `NOT EXISTS` / `EXISTS`
- JOIN Fanout, Anti-Join patterns, and grain preservation with `EXISTS`
- Grain reasoning and multi-stage aggregation
- Window Function grain, ranking functions, `LAG()` / `LEAD()`, and `PARTITION BY`
- Window Frame / Peer Rows: default peer-aware behavior, `ROWS` vs `RANGE`, ties, deterministic ordering, and partitioned running totals passed multi-variant review on 2026-09-19; retain low-frequency delayed review because this concept previously recurred
- PostgreSQL keys, constraints, and `ON CONFLICT`
- ETL / Canonicalization and Data Quality
- Business Key / Surrogate Key and Idempotency
- REST API Pagination
- Python keyword-only arguments
- Python mutable default arguments and `dict.get()` versus key existence after repeated delayed re-test
- Backfill basics and idempotent overlap handling
- Incremental Load failure-order reasoning, composite checkpoints, lookback windows, late-arriving data, and replay-safe writes
- CDC, hard delete, soft delete, tombstone, and delete-event basics
- Snapshot Diff classifications and business-fields-versus-technical-metadata comparisons
- PostgreSQL selectivity, cardinality estimates, `EXPLAIN ANALYZE`, and `ANALYZE`
- ACID properties, transaction rollback basics, and normalization anomalies after targeted review
- Composite indexes, equality / range, index-assisted ordering, `EXPLAIN`, and planner estimates
- Profiling findings versus rule-backed validation failures

## Next Session

Goal: shift away from already stable recognition topics toward unassessed and implementation-oriented areas, while retaining a small delayed-review sample for Window Frame / Peer Rows.

Suggested focus:
- 20% SQL Query Debugging / CTE
- 15% Observability / Monitoring
- 10% API Retries / Rate Limits
- 10% Warehouse vs Lake vs Lakehouse
- 10% DAG / Scheduling / Dependencies
- 10% Git Fundamentals
- 10% GitHub Actions workflow debugging
- 10% Data Modeling practical design
- 5% Window Frame / Peer Rows delayed review

Increase the proportion of AI code review, scenario reasoning, bug diagnosis, and micro-practical tasks; reduce pure definition-recognition questions.

## Session History

| Date / Block | Questions | Correct | Accuracy | Notes |
|---|---:|---:|---:|---|
| 2026-09-03 AM | 60 | 53 | 88.3% | 3 rounds; Grain improved but remains a priority |
| 2026-09-03 PM | 80 | 72 | 90.0% | 4 rounds; Window Functions improved, but `PARTITION BY` remains unstable |
| 2026-09-04 PM | 46 | 40 | 87.0% | 2 completed rounds + 1 partial round; Window Frame and incremental-load recovery were the main review areas |
| 2026-09-05 | 20 | 18 | 90.0% | 1 round; Backfill and failure recovery were strong, while Window Frame / Peer Rows and Snapshot Diff `Changed` remain review priorities |
| 2026-09-06 | 60 | 60 | 100.0% | 3 rounds; delayed review passed for Window Frame and Snapshot Diff; advanced incremental load and newly assessed architecture/CI/modeling topics were strong |
| 2026-09-18 | 20 | 19 | 95.0% | 1 round; schema migration, CI, layered architecture, grain/fanout, and Python topics were stable; Window Frame / Peer Rows recurred |
| 2026-09-19 | 20 | 20 | 100.0% | 1 round; Window Frame / Peer Rows passed multiple variants including `ROWS`, `RANGE`, ties, deterministic ordering, and full debugging; no new conceptual mistakes |
| **Total** | **306** | **282** | **92.2%** | **7 practice blocks across 6 calendar days** |
