# Requirements Traceability Matrix (RTM)

> **Status:** Draft
> **Owner:** [Name/role]
> **Last Updated:** [YYYY-MM-DD]
> **Version:** 0.1
> **Related Documents:** All artefacts in this repository

## 1. Purpose

The RTM is the single place to verify that every requirement traces forward to delivery and testing, and backward to a business objective. Update it whenever a requirement, story, or test case is added, changed, or retired — do not let it fall out of sync with the source documents.

## 2. Traceability Matrix

| Business Objective (OBJ) | Requirement (FR/NFR) | Business Rule (BR) | User Story (US) | Acceptance Criteria (AC) | Test Case (TC) | UAT Scenario (UAT) | Status |
|---|---|---|---|---|---|---|---|
| OBJ-001 | FR-001 | BR-001 | US-001 | AC-001 | TC-001 | UAT-001 | [Not Started/In Progress/Delivered/Verified] |

*Add one row per requirement (or per requirement/story pair if a requirement maps to multiple stories). Leave a cell blank with `—` if not yet applicable, not empty — a truly empty cell should be treated as a gap to investigate.*

## 3. Coverage Checks

*Run these checks periodically, especially before development starts and before UAT sign-off.*

- [ ] Every objective in `../01-business-context/business-objectives.md` has at least one requirement.
- [ ] Every Must-priority requirement has at least one user story.
- [ ] Every user story has at least one acceptance criterion.
- [ ] Every acceptance criterion has at least one test case.
- [ ] Every Must-priority requirement has at least one UAT scenario.
- [ ] No orphaned rows (an item with no upstream or downstream link).

## 4. Change History

*Track structural changes to scope/requirements that affect traceability, not routine status updates.*

| Date | Change | Reason | Updated By |
|---|---|---|---|
| [YYYY-MM-DD] | [To be completed] | [To be completed] | [To be completed] |
