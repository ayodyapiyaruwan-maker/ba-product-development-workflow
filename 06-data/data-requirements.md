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
| [To be completed] | [To be completed] | [To be completed] | [To be completed] | [To be completed] |

## 2. Entity Attributes

*Duplicate this table per entity.*

### Entity: [Name]

| Attribute | Data Type | Required? | Format/Validation Rule | Default | Notes |
|---|---|---|---|---|---|
| [To be completed] | [To be completed] | [Y/N] | [To be completed] | [To be completed] | [To be completed] |

## 3. Data Sources & Integrations

| Source System | Data Provided | Integration Method (API/File/DB/Manual) | Frequency | Owner |
|---|---|---|---|---|
| Accredo ERP **[Confirmed to exist; used today for selling products to customers, i.e. order processing]** | Presumed: historical customer order/purchase data, used today by the Sales Service Team manually. **[Open Question — not yet confirmed which specific data fields/entities are available or needed]** | [Open Question — not yet confirmed: API, file export, direct DB access, or manual only] | [Open Question] | [Open Question] |
| SR6 (Sales Rep 6) CRM **[Confirmed to be named as the CRM the Service Team is supposed to use; status as already-in-use vs newly introduced is an Open Question]** | Presumed: surfaces order predictions to reps for outreach; connects to Accredo ERP. | **[Confirmed: connects to Accredo ERP]**; exact method (API/DB/file) not yet confirmed | [Open Question] | [Open Question] |
| Vision (order prediction engine) **[Confirmed as the name of the tool; status as an already-selected/licensed product vs still-to-be-built/procured is an Open Question]** | Generates the customer + product reorder predictions, derived from historical buying patterns. | **[Confirmed: plugs into SR6 CRM]**; exact method not yet confirmed | [Open Question] | [Open Question] |

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
