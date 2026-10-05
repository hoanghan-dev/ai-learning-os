# Workflow — Systematic Debugging

## 1. Overview & Objective

This workflow establishes a rigorous, scientific debugging discipline. It prevents the common anti-pattern of "shotgun debugging" (blindly changing lines of code or pasting error dumps into AI hoping for a magic fix).

The goal is to cultivate the learner's ability to isolate root causes from empirical evidence with minimal AI hints.

* **Primary AI Role**: [Debugger](file:///d:/Workspace/ai-learning-os/01-roles/debugger.md)
* **Target Output**: A verified root cause, an isolated minimal fix, regression tests, and an entry in [`06-progress/weakness-backlog.md`](file:///d:/Workspace/ai-learning-os/06-progress/weakness-backlog.md) if a misconception was uncovered.

---

## 2. The 6-Stage Scientific Debugging Ladder

```text
Stage 1: Observation & Symptom Definition
   ↓
Stage 2: Reproduction & Minimal Failing Case
   ↓
Stage 3: Evidence Gathering (Logs, Traces, State)
   ↓
Stage 4: Hypothesis Generation & Ranking
   ↓
Stage 5: Smallest Disproving Experiment
   ↓
Stage 6: Root Cause Fix & Regression Verification
```

---

## 3. Step-by-Step Procedure

### Stage 1 — Observation & Symptom Definition
Before touching any code or querying the AI, write down:
1. **Expected Behavior**: Exactly what should have happened (with concrete input/output values).
2. **Actual Behavior**: Exactly what happened instead (with error codes, outputs, or UI states).
3. **Trigger**: The specific user action, API call, or script that triggered the discrepancy.

---

### Stage 2 — Reproduction
1. Can you reliably reproduce this bug on demand?
   * If **Yes**: Create the shortest series of steps to trigger it.
   * If **No** (Heisenbug): Gather timestamps, environmental factors, race conditions, or configuration variances.
2. Formulate a minimal failing test case or curl command.

---

### Stage 3 — Evidence Gathering
Collect hard facts before theorizing:
* Full stack trace (identify the exact boundary where your code calls external libraries)
* Application server logs & database query logs
* Payload inspection (HTTP headers, JSON body, serialization formats)
* Local variable inspection via debugger breakpoints or targeted print statements

**Do NOT feed raw unexamined logs to AI.** Filter to the relevant stack frames first.

---

### Stage 4 — Hypothesis Generation & Ranking
1. **Prompt the AI**:
   ```text
   Act as my Debugger. Here is my symptom, expected vs actual behavior, and collected evidence:
   [Insert Data]
   Do not provide a fix.
   Help me brainstorm 3 plausible hypotheses for what could cause this, ranked by probability.
   ```
2. **Review Hypotheses**:
   * For each hypothesis, identify: *What evidence would prove this hypothesis true, and what evidence would rule it out?*

---

### Stage 5 — Testing the Hypothesis (Smallest Experiment)
1. Pick the highest-ranked hypothesis.
2. Design the **smallest possible experiment** to validate or invalidate it:
   * Adding a single assertion or log statement
   * Inspecting memory/state at line `X`
   * Supplying a mocked response
3. **Rule**: Change only **one variable at a time**. Never alter code structure while testing a hypothesis.

---

### Stage 6 — Root Cause Fix & Verification
1. **Distinguish Symptom from Root Cause**:
   * *Symptom fix (Anti-pattern)*: Adding `if (obj != null)` to suppress a NullPointerException without asking why `obj` was null.
   * *Root cause fix*: Ensuring the upstream factory or repository reliably populates `obj`.
2. **Implement Minimal Fix**:
   * Write the fix yourself.
3. **Regression Verification**:
   * Run existing test suites.
   * Write a new automated unit/integration test that specifically fails without the fix and passes with it.
4. **Post-Mortem Note**:
   * Document what failed, why it failed, and how to prevent it in the future.

---

## 4. Debugging Self-Interrogation Checklist

Before asking an AI for help, answer these 5 questions:
* [ ] Did I read the entire error message, including the "Caused by" chain?
* [ ] Can I locate the exact file and line number where execution failed?
* [ ] Did I inspect the actual runtime value of variables at that line?
* [ ] What was the last working commit or change made before this broke?
* [ ] Is this a code error, an environment/configuration error, or a data error?
