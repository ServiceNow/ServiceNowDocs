---
title: View CI health in Metric Explorer
description: View the health and performance of an alert's CI using Metric Explorer, to help troubleshoot problematic areas in the CI.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [CI health in SOW ITOM]
breadcrumb: [Service Operations Workspace, Configuring SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View CI health in Metric Explorer

View the health and performance of an alert's CI using Metric Explorer, to help troubleshoot problematic areas in the CI.

## Before you begin

All plugins related to Event Management, Metric Intelligence, and Metric Explorer, are required.

Roles required:

-   To access Metric Intelligence metrics in Metric Explorer, the workspace\_agent and itil roles are required.
-   To configure the set of metrics that appears in Metric Explorer for a class, the admin or evt\_mgmt\_admin role is required.

## About this task

Metric Explorer displays the following Metric Intelligence data:

-   Charts, control bounds, and aggregations for key metrics for Configuration Items \(CIs\), in a single location.
-   Aggregation of metrics for CIs with resources, in a single consolidated time series.
-   Ability for administrators to configure which metric types appear for each CI class.

Metrics are displayed only for alerts containing a CI.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the List icon: ![List icon](../image/list-icon-sow-itom.png).

3.  Select **Lists** &gt; **Alerts** &gt; **All Alerts**.

    The Alerts - All Alerts page opens.

4.  Select the alert number to open it.

    The alert opens in a separate tab, displaying the **Overview** tab.

5.  Select the **Metrics** tab.

6.  Select the **Metric explorer** button.

    The **Metric explorer** interface opens. ![Metric explorer interface.](../image/metric-explorer.png)

    **Note:** You can also access the **Metrics** subtab and **Metric Explorer** button when selecting a CI.

7.  Select metrics in the Explore section to display the metrics in graph format in the **Custom chart** section.

    Metrics are divided according to the following subtabs:

<table id="table_ccd_ft5_jzb"><thead><tr><th>

Subtab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Metrics on the current CI icon.](../image/metrics-on-this-ci-icon.png)

</td><td>

Displays metrics on the current CI.

</td></tr><tr><td>

![Metrics on other CIs from the same host icon.](../image/metrics-other-ci-icon.png)

</td><td>

Displays metrics on other CIs on the same host.

</td></tr><tr><td>

![Metrics from impacted services icon.](../image/metrics-impacted-services-icon.png)

</td><td>

Displays metrics on entry points that relate to the service that the CI is impacting.**Note:** When working with large quantities of entry points \(100K or more\), collecting entry point metrics may cause system degradation. To prevent this, create the **sn\_disable\_selection\_entry\_point** property \(**All** &gt; **System Properties** &gt; **All Properties**\) and set it to **true** to turn off metric collection for entry points.

</td></tr></tbody>
</table>8.  In the **Custom chart** section, configure a time range for which you want to view the displayed metrics.

9.  Label alerts on the Custom chart by turning on the **Show alerts on CI** option.

    An alert icon \(![Alert icon](../../event-management/image/alert-icon.png)\) appears at the top of the graph at the point where the alert occurred.

    ![Alert indicator on graph](../image/alert-on-CI.png)


