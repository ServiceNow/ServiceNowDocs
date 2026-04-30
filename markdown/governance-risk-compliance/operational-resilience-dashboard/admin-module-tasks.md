---
title: Completing general administrative tasks
description: A user with the sn\_oper\_res.admin role can perform the setup tasks in the Operational Resilience application.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Completing general administrative tasks

A user with the sn\_oper\_res.admin role can perform the setup tasks in the Operational Resilience application.

## Admin module in the classic Operational Resilience view

If you have the sn\_oper\_res.admin role, you can configure the Admin module and set up the administrative tasks in the Operational Resilience Workspace as shown in the following example:

![Admin module in the classic view.](../image/admin-tasks.png "Admin module in the classic view")

A user with the sn\_oper\_res.admin role can set up the following entities by using the Admin module:

-   Entity Types

    **Note:** Installing the Operational Resilience application inserts seed data to the Entity type \[sn\_grc\_profile\_type\] table. Both entity types and entity filters are installed as inactive. When you activate them, it could lead to generation of thousands of entity records.

-   Pillars
-   Scenarios
-   Event Groups
-   Events
-   Participant Roles
-   Important Choices
-   Importance and Impact Tolerance Rating Scale
-   Attestation Templates
-   Assessment Templates

**Note:** When you log in to the application as a user with the sn\_oper\_res.admin role, you can view the Admin module.

Operational Resilience administrators can create pillars and can also modify the reports on the dashboard.

**Note:** Though you can modify the entity types, their filters, and pillars as a user with the sn\_oper\_res.admin role, you must exercise proper caution while modifying them.

## Administrative setup tasks

As a user with the sn\_oper\_res.admin role, you can complete the following general setup tasks:

-   Create a scenario that represents a risk. For more information, see [Create a scenario and link it to an event](../task/define-scenarios.md).
-   Classify an event by associating it with an event group. For more information, see [Create an event group for the scenario](../task/create-event-group.md).
-   Create an event that you can associate with a scenario. For more information, see [Create an event for the scenario](../task/create-events.md).
-   Add a participant role for your scenario analysis. For more information, see [Add a participant role for the scenario analysis](../task/add-participant-role.md).
-   Update the assessment rating by using the Important choices module. For more information, see [Update the Important choices module](../task/set-up-important-choices.md).
-   Update the importance and impact rating scale. For more information, see [Set up the Importance and Impact Tolerance Rating Scale](../task/create-importance-impact-rating-scale.md).
-   Create an attestation template. For more information, see [Create and edit the attestation template](../task/create-new-attestation-template.md).

