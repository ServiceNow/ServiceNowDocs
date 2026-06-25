---
title: Explore playbooks for retail projects
description: Playbooks in Retail Strategic Portfolio Management Suite provide a guided, structured approach to managing store life cycle projects from initiation to completion, helping project teams follow a consistent process across every store scenario.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/playbooks-spm-retail-suite.html
release: australia
topic_type: concept
last_updated: "2026-05-14"
reading_time_minutes: 7
keywords: [playbooks, SPM retail suite, SPM Retail, store life cycle playbook, retail project playbook]
breadcrumb: [Explore, Retail Strategic Portfolio Management Suite, Strategic Portfolio Management]
---

# Explore playbooks for retail projects

Playbooks in Retail Strategic Portfolio Management Suite provide a guided, structured approach to managing store life cycle projects from initiation to completion, helping project teams follow a consistent process across every store scenario.

Without prescribed playbooks, high-volume store projects typically have three core problems.

-   No prescribed workflow: Every project manager decides their own activity sequence, and approval points. Store \#412 might run a permit check before site survey and store \#413 might run them in reverse, created by different project managers. There is no consistency in how activities are executed or when stage transitions occur.
-   Activities executed at the wrong time or skipped entirely: a single new store opening requires dozens of coordinated activities such as site approval, lease execution, fit-out sign-off, IT readiness, and pre-opening compliance. Without a playbook enforcing sequence and completion, activities get skipped, executed out of order, or repeated unnecessarily.

    For example: If the pre-opening compliance check happens before fixtures are installed, the inspection has to be redone, delaying the grand opening.

-   No embedded approvals and checkpoints: leadership needs gated approval points to control go/no-go decisions on capital spend, lease commitments, and store readiness. Without a playbook \(shared stages, shared approvals, shared exit criteria\), enforcing consistent governance across every store project is difficult.

## Common playbook structure for every store scenario

When a project of a given type is created, the corresponding playbook attaches automatically and guides the project through a predefined sequence of stages. Each stage contains the prescribed activities, approvals, and exit criteria for that scenario. Every new store opening follows the same playbook sequence. Every closure follows the same wind-down playbook.

For example, a New Store Opening playbook comes preloaded with stages such as initiation, design and permitting, procurement, site readiness, construction, IT setup, fixtures, and go-live, each containing the prescribed activities that must be completed before transitioning to the next stage.

## Retail-specific playbook stages that enable guided execution

Each playbook is organized into stages tailored to the scenario, with the prescribed activities and approvals that must be completed at each stage.

-   For a New Store Opening, you get stages such as Site selection and approval, Lease execution, Design and permitting, Construction, IT and fixtures, and Pre-opening readiness.
-   For a Store Closure, you get stages such as Closure planning, Customer and employee communication, Final trading, Asset recovery and decommissioning, and Financial reconciliation.
-   For a Technology Refresh, you get stages such as Refresh planning, Hardware procurement, Installation scheduling, On-site installation, and Store handover.

|Scenario|Playbook coverage|Key stages offered|
|--------|-----------------|------------------|
|New Store Opening|End-to-end guided execution from business case through grand opening and handover|Site selection and approval, Lease execution, Design and permitting, Construction, IT and fixtures, Pre-opening readiness, Go-live|
|Store Refurbishment|Guided sequence for temporary shutdown, renovation, technology re-enablement, and reopening of an existing store|Refurbishment planning, Decommissioning, Fit-out and renovation, Technology re-enablement, Reopening readiness|
|Store Closure|Controlled wind-down playbook from closure decision through asset recovery, decommissioning, and financial reconciliation|Closure planning, Customer and employee communication, Final trading, Asset recovery and decommissioning, Financial reconciliation|
|Store Relocation|Guided sequence for decommissioning the current store, preparing the new site, and transferring operations|Relocation planning, Current store wind-down, New site readiness, Operations transfer, Relocation closeout|
|Technology Refresh|Guided sequence for replacing aging IT hardware \(POS, routers, network\) in an operational store|Refresh planning, Hardware procurement, Installation scheduling, On-site installation, Store handover|

These stages serve two purposes: they give project managers a prescribed sequence of activities to execute without inventing the process, and they give leadership consistent stage-based status across every project of the same type. When every new store opening progresses through the same Pre-opening readiness stage, you can report on stage-level progress across the entire portfolio.

## Embedded approvals and exit criteria at every stage

Every playbook stage includes the approvals, sign-offs, and exit criteria required before the project can transition to the next stage. With the Retail Strategic Portfolio Management Suite playbooks, governance is built into the project flow rather than relying on offline review meetings or ad hoc emails, so capital commitments, lease decisions, and go-live readiness are gated consistently across every project.

## Portfolio-level visibility across all playbook stages

Every project of a given type runs the same playbook with the same stages and activities, enabling a consistent stage-based reporting layer. With the Retail Strategic Portfolio Management Suite playbooks, stage progress and activity completion rollups are available automatically without manually gathering status from differently structured project plans.

## Purpose of playbooks in Retail Strategic Portfolio Management Suite

Playbooks provide a structured way to manage store life cycle projects by guiding project teams through predefined stages and activities. They show what to do, when to do it, and what information is required to complete each step. For more information on playbooks and how to create them, see [Workflow studio playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer.md).

In Retail Strategic Portfolio Management Suite, playbooks help project managers and delivery teams in the following ways:

-   Understand which activities must be completed at each stage of a store project.
-   Track required inputs, approvals, and validations before a project can progress to the next stage.
-   Verify that every store project follows the organization's standard governance process regardless of the project manager or store location.
-   Provide built-in process guidance within the project record, reducing dependency on informal or undocumented knowledge.
-   Maintain consistency across all store projects of the same type, whether a new store opening or a technology refresh.
-   Define multiple standardized governance processes to support different store life cycle scenarios.

## How playbooks work for store projects

When a playbook is applied to a store project, the following processes take place:

-   Store project life cycle stages such as initiation, site readiness, construction, IT setup, and go-live are outlined.
-   Stages contain activities and tasks tailored to the specific store scenario, such as obtaining site approval, scheduling IT installation, or confirming asset recovery.
-   Project managers are guided through stage dependencies before the project can advance to the next phase.
-   Project records automatically capture progress and trigger actions such as service requests and approvals as tasks are completed.

For example, a New Store Opening project uses a playbook to guide its progress as follows:

-   The initiation stage prompts the project manager to capture the site approval date and confirm the project scope.
-   The construction stage tracks the construction start date and triggers a service request to the IT deployment team when the construction milestone is complete.
-   The IT setup stage guides the team through various stages such as POS installation, network configuration, and system testing.
-   The go-live stage confirms the store go-live date and finalizes the handover to store operations.

As each stage is completed, the playbook helps verify that the project follows the standard life cycle without missing any required steps.

In Retail Strategic Portfolio Management Suite, playbooks are triggered by project creation. A playbook is associated with a project record based on the selected project type, and the Playbook page appears in the project record when the trigger condition is met.

## Playbooks for store life cycle scenarios

Retail Strategic Portfolio Management Suite includes predefined playbooks for each store life cycle scenario, available in Workflow Studio. Each playbook is a stage-gate playbook in which each stage must be finished before moving to the next one. Stages are visible only after all activities in the preceding stage are completed or skipped.

**Note:** These playbooks are ready to use without additional configuration. Configure playbooks only when you must customize an existing playbook or create one for your organization's specific store workflows.

-   New Store Opening playbook — Guides the project team from business case approval through site readiness, construction, IT installation, and store go-live.
-   Store Refurbishment playbook — Covers the temporary shutdown, renovation, technology re-enablement, and reopening of an existing store.
-   Store Closure playbook — Manages the controlled wind-down from closure decision through last trading day, asset recovery, and closure confirmation.
-   Store Relocation playbook — Guides decommissioning of the current store, preparation of the new site, and transfer of operations.
-   Technology Refresh playbook — Covers the replacement of aging IT hardware such as POS systems, routers, and network equipment in an operational store.

## Playbook benefits

Playbooks add value to store life cycle management in the following ways:

-   Standardizing project intake: Confirming that required information such as project type, key dates, and site details is captured at the start of every project.
-   Providing step-by-step guidance: Supporting project managers and delivery teams through each stage of a store project.
-   Supporting governance: Providing stage gating for approvals, site readiness checks, and handover confirmations.
-   Improving portfolio visibility: Showing exactly where each store project sits in its life cycle and what is blocking its progress.

**Related topics**  


[Workflow Studio playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio-playbooks-landing.md)

[Building Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/building-a-process.md)

[Designing Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-experience-admins.md)

[Explore Retail Strategic Portfolio Management Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/explore-spm-retail-suite.md)

