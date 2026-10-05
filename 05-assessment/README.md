# Assessment Framework

## 1. Overview & Philosophy

In typical learning environments, learners evaluate their understanding based on **fluency** (e.g., *"I read the article and it made sense"* or *"I watched the tutorial and understood it"*). Cognitive science demonstrates that subjective fluency is almost completely uncorrelated with actual retrieval capability.

In **AI Learning OS**, learning is verified strictly through **demonstrated empirical evidence**.

* **Primary AI Role**: [Examiner](file:///d:/Workspace/ai-learning-os/01-roles/examiner.md)
* **Core Rule**: **No unrequested assistance during assessment.** The AI evaluates what you can do without help.

---

## 2. The 6 Levels of Competence

| Level | Competency Name | Behavioral Description | Proof Required |
| :---: | :--- | :--- | :--- |
| **L1** | **Recognition** | Identifies the concept or term when presented. | Multiple choice / definition selection. |
| **L2** | **Explanation** | Explains the mechanism in own words without notes. | Unassisted verbal / written explanation. |
| **L3** | **Guided Implementation** | Builds solution with conceptual hints or pseudocode. | Completes problem using L1–L3 hints. |
| **L4** | **Independent Implementation**| Implements cleanly from scratch using only docs (D0–D1). | Working code + unit tests with zero AI hints. |
| **L5** | **Systematic Debugging** | Isolates and fixes unfamiliar bugs in complex code. | Identifies root cause from logs without guessing. |
| **L6** | **Architectural Design** | Designs systems and defends trade-offs against alternatives.| Defends design in mock interview or code defense. |

---

## 3. The 6-Dimensional Evaluation Matrix (0–5 Scale)

When an assessment is scored, the AI evaluates performance across these 6 dimensions:

```text
1. Understanding  (0–5): Mental model accuracy; grasp of internal mechanics.
2. Recall         (0–5): Retrieval speed and accuracy without referencing materials.
3. Implementation (0–5): Cleanliness, idiomacy, edge-case coverage, and correctness of code.
4. Debugging      (0–5): Scientific diagnosis from evidence vs trial-and-error guessing.
5. Explanation    (0–5): Ability to articulate the "Why", "How", and constraints clearly.
6. Design         (0–5): Ability to navigate architectural trade-offs and system limits.
```

### Scoring Scale:
* **0**: No understanding / complete misconception.
* **1**: Superficial recognition; cannot explain mechanism.
* **2**: Partial understanding; requires heavy guidance; fragile mental model.
* **3**: Competent; can explain and implement standard cases independently.
* **4**: Advanced; anticipates edge cases, failure modes, and performance impacts.
* **5**: Master; effortlessly teaches, modifies internals, and defends architectural trade-offs.

---

## 4. Assessment Types & Rhythms

1. **Daily Session Assessment**:
   * Evaluated at the end of every study session using [`session-assessment-template.md`](file:///d:/Workspace/ai-learning-os/05-assessment/templates/session-assessment-template.md).
2. **Spaced Active Recall Quizzes**:
   * Conducted weekly on previously learned concepts to arrest the Ebbinghaus forgetting curve.
3. **Oral Code Defense**:
   * Conducted after finishing a project milestone. The AI Examiner interrogates the learner on every design choice and line of code.

---

## 5. Templates in this Directory

* [`templates/session-assessment-template.md`](file:///d:/Workspace/ai-learning-os/05-assessment/templates/session-assessment-template.md)
* [`templates/active-recall-quiz-template.md`](file:///d:/Workspace/ai-learning-os/05-assessment/templates/active-recall-quiz-template.md)
* [`templates/skill-rubric-template.md`](file:///d:/Workspace/ai-learning-os/05-assessment/templates/skill-rubric-template.md)
* [`templates/code-defense-template.md`](file:///d:/Workspace/ai-learning-os/05-assessment/templates/code-defense-template.md)
