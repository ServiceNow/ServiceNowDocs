---
title: View links between alerts in a group in Express List
description: When an alert group is generated, understand better how the alerts in the group are linked by viewing a visual representation of their relationships in Link View.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Viewing links between alerts in alert groups in Express List, Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View links between alerts in a group in Express List

When an alert group is generated, understand better how the alerts in the group are linked by viewing a visual representation of their relationships in Link View.

## Before you begin

For an overview of Link View in Express List, see [Viewing links between alerts in alert groups in Express List](../concept/el-link-view.md).

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation, select the Express List icon \(![Express List icon](../../event-management/image/express-list1.png)\).

3.  In the fields in the interactive filter panel, select **Group** and then the check box for the alert groups you want to display.

    **Note:** Currently, Link View is supported for tag-based, rules-based, CMDB-based, and network traffic-based alert groups.

    -   **Tag Cluster**
    -   **Rules-based**
    -   **CMDB**
    -   **Network Traffic**
4.  In the **Active alerts** list, select the description of an alert group.

    The preview panel opens to the **Alerts in group** tab, which lists all the correlated alerts in the selected group.

5.  Navigate to **Link View**.

6.  View the relationships between all the alerts in the selected group.

7.  Perform the following optional tasks.

<table id="choicetable_vyh_rzk_21c"><thead><tr><th align="left" id="d610186e170">

Task

</th><th align="left" id="d610186e173">

Action

</th></tr></thead><tbody><tr><td id="d610186e179">

**Focus on an area of interest**

</td><td>

Select one or more nodes and rearrange them in Link View by dragging them to a new location.**Note:** After refreshing the alert group, the nodes appear in their original position again.

</td></tr><tr><td id="d610186e190">

**Refresh the alert group**

</td><td>

Select **Refresh**. When you've refreshed the alert group, rearranged nodes appear in their original position again. Newly-added nodes are marked as New.

**Note:** The **Refresh** button is enabled when new data for the alert group is available. Link View doesn't refresh automatically.

</td></tr><tr><td id="d610186e212">

**View the meaning of icons and colors**

</td><td>

Select the Link View legend.The legend also indicates the number of unique nodes displayed per tag. For a description of each tag, see [Attributes in Express List Link View](../reference/link-view-tags-icons-descriptions.md).

</td></tr><tr><td id="d610186e230">

**Reduce noise**

</td><td>

In the Link View legend, toggle between hiding and showing a tag type.

</td></tr><tr><td id="d610186e240">

**View information about an alert**

</td><td>

Hover over a node to display a tooltip with information.

</td></tr></tbody>
</table>
