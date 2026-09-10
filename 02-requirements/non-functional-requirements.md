# Non-Functional Requirements (NFRs)

> **Status:** Draft
> **Owner:** [Name/role]
> **Last Updated:** [YYYY-MM-DD]
> **Version:** 0.1
> **Related Documents:** [`functional-requirements.md`](./functional-requirements.md), [`../01-business-context/assumptions-and-constraints.md`](../01-business-context/assumptions-and-constraints.md)

## 1. Conventions

- **ID format:** `NFR-###`.
- Each NFR must state a measurable target, not a vague aspiration (e.g., "page loads in under 2 seconds at 95th percentile" not "the system should be fast").

## 2. Requirements by Category

### 2.1 Performance

| ID | Requirement | Target/Metric | Priority | Status |
|---|---|---|---|---|
| NFR-001 | [To be completed] | [To be completed] | [Must/Should/Could] | Draft |

### 2.2 Scalability

| ID | Requirement | Target/Metric | Priority | Status |
|---|---|---|---|---|
| NFR-010 | [To be completed] | [To be completed] | [Must/Should/Could] | Draft |

### 2.3 Availability & Reliability

| ID | Requirement | Target/Metric | Priority | Status |
|---|---|---|---|---|
| NFR-020 | [To be completed] | [To be completed] | [Must/Should/Could] | Draft |

### 2.4 Security

| ID | Requirement | Target/Metric | Priority | Status |
|---|---|---|---|---|
| NFR-030 | **[Confirmed default access model]** Field Sales Representatives have access to SR6 (base) by default; the Service Team has access to Vision by default. Dual access (a person with both SR6 and Vision) is an **exception**, granted by the Sales Manager/Team Manager or the Admin role. | [Open Question — not yet defined] | [Open Question] | Draft |
| NFR-031 | **[Confirmed]** The Manager's elevated visibility (prediction list, performance dashboard, promotion suggestions) is scoped to **their own team only**, not the whole organisation. | [Open Question — not yet defined] | [Open Question] | Draft |
| NFR-032 | **[Confirmed]** The Manager has the **same functionality as a rep** — i.e., the Manager can act on a prediction (send as-is/edit/add/decline) on behalf of a rep on their team, not just view. **[Confirmed business rule]** When a Manager acts on a rep's behalf, the rep must be **notified/informed** that the Manager acted for them. Exact notification mechanism (in-app, email, etc.) not yet defined. | [Open Question — notification mechanism not yet defined] | [Open Question] | Draft |

### 2.5 Usability & Accessibility

| ID | Requirement | Target/Metric | Priority | Status |
|---|---|---|---|---|
| NFR-040 | [To be completed] | [To be completed] | [Must/Should/Could] | Draft |

### 2.6 Compliance & Regulatory

| ID | Requirement | Target/Metric | Priority | Status |
|---|---|---|---|---|
| NFR-050 | [To be completed] | [To be completed] | [Must/Should/Could] | Draft |

### 2.7 Maintainability & Supportability

| ID | Requirement | Target/Metric | Priority | Status |
|---|---|---|---|---|
| NFR-060 | [To be completed] | [To be completed] | [Must/Should/Could] | Draft |

### 2.8 Data Retention & Privacy

*Cross-reference [`../06-data/data-requirements.md`](../06-data/data-requirements.md) for detail.*

| ID | Requirement | Target/Metric | Priority | Status |
|---|---|---|---|---|
| NFR-070 | [To be completed] | [To be completed] | [Must/Should/Could] | Draft |
