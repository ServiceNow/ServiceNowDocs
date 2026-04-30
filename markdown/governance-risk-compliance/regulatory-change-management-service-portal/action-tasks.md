---
title: Action tasks in Regulatory Change Management
description: The action tasks facilitating the change management process are associated with Regulatory Change. The ownership of these action tasks is managed by the respective business owners affected due to the regulatory change.
locale: en-US
release: yokohama
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Action tasks in Regulatory Change Management

The action tasks facilitating the change management process are associated with Regulatory Change. The ownership of these action tasks is managed by the respective business owners affected due to the regulatory change.

Action tasks are related to regulatory change tasks and to source document import tasks. Users with the `sn_grc_reg_change.manager`, `sn_grc_reg_change.user`, or `sn_grc_reg_change.admin` role create regulatory action tasks and source document import tasks. These tasks are related to the Compliance and Risk areas in the GRC library. The Compliance Manager and Risk Manager assign the tasks to the correct Risk or Compliance group.

There are two categories of action tasks in the Regulatory Change Management application:

-   Compliance: Contains all compliance-related action tasks. Compliance users can select a specific Compliance record in the GRC library, such as policies and controls.
-   Risk: Contains all risk-related action tasks. Risk users can select a specific Risk record in the GRC library, such as risk statements.

Action tasks are created automatically for potentially impacted risk statements and policies.

Managers with the `sn_grc_reg_change.manager` role can view and sort the action tasks using the following tabs:

-   **All assigned tasks**
-   **Unassigned compliance tasks**
-   **Unassigned risk tasks**
-   **Ready tasks**
-   **In Progress tasks**
-   **Closed tasks**

Starting with version 19.0.x, you can initiate and complete the action tasks independently without requiring prior approval from users who are assigned with the `sn_grc_reg_change.manager` role. You can execute assigned responsibilities in a timely manner and reduce unnecessary approval bottlenecks. The access to action tasks remains governed by user permissions and role-based access controls to ensure proper accountability and oversight.

Staring with version 21.0.x, you can reopen the action tasks for a regulatory task when it's rejected and transitions back to the Implementation state. You can review and rework the tasks to address the feedback or incorporate the updated requirements. You can also modify and resubmit the reopened action tasks so that the implementation aligns with regulatory expectations before you resubmit the change task.

## Types of action tasks

The following types of action tasks are available in Regulatory Change Management:

-   Business Impact
-   Change Policies
-   Executive Briefing
-   Legal Review
-   Notification
-   Others
-   None

