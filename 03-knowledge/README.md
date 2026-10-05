# Knowledge Base & Mental Models

## 1. Overview & Philosophy

In typical learning, people suffer from the **Collector's Fallacy**: hoarding articles, saving bookmarks, and pasting AI-generated text into notes without internalizing anything. Having a document saved on disk is not the same as having a mental model inside your brain.

In **AI Learning OS**, the `03-knowledge/` directory is **NOT** a dump of raw AI explanations. It is a curated repository of **verified, synthesized mental models** that you have personally inspected, articulated, and tested.

---

## 2. Core Principles of Knowledge Storage

1. **Synthesized, Not Copy-Pasted**:
   * Every note must be written in your own words.
   * If you cannot write a 2-paragraph summary without looking at the AI output, you do not understand it well enough to store it.
2. **Mental Models First, Syntax Second**:
   * Syntax changes across versions and frameworks. Mental models (e.g., event loops, filter chains, connection pooling, ACID guarantees) endure.
3. **Retrieval-Oriented**:
   * Every concept note must include **Active Recall Prompts** (flashcard-style questions) to enable closed-book testing later.
4. **Primary Source Anchored**:
   * Every note must cite the official documentation, RFC standard, or primary source so you can verify it when APIs change.

---

## 3. Directory Structure

```text
03-knowledge/
├── README.md                          # Knowledge base architecture & principles (this file)
├── index.md                           # Map of Content (MOC) cataloging all domains
└── templates/                         # Standardized schemas for notes
    ├── concept-note-template.md       # Atomic technical concept note
    ├── tech-mental-model-template.md  # Comprehensive system/framework mental model
    └── cheatsheet-template.md         # Rapid syntax & CLI reference
```

---

## 4. How to Use the Templates

1. When you master a new topic using the [Concept Learning Workflow](file:///d:/Workspace/ai-learning-os/02-workflows/concept-learning-workflow.md), copy the relevant template from `templates/` into the appropriate subfolder or root of `03-knowledge/`.
2. Fill out the note in your own words.
3. Fill out the **Active Recall Questions** section at the bottom.
4. Add the note link to [`03-knowledge/index.md`](file:///d:/Workspace/ai-learning-os/03-knowledge/index.md).
