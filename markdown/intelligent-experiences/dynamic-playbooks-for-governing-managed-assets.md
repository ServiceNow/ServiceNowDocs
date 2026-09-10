---
title: Updated playbooks for governing managed assets
description: Manage AI assets through structured lifecycle workflows using the updated playbooks that automate governance tasks, route approvals, and track compliance requirements across onboarding, maintenance, and retirement phases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/dynamic-playbooks-for-governing-managed-assets.html
release: zurich
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 3
keywords: [dynamic playbooks, AI governance, lifecycle management, AI asset onboarding, approval workflows, governance automation]
breadcrumb: [Explore, AI Control Tower, Enable AI experiences]
---

# Updated playbooks for governing managed assets

Manage AI assets through structured lifecycle workflows using the updated playbooks that automate governance tasks, route approvals, and track compliance requirements across onboarding, maintenance, and retirement phases.

## Overview of the updated playbooks

The legacy playbooks experience inhibits flexible, risk-aware governance at scale. Tasks originate from disparate integrations rather than the playbook itself, removing context between stages and task origins. When tasks fail or don't appear, users don't have an easy way of determining whether the tasks skipped or encountered errors. Governance tasks apply uniformly across assets regardless of risk classification.

The updated playbooks improve on existing playbooks by introducing centralized task creation. This enables visibility into task lifecycle, providing a single source of truth for changes, allowing risk-based task differentiation, and improving discoverability through clearer navigation paths. The new playbooks provide structured workflows that guide AI stewards and asset owners through the complete lifecycle of AI assets. Playbooks automate governance tasks, assign responsibilities, and enforce compliance checkpoints as assets progress from initial onboarding through deployment, maintenance, and eventual retirement.

## How playbooks work

Playbooks operate as workflow templates that activate when specific lifecycle events occur. Each playbook defines a sequence of activities and tasks that must be completed before an asset can advance to the next lifecycle phase. When an AI asset enters a new lifecycle stage, the corresponding playbook generates a set of activities and tasks tailored to that stage. Each activity represents a logical grouping of related governance work, such as risk assessment, security review, or deployment approval. This approach ensures that governance, risk, and compliance requirements are addressed operationally as part of the asset lifecycle rather than as separate processes.

Tasks within each activity are assigned to appropriate roles based on the type of review required. For example, impact assessments might be assigned to AI stewards, while security clearances are routed to security teams. The asset cannot progress to the next activity until all required tasks for the current activity are completed or approved. To learn more about the playbooks offered, see [AI Control Tower playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-playbooks-reference.md).

## Key benefits of the updated playbook

The updated playbook provides the following benefits:

-   Task creation is handled by the playbook and is not dependent on separate workstream integrations.
-   A consolidated overview of all tasks and their statuses are maintained in a single place. Tasks appear created, errored with a message, or skipped—all recorded in one place.
-   Each workstream reads its own decision table. Task types are added or changed by configuration, not code.
-   Asset attributes such as risk tier, phase, and use and purpose are considered before the tasks are assigned.
-   Playbooks are shipped as protected. However, they can be cloned with the workflow and then customized to suit business requirements.

## Lifecycle tasks

Lifecycle tasks are units of governance work that playbooks generate as assets progress through their lifecycle. Each task corresponds to a step in a playbook activity that requires human review, approval, or completion. Tasks include impact assessments, architecture reviews, security clearances, value template approvals, and other reviews that must be completed before an asset can advance.

Playbooks generate tasks based on the asset type, risk classification, and lifecycle phase. Tasks are assigned to specific roles or individuals based on the type of review required. For example, a high-risk AI system might trigger additional security review tasks that are not required for lower-risk assets.

Tasks appear in multiple locations for visibility and action. Asset owners see tasks on the asset record within the playbook visualization. AI stewards and reviewers see assigned tasks in the Activity Center and can filter by task type, priority, or due date. Tasks can also generate recommendations when they become overdue or when activities have no associated tasks.

## Automated triggering of playbooks

Playbooks can be configured to trigger automatically when specific conditions are met. When the Automatically trigger playbooks setting is active in Builder controls, approval playbooks run automatically when a new AI asset is added. This ensures that governance workflows begin immediately when assets enter the system.

When automatic triggering is inactive, asset managers can still initiate approval playbooks manually from the asset record. This provides flexibility for organizations that want to control when governance workflows begin or that have different approval requirements for different asset types.

Automatic triggering reduces manual overhead and helps prevent ungoverned assets from progressing through the lifecycle without required reviews. It also ensures consistent application of governance policies across all AI assets.

