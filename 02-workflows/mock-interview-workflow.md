# Workflow — Mock Interview

## 1. Overview & Objective

This workflow prepares the learner for technical interviews and oral code defenses. It tests retrieval speed, communication clarity, conceptual depth, and the ability to reason under pressure.

* **Primary AI Role**: [Interviewer](file:///d:/Workspace/ai-learning-os/01-roles/interviewer.md)
* **Target Output**: A transcript of multi-turn Q&A, an objective score across 5 dimensions, and a list of identified knowledge gaps logged into [`06-progress/weakness-backlog.md`](file:///d:/Workspace/ai-learning-os/06-progress/weakness-backlog.md).

---

## 2. Interview Protocol Rules

1. **One Question at a Time**: The AI must never dump multiple questions at once.
2. **No Hints During the Session**: The session simulates real interview pressure. The AI will not teach or provide answers mid-interview.
3. **Adaptive Probing**: If an answer sounds memorized, the AI must ask a follow-up probing the internal mechanism or trade-offs.
4. **Time & Pressure**: The learner should answer in real-time without browsing documentation or asking other AI tools.

---

## 3. Step-by-Step Procedure

### Step 1 — Setup & Topic Selection
1. Choose domain and seniority target:
   * Target Role: (e.g., *Junior Java Backend Engineer*, *Senior React Developer*, *Distributed Systems Engineer*).
   * Topic: (e.g., *Concurrency & Thread Safety*, *Spring Boot & Transactions*, *Database Indexing & Query Optimization*).
2. Configure Session Duration: (e.g., 5 questions or 30 minutes).

### Step 2 — Interview Activation
Prompt the AI:
```text
Act as my Technical Interviewer for [Target Role / Topic].
Rules:
- Ask ONE question at a time.
- Start with a foundational question, then adaptively increase difficulty.
- Probe my answers with follow-ups to test depth and trade-offs.
- Do NOT teach or reveal answers until the entire interview is concluded.
- When I say "End Interview" or when 5 questions are complete, provide a structured evaluation report.

Let's begin. Ask me question 1.
```

---

### Step 3 — Multi-Turn Dialogue
* **Learner Answers**: Structure answers logically using the **PREP framework**:
  * **P**oint: Direct thesis answer.
  * **R**eason: The underlying architectural or mechanical reason.
  * **E**xample: A concrete code or production scenario.
  * **P**oint (Summary): Restate conclusion with trade-offs.
* **AI Probing**: The AI asks follow-up questions:
  * *"Why did you choose that data structure over an alternative?"*
  * *"What happens under heavy concurrent writes?"*
  * *"How does the garbage collector handle that lifecycle?"*

---

### Step 4 — Debrief & Scoring
When the session ends, the AI evaluates performance across 5 key dimensions (0–5 scale):

1. **Technical Correctness** (0–5): Accuracy of statements.
2. **Depth of Understanding** (0–5): Explaining underlying mechanisms vs surface keywords.
3. **Trade-off Awareness** (0–5): Knowing when NOT to use an approach.
4. **Communication Clarity** (0–5): Structured, concise explanations.
5. **Practical Experience** (0–5): Connecting theoretical concepts to real-world edge cases.

---

### Step 5 — Gap Remediation
1. Copy any failed or weak topics into [`06-progress/weakness-backlog.md`](file:///d:/Workspace/ai-learning-os/06-progress/weakness-backlog.md).
2. Schedule a [Concept Learning Session](file:///d:/Workspace/ai-learning-os/02-workflows/concept-learning-workflow.md) with the Teacher role to remediate the gaps.
