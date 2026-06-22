---
title: View links between alerts in a group in Express List
description: Use Link View in Express List to view a visual representation of the relationships between alerts in a group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-operations-workspace-for-itom-apps/view-relationships-between-alerts-in-groups.html
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Viewing links between alerts in alert groups in Express List, Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View links between alerts in a group in Express List

Use Link View in Express List to view a visual representation of the relationships between alerts in a group.

## Before you begin

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## About this task

For an overview of Link View in Express List, see [Viewing links between alerts in alert groups in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/el-link-view.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation, select the Express List icon \(\[Omitted image "express-list1.png"\] Alt text: Express List icon\).

3.  In the fields in the interactive filter panel, select **Group** and then the check box for the alert groups to display.

    **Note:** Link View is supported for the following alert group types:

    -   Network traffic-based
    -   Rules-based
    -   Mixed alert groups, which include:
        -   CMDB-based alert groups
        -   Tag cluster-based alert groups
        -   Related log entities
        -   Shared impacted services
4.  In the **Active alerts** list, select the description of an alert group.

    The preview panel opens to the **Alerts in group** tab, which lists all the correlated alerts in the selected group.

5.  Navigate to **Link View**.

    Link View opens, displaying the relationships between the alerts in the selected group.

6.  Customize the Link View display.

<table id="choicetable_vyh_rzk_21c"><thead><tr><th align="left" id="d555296e178">

Task

</th><th align="left" id="d555296e181">

Action

</th></tr></thead><tbody><tr><td id="d555296e187">

**Focus on an area of interest**

</td><td>

Select one or more nodes and rearrange them in Link View by dragging them to a new location.

</td></tr><tr><td id="d555296e196">

**Refresh the alert group**

</td><td>

Select **Refresh**. After refreshing the alert group, rearranged nodes appear in their original position again. Newly added nodes are marked as New.

**Note:** The **Refresh** button is enabled when new data for the alert group is available. Link View doesn't refresh automatically.

</td></tr><tr><td id="d555296e218">

**View the meaning of icons and colors**

</td><td>

Select the Link View legend.The legend also indicates the number of unique nodes displayed per tag. For a description of each tag, see [Attributes in Express List Link View](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/link-view-tags-icons-descriptions.md).

</td></tr><tr><td id="d555296e236">

**Reduce noise**

</td><td>

In the Link View legend, toggle between hiding and showing a tag type.

</td></tr><tr><td id="d555296e246">

**View information about an alert**

</td><td>

Hover over a node to display text with information about the alert.

</td></tr></tbody>
</table>
