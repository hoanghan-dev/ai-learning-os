# Workflow — Concept Learning

## 1. Overview & Objective

This workflow defines the standard operating procedure for learning a new technical concept, protocol, framework component, or algorithm.

The objective is to guide the learner from zero knowledge to **D0/D1 mastery** (independent understanding and ability to explain without assistance), while strictly avoiding the illusion of competence.

* **Primary AI Role**: [Teacher](file:///d:/Workspace/ai-learning-os/01-roles/teacher.md)
* **Target Output**: A verified mental model, an isolated working example built by the learner, and a captured note in [`03-knowledge/`](file:///d:/Workspace/ai-learning-os/03-knowledge/).

---

## 2. The 5-Phase Learning Cycle

```text
Phase 1: Diagnosis & Prerequisites
   ↓
Phase 2: Mental Model & First Principles
   ↓
Phase 3: Minimal Working Example (Spike)
   ↓
Phase 4: Active Recall & Stress Testing
   ↓
Phase 5: Synthesis & Knowledge Capture
```

---

## 3. Step-by-Step Execution

### Phase 1 — Diagnosis & Prerequisites
1. **Prompt the AI**:
   ```text
   Act as my Teacher. I want to learn [Topic/Concept].
   Before explaining, ask me 3–5 diagnostic questions to determine what I already know and what prerequisites I need.
   ```
2. **Learner Action**:
   * Answer the diagnostic questions purely from memory.
   * Explicitly state what you do NOT know or find confusing.
3. **AI Action**:
   * Identifies gaps and calibrates explanation depth.

---

### Phase 2 — Mental Model & First Principles
1. **Core Understanding Inquiries**:
   The AI must explain the concept by answering:
   * **Why does this exist?** What real problem does it solve that prior tools could not?
   * **What is the mental model?** (Analogy or high-level abstraction).
   * **What are the key moving parts?** (Components, boundaries, responsibilities).
   * **What is the lifecycle/flow of execution?** (How data/control moves through the parts).
2. **Rule**:
   * No production-sized code during this phase. Only architectural diagrams (ASCII/Mermaid) and conceptual explanations.

---

### Phase 3 — Minimal Working Example (MWE)
1. **Request the Minimalist Representation**:
   * The AI provides the absolute smallest code snippet that demonstrates the core mechanism (no boilerplate, no extraneous dependencies).
2. **Learner Inspection**:
   * The learner must inspect:
     - What each line does
     - What happens if a specific line or parameter is removed
     - How inputs transform into outputs
3. **Hands-On Reproduction**:
   * The learner retypes and runs the MWE locally. **Do not copy-paste.**

---

### Phase 4 — Active Recall & Stress Testing
1. **Active Recall Prompt**:
   * The AI asks the learner to explain the concept in their own words without referring to the documentation or earlier chat messages.
2. **Prediction Exercise**:
   * The AI presents 2 "What happens if..." scenarios (e.g., throwing an unhandled exception, network timeout, null value).
   * The learner predicts the outcome and verifies with code or execution.
3. **Edge Case & Gotchas**:
   * The AI highlights common pitfalls, anti-patterns, and security/performance failure modes.

---

### Phase 5 — Synthesis & Knowledge Capture
1. **Write Concept Note**:
   * The learner fills out a [`03-knowledge/templates/concept-note-template.md`](file:///d:/Workspace/ai-learning-os/03-knowledge/templates/concept-note-template.md).
2. **Session Assessment**:
   * Complete the 6-point session closing:
     - What was learned
     - What was demonstrated
     - Remaining weaknesses
     - Active recall question for tomorrow
     - Independent exercise
     - Next step
3. **Record in Progress Log**:
   * Log the session in [`06-progress/learning-log.md`](file:///d:/Workspace/ai-learning-os/06-progress/learning-log.md).

---

## 4. Anti-Patterns to Prevent

| Anti-Pattern | Why It Fails | Correction |
| :--- | :--- | :--- |
| **Passive Tutorial Reading** | Reading creates familiarity, not comprehension. | Stop every 5 minutes and explain the concept out loud. |
| **Instant Solution Copying** | Bypasses the cognitive struggle required for memory formation. | Hand-code every snippet and inspect behavior. |
| **Skipping Prerequisites** | Trying to learn complex frameworks (e.g. Spring Security) without core basics (Servlet filters). | Allow AI to check and teach missing prerequisites first. |
| **No Retrieval Practice** | Concept disappears within 48 hours. | Formulate at least 1 active recall flash question for tomorrow. |
