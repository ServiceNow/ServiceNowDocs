---
title: View alert metric trends in Service Operations Workspace
description: View the metrics for an alert and adjust the time range to see the trends for either the alert or its associated Configuration Item \(CI\), enabling more accurate analysis and timely decision-making.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Alert metrics in SOW ITOM, Metric trends in SOW ITOM]
breadcrumb: [Service Operations Workspace, Configuring SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View alert metric trends in Service Operations Workspace

View the metrics for an alert and adjust the time range to see the trends for either the alert or its associated Configuration Item \(CI\), enabling more accurate analysis and timely decision-making.

## Before you begin

Ensure you have the Metric Intelligence \(sn\_metrics\_ng\) plugin installed.

Configure the metrics to be displayed for the alert, as described in [Configure alert metrics](configure-alert-metrics-itom.md).

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the List icon: ![List icon](../image/list-icon-sow-itom.png).

3.  Select **Lists** &gt; **Alerts** &gt; **All Alerts**.

    The Alerts - All Alerts page opens.

4.  Select the alert number to open it.

    The alert opens in a separate tab, displaying the **Overview** tab.

5.  Select the **Metrics** tab.

    ![Metrics tab](../image/metrics-tab.png "Metrics tab")

6.  In the fields above the metric charts, configure the time range for the alert's metrics.

    ![Metrics time range](../image/sow-time-range.png)

    To customize the metrics display, configure the following properties on the **System Properties** &gt; **All Properties** page:

    -   **ws\_metric.widgets\_number\_limit**: Specify the number of widgets/records that can be displayed on the metrics tab.
    -   **ws\_metric.datasets\_per\_widget\_limit**: Specify the number of charts/datasets that can be displayed on a chart.
    |Field name|Description|
    |----------|-----------|
    |Time range relevant to alert|Duration for calculating metrics around the alert.|
    |Start time|Start date and time for metric calculations.|
    |End time|End date and time for metric calculations.|

7.  Select a parameter below a chart to hide the specified parameter's data on the chart.

8.  Select the **Insights Explorer** button to view metrics by dragging and dropping them onto a timeline.

9.  Select **Save**.

10. View a time range for an alert's CI.

    1.  Select the **Overview** tab.

    2.  Under the Impact section, on the **Configuration item** card, select the link to the CI that appears under the **Name** field.

        ![Link to CI.](../image/sow-impact-section-metrics.png)

    3.  Select the **Metrics** tab.

    4.  Select **Save**.


**Parent Topic:**[Service Operations Workspace](../concept/workspace-dashboard-use.md)

