# Workflow — Code Review

## 1. Overview & Objective

This workflow establishes a structured process for evaluating code quality, architectural soundess, security, and maintainability.

The goal is not to have AI rewrite your code into a different style, but to hone your **engineering judgment** by identifying bugs, design vulnerabilities, and missing edge cases.

* **Primary AI Role**: [Code Reviewer](file:///d:/Workspace/ai-learning-os/01-roles/code-reviewer.md)
* **Target Output**: A prioritized review report, an understanding of trade-offs, learner-implemented fixes, and a verified git commit/merge.

---

## 2. Review Stages

```text
Stage 1: Pre-Review Self-Check (Learner)
   ↓
Stage 2: Context & Scope Formulation
   ↓
Stage 3: AI Code Review Execution (No Rewriting)
   ↓
Stage 4: Triage & Problem Resolution (Learner Fixes)
   ↓
Stage 5: Verification & Architectural Retrospective
```

---

## 3. Step-by-Step Procedure

### Stage 1 — Pre-Review Self-Check
Before submitting code to AI or peer review, perform this quick self-audit:
* [ ] Does the code compile cleanly with zero warnings?
* [ ] Are all variables, functions, and classes named accurately according to domain concepts?
* [ ] Have dead code, temporary debug logs, and commented-out blocks been removed?
* [ ] Are error states handled explicitly (no empty catch blocks)?
* [ ] Do automated tests cover both happy paths and edge cases?

---

### Stage 2 — Context & Scope Formulation
When invoking the AI Code Reviewer, provide clear context rather than naked code snippets:
1. **Goal/Requirements**: What business or technical requirement is this code fulfilling?
2. **Key Constraints**: What constraints (performance, memory, framework versions) apply?
3. **Target Files / Diff**: Supply the code or git diff.

```text
Act as my Code Reviewer.
Requirements: [Describe what this feature/fix does]
Architecture: [Describe where this component lives in the architecture]
Code:
[Insert Code or Git Diff]

Inspect the requirements and code. Categorize findings into Critical, High, Medium, and Low.
Do not rewrite my code. Explain WHY each issue matters and let me fix it.
```

---

### Stage 3 — AI Review Evaluation Areas
The AI reviews code along 5 standard dimensions:

1. **Correctness & Logic**:
   * Boundary checks, off-by-one errors, nullability, state mutation issues, async race conditions.
2. **Architecture & Clean Code**:
   * Single Responsibility Principle (SRP), coupling, inversion of control, leaking abstractions.
3. **Security (OWASP & Best Practices)**:
   * Injection points (SQL, Command, XSS), broken authentication, improper access control, sensitive data exposure in logs.
4. **Maintainability & Readability**:
   * Cognitive complexity, clear naming conventions, testability, code duplication.
5. **Performance (Where Justified)**:
   * N+1 database queries, algorithmic complexity ($O(N^2)$ loops), memory leaks, unclosed streams/connections.

---

### Stage 4 — Triage & Problem Resolution
1. **Prioritize Findings**:
   * **Critical**: Must fix immediately before running or committing.
   * **High**: Architectural flaw or serious bug; resolve before merging.
   * **Medium**: Maintainability debt or minor edge-case bug.
   * **Low / Suggestion**: Stylistic or optional refinement.
2. **Implement Fixes Independently**:
   * The learner writes the modifications.
   * If unsure of a solution, request a hint at level L2 or L3 (never a full rewrite).

---

### Stage 5 — Verification & Retrospective
1. Re-submit the updated diff to the AI:
   ```text
   Here is my updated implementation addressing [Issue #1] and [Issue #2].
   Did my fix resolve the root cause without introducing new regressions?
   ```
2. Once approved, commit code with an informative commit message following Conventional Commits format (`feat:`, `fix:`, `refactor:`, etc.).
3. Record any recurring design mistakes in [`06-progress/weakness-backlog.md`](file:///d:/Workspace/ai-learning-os/06-progress/weakness-backlog.md).
