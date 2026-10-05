# Anti-Dependency Tracker & Behavioral Audit

## 1. Overview & Purpose

The greatest danger when learning with AI is **insidious dependency creep**: gradually defaulting to copy-pasting code because it is fast, convenient, and feels productive.

This tracker is a self-auditing tool to monitor prompts, habits, and red-flag behaviors, ensuring you stay in the **healthy learning zone (D0–D2)**.

---

## 2. Red Flag Indicators (Symptom Check)

Audit your past week against these warning signs:

| Warning Sign | Danger Level | Meaning | Remediation Trigger |
| :--- | :---: | :--- | :--- |
| **"Write this file for me"** | 🚨 **Severe (D4/D5)** | Outsourcing implementation completely. | Switch immediately to **L0 (Attempt)** or **L4 (Pseudocode)**. |
| **Pasting raw error dumps without reading** | 🚨 **Severe (D5)** | Refusing to diagnose the stack trace. | Run [Systematic Debugging Workflow](file:///d:/Workspace/ai-learning-os/02-workflows/systematic-debugging-workflow.md) Stage 1–3 before asking. |
| **Inability to explain imported libraries** | ⚠️ **Moderate (D3/D4)** | Blindly trusting AI dependencies. | Conduct an oral [Code Defense](file:///d:/Workspace/ai-learning-os/05-assessment/templates/code-defense-template.md). |
| **Skipping unit test creation** | ⚠️ **Moderate (D3)** | Assuming AI generated code works. | Write tests before or alongside code. |
| **Reading explanation without recall test** | ℹ️ **Mild (D2)** | Passive consumption illusion. | Close window and explain out loud. |

---

## 3. Weekly Dependency Log

### Week of [2026-10-05]
* **Target AI Dependency**: D1 (Docs Assisted)
* **Estimated Actual Breakdown**:
  * D0 (Independent): 35%
  * D1 (Docs Assisted): 45%
  * D2 (Hint Assisted): 15%
  * D3 (Guided Implementation): 5%
  * D4 (AI Implementation): 0%
  * D5 (Copy Dependency): 0%
* **Triggers Where Urge to Copy Occurred**:
  * Writing boilerplate configuration for Spring Security filter registration. Resisted urge by reading official reference manual instead.
* **Weekly Score**: **PASS** (Healthy independent practice maintained).

---

### Weekly Audit Template (Copy for New Weeks)

```markdown
### Week of [YYYY-MM-DD]
* **Target AI Dependency**: [D0 / D1 / D2]
* **Estimated Actual Breakdown**:
  * D0 (Independent): %
  * D1 (Docs Assisted): %
  * D2 (Hint Assisted): %
  * D3 (Guided Implementation): %
  * D4 (AI Implementation): %
  * D5 (Copy Dependency): %
* **Triggers Where Urge to Copy Occurred**:
  * [Identify moments of cognitive fatigue or impatience]
* **Remediation Action for Next Week**:
  * [Specific countermeasure]
* **Weekly Score**: [PASS / WARNING / FAIL]
```
