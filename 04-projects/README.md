# Projects & Lab Practice

## 1. Overview & Methodology

In software engineering, passive knowledge does not translate into real-world capability. Building complete, functioning projects is the ultimate crucible for learning.

However, in the era of LLMs, building a project can become completely meaningless if the developer falls into **AI Vibe Coding**: letting the AI generate 90% of the project while the human merely pastes it into an editor. The project runs, but the developer has learned almost nothing.

In **AI Learning OS**, projects are designed for **Deliberate Engineering Practice**:
1. You establish **Target AI Dependency Levels (D0–D2)** for each subsystem before starting.
2. You design the architecture and data flow **before** writing code.
3. You write the code yourself. AI assists via questions, conceptual hints, and pseudocode.
4. You subject every completed module to an **Explainability Defense**.

---

## 2. The 3 Types of Projects

### Type 1: Core Labs (Target: D0–D1)
* **Goal**: Master fundamentals and specific mechanisms.
* **Scope**: Small, focused repositories (100–500 lines of code).
* **Examples**:
  * Implementing an in-memory HTTP server from raw TCP sockets.
  * Building an inverted index search engine from scratch.
  * Creating a custom JWT authentication filter in Spring Security without helper starters.
* **AI Rule**: Strictly **D0–D1** (AI can only act as Examiner or Documentation Guide).

### Type 2: Full-Stack Domain Applications (Target: D1–D3)
* **Goal**: Master integration, architecture, persistence, and state management.
* **Scope**: Realistic multi-tiered applications (API + DB + Auth + UI).
* **Examples**:
  * An e-commerce order management system with distributed locking.
  * A real-time collaborative document editor using WebSockets.
* **AI Rule**: **D1–D2** for business logic and core components; **D3** allowed for unfamiliar third-party APIs or infrastructure setup.

### Type 3: Spikes & Architectural Experiments (Target: D2–D4)
* **Goal**: Rapidly de-risk an unfamiliar technology or benchmark performance before committing to an architecture.
* **Scope**: Disposable scratch code.

---

## 3. Directory Conventions

For each project, maintain a dedicated folder under `04-projects/`:

```text
04-projects/
├── README.md                          # Methodology & guidelines (this file)
├── templates/                         # Specification & retro templates
│   ├── project-spec-template.md       # Project architecture & milestone blueprint
│   ├── feature-plan-template.md       # Individual feature design & checklist
│   └── project-retro-template.md      # Post-project evaluation & D-scale audit
│
└── [project-name]/                    # Dedicated project workspace
    ├── PROJECT-SPEC.md                # Instance of project-spec-template
    ├── RETROSPECTIVE.md               # Instance of project-retro-template
    └── docs/                          # Architecture diagrams, API specs
```

---

## 4. The Rule of Explainability

> If you cannot explain the control flow, error handling, and trade-offs of a component to another engineer without looking at an AI prompt, **you do not own that code.**

Before marking any project milestone complete:
1. Conduct a self-check or invoke the [Examiner](file:///d:/Workspace/ai-learning-os/01-roles/examiner.md).
2. Defend your code against simulated failure scenarios.
3. Document any lingering confusion in [`06-progress/weakness-backlog.md`](file:///d:/Workspace/ai-learning-os/06-progress/weakness-backlog.md).
