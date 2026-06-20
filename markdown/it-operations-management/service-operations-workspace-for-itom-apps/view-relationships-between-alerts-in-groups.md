---
title: View links between alerts in a group in Express List
description: When an alert group is generated, understand better how the alerts in the group are linked by viewing a visual representation of their relationships in Link View.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-operations-workspace-for-itom-apps/view-relationships-between-alerts-in-groups.html
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Viewing links between alerts in alert groups in Express List, Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View links between alerts in a group in Express List

When an alert group is generated, understand better how the alerts in the group are linked by viewing a visual representation of their relationships in Link View.

## Before you begin

For an overview of Link View in Express List, see [Viewing links between alerts in alert groups in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/el-link-view.md).

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation, select the Express List icon \(\[Omitted image "express-list1.png"\] Alt text: Express List icon\).

3.  In the fields in the interactive filter panel, select **Group** and then the check box for the alert groups you want to display.

4.  In the **Active alerts** list, select the description of an alert group.

    The preview panel opens to the **Alerts in group** tab, which lists all the correlated alerts in the selected group.

5.  Navigate to **Link View**.

6.  View the relationships between all the alerts in the selected group.

7.  Perform the following optional tasks.

<table id="choicetable_vyh_rzk_21c"><thead><tr><th align="left" id="d550552e140">

Task

</th><th align="left" id="d550552e143">

Action

</th></tr></thead><tbody><tr><td id="d550552e149">

**Focus on an area of interest**

</td><td>

Select one or more nodes and rearrange them in Link View by dragging them to a new location.**Note:** After refreshing the alert group, the nodes appear in their original position again.

</td></tr><tr><td id="d550552e160">

**Refresh the alert group**

</td><td>

Select **Refresh**. When you've refreshed the alert group, rearranged nodes appear in their original position again. Newly-added nodes are marked as New.

**Note:** The **Refresh** button is enabled when new data for the alert group is available. Link View doesn't refresh automatically.

</td></tr><tr><td id="d550552e182">

**View the meaning of icons and colors**

</td><td>

Select the Link View legend.The legend also indicates the number of unique nodes displayed per tag. For a description of each tag, see [Attributes in Express List Link View](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/link-view-tags-icons-descriptions.md).

</td></tr><tr><td id="d550552e200">

**Reduce noise**

</td><td>

In the Link View legend, toggle between hiding and showing a tag type.

</td></tr><tr><td id="d550552e210">

**View information about an alert**

</td><td>

Hover over a node to display a tooltip with information.

</td></tr></tbody>
</table>
