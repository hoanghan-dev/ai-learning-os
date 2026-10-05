# Daily Learning Log

This log captures daily deliberate practice sessions. Every entry must document the **evidence produced** and the **demonstrated AI dependency level**.

---

## Log Entries

### [2026-10-05] — Spring Security Filter Chain Internals
* **Session Topic**: Spring Security Filter Chain & DelegatingFilterProxy
* **Role Used**: [Teacher](file:///d:/Workspace/ai-learning-os/01-roles/teacher.md)
* **Assistance Level**: L2 (Targeted hints)
* **Demonstrated Dependency**: **D1** (Docs assisted)
* **Evidence Produced**:
  * Built an isolated test case with a custom `OncePerRequestFilter`.
  * Created knowledge note: [Spring Security Filter Chain](file:///d:/Workspace/ai-learning-os/03-knowledge/).
  * Accurately explained why `DelegatingFilterProxy` is needed to bridge Servlet containers with Spring ApplicationContext.
* **Weaknesses Discovered**:
  * Momentarily confused on filter order precedence when registering via `@Bean` vs `http.addFilterBefore()`.
* **Recall Question for Tomorrow**:
  * *Why cannot the Servlet container natively instantiate Spring-managed filters directly?*

---

### [2026-10-04] — Database Transactions & Isolation Levels
* **Session Topic**: PostgreSQL Repeatable Read vs Read Committed Anomalies
* **Role Used**: [Examiner](file:///d:/Workspace/ai-learning-os/01-roles/examiner.md)
* **Assistance Level**: L0 (Attempt unassisted)
* **Demonstrated Dependency**: **D0** (Independent)
* **Evidence Produced**:
  * Wrote SQL scripts demonstrating Phantom Read prevention under Postgres Repeatable Read (using snapshot isolation).
  * Passed Examiner oral test on serialization anomalies.
* **Weaknesses Discovered**:
  * Need to clarify Write Skew anomaly in PostgreSQL.
* **Recall Question for Tomorrow**:
  * *How does PostgreSQL prevent Phantom Reads in Repeatable Read without locking the entire table?*

---

## Daily Log Entry Template (Copy for New Sessions)

```markdown
### [YYYY-MM-DD] — [Topic Name]
* **Session Topic**: [Concept / Feature / Bug]
* **Role Used**: [Teacher / Researcher / Code Reviewer / Debugger / Interviewer / Examiner]
* **Assistance Level**: [L0 Attempt / L1–L3 Hints / L4 Pseudocode / L5 Example / L6 Code]
* **Demonstrated Dependency**: [D0 Independent / D1 Docs Assisted / D2 Hint Assisted / D3 Guided / D4 AI Impl]
* **Evidence Produced**:
  * [Working code, unit test, note, or solved problem]
* **Weaknesses Discovered**:
  * [Specific misconception or knowledge gap logged to weakness-backlog.md]
* **Recall Question for Tomorrow**:
  * [Question to answer without notes tomorrow]
```
