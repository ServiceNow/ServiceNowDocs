---
title: View Log Analytics anomaly alert charts in Express List
description: View visualizations for Health Log Analytics anomaly alerts to identify periods of behavior that deviate from expected ranges. You can view visualizations from the Express List preview panel or the alert record.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View Log Analytics anomaly alert charts in Express List

View visualizations for Health Log Analytics anomaly alerts to identify periods of behavior that deviate from expected ranges. You can view visualizations from the Express List preview panel or the alert record.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon: ![Express list icon](../../event-management/image/express-list1.png).

3.  In the Active Alerts list, locate a Log Analytics based alert.

    This option is available only for individual alerts or the underlying individual alerts within a group.

4.  Choose where to view the anomaly chart.

<table id="choicetable_kfx_rzl_33c"><thead><tr><th align="left" id="d353653e113">

Option

</th><th align="left" id="d353653e116">

Procedure

</th></tr></thead><tbody><tr><td id="d353653e122">

**View the chart in the preview panel**

</td><td>

1.  Select the check box for a Log Analytics based alert.
2.  In the preview panel, select the **Info** tab.

A chart with a visual representation of the anomaly appears.

</td></tr><tr><td id="d353653e148">

**View the chart in the alert record**

</td><td>

Select the number of the anomaly alert to open the alert record.

 The **Overview** tab opens by default. The anomaly chart is displayed.

</td></tr></tbody>
</table>5.  Select the parameter to visualize anomaly data within that time period:

    -   **Events per minute** - The default setting, which shows the detected anomaly.
    -   **Day ago**
    -   **Week ago**
6.  Review relevant logs in context by selecting the Open in Surrounding logs icon:![Open in Surrounding logs icon](../image/icon-anomaly-logs-link.png).

    The **Surrounding logs** tab displays the list of log lines that were generated one minute before and one second after the Log Analytics alert. For more information, see [How Health Log Analytics generates alerts](../../health-log-analytics-operator/concept/hla-op-anomalies-detecting.md).


