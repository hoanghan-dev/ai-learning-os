# Feature Plan: [Feature Name]

* **Project**: [Link to Project Spec]
* **Target Dependency**: [D0 Independent / D1 Docs Assisted / D2 Hint Assisted]
* **Estimated Effort**: [e.g., 2 hours]
* **Status**: [Draft / In Progress / Implemented / Reviewed]

---

## 1. User Story & Acceptance Criteria

### User Story:
> As a [Role], I want [Action], so that [Value/Goal].

### Acceptance Criteria:
* [ ] **Given** [Initial state], **When** [Action taken], **Then** [Expected outcome].
* [ ] **Given** [Invalid input], **When** [Submitted], **Then** [Specific 4xx error returned].
* [ ] **Given** [Concurrent requests], **When** [Triggered], **Then** [State consistency maintained].

---

## 2. Technical Design & Contracts

### API Contract (If Applicable):
* **Endpoint**: `POST /api/v1/resource`
* **Request Payload**:
  ```json
  {
    "field": "value"
  }
  ```
* **Success Response (201 Created)**:
  ```json
  {
    "id": "uuid",
    "status": "ACTIVE"
  }
  ```

### Database Schema Changes:
* [Table additions, column definitions, or index creations]

---

## 3. Step-by-Step Implementation Sequence

1. [ ] **Step 1**: Write domain entity and unit test.
2. [ ] **Step 2**: Implement repository query and database migration.
3. [ ] **Step 3**: Implement service layer logic with error handling.
4. [ ] **Step 4**: Implement REST controller and validation annotations.
5. [ ] **Step 5**: Write end-to-end integration test.

---

## 4. Explainability Checkpoint (Pre-Merge Audit)

Answer these questions before submitting this feature:
* [ ] What exception handling exists if the persistence layer fails?
* [ ] How is the transaction boundary defined, and what happens on rollback?
* [ ] What is the time complexity of any collection operations in this feature?
* [ ] Did I write every line of code myself or fully inspect and understand any hints used?
