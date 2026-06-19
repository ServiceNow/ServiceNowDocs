---
title: Close an alert in Express List
description: Manually close alerts directly from the Express List pane or from the preview panel without waiting for them to be automatically closed if you already know the root cause or have fixed the problem.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-operations-workspace-for-itom-apps/close-alert.html
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Close an alert in Express List

Manually close alerts directly from the Express List pane or from the preview panel without waiting for them to be automatically closed if you already know the root cause or have fixed the problem.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

**Note:** The evt\_mgmt\_user role is view-only and does not have permission to perform this action.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon: \[Omitted image "express-list1.png"\] Alt text: Express list icon.

3.  Close selected alerts.

    You can close alerts regardless of whether you are working in the main pane or in the preview panel. The preview panel opens only when a single alert or alert group is selected.

<table id="choicetable_s4j_1yg_vzb"><thead><tr><th align="left" id="d315477e91">

Location

</th><th align="left" id="d315477e94">

Action

</th></tr></thead><tbody><tr><td id="d315477e100">

**The Express List pane**

</td><td>

1.  In the Express List pane, select the alert.

You can select more than one alert row.

**Note:** You can perform the action on up to 1,000 alerts simultaneously by selecting the **Select All** check box in the Active alerts list. \[Omitted image "el-select-all.png"\] Alt text: Select All check box.

To display the individual alerts inside a group, select the chevron icon \(\[Omitted image "icon-chevron.png"\] Alt text: Chevron icon.\) at the beginning of the alert group row.

2.  From the **Close** drop-down list at the top right of the alert list, select **Close alert**.


</td></tr><tr><td id="d315477e153">

**The Express List preview panel for group alerts**

</td><td>

1.  Select an alert group row.
2.  In the **Alerts in group** tab, select an alert tile.
3.  Select the more actions icon \(\[Omitted image "more-actions-icon.png"\] Alt text: More actions icon\).
4.  Select **Close alert**.


</td></tr></tbody>
</table>
## Result

The alert is closed and its status is displayed at the top of the preview panel.

