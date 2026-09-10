# BA Product Development Workspace

This repository is a **Business Analyst (BA) workspace** for taking a product from a raw business problem through to a development-ready, testable specification. It does not contain product code. It contains the artefacts a BA produces and maintains across the product lifecycle, structured so that every requirement can be traced from business problem → requirement → user story → acceptance criteria → test case.

## How this repository is organized

Folders are numbered in the order a BA typically works through them, though in practice the work is iterative — you will revisit earlier folders as understanding deepens.

| Folder | Purpose |
|---|---|
| `01-business-context/` | Why this initiative exists: the business problem, objectives, stakeholders, scope, and the assumptions/constraints bounding the work. |
| `02-requirements/` | The requirements themselves: functional, non-functional, and business rules. |
| `03-users/` | Who the product is for: personas and the journeys they take. |
| `04-process/` | How work happens today and/or will happen: process flows (current-state and future-state). |
| `05-agile-artefacts/` | Delivery-ready breakdown: user stories and their acceptance criteria. |
| `06-data/` | Data entities, sources, quality rules, and data flows the solution depends on. |
| `07-ux-ui/` | UX/UI requirements and prototype references. |
| `08-handoff/` | The developer handoff package — what engineering needs to build from. |
| `09-testing-uat/` | Test strategy, test cases, and User Acceptance Testing plan/sign-off. |
| `10-traceability/` | The Requirements Traceability Matrix (RTM) linking every artefact together. |

Every template file starts with a status block (Status / Owner / Last Updated / Version) so you can track maturity at a glance, and a **Related Documents** section so artefacts stay linked to each other.

## How a BA should use this repository through the product lifecycle

### 1. Discovery & Framing (`01-business-context/`)
Start here. Capture the business problem in the stakeholders' own words before proposing solutions. Confirm objectives are measurable, map every stakeholder and their influence/interest, and agree scope boundaries and constraints in writing before requirements work begins. This folder is your anchor — if a later requirement can't be traced back to something here, question whether it belongs in this initiative.

### 2. Requirements Elicitation & Analysis (`02-requirements/`, `03-users/`, `04-process/`)
Run elicitation sessions (interviews, workshops, surveys, document analysis, observation) and record:
- **Personas** for each distinct user type, and the **journeys** they take through the product.
- **Process flows** for current-state ("as-is") and future-state ("to-be") processes.
- **Functional requirements** — what the system must do.
- **Non-functional requirements** — performance, security, usability, compliance, availability, etc.
- **Business rules** — constraints and logic that govern behaviour regardless of which feature implements it.

Keep requirements atomic, testable, and uniquely IDed (see the ID conventions in each template) so they can be tracked in the RTM.

### 3. Delivery Preparation (`05-agile-artefacts/`)
Decompose approved requirements into user stories with clear acceptance criteria. Each story should trace back to one or more functional/non-functional requirements. This is the handoff point between "what the business needs" and "what a delivery team will build in a sprint."

### 4. Data & Experience Design (`06-data/`, `07-ux-ui/`)
Define data requirements (entities, attributes, sources, quality, retention, privacy) and UX/UI requirements. Link to prototypes/wireframes/mockups (Figma, etc.) rather than duplicating design files here — this repo tracks the *requirements the design must satisfy*, not the design artefacts themselves.

### 5. Developer Handoff (`08-handoff/`)
Before development starts, assemble the handoff package: confirmed requirements, stories, acceptance criteria, data model, UX/UI specs, open questions/decisions log, and definition of done. This is the BA's quality gate — nothing should reach engineering that hasn't passed through this checklist.

### 6. Testing & UAT (`09-testing-uat/`)
Define the test strategy and UAT plan before development finishes, not after. Acceptance criteria from `05-agile-artefacts/` should map directly into test cases here, and UAT sign-off should map back to business objectives in `01-business-context/`.

### 7. Traceability (`10-traceability/`)
Maintain the Requirements Traceability Matrix continuously, not as an afterthought. Every row should let you answer: *which business objective does this serve, which requirement defines it, which story delivers it, which test verifies it, and what is its current status?*

## Working principles

- **No fabricated content.** Every template in this repository is intentionally empty of specific business content — placeholders only. Nothing should be filled in until it has come from a real stakeholder, workshop, document, or decision.
- **One source of truth per fact.** Don't duplicate a requirement's definition across files — link to it by ID instead.
- **Version and date everything.** Use the status block at the top of each document; update "Last Updated" whenever content materially changes.
- **Trace everything.** If you can't trace a requirement to a business objective, or a story to a requirement, treat that as a gap to resolve, not a formatting nicety.

## Next step

See the prompt at the end of the session for what information is needed from you to begin populating `01-business-context/`.
