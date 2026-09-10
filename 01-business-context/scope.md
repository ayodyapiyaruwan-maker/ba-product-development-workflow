# Scope Definition

> **Status:** Draft
> **Owner:** [Name/role]
> **Last Updated:** [YYYY-MM-DD]
> **Version:** 0.1
> **Related Documents:** [`business-objectives.md`](./business-objectives.md), [`assumptions-and-constraints.md`](./assumptions-and-constraints.md)

## 1. In Scope

*What is definitely being delivered as part of this initiative.*

**[Confirmed — from the signed Native Software proposal for Jasco Distributing]** The currently signed scope is **BASE INSTALLATION ONLY** of two vendor products: SR6 Base and the Vision base module. Per the proposal's own "Out of Scope" statement: *"Only functions described in this document are in scope... No customisations are included in this proposal."* The five high-level requirements confirmed in scope are:
1. SR6 Base + Vision base module for order prediction, using 12–24 months of sales history.
2. Handling product replacements (superseded products).
3. Sending predicted orders via email and/or SMS, with Customer Service Team message personalisation.
4. Including customer-specific promotions in messaging.
5. A way to check performance of the prediction and messaging systems.

- **[Proposed — not yet approved as a customisation]** Define and implement the urgency rating calculation criteria (not covered by the base product — see RSK-001).
- **[Proposed — not yet approved as a customisation]** Define the specific access-level permission matrix for Field Sales Representatives, Service Team, Sales Manager/Team Manager, and Admin roles (base product likely ships generic roles; Jasco-specific rules not yet defined).
- **[Proposed — not yet approved]** Preserve the rep's existing ability to follow up by phone call — calls are not being removed, just preceded by an SMS/Email first-touch step (base product does not manage phone calls; this remains a manual, out-of-system activity).

## 2. Out of Scope

*What is explicitly excluded, and why (e.g., future phase, different team, not aligned to objectives).*

- **[Confirmed]** Building SR6 or Vision from scratch — both are existing Native Software/integraSell products; this initiative covers **base installation and configuration**, not ground-up development.
- **[Confirmed]** Any customisation not explicitly listed in the signed proposal's five high-level requirements — per the vendor, these require a separate, further-costed **Detailed Requirements Analysis** and **Project Specification** sign-off before build (this is the stage this BA discovery is feeding).
- **[Correction — a prior version of this document incorrectly proposed excluding phone calls]** Phone call outreach is **in scope of the business process** (as a rep-initiated follow-up channel) even though it is not a feature the base SR6/Vision product manages.

## 3. Scope Boundaries by Area

| Area | In Scope | Out of Scope |
|---|---|---|
| Users/Audience | [To be completed] | [To be completed] |
| Processes | [To be completed] | [To be completed] |
| Systems/Platforms | [To be completed] | [To be completed] |
| Geography/Market | [To be completed] | [To be completed] |
| Data | [To be completed] | [To be completed] |

## 4. Phasing / Release Boundaries

*If delivery is split into phases or releases, define what belongs in each.*

| Phase | Scope Summary | Target Timeframe |
|---|---|---|
| Vendor Phase 1 — Proposal | **[Confirmed]** Native Software's Proposal document produced and (per the user) signed off by Jasco Distributing, covering base SR6 + Vision installation only. | Proposal dated 28 Jul 2026; valid for one month from review/release per its own terms |
| Vendor Phase 2 — Detailed Requirements Analysis | **[Confirmed as the current stage]** This is the stage this BA discovery workspace is operating in — capturing Jasco's detailed requirements (e.g., urgency rating criteria, access-level matrix, promotion segment definitions) ahead of a costed Project Specification. | In progress |
| Vendor Phase 3 — Project Specification & Build | Not yet started — requires sign-off of the Detailed Requirements Analysis and Project Specification per the proposal's Responsibilities Matrix. | Not yet defined |
| Future phase(s) (broader rollout) | **[Confirmed direction, not yet formally approved]** Vision is intended as a **generic product usable by any customer that uses Accredo ERP**, not bespoke to Jasco only. Scope/timing of broader rollout not yet defined. | [To be completed] |

## 5. Scope Change Control

*Process for raising, assessing, and approving scope changes once baselined.*

[To be completed]
