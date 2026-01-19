# Roles and Personas — OctoAcme Project Management

This document describes project roles and personas, their responsibilities, decision authority, and how they interact with other roles. It extends the existing documentation by adding additional personas and clarifying handoffs and accountability.

## Summary of additions
Added the following personas with responsibilities and interaction notes:
- Product Owner
- QA Lead
- DevOps Engineer
- UX Designer
- Business Analyst

---

## Existing core roles (reference)
- Project Manager (PM)
- Engineering Lead
- Release Manager
(Keep existing project-specific descriptions here. The new personas below describe how they interact with these core roles.)

---

## New personas

### Product Owner
- Responsibility
  - Represents business stakeholders and customers.
  - Defines and prioritizes the product backlog and success criteria.
  - Approves scope changes and acceptance criteria for deliverables.
- Decision authority
  - Final say on feature priorities and acceptance of completed work.
- Interactions / Handoffs
  - Works closely with the Project Manager to align priorities to schedule and resource constraints.
  - Collaborates with the Engineering Lead and UX Designer on feasibility and design tradeoffs.
  - Engages QA Lead to confirm acceptance criteria and test scenarios.
- Escalation
  - Escalate scope conflicts to PM; escalate stakeholder disagreements to senior stakeholders or sponsor.

### QA Lead
- Responsibility
  - Defines test strategy, test plans, and acceptance criteria coverage.
  - Coordinates testing schedules across teams and verifies deliverables meet quality gates.
  - Maintains test automation priorities and quality metrics.
- Decision authority
  - Authority to block releases that do not meet defined exit criteria.
- Interactions / Handoffs
  - Receives feature definitions and acceptance criteria from Product Owner.
  - Coordinates test environments and deployments with DevOps Engineer and Release Manager.
  - Reports quality status to PM and Product Owner; coordinates defect triage with Engineering Lead.
- Escalation
  - Escalate critical test-blocking issues to Engineering Lead and PM.

### DevOps Engineer
- Responsibility
  - Design and maintain CI/CD pipelines, environment provisioning, and deployment automation.
  - Ensure production deployments are reproducible, monitored, and can be rolled back.
  - Manage configuration drift, infrastructure-as-code, and release automation.
- Decision authority
  - Responsible for deployment timing and the technical approach for release automation.
- Interactions / Handoffs
  - Works with Engineering Lead for build and pipeline changes; with Release Manager for release windows and rollback plans.
  - Coordinates with QA Lead to provide test environments and automated job scheduling.
- Escalation
  - Escalate unrecoverable deployment or infrastructure incidents to Engineering Lead and PM.

### UX Designer
- Responsibility
  - Conduct user research, design wireframes and prototypes, and validate usability.
  - Ensure user needs are incorporated into acceptance criteria.
- Decision authority
  - Responsible for UX deliverables and sign-off of design-related acceptance criteria.
- Interactions / Handoffs
  - Collaborates with Product Owner to translate business requirements into user journeys.
  - Works with Engineering Lead to ensure feasible implementation of designs.
  - Provides test cases for usability with QA Lead.
- Escalation
  - Escalate major UX tradeoffs to Product Owner and PM.

### Business Analyst
- Responsibility
  - Elicit, document, and clarify business requirements into actionable user stories and acceptance criteria.
  - Maintain traceability between business objectives and deliverables.
- Decision authority
  - Responsible for the correctness and completeness of documented requirements.
- Interactions / Handoffs
  - Works with stakeholders and Product Owner to gather requirements.
  - Hand off finalized user stories to Engineering Lead and QA Lead.
- Escalation
  - Escalate unclear or conflicting requirements to Product Owner or PM.

---

## Interaction patterns and RACI-style guidance
- R (Responsible): Role that performs the work.
- A (Accountable): Role that signs off on work/results.
- C (Consulted): Roles consulted for input.
- I (Informed): Roles kept informed.

Example: Feature delivery
- Requirements: BA (R), Product Owner (A), UX (C), PM (I)
- Implementation: Engineering Lead / Team (R), Product Owner (C), PM (I)
- QA & Acceptance: QA Lead (R), Product Owner (A), Engineering Lead (C)
- Release: DevOps (R), Release Manager (A), PM (I)

---

## Handoff checklist (summary)
For each stage transition (e.g., design → development, development → QA, QA → release), use the Project Handoff Checklist (docs/checklists/project-handoff-checklist.md) to ensure clarity and reduce rework.

---