# Business Problem Statement

> **Status:** Draft
> **Owner:** [Name/role]
> **Last Updated:** [YYYY-MM-DD]
> **Version:** 0.1
> **Related Documents:** [`business-objectives.md`](./business-objectives.md), [`stakeholders.md`](./stakeholders.md)

## 1. Problem Statement

*Describe, in the stakeholders' own language, the problem that exists today. What is happening, to whom, and why does it matter? Avoid describing a solution here.*

**[Confirmed]** The Sales Service Team wants visibility of which existing customers are likely to place an order in the next 24–72 hours, so they can proactively contact those customers (by email or message) and convert the likely intent into an actual, completed ("materialised") order. The stated purpose is not only short-term conversion but building long-lasting relationships with existing customers through a consistent, automated outreach process.

**[Confirmed]** An "order prediction" is at the **customer + product level** — i.e., a prediction that a specific existing customer is likely to reorder a specific product, within the 24–72 hour window. The prediction is derived from that customer's previous buying patterns (historical order data).

**[Confirmed]** No automated order-prediction capability exists today anywhere in the business. Generating the prediction is new ground for this initiative (see Current State below).

**[Open Question]** The stakeholder mentioned "Accredo ERP ... and order prediction engine" in the same breath, but also separately confirmed "nothing exists today." This needs clarifying: is there any prediction engine (even a basic/legacy one, inside or outside Accredo) that already exists in any form, or was "order prediction engine" referring to the capability this initiative is meant to introduce? Currently assumed to mean the latter, but not yet confirmed.

## 2. Context and Background

*What is the history of this problem? How was it identified? What triggered this initiative (e.g., customer complaints, an audit finding, a strategic decision, a competitive pressure)?*

**[Confirmed]** This requirement originates from the Sales Service Team (specifically raised by a Service Team Rep).
**[Open Question]** What triggered this now — is there a specific event, target, or strategic goal driving it (e.g., a retention KPI, a competitive pressure, a customer churn concern)? Not yet provided.

## 3. Current State ("As-Is")

*How are things done today, if at all? What workarounds exist?*

**[Confirmed]** Today the process is entirely manual: the Sales Service Team looks at previous order data (held in Accredo ERP) and guesses which customers are likely to reorder, then calls the customer directly.

**[Open Question]** The original ask described outreach via "email or message," but the current-state description here uses "give a call." Is phone call an acceptable/desired channel for the future automated process too, or should the future state be limited to email/message as originally stated? Needs confirming — not yet a decision.

## 4. Impact of the Problem

| Impact Area | Description | Evidence / Data Source |
|---|---|---|
| Financial | [To be completed] | [To be completed] |
| Operational | [To be completed] | [To be completed] |
| Customer/User | [To be completed] | [To be completed] |
| Compliance/Risk | [To be completed] | [To be completed] |

## 5. Who Is Affected

*Reference [`stakeholders.md`](./stakeholders.md) for full detail; summarise the affected groups here.*

[To be completed]

## 6. Cost of Doing Nothing

*What happens if this problem is not addressed?*

[To be completed]

## 7. Sources

*Interviews, workshops, documents, data analysis, or other evidence used to compile this problem statement.*

| Source | Type | Date | Notes |
|---|---|---|---|
| Discovery conversation with Business Analyst/Product Owner | Interview | 2026-09-10 | Initial framing of the Sales Service Team's order-prediction outreach need. |
