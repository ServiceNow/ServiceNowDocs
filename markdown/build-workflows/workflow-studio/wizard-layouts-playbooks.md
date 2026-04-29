---
title: Wizard layouts for playbooks
description: Wizard layouts present a playbook as a guided, step-by-step experience that helps end users complete a process in a clear and structured way.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Wizard layouts for playbooks

Wizard layouts present a playbook as a guided, step-by-step experience that helps end users complete a process in a clear and structured way.

A wizard layout organizes playbook activities into sequential steps. Each step focuses the user on the current activity and provides navigation controls to move forward or backward through the process. This approach is especially useful for multi-step workflows or scenarios where users benefit from explicit guidance and clear progression through their tasks.

Wizard layouts are configured using UI Builder bundles. When you add a Playbook Wizard layout bundle to a UI Builder page, the required playbook components and connections are created automatically, which reduces the need for manual configuration.

## When to use a wizard layout

Use a wizard layout when:

-   A playbook contains multiple activities that must be completed in a specific order.
-   End users need clear guidance through a complex or unfamiliar process.
-   You want to limit distraction by focusing the user on one step at a time.

For complex playbooks with additional logic or scenarios where users can choose activities freely, other playbook layouts might be more appropriate.

## How wizard layouts display and control playbooks

In a wizard layout:

-   Each wizard step corresponds to a playbook activity.
-   Navigation controls guide users between activities.
-   Completion rules ensure that required information is provided before users proceed.

![Playbook wizard layout](../images/playbk-wizard-layout.png "Playbook wizard layout")

The underlying playbook logic and activity configuration remain the same. The wizard layout changes how the playbook is presented to end users, not what the playbook does.

-   **[Configure a wizard layout for a playbook](../task/add-wizard-layout-playbooks.md)**  
Configure a wizard layout that presents a playbook as a guided, step-by-step experience for end users.

**Parent Topic:**[Designing Playbook Experience](../../workspace/concept/playbook-experience-admins.md)

