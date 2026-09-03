# Data Engineer Learning Tracker

## Overall

- Total Questions: 60
- Correct: 53
- Accuracy: 88.3%
- Total Sessions: 1
- Current Streak: 1 day
- Best Streak: 1 day
- Last Session: 2026-09-03
- Current Phase: Foundation

> Session counting convention: one dated file represents one complete learning session. The
> 2026-09-03 session contains three 20-question rounds.

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
| SQL | Grain | 2.75 | — | — | 2026-09-03 | High |
| SQL | Subquery / EXISTS | 3.0 | — | — | 2026-09-03 | Medium |
| SQL | CTE | 1.5 | 0 | - | - | Medium |
| SQL | Window Functions | 0.5 | 0 | - | - | High |
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
| Database | Indexes | 0.5 | 0 | - | - | High |
| Database | Transactions / ACID | 0.5 | 0 | - | - | High |
| Database | Normalization | 1.0 | 0 | - | - | Medium |
| Data Engineering | ETL / ELT | 3.0 | — | — | 2026-09-03 | High |
| Data Engineering | Batch Pipelines | 2.0 | 0 | - | - | High |
| Data Engineering | Incremental Load | 0.5 | 0 | - | - | High |
| Data Engineering | Idempotency | 2.5 | — | — | 2026-09-03 | High |
| Data Engineering | Data Quality | 3.0 | — | — | 2026-09-03 | High |
| Data Engineering | Profiling vs Validation | 3.0 | — | — | 2026-09-03 | Medium |
| Data Engineering | Snapshot Diff | 2.0 | — | — | 2026-09-03 | High |
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

- **Grain** — improved after targeted practice, but still needs deliberate tracking through
  `JOIN`, `GROUP BY`, and `DISTINCT`.
- **Snapshot Diff** — reinforce the direction of `Inserted`, `Changed`, and `Disappeared`,
  especially `A 有、B 無 = Disappeared`.
- **Python data-structure semantics** — distinguish mutable default arguments, a missing key,
  and a key whose value is `None`.
- **GROUP BY / Aggregation** — continue checking the output grain after aggregation.

## Strong Topics

- SQL `COUNT(*)` vs `COUNT(column)`
- `NOT IN` / `NOT EXISTS` / `EXISTS`
- JOIN Fanout and Anti-Join patterns
- PostgreSQL keys, constraints, and `ON CONFLICT`
- ETL / Canonicalization and Data Quality
- Business Key / Surrogate Key and Idempotency
- REST API Pagination
- Python keyword-only arguments

## Next Session

Goal: establish a measurable baseline across core Data Engineering foundations.

Suggested focus:
- SQL Grain with mixed `JOIN` / `GROUP BY` / `DISTINCT` cases
- Snapshot Diff state classification
- Python mutable default arguments and `dict.get()` vs key existence
- One small code-review or micro-practical task to validate transfer beyond recognition

## Session History

| Date | Questions | Correct | Accuracy | Notes |
|---|---:|---:|---:|---|
| 2026-09-03 | 60 | 53 | 88.3% | 3 rounds; Grain improved but remains a priority |
