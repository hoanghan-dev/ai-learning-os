# Technology Mental Model: [Technology / System Name]

* **Category**: [Framework / Database / Distributed Engine / Runtime]
* **Version Evaluated**: [e.g., Spring Boot 3.3 / PostgreSQL 16 / React 18]
* **Last Verified Date**: [YYYY-MM-DD]
* **Authoritative Documentation**: [URL to official specs]

---

## 1. Executive Summary & Paradigm
* **What is it?**: [One-sentence formal definition]
* **Core Paradigm**: [e.g., Inversion of Control, Event-Driven, Append-Only Log, Functional Reactive]
* **Fundamental Invariant**: [The core promise or guarantee this system provides to developers]

---

## 2. Core Abstractions & Terminology

| Abstraction / Entity | Definition | Boundary / Scope |
| :--- | :--- | :--- |
| **[Term 1]** | [What it represents] | [Where it lives] |
| **[Term 2]** | [What it represents] | [Where it lives] |
| **[Term 3]** | [What it represents] | [Where it lives] |

---

## 3. Architecture & Internal Data Flow

```text
[Client / External World]
           │
           ▼
   ┌──────────────────────────────────────────────┐
   │             Boundary / Gateway               │
   └──────────────────────┬───────────────────────┘
                          ▼
   ┌──────────────────────────────────────────────┐
   │           Core Processing Engine             │
   │  ┌────────────────┐     ┌─────────────────┐  │
   │  │ Subsystem 1    │ ──→ │ Subsystem 2     │  │
   │  └────────────────┘     └─────────────────┘  │
   └──────────────────────┬───────────────────────┘
                          ▼
   ┌──────────────────────────────────────────────┐
   │            State / Persistence Store         │
   └──────────────────────────────────────────────┘
```

### Lifecycle / Request Flow:
1. **Ingestion**: [How inputs arrive]
2. **Transformation / Routing**: [How data is processed]
3. **Commit / Persistence**: [How state is persisted]
4. **Response / Event Egress**: [How outputs return]

---

## 4. Key Guarantees & Non-Guarantees
* **What the system guarantees**:
  * [e.g., Exactly-once delivery within a transaction, Serializability, At-least-once processing]
* **What the system does NOT guarantee**:
  * [e.g., Global ordering across partitions, Zero downtime on master failover]

---

## 5. Critical Failure Modes & Edge Cases
1. **Resource Exhaustion**: [Out of memory, thread starvation, connection pool exhaustion]
2. **Network Partitions / Timeouts**: [Split-brain scenarios, stale reads]
3. **Misconfiguration Gotchas**: [Common subtle errors in production setup]

---

## 6. Decision Matrix: When to Adopt vs Avoid

| Dimension | Ideal Fit | Poor Fit / Overkill |
| :--- | :--- | :--- |
| **Scale / Load** | [e.g., > 10k req/sec with caching] | [Simple CRUD with < 100 users] |
| **Team Size** | [Strict separation of concerns] | [Solo hackathon prototype] |
| **Consistency Needs** | [Strict ACID financial ledger] | [Eventual consistency analytics] |

---

## 7. Deep Recall Verification Prompts
*Can you explain the following without referencing this document or AI?*
1. [Explain the exact path of a request from arrival to response]
2. [Explain how this system behaves when its underlying storage becomes unavailable]
3. [Compare this technology with its primary competitor on 3 key trade-offs]
