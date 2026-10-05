# Workflow — Feature Implementation

## 1. Overview & Objective

This workflow guides how to implement a software feature inside a real project while maximizing learning and preventing AI dependency.

The biggest risk during feature development is the "Vibe Coding Trap" — asking AI to write entire controllers, services, and repositories, resulting in code that the developer cannot defend, maintain, or debug.

* **Primary AI Roles**: [Teacher](file:///d:/Workspace/ai-learning-os/01-roles/teacher.md) (during design), [Code Reviewer](file:///d:/Workspace/ai-learning-os/01-roles/code-reviewer.md) (during verification)
* **Target Output**: A fully functioning feature, automated tests, clean git commits, and a completed [Code Defense Check](file:///d:/Workspace/ai-learning-os/05-assessment/templates/code-defense-template.md).

---

## 2. The 6-Step Implementation Cycle

```text
Step 1: Requirement & Acceptance Criteria Definition
   ↓
Step 2: Architecture & Data Flow Design (No Code)
   ↓
Step 3: Test-First / Spike Implementation
   ↓
Step 4: Independent Implementation (Assistance L0–L3)
   ↓
Step 5: Code Review & Security/Edge-Case Audit
   ↓
Step 6: The "Explainability Defense" Gate
```

---

## 3. Step-by-Step Procedure

### Step 1 — Requirements & Acceptance Criteria
1. Clarify what the feature does:
   * **Given / When / Then** user stories.
   * Happy paths and error paths.
   * Target performance & constraints.
2. Fill out a [`04-projects/templates/feature-plan-template.md`](file:///d:/Workspace/ai-learning-os/04-projects/templates/feature-plan-template.md).

---

### Step 2 — Architecture & Data Flow Design
Before typing application code, sketch the execution path:
* **Controller / Entrypoint**: Route, HTTP method, request validation DTO.
* **Service / Domain**: Business logic rules, invariants, domain events.
* **Repository / Persistence**: Database entities, queries, transaction boundaries.
* **External Systems**: Third-party APIs, messaging queues.

Prompt the AI to critique your design:
```text
Act as my Code Reviewer / Architect.
Here is my proposed data flow and component boundaries for [Feature]:
[Insert Diagram / Text Plan]
Do not write code for me. Critique my boundaries, failure handling, and transaction scope.
```

---

### Step 3 — Test-First / Spike Implementation
1. Write an integration or unit test reflecting the acceptance criteria.
2. If unfamiliar with an external API or library, build an isolated throwaway spike in a scratch file to understand the mechanism before integrating it into the core project.

---

### Step 4 — Independent Implementation (L0–L3)
1. Write the code yourself.
2. **If stuck**:
   * Do NOT prompt: *"Write the service layer for me."*
   * DO prompt: *"I am stuck on handling token expiration inside the interceptor. Can you provide a conceptual hint (L1) or pseudocode (L4)?"*
3. Limit assistance strictly to **D1 (Docs)** or **D2 (Hints)**.

---

### Step 5 — Code Review & Quality Audit
1. Submit the working feature to the [Code Reviewer](file:///d:/Workspace/ai-learning-os/01-roles/code-reviewer.md) using the [Code Review Workflow](file:///d:/Workspace/ai-learning-os/02-workflows/code-review-workflow.md).
2. Fix any Critical or High issues independently.

---

### Step 6 — The "Explainability Defense" Gate
Before merging the branch, the learner must pass this test:
* Can you explain every imported package and dependency?
* Can you explain every line of configuration?
* Can you explain how errors propagate to the client?
* What happens if the database connection drops halfway through the operation?

If you cannot answer these questions, do not merge. Investigate until the code is fully transparent.
