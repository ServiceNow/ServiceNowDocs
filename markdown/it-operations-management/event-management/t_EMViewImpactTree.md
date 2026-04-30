---
title: View the impact tree
description: The impact tree shows the relationships between CIs and the relative percentage impact for each child CI. This information is available for both discovered services and application services.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Alert impact calculation, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# View the impact tree

The impact tree shows the relationships between CIs and the relative percentage impact for each child CI. This information is available for both discovered services and application services.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

The impact tree shows the result of impact rules on CI parent and child relationships. The tree represents a service map with CIs from the Service Configuration Item Associations \[svc\_ci\_assoc\] table. When related CIs are connected but not part of the service map, the impact for the related CIs can also appear in the impact tree.

The numbers or percentages on a parent CI summarize overall severity based on alerts from child CIs. The parent severity is based on impact rule computations.

You can also learn about the impact tree from the following video tutorial.

Event Management Part 2 \| Impact Tree

![Impact Tree](../image/EMImpactTree.png "Impact Tree")

## Procedure

1.  Open the service map for the service from the Application service list.

    1.  Navigate to **Event Management** &gt; **Services** &gt; **Application Services**.
    2.  Click **View service** next to the service.
2.  On the service map, click a CI that has a severity color.

3.  Click the **Impact** tab.

4.  From the **Impact Tree** tab in the side pane, expand the parent CI and click the CI that generated alerts.

5.  Use the severity color to locate CIs that contain alerts:

    -   **Critical \(red\)**: Immediate action is required. The resource is either not functional or critical problems are imminent.
    -   **Major \(orange\)**: Major functionality is severely impaired or performance has degraded.
    -   **Minor \(yellow\)**: Partial, non-critical loss of functionality or performance degradation occurred.
    -   **Warning \(blue\)**: Attention is required, even though the resource is still functional.
    -   **OK \(green\)**: An alert is created. The resource is still functional.
6.  Do one or more of the following.

<table id="choicetable_rdg_w1m_35"><tbody><tr><td id="d495494e217">

**Adjust impact rules**

</td><td>

1.  Click the **Impact** tab.
2.  Review and adjust the impact rules as necessary.


</td></tr><tr><td id="d495494e238">

**Remediate an alert**

</td><td>

1.  Click the **Alerts**.
2.  Right-click the alert and select **Run remediation**.


</td></tr></tbody>
</table>    Network paths appearing in the impact tree can use a large amount of resources, which degrades system performance. To disable network paths from appearing in the impact tree, navigate to **System Properties** &gt; **All Properties** and set the **evt\_mgmt.network\_path\_excluded** property to **true**.

    To view impact tree using Service Operations Workspace, see [View impact tree using Service Operations Workspace](../../service-operations-workspace-itom/task/view-impact-tree.md).


