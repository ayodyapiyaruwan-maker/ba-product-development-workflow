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

**[Confirmed]** Resolved: the order prediction engine is a separate, named tool called **"Vision"**. It is intended to be integrated (embedded) into a CRM called **SR6 (Sales Rep 6)**, which the Service Team is supposed to use, and which is connected to Accredo ERP. This is consistent with "nothing exists today" — Vision/SR6 integration is the planned future-state capability, not something already running.

**[Confirmed]** SR6 CRM already exists/is already built. The SR6–Accredo connection is also already built. **Vision does not yet exist and is something to be built** as part of this initiative; once built, it will be embedded into SR6 for the Service Team to use.

**[Correction — supersedes the previous version of this line]** Phone calls are **not** being dropped. Today, phone call is the **only** mechanism reps have to contact customers. In the future state, the first outreach attempt will be an SMS or Email (with AI suggesting which of the two is the best method for that customer/rep to use); if the rep judges a phone call is needed, they place it next as a manual follow-up. So the future channel set is SMS + Email (AI-suggested, first attempt) plus phone call (rep-initiated, follow-up) — phone call remains in the picture throughout.

**[Confirmed]** The future-state prediction list will be **ordered/prioritised by an "urgency rating"**, and each item will show customer details plus **which product(s) and what quantities** the customer is likely to order.

**[Confirmed]** Resolved: AI **only recommends** the channel (SMS or Email) — it does not send automatically. The rep manually decides what happens next, choosing to: (a) send the predicted order as-is, (b) edit the products on the predicted order, or (c) add new products to the order, before any outreach goes out.

**[Confirmed]** Urgency rating is based on **order history**, but the specific calculation criteria have **not yet been decided by the business**. This is not a knowledge gap on the BA's side — it is an undecided business decision. **[Decision Needed]** The Business Analyst/Product Owner must define the urgency rating criteria before Vision's design can proceed.

**[Confirmed]** The following data fields will be fed from Accredo ERP to Vision (the order prediction engine): customer name, account ID, contact person(s), contact info, order history summary, product name, product code, quantity.

**[Open Question]** The stakeholder referenced "bulk food industry" customers when listing the data fields above. Is this initiative scoped to a **specific customer segment/industry** (e.g., bulk food industry customers only), or was this just an illustrative example? This affects scope and needs explicit confirmation — not assumed either way.

**[Open Question]** Earlier discovery confirmed SR6 CRM is already connected to Accredo ERP, and Vision will be embedded into SR6. This message states data is "fed by Accredo to the order prediction engine [Vision]" directly. Does data flow **Accredo → SR6 → Vision**, or **Accredo → Vision directly** (separately from the existing SR6–Accredo connection)? Not yet confirmed — matters for integration understanding.

## 2. Context and Background

*What is the history of this problem? How was it identified? What triggered this initiative (e.g., customer complaints, an audit finding, a strategic decision, a competitive pressure)?*

**[Confirmed]** This requirement originates from the Sales Service Team (specifically raised by a Service Team Rep).
**[Open Question]** What triggered this now — is there a specific event, target, or strategic goal driving it (e.g., a retention KPI, a competitive pressure, a customer churn concern)? Not yet provided.

## 3. Current State ("As-Is")

*How are things done today, if at all? What workarounds exist?*

**[Confirmed]** Today the process is entirely manual: the Sales Service Team looks at previous order data (held in Accredo ERP) and guesses which customers are likely to reorder. **Phone call is currently the only mechanism reps have to contact customers** — there is no SMS/Email outreach step today.

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
