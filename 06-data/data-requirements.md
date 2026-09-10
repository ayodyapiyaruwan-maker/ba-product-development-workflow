# Data Requirements

> **Status:** Draft
> **Owner:** [Name/role]
> **Last Updated:** [YYYY-MM-DD]
> **Version:** 0.1
> **Related Documents:** [`../02-requirements/non-functional-requirements.md`](../02-requirements/non-functional-requirements.md), [`../08-handoff/developer-handoff.md`](../08-handoff/developer-handoff.md)

## 1. Data Entities

*High-level list of the core data objects this product needs to create, read, update, or delete.*

| Entity | Description | Source System(s) | Owner | Sensitivity (Public/Internal/Confidential/Restricted) |
|---|---|---|---|---|
| Order Prediction **[Confirmed to be needed — this is what Vision must produce]** | A predicted reorder for a specific customer + product, within a 24–72 hour window | Vision (generated), sourced from Accredo order history via SR6 | [Open Question] | [Open Question] |

## 2. Entity Attributes

*Duplicate this table per entity.*

### Entity: Order Prediction

| Attribute | Data Type | Required? | Format/Validation Rule | Default | Notes |
|---|---|---|---|---|---|
| Customer Name | [Open Question] | Y **[Confirmed]** | [To be completed] | — | Fed from Accredo |
| Account ID | [Open Question] | Y **[Confirmed]** | [To be completed] | — | Fed from Accredo |
| Contact Person(s) | [Open Question] | Y **[Confirmed]** | [To be completed] | — | Fed from Accredo; customer may have multiple contacts |
| Contact Info | [Open Question] | Y **[Confirmed]** | [To be completed] | — | Fed from Accredo; presumably needed to enable SMS/Email send |
| Order History Summary | [Open Question] | Y **[Confirmed]** | [To be completed] | — | Fed from Accredo |
| Product Name | [Open Question] | Y **[Confirmed]** | [To be completed] | — | Fed from Accredo |
| Product Code | [Open Question] | Y **[Confirmed]** | [To be completed] | — | Fed from Accredo |
| Quantity (predicted) | [Open Question] | Y **[Confirmed]** | [To be completed] | — | Fed from Accredo |
| Urgency Rating | [Open Question] | Y **[Confirmed needed]** | **[Decision Needed]** Based on order history; exact calculation criteria not yet decided by the business | — | Used to prioritise/order the prediction list |
| AI-Suggested Channel (SMS/Email) | [Open Question] | Y **[Confirmed needed]** | [Open Question — how the AI decides is not yet provided] | — | Recommendation only — rep manually acts on it (send as-is / edit products / add products) |

## 3. Data Sources & Integrations

| Source System | Data Provided | Integration Method (API/File/DB/Manual) | Frequency | Owner |
|---|---|---|---|---|
| Accredo ERP **[Confirmed to exist; used today for selling products to customers, i.e. order processing]** | **[Confirmed]** Feeds, via the Adapter/Integration Service: customer name, account ID, contact person(s), contact info, order history summary, product name, product code, quantity. | **[Confirmed, per architecture diagram]** Accredo → Adapter/Integration Service → Vision (not through the existing SR6–Accredo connection). Exact protocol (API/file/DB) not yet confirmed. | [Open Question] | [Open Question] |
| Adapter/Integration Service **[Confirmed to exist in the architecture; build status (existing vs to-be-built) not yet confirmed]** | Middleware that integrates Accredo ERP with Vision, Customer Data, Admin Service, and Agent Service. | Sits between Accredo ERP and Vision Order Prediction Engine | [Open Question] | [Open Question] |
| Customer Data (store) **[Confirmed to exist in the architecture as a separate store; relationship to Accredo's customer fields not yet confirmed]** | Used by Vision (alongside the Accredo feed) — exact content/overlap with Accredo customer data not yet confirmed | Integrated via Adapter/Integration Service | [Open Question] | [Open Question] |
| SR6 (Sales Rep 6) CRM **[Confirmed: already built/existing, already connected to Accredo ERP]** | Surfaces Vision's order predictions to reps for outreach via the embedded Vision Module; has its own SR6 Database. | **[Confirmed: connected to Accredo ERP already]**; exact method (API/DB/file) not yet confirmed | [Open Question] | [Open Question] |
| Vision Order Prediction Engine **[Confirmed: does not exist yet — to be built as part of this initiative]** | Generates the customer + product reorder predictions, derived from historical buying patterns (via Accredo, through the Adapter/Integration Service) and Customer Data. Stores output in its own **separate Vision Database**, which the Vision Module (embedded in SR6) reads/writes. | Embedded into SR6 CRM; own separate Vision Database (not the SR6 Database) | [Open Question] | [Open Question] |
| Admin Service **[Confirmed to exist in the architecture; purpose not yet explained]** | [Open Question — purpose not yet described] | Integrated via Adapter/Integration Service | [Open Question] | [Open Question] |
| Agent Service **[Confirmed to exist in the architecture; purpose not yet explained — possibly related to the AI channel-recommendation logic, not confirmed]** | [Open Question — purpose not yet described] | Integrated via Adapter/Integration Service | [Open Question] | [Open Question] |

## 4. Data Quality Rules

| Rule | Applies To | Validation Logic | Action on Failure |
|---|---|---|---|
| [To be completed] | [Entity/Attribute] | [To be completed] | [To be completed] |

## 5. Data Migration (if applicable)

- **Source of legacy data:** [To be completed]
- **Volume:** [To be completed]
- **Migration approach:** [To be completed]
- **Reconciliation/validation approach:** [To be completed]

## 6. Data Privacy & Retention

| Data Element | Classification | Regulatory Requirement (e.g., GDPR) | Retention Period | Disposal Method |
|---|---|---|---|---|
| [To be completed] | [To be completed] | [To be completed] | [To be completed] | [To be completed] |

## 7. Reporting & Analytics Needs

*What data needs to be reportable, and to whom?*

[To be completed]
