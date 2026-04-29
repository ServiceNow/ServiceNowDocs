---
title: View anomaly alert metric data on the preview panel in Express List
description: View visualizations for anomaly alerts to investigate anomalies using metric data. You can view visualizations from the Express List preview panel or the alert record.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View anomaly alert metric data on the preview panel in Express List

View visualizations for anomaly alerts to investigate anomalies using metric data. You can view visualizations from the Express List preview panel or the alert record.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon ![](../../event-management/image/express-list1.png).

3.  In the Active alerts list, locate an anomaly alert.

    Information in the **Description** column can help you determine which alerts are anomaly alerts. For example, an alert description might warn about values nearing or exceeding configured thresholds, or metrics above or below a defined boundary.

4.  Choose where to view the anomaly chart.

<table id="choicetable_kfx_rzl_33c"><thead><tr><th align="left" id="d351149e103">

Option

</th><th align="left" id="d351149e106">

Procedure

</th></tr></thead><tbody><tr><td id="d351149e112">

**To view the chart in the preview panel**

</td><td>

1.  Select the check box for the anomaly alert.
2.  In the preview panel, select the **Info** tab.

A chart with a visual representation of the anomaly appears.

</td></tr><tr><td id="d351149e135">

**To view the chart in the alert record**

</td><td>

Select the number of the anomaly alert to open the alert record.

 The **Overview** tab opens by default. The anomaly chart is displayed.

</td></tr></tbody>
</table>    Depending on how the metric anomaly is configured, one of two charts is displayed.

    -   When the Metric Intelligence statistical model is used to detect anomalies, the anomaly alert chart is displayed with upper and lower bounds based on machine learning models. ![Anomaly alert graph](../image/preview_panel_metric_static.png)

        For more information, see [Understanding Metric Intelligence](../../event-management/concept/operational-intelligence-overview.md).

    -   When thresholds are configured by administrators, the static threshold metric anomaly alert chart shows anomalies defined using the configured thresholds.![Static threshold metric anomaly alert graph](../image/preview_panel_metric_threshold.png)

    **Note:**

    The raw data used for the metric chart in the preview panel is available only for seven days. If older alerts are selected and the raw data is no longer available, a chart isn’t shown.

    For more information, see [Create metric rules](../../agent-client-collector/task/create-metric-rules.md).

5.  Review surrounding metric data by selecting the **Open in Metric explorer** icon \(![Open in Metric explorer icon](../image/icon-anomaly-logs-link.png)\) in the information panel.

    The **Metric Explorer** tab displays the time frame of the anomaly. For an open alert, the chart shows one hour before and after the last time of event generation. For a closed alert, the chart shows one hour before and after the first event that created an alert. If there’s no data, the chart isn’t displayed.

    For more information, see [Metric Explorer](../../event-management/concept/agent-workspace-ops-intelligence.md).


