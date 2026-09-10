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
| CON-001 | **[Correction — supersedes the prior version of this row, per the signed Native Software proposal]** SR6 and Vision are existing vendor (Native Software/integraSell) products, not to be built from scratch. Vision is currently in "alpha testing" at the vendor. This initiative covers **base installation** of both, plus scoping of any Jasco-specific **customisations** beyond the base (separately costed, requiring a signed Project Specification before build). | Technical/Commercial | The Service Team (and Field Sales Reps) will consume predictions through SR6 with the Vision module installed — this is a vendor product configuration/customisation exercise, not internal ground-up development. | If misunderstood, effort/budget could be misallocated to building functionality the vendor already provides, or customisations could be assumed "free" when they require separate costing. |
| CON-003 | **[Confirmed — from the signed proposal's commercial terms]** Base installation costs: SR6 Base $2,380 + Vision Base module $3,780 = $6,160 (excl. GST), one-off. Ongoing: $80/month (2 licences included), $35/rep/month for additional licences. Any billable support/customisation work beyond base is charged at $200/hour and requires client approval. **No customisations are currently costed** — the proposal states "No Customisations are currently known." | Budget | Any requirement surfaced during this discovery that goes beyond the five base high-level requirements will need separate costing/approval before it can be built. | Scope creep into "customisation" territory without budget approval could stall or derail the project. |
| CON-004 | **[Confirmed — from the proposal's Key Risks]** Native Software cannot guarantee the performance of the external tools this solution depends on: AI, SMS messaging, and email delivery. | Technical | The solution's reliability for message delivery and AI-driven interpretation depends on third-party service availability outside the vendor's control. | Message delivery failures or AI misinterpretation of customer replies could go unnoticed without adequate monitoring. |
| CON-002 | **[Correction — a prior version of this row incorrectly stated SMS/Email only]** Phone calls are not being dropped. Future-state outreach is: SMS or Email as the first attempt (AI-suggested best channel), with phone call available as a rep-initiated manual follow-up if judged necessary. | Business/Technical | Phone call remains the reps' only outreach mechanism today and stays available going forward; SMS/Email is a new, additional first-touch step, not a replacement. | If misunderstood, the solution could wrongly remove reps' ability to call, which is their current sole channel. |

## 3. Dependencies

*External systems, teams, or deliverables this initiative depends on, or that depend on it.*

| ID | Dependency | Direction (Depends On / Depended On By) | Owner/Team | Status | Target Date |
|---|---|---|---|---|---|
| DEP-001 | **[Confirmed — from the proposal's Responsibilities Matrix]** Moving to build (Vendor Phase 3) depends on completing this Detailed Requirements Analysis (Phase 2) and Native Software producing and Jasco signing off a Project Specification document. | Depends On | Native Software (produces spec) / Jasco Distributing (signs off) | In Progress (this discovery) | [To be completed] |
| DEP-002 | **[Confirmed — from the proposal]** Vision is currently in "alpha testing" at the vendor — this initiative's timeline depends on Vision's own release/stability status, which is outside Jasco's or this BA's control. | Depends On | Native Software | [Open Question — current alpha status/timeline not known] | [To be completed] |

## 4. Risks Arising from Assumptions/Constraints

*Link to a risk register if one exists elsewhere; otherwise track lightly here.*

| ID | Risk | Likelihood | Impact | Mitigation | Owner |
|---|---|---|---|---|---|
| RSK-001 | **[Confirmed as a real gap]** Urgency rating calculation criteria (how "order history" translates into a rating) has not been decided by the business. Vision's core prioritisation logic cannot be finalised until this is resolved. **[Confirmed]** The base product itself does not define or provide this — it is not covered in the signed proposal's five high-level requirements, reinforcing that it is a customisation to be scoped here. **[Proposed — drafted by the BA/AI assistant at the stakeholder's request; NOT yet approved]** A candidate urgency rating model for the cleaning-products/hotel-industry context is documented in `business-problem.md` §1. It still requires the Business Analyst/Product Owner's review, adjustment, and formal approval before it can move from "Proposed" to "Decision." | [To be completed] | Medium–High — blocks Vision design/build | Business Analyst/Product Owner to define and approve urgency rating criteria before requirements are finalised for this feature. | [To be completed] |
| RSK-002 | **[Confirmed — from the proposal's own Key Risks]** The vendor recommends thorough testing and an initial **manual-messaging-only pilot** (no scheduled/automated sending) for a handful of customers before enabling full automation, because the system will send many customer-facing messages that must present Jasco Distributing positively. | Medium | Medium–High — reputational risk if messages are wrong/unclear at scale | Launch with manual messaging for a pilot group; only enable the Scheduler (automated nightly prediction + timed sends) once validated. | [To be completed] |
