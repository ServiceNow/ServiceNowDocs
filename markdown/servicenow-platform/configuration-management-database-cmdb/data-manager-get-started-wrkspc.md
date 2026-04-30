---
title: Get started with CMDB Data Manager
description: The Data Manager overview page in CMDB Workspace and in Service Graph Workspace provides a dashboard view of Data Manager tasks, and lets you get started in using the CMDB Data Manager.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Administer CMDB Data Manager, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Get started with CMDB Data Manager

The Data Manager overview page in CMDB Workspaceand in Service Graph Workspace provides a dashboard view of Data Manager tasks, and lets you get started in using the CMDB Data Manager.

## Before you begin

Role required: sn\_cmdb\_admin

## Procedure

1.  Open either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace**, and then select the **Data Manager** quick link on the Home view.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**. Then, in the navigation panel, select the Governance icon. Then, in the Governance navigation pane, select **Data Manager overview**.
2.  Select **Data Manager overview** in the left navigation bar.

    The Data Manager overview page provides the following cards:

    -   **Open tasks**

        Count of the open tasks created for Data Manager policies.

        Drill down the card to open a list view with details of the tasks associated with the card.

    -   **Unassigned tasks**

        Count of the open tasks created for Data Manager policies, which aren't assigned.

        Drill down the card to open a list view with details of the tasks associated with the card.

    -   **Pending tasks**

        Tasks in Pending state, such as archive tasks where archive is still being processed.

    -   **Closed incomplete tasks**

        Tasks that encountered errors while processing, resulting with the task not completing successfully. Such tasks are in a Closed Incomplete state.

    -   **Overdue tasks**

        Count of tasks with a due date, such as attestation tasks, whose due date has passed.

    -   **Aging tasks**

        A bar chart showing counts of tasks without a due date and with no activity for over the number of days specified by the **sn\_cmdb\_ws.glide.cmdb.data.manager.aging.policy.task.timeframe** system property \(30 by default\).

    -   **Policies failing evaluation**

        Policies whose evaluation failed at some point and are in an error state. These policies require your attention, and after resolving any issues, you can publish them again.

    -   **Workload**
        -   Groups: Tasks that are assigned to a group.
        -   Individuals: Tasks that are assigned to individual users.

## What to do next

-   [Create a CMDB Data Manager policy](data-manager-create-policy-wrkspc.md).
-   [Manage retirement definitions for CMDB Data Manager](data-manager-manage-ret-def-wrkspc.md#).
-   [Manage exclusion lists for CMDB Data Manager](data-mgr-manage-ci-exclusion-wrkspc.md).
-   [View CMDB Data Manager analytics](../concept/data-manager-view-analytics-wrkspc.md).
-   View properties and other settings for CMDB Data Manager by selecting **Settings** in the left navigation pane. For details about the system properties associated with those settings, see [Components related to CMDB Data Manager](../reference/components-cmdb-data-manager.md).

