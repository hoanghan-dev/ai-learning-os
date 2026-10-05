# Weakness & Misconception Backlog

This backlog maintains a prioritized queue of discovered misconceptions, knowledge gaps, failed recall questions, and debugging blind spots.

Review this backlog before starting any new learning session and prioritize items during weekly review.

---

## Priority Scale

* **P0 — Critical**: Blocks independent development or causes severe bugs / security holes.
* **P1 — High**: Frequent friction point; fragile mental model; high AI dependency (D3–D4).
* **P2 — Medium**: Edge-case gap or secondary architectural concept.
* **P3 — Low**: Minor syntax or stylistic unfamiliarity.

---

## Active Backlog Items

| ID | Priority | Topic / Misconception | Discovered Date | Source Session | Status | Resolution Criteria | Retest Date |
| :---: | :---: | :--- | :---: | :---: | :---: | :--- | :---: |
| **WB-01** | **P1** | Filter order precedence when registering via `@Bean` vs `SecurityFilterChain` | 2026-10-05 | [Learning Log](file:///d:/Workspace/ai-learning-os/06-progress/learning-log.md) | **Open** | Build a lab verifying exact order with multiple custom filters. | 2026-10-08 |
| **WB-02** | **P1** | Write Skew anomaly and SSI (Serializable Snapshot Isolation) in PostgreSQL | 2026-10-04 | [Learning Log](file:///d:/Workspace/ai-learning-os/06-progress/learning-log.md) | **Open** | Write a test reproducing Write Skew under Repeatable Read and verify fix under Serializable. | 2026-10-07 |
| **WB-03** | **P2** | Handling thread propagation in `SecurityContextHolder` with async threads | 2026-10-03 | [Session Retro](file:///d:/Workspace/ai-learning-os/05-assessment/) | **Open** | Explain and implement `DelegatingSecurityContextAsyncTaskExecutor`. | 2026-10-09 |
| **WB-04** | **P0** | Hibernate N+1 queries with `@OneToMany` and lazy loading | 2026-10-02 | [Code Review](file:///d:/Workspace/ai-learning-os/02-workflows/code-review-workflow.md) | **Resolved** | Mastered `JOIN FETCH` and Entity Graphs. Verified via query count assertions. | 2026-10-04 |

---

## Resolved Archive

### [WB-04] — Hibernate N+1 Queries with `@OneToMany`
* **Root Misconception**: Assumed calling `findAll()` with `FetchType.LAZY` would batch child entity queries automatically.
* **Key Learning**: Hibernate executes 1 query for parent entities, and subsequent $N$ queries for child collections when accessed. Solved using `JOIN FETCH` or `@EntityGraph`.
* **Verification Evidence**: Automated test asserting exact SQL statement counts using a custom JDBC statement inspector.
* **Resolved On**: 2026-10-04.
