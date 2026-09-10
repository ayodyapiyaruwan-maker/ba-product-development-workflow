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

**[Confirmed]** Resolved: the order prediction engine is a separate, named tool called **"Vision"**. It is intended to be integrated (embedded) into a CRM called **SR6 (Sales Rep 6)**, which the Service Team is supposed to use, and which is connected to Accredo ERP. This is consistent with "nothing exists today" — Vision/SR6 integration is the planned future-state capability, not something already running internally.

**[Correction — supersedes the previous version of this line, per the signed Native Software proposal for Jasco Distributing]** SR6 and Vision are **not being built from scratch by this initiative**. Both are existing products of the vendor **Native Software**, branded "integraSell Sales Rep 6" and "integraSell Vision." Vision is currently in **"alpha" testing** at the vendor. What this initiative involves is the **base installation** of SR6 and the Vision module for Jasco Distributing (the client), plus scoping any **customisations** beyond that base (e.g., the still-undecided urgency rating logic) through a separate, further-costed analysis — which is what this discovery process is feeding into.

**[Confirmed]** The client is **Jasco Distributing**. The vendor/solution provider is **Native Software**. A formal Proposal document (v1.0, 28 Jul 2026, "Proposal – Order Prediction and Sales Team Support") has been produced by Native Software for Jasco Distributing, covering the **Phase 1 "Proposal"** stage of their project lifecycle. Per that document's own Responsibilities Matrix, signing this Proposal is agreement to move into **Phase 2 "Detailed Requirements Analysis"** — which aligns with where this BA discovery currently sits. Signing it is not yet approval to build; a further **Project Specification** must be produced and signed off before build starts.

**[Correction — supersedes the previous version of this line]** Phone calls are **not** being dropped. Today, phone call is the **only** mechanism reps have to contact customers. In the future state, the first outreach attempt will be an SMS or Email (with AI suggesting which of the two is the best method for that customer/rep to use); if the rep judges a phone call is needed, they place it next as a manual follow-up. So the future channel set is SMS + Email (AI-suggested, first attempt) plus phone call (rep-initiated, follow-up) — phone call remains in the picture throughout.

**[Confirmed]** The future-state prediction list will be **ordered/prioritised by an "urgency rating"**, and each item will show customer details plus **which product(s) and what quantities** the customer is likely to order.

**[Confirmed]** Resolved: AI **only recommends** the channel (SMS or Email) — it does not send automatically. The rep manually decides what happens next, choosing to: (a) send the predicted order as-is, (b) edit the products on the predicted order, or (c) add new products to the order, before any outreach goes out.

**[Confirmed]** Urgency rating is based on **order history**, but the specific calculation criteria have **not yet been decided by the business**. This is not a knowledge gap on the BA's side — it is an undecided business decision. **[Decision Needed]** The Business Analyst/Product Owner must define the urgency rating criteria before Vision's design can proceed.

**[Proposed — drafted at the stakeholder's explicit request; NOT a decision, requires review/approval]** A candidate urgency rating model for the cleaning-products/hotel-industry context, combining five weighted factors into a single score (e.g., 0–100):

1. **Predicted-order timing** — how soon/overdue the predicted reorder date is within the 24–72 hour window (closer/overdue = more urgent). Weighted highest, since this is the core "act now" signal.
2. **Estimated stock depletion** — using the hotel's historical consumption rate vs. their last order quantity, estimate how many days of supply they likely have left (fewer days left = more urgent). Relevant because hotels can't have gaps in essential cleaning/hygiene supply for guest-facing and compliance reasons.
3. **Product criticality** — core hygiene/sanitation items (e.g., disinfectant, surface cleaner) weighted higher than discretionary/promotional items, since a stock-out on essentials has bigger operational impact for a hotel.
4. **Customer value/tier** — higher-value or strategic hotel accounts weighted higher, so rep attention goes where relationship/revenue impact is greatest.
5. **Prediction confidence** — how consistent the customer's historical order cycle is (a hotel with a very regular 30-day cycle = high confidence; erratic history = lower confidence, which could reduce urgency or flag the prediction for manual review rather than automatic high-priority placement).

Example structure: `Urgency Score = (W1 × Timing) + (W2 × Stock Depletion) + (W3 × Product Criticality) + (W4 × Customer Tier) + (W5 × Prediction Confidence)`, with weights (W1–W5) to be set/tuned by the business. **This is a starting proposal only** — factors, weights, and even whether all five are relevant to Jasco's actual operation need the Business Analyst/Product Owner's review before this becomes an approved requirement.

**[Confirmed]** The following data fields will be fed from Accredo ERP to Vision (the order prediction engine): customer name, account ID, contact person(s), contact info, order history summary, product name, product code, quantity.

**[Confirmed — via architecture diagram]** The data flow is: **Accredo ERP → Adapter/Integration Service → Vision Order Prediction Engine**. The Adapter/Integration Service also integrates with a separate **Customer Data** store (used by Vision), an **Admin Service**, and an **Agent Service**. Vision stores its output in its own **separate Vision Database** (distinct from the SR6 Database). The **Vision Module embedded in SR6** reads/writes the Vision Database; SR6's own **Controllers and Views** read/write the SR6 Database. So Vision does not receive data through the pre-existing SR6–Accredo connection — it has its own integration path via the Adapter/Integration Service.

**[Open Question]** What are the **Admin Service** and **Agent Service** shown in the architecture — what do they do, and are they existing or to-be-built? Not yet explained. **[Partial update]** Both Field Sales Representatives and Service Team can use Vision, with access levels defined by a Sales Manager/Team Manager, plus a separate Admin role — see `stakeholders.md` (STK-003, STK-004). Whether the Admin role corresponds to the diagram's "Admin Service" is still unconfirmed.

**[Confirmed]** The business's customers span **different industries**, not just one. There is a specific **customer proposal** driving the initial build focus — development is prioritising that first, but the underlying architecture is intended as a **generic product usable by any customer that uses Accredo ERP**, not something bespoke to one customer only.

**[Resolved]** The "customer proposal" driving the initial focus is confirmed to be **Jasco Distributing** (see signed proposal, logged as a Source below).

**[Confirmed]** Jasco Distributing's customer base includes multiple segments, but **hotels** is confirmed as the primary segment identified so far, and the **prototype will be based on/scoped to hotels first**. Other segments exist and will be considered later — hotels is the initial focus, not the only one.

**[Reaffirmed — still open, not resolved]** The urgency rating calculation criteria remain **undecided**. The stakeholder has explicitly confirmed this should stay logged as an open question requiring an answer, rather than being resolved now — see RSK-001 in `assumptions-and-constraints.md`.

**[Confirmed]** Jasco Distributing's business is **cleaning products**. This is consistent with the proposal's own promotion examples ("Promote Nitrile gloves to all hotels," "promote mop pads to those that order the appropriate mop") and **corrects** the earlier "bulk food industry" mention from discovery — that was not accurate; cleaning products is the confirmed industry.

**[Confirmed — from the signed proposal's High-Level Requirements]** The following are the vendor-recorded high-level requirements for this initiative:
1. Implement SR6 Base and the Vision base module for order prediction, using **12–24 months** of sales history to determine usage/seasonality patterns.
2. Cater for **product replacements** (where products are superseded).
3. Send predicted orders via **email and/or SMS**, allowing the Customer Service Team user to **personalise the message** if required.
4. Include **promotions** in the messaging, specific to the customer.
5. Provide a way to **check performance** of the prediction and messaging systems.

**[Confirmed — new detail from the proposal, not previously known]** Beyond the rep-side "send as-is / edit / add" decision already logged, the proposal describes what happens **after** a message is sent: the **customer** may reply directly to the SMS/Email (e.g., "Yes please"), and an **AI Message Handler** automatically interprets the reply and acts — submitting the order, editing and submitting it, marking it declined, or asking the customer to confirm a swap. The message also contains a link to a **customer-facing Order Portal** (no login required — a unique code identifies the customer) where the customer can themselves swap, remove, or add products and submit the order directly.

**[Confirmed — from the proposal]** Promotions can be included in predicted-order messaging via three approaches: (a) **customer segment**-based (e.g., a product promoted to a whole segment), (b) **cross-sell** (promote a related product when a specific product is on the order), and (c) **dynamic**, where AI scans the predicted order, order history, and current promotions to select good-match promotional items.

**[Confirmed — from the proposal, resolves the Reporting/Performance discovery topic]** A **performance dashboard** is available to both the Customer Service Team user and their manager, showing: prediction accuracy, message engagement, promotion success, sales generated from Vision predictions, and the count of swaps/other order changes.

**[Confirmed — from the proposal's Key Risks]** The vendor recommends **launching with manual messages only (no scheduled/automated sending) for a handful of customers** first, to thoroughly test the prediction system before enabling the optional Scheduler component (which can automate nightly prediction generation and timed SMS/email sending). This refines the earlier-confirmed "AI recommends, rep manually decides" flow — that manual mode is explicitly the recommended starting point, with scheduled automation as a later, optional step.

**[Confirmed — from the proposal's Out of Scope / commercial terms]** The currently signed proposal covers **base installation only** (SR6 Base: $2,380; Vision Base module: $3,780; total $6,160 excl. GST, one-off) plus ongoing monthly fees ($80/month for 2 licences, $35/rep/month for additional licences). **No customisations are included.** Anything beyond the five high-level requirements above — including the still-undecided urgency rating logic, specific promotion segment definitions, and the exact access-level permission matrix — counts as a customisation requiring further analysis and separate costing before it can be built.

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
| "Proposal – Order Prediction and Sales Team Support," Native Software, for Jasco Distributing, v1.0 | Document (signed Proposal, Phase 1) | 28 Jul 2026 (proposal date); received 2026-09-10 | Authoritative source for objectives, high-level requirements, vendor/client identity, base-vs-customisation scope boundary, and Phase 1→2 gating. |
