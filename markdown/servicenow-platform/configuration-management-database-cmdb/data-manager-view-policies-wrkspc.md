---
title: View CMDB Data Manager policies
description: View Data Manager policies on a dashboard view in CMDB Workspace or in Service Graph Workspace, with a timeline of upcoming scheduled policies, counts, and grouped by policy status.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer CMDB Data Manager, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View CMDB Data Manager policies

View Data Manager policies on a dashboard view in CMDB Workspaceor in Service Graph Workspace, with a timeline of upcoming scheduled policies, counts, and grouped by policy status.

## Before you begin

Role required: sn\_cmdb\_admin

## Procedure

1.  Open either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace**, and then select the **Data Manager** quick link on the Home view.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**. Then, in the navigation panel, select the Governance icon. Then, in the Governance pane, select **Data Manager overview**.
2.  Select **Policies** in the left-side bar.

    Select a tab on the Data Manager policies page:

    -   Published policies: Provides the following cards:
        -   **Upcoming scheduled policies**

            Timeline showing scheduled policies across time. On the timeline, you can:

            -   Point to indicators to show details about a scheduled policy.
            -   Zoom in or out to extend or shorten the time span of the timeline.
            -   Go forward or backward in time.
            -   Show or hid the timeline legend, where you can toggle the Attestation Policy switch to show or hide attestation policy indicators on the timeline.
        -   **Policies**

            Pie chart showing the breakdown of policies by policy type.

        -   **Published policies**

            List view of policies that are published. You can drill down a policy to show the policy form view with further details about the policy.

    -   Draft policies: Policies in draft state.
    -   De-activated policies: Policies that have been de-activated and therefore aren't active.
    -   Policies failing evaluation: Policies that are invalid and therefore require your attention.

## What to do next

-   [Create a CMDB Data Manager policy](data-manager-create-policy-wrkspc.md)
-   [Manage retirement definitions for CMDB Data Manager](data-manager-manage-ret-def-wrkspc.md#)

