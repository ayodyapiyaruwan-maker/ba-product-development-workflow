# Assumptions, Constraints, and Dependencies

> **Status:** Draft
> **Owner:** [Name/role]
> **Last Updated:** [YYYY-MM-DD]
> **Version:** 0.1
> **Related Documents:** [`scope.md`](./scope.md), [`../02-requirements/non-functional-requirements.md`](../02-requirements/non-functional-requirements.md)

## 1. Assumptions

*Things believed to be true, not yet validated, that the initiative is planning around. Each should be validated or converted to a risk if it proves false.*

| ID | Assumption | Validation Status | Validation Method | Owner |
|---|---|---|---|---|
| ASM-001 | [To be completed] | [Unvalidated/Validated/Invalidated] | [To be completed] | [To be completed] |

## 2. Constraints

*Fixed limitations the solution must operate within (budget, timeline, technology, regulatory, resourcing).*

| ID | Constraint | Type (Budget/Time/Technical/Regulatory/Resource/Other) | Description | Impact if Violated |
|---|---|---|---|---|
| CON-001 | **[Confirmed]** Technical landscape already fixed: SR6 (Sales Rep 6) CRM already exists and is already connected to Accredo ERP. "Vision" (the order prediction engine) does not exist yet and must be built, then embedded into SR6. | Technical | The Service Team is expected to consume predictions through SR6 CRM (with Vision embedded as the prediction engine), not through a new/different interface. This initiative's build scope is effectively Vision itself plus its embedding into SR6 — not SR6 or the Accredo connection, which already exist. | If misunderstood, effort could be wrongly spent rebuilding SR6/Accredo connectivity instead of focusing on Vision. |
| CON-002 | **[Confirmed]** Future-state outreach channels are limited to SMS and Email only. | Technical/Business | Phone calls (used in today's manual process) are not part of the future automated outreach channel set. | If incorrect, the solution would omit a channel reps currently rely on. |

## 3. Dependencies

*External systems, teams, or deliverables this initiative depends on, or that depend on it.*

| ID | Dependency | Direction (Depends On / Depended On By) | Owner/Team | Status | Target Date |
|---|---|---|---|---|---|
| DEP-001 | [To be completed] | [To be completed] | [To be completed] | [To be completed] | [YYYY-MM-DD] |

## 4. Risks Arising from Assumptions/Constraints

*Link to a risk register if one exists elsewhere; otherwise track lightly here.*

| ID | Risk | Likelihood | Impact | Mitigation | Owner |
|---|---|---|---|---|---|
| RSK-001 | [To be completed] | [Low/Med/High] | [Low/Med/High] | [To be completed] | [To be completed] |
