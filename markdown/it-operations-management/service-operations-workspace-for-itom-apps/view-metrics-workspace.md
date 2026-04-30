---
title: View metrics for an alert
description: Viewing metrics enables you to understand historical data related to an alert's CI.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View metrics for an alert

Viewing metrics enables you to understand historical data related to an alert's CI.

## Before you begin

-   Ensure that you install the Operational Intelligence \(com.snc.sa.metric\) plugin.
-   Configure the metrics to be displayed for the alert, as described in [Configure alert metrics](../../service-operations-workspace-itom/task/configure-alert-metrics-itom.md).

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon: ![Express list icon](../image/express-list1.png).

3.  Select an alert to open it.

4.  Click the **Metrics** subtab.

    The configured metrics appear on the page.

    ![Metrics subtab](../image/alert-metrics-new.png)

    To customize the metrics display, configure the following properties on the **System Properties** &gt; **All Properties** page:

    -   **ws\_metric.widgets\_number\_limit**: Specify the number of widgets/records that can be displayed on the metrics tab.
    -   **ws\_metric.datasets\_per\_widget\_limit**: Specify the number of charts/datasets that can be displayed on a chart.
5.  In the **Time range relative to alert** list, select the time range for which you want the metrics to be displayed for the alert:

    -   1 hour before and after \(default setting\)
    -   3 hours before and after
    -   5 hours before and after
    -   Custom range \(to configure a customized time range for the metrics to measure\)
6.  Click a parameter below a chart to hide the specified parameter's data on the chart.

7.  Click the **Insights Explorer** button to view metrics by dragging and dropping them onto a timeline.


**Related topics**  


[View metric values in the Insights Explorer](view-metrics-explorer.md)

