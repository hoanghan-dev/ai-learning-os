# Workflow — Technical Research

## 1. Overview & Objective

This workflow governs how to conduct rigorous technical investigations, evaluate third-party libraries, validate architectural trade-offs, and research framework behavior.

It eliminates hallucinated claims, outdated blog tutorials, and unverified assumptions by enforcing a strict **source hierarchy** and **evidence classification**.

* **Primary AI Role**: [Researcher](file:///d:/Workspace/ai-learning-os/01-roles/researcher.md)
* **Target Output**: A verified research note, an architectural decision record (ADR), or a technology comparison matrix in [`03-knowledge/`](file:///d:/Workspace/ai-learning-os/03-knowledge/).

---

## 2. The 6-Stage Research Methodology

```text
Stage 1: Problem Definition & Scope Framing
   ↓
Stage 2: Primary Source & Spec Retrieval
   ↓
Stage 3: Evidence Verification & Version Matching
   ↓
Stage 4: Trade-Off Analysis (Pros, Cons, Constraints)
   ↓
Stage 5: Synthesis & Decision Recording
   ↓
Stage 6: Uncertainty Disclosure
```

---

## 3. Step-by-Step Execution

### Stage 1 — Problem Definition & Scope Framing
1. Avoid vague queries like *"How do I do auth?"*.
2. Formulate a precise technical question:
   * **Question**: *"What are the trade-offs between session-based cookies vs stateless JWT in Spring Boot 3.3 for a horizontally scaled REST API with a mobile client?"*
   * **Scope**: Specific runtime version, platform, scalability target, security boundary.

---

### Stage 2 — Primary Source Retrieval
Always consult sources in hierarchical order:

1. **Tier 1 (Authoritative)**:
   * Official framework documentation, official RFCs / standards (e.g. RFC 7519, RFC 6749), upstream GitHub release notes.
2. **Tier 2 (High Quality Secondary)**:
   * Engineering blogs from reputable tech organizations (e.g., Netflix TechBlog, Martin Fowler, Uber Engineering).
3. **Tier 3 (Community)**:
   * StackOverflow answers, medium blogs, forum discussions (treat only as hints, never as proof).

Prompt the AI:
```text
Act as my Researcher.
Research Question: [State question]
Scope: [State versions and constraints]
Prefer official documentation and RFC standards.
Distinguish verified facts from interpretations, hypotheses, and recommendations.
```

---

### Stage 3 — Evidence Classification
Every finding must be tagged:
* **Fact**: Directly quoted/cited from official specs or release notes.
* **Interpretation**: Deductive reasoning based on facts.
* **Hypothesis**: Plausible assumption needing verification via benchmark or spike.
* **Recommendation**: Suggested path given specific business trade-offs.

---

### Stage 4 — Trade-Off Analysis Matrix
Never evaluate a technology in isolation. Build an explicit comparison table:

| Dimension | Option A (e.g., PostgreSQL JSONB) | Option B (e.g., MongoDB) |
| :--- | :--- | :--- |
| **ACID & Transactions** | Strong relational consistency | Document-level atomicity |
| **Schema Flexibility** | Hybrid relational + dynamic schema | Fully schema-less |
| **Tooling & Ecosystem** | Standard SQL, flyway, pgAdmin | Mongo shell, Compass |
| **Operational Overhead**| Existing relational cluster | New cluster to monitor & backup |
| **Failure Modes** | Large JSONB updates rewrite entire row | Inconsistent schemas across records |

---

### Stage 5 — Synthesis & Decision Recording
Synthesize findings into an Architectural Decision Record (ADR) or Concept Note:
1. **Context**: Why was the decision necessary?
2. **Decision**: What did we choose?
3. **Status**: Accepted / Proposed / Rejected.
4. **Consequences**: What becomes easier? What becomes harder? What debt are we taking on?

---

### Stage 6 — Uncertainty Disclosure
Explicitly list what remains uncertain:
* Unverified performance under extreme loads
* Upcoming breaking changes in future framework versions
* Missing official benchmarks
