---
title: Acknowledge viewed alerts in Express List
description: Acknowledge alerts that you’ve viewed to remove clutter in the Express List pane.
locale: en-US
release: yokohama
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Express List in the Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Acknowledge viewed alerts in Express List

Acknowledge alerts that you’ve viewed to remove clutter in the Express List pane.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

**Note:** The evt\_mgmt\_user role is view-only and does not have permission to perform this action.

## About this task

Use Acknowledge to denote that the alert is known, and can temporarily be ignored. Do not use Acknowledge to mark an alert as needing attention.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon: ![Express list icon](../../event-management/image/express-list1.png).

3.  Acknowledge selected alerts.

    You can acknowledge alerts regardless of whether you are working in the main pane or in the preview panel. The preview panel opens only when a single alert or alert group is selected.

<table id="choicetable_s4j_1yg_vzb"><thead><tr><th align="left" id="d202594e99">

Location

</th><th align="left" id="d202594e102">

Action

</th></tr></thead><tbody><tr><td id="d202594e108">

**The Express List pane**

</td><td>

1.  In the Express List pane, select the alert to acknowledge.

You can select more than one alert row.

**Note:** You can perform the action on up to 1,000 alerts simultaneously by selecting the **Select All** check box in the Active alerts list. ![Select All check box.](../image/el-select-all.png)

To display the individual alerts inside a group, select the chevron icon \(![Chevron icon.](../image/icon-chevron.png)\) at the beginning of the alert group row.

2.  From the **Close** drop-down list at the top right of the alert list, select **Acknowledge**.


</td></tr><tr><td id="d202594e161">

**The Express List preview panel for group alerts**

</td><td>

1.  Select an alert group row check box.
2.  In the **Alerts in group** tab, select an alert tile.
3.  Select the more actions icon \(![More actions icon](../../event-management/image/more-actions-icon.png)\).
4.  Select **Acknowledge**.


</td></tr></tbody>
</table>
## Result

The alert is acknowledged and its status is displayed at the top of the preview panel.

