# AI Learning OS

An intentional, evidence-based operating system designed to use Artificial Intelligence as a cognitive amplifier and rigorous tutor, rather than an intellectual crutch.

---

## 1. Executive Summary & Philosophy

In modern software development and engineering, AI models can effortlessly generate working code, draft architecture designs, and fix bugs. While this dramatically accelerates short-term task completion, it introduces a severe cognitive hazard: **The Illusion of Competence**.

When learners consume AI-generated code without mental struggle, they remain stuck at high dependency levels (D4–D5), unable to recall, debug, explain, or design systems independently when the AI is absent.

**AI Learning OS** solves this problem by reversing the standard human-AI interaction:
* The AI does **not** write your code by default.
* The AI **diagnoses** your understanding before explaining.
* The AI **asks questions** and forces active recall.
* The AI **guides through hints** (progressive disclosure ladder: L0–L7).
* The AI **evaluates evidence** of mastery before you move on.

The ultimate objective of this OS is **independent competence (D0–D2)**.

---

## 2. System Architecture

The AI Learning OS is organized into 8 modular directories:

```text
ai-learning-os/
│
├── AI-LEARNING-OS.md         # Master architecture and operating manual (this document)
│
├── 00-core/                  # First principles, behavioral rules, anti-dependency metrics
│   ├── learning-principles.md
│   ├── ai-behavior-rules.md
│   └── anti-dependency.md
│
├── 01-roles/                 # Specialized AI persona operational specifications
│   ├── teacher.md            # Diagnoses, builds mental models, guides practice
│   ├── researcher.md         # Explores primary sources, verifies facts vs hypotheses
│   ├── code-reviewer.md      # Evaluates correctness, security, design without rewriting
│   ├── debugger.md           # Teaches systematic diagnosis (symptom → evidence → root cause)
│   ├── interviewer.md        # Simulates realistic multi-turn technical interviews
│   └── examiner.md           # Measures independent capability without giving hints
│
├── 02-workflows/             # Standard Operating Procedures for learning activities
│   ├── concept-learning-workflow.md
│   ├── systematic-debugging-workflow.md
│   ├── code-review-workflow.md
│   ├── technical-research-workflow.md
│   ├── feature-implementation-workflow.md
│   └── mock-interview-workflow.md
│
├── 03-knowledge/             # Personal verified knowledge base & mental model repository
│   ├── README.md
│   ├── index.md
│   └── templates/
│       ├── concept-note-template.md
│       ├── tech-mental-model-template.md
│       └── cheatsheet-template.md
│
├── 04-projects/              # Deliberate project-based practice and lab environments
│   ├── README.md
│   └── templates/
│       ├── project-spec-template.md
│       ├── feature-plan-template.md
│       └── project-retro-template.md
│
├── 05-assessment/            # Evidence-based evaluation, quizzes, rubrics & code defense
│   ├── README.md
│   └── templates/
│       ├── session-assessment-template.md
│       ├── active-recall-quiz-template.md
│       ├── skill-rubric-template.md
│       └── code-defense-template.md
│
├── 06-progress/              # Tracking skill levels, weaknesses, and dependency metrics
│   ├── README.md
│   ├── skill-matrix.md
│   ├── learning-log.md
│   ├── weakness-backlog.md
│   └── anti-dependency-tracker.md
│
└── 07-prompts/               # Master prompt and invocation configurations
    └── master-prompt.md      # System-wide operational prompt for AI assistants
```

---

## 3. Core Frameworks

### 3.1 The Anti-Dependency Scale (D-Scale)

| Level | Name | Description | Status |
| :--- | :--- | :--- | :--- |
| **D0** | **Independent** | Solves and builds completely unassisted. | Target for core skills |
| **D1** | **Docs Assisted** | Solves using official documentation and primary specs. | Healthy professional state |
| **D2** | **Hint Assisted** | Needs conceptual or directional cues from AI. | Healthy learning state |
| **D3** | **Guided Implementation** | AI guides step-by-step; learner writes and understands code. | Transition state |
| **D4** | **AI Implementation** | AI writes the majority; learner reviews and verifies. | Acceptable for unfamiliar chores |
| **D5** | **Copy Dependency** | Learner copies code without understanding. Cannot explain or debug. | **Critical failure state** |

### 3.2 The Progressive Assistance Ladder (L-Ladder)

When a learner gets stuck, AI assistance must ascend gradually:

```text
L0: Ask learner to attempt / articulate reasoning
 ↓
L1: High-level conceptual hint
 ↓
L2: Targeted directional hint
 ↓
L3: Explain the core underlying concept
 ↓
L4: Provide architectural pseudocode
 ↓
L5: Provide an isolated minimal reproducible example
 ↓
L6: Provide complete implementation (Explicit request only)
 ↓
L7: Explain implementation line-by-line with edge cases & trade-offs
```

---

## 4. Operating Modes

You can switch the operating behavior of the AI assistant by specifying the mode in your prompt:

1. **Learning Mode (Default)**:
   * Optimized for deep understanding and skill retention.
   * AI diagnoses existing knowledge, asks probing questions, and forces active recall.
2. **Execution Mode**:
   * Activated when you must complete a production task under time constraints.
   * AI inspects context, suggests minimal safe changes, but still highlights architectural trade-offs.
3. **Research Mode**:
   * AI activates the [Researcher](file:///d:/Workspace/ai-learning-os/01-roles/researcher.md) persona.
   * Filters out hallucinations, distinguishes facts from interpretations, and cites primary sources.
4. **Review Mode**:
   * AI activates the [Code Reviewer](file:///d:/Workspace/ai-learning-os/01-roles/code-reviewer.md) persona.
   * Evaluates correctness, security, architecture, and maintainability without rewriting code.
5. **Debug Mode**:
   * AI activates the [Debugger](file:///d:/Workspace/ai-learning-os/01-roles/debugger.md) persona.
   * Enforces evidence collection and hypothesis ranking before touching any code.
6. **Exam / Interview Mode**:
   * AI activates the [Examiner](file:///d:/Workspace/ai-learning-os/01-roles/examiner.md) or [Interviewer](file:///d:/Workspace/ai-learning-os/01-roles/interviewer.md).
   * Strictly evaluates knowledge without giving away hints.

---

## 5. Daily & Weekly Operating Rhythm

### Daily Learning Session Routine (45–90 min)
1. **Intention & Target** (3 min):
   * Select a topic from [`06-progress/weakness-backlog.md`](file:///d:/Workspace/ai-learning-os/06-progress/weakness-backlog.md) or [`04-projects/`](file:///d:/Workspace/ai-learning-os/04-projects/).
   * Declare desired target D-level (e.g., target D1 for Spring Security filters).
2. **Setup Prompt**:
   * Load [`07-prompts/master-prompt.md`](file:///d:/Workspace/ai-learning-os/07-prompts/master-prompt.md) into your AI session context.
   * Activate the appropriate role (e.g., *Teacher* or *Debugger*).
3. **Deliberate Practice Cycle**:
   * Follow the relevant SOP in [`02-workflows/`](file:///d:/Workspace/ai-learning-os/02-workflows/).
   * Resist the urge to copy complete code solutions. Demand hints at L1–L3 levels.
4. **Session Closing & Evidence Gate** (7 min):
   * Complete the 6-point closing summary: **Learned, Demonstrated, Weaknesses, Recall Question, Independent Exercise, Next Step**.
   * Log the session in [`06-progress/learning-log.md`](file:///d:/Workspace/ai-learning-os/06-progress/learning-log.md).
   * If a new mental model was unlocked, extract it to [`03-knowledge/`](file:///d:/Workspace/ai-learning-os/03-knowledge/).

### Weekly Maintenance & Review (60 min)
1. **Active Recall Testing**:
   * Run the recall questions collected in `05-assessment/` and `06-progress/weakness-backlog.md` without AI assistance.
2. **Code Defense Session**:
   * Submit one major feature implemented during the week to the AI Examiner for a rigorous oral defense.
3. **Anti-Dependency Audit**:
   * Review [`06-progress/anti-dependency-tracker.md`](file:///d:/Workspace/ai-learning-os/06-progress/anti-dependency-tracker.md). Are you slipping into D4/D5 copy habits? Adjust assistance ladder accordingly.
4. **Update Skill Matrix**:
   * Update mastery scores in [`06-progress/skill-matrix.md`](file:///d:/Workspace/ai-learning-os/06-progress/skill-matrix.md).

---

## 6. Getting Started

1. Open your AI client of choice (Claude, ChatGPT, Gemini, Cursor, or local LLM).
2. Copy the contents of [`07-prompts/master-prompt.md`](file:///d:/Workspace/ai-learning-os/07-prompts/master-prompt.md) into your system prompt or initial message.
3. Paste the role activation block for your current task (from [`01-roles/`](file:///d:/Workspace/ai-learning-os/01-roles/)).
4. Begin learning with deliberate friction!
