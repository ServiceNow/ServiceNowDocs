---
title: Managing MetricBase
description: View the overall health and performance of MetricBase, and debug its triggers and scripts.View the status and health of the connection to your MetricBase database.Monitor the usage and efficiency of your MetricBase time series data.You can view the status of the MetricBase database.You can display the results of debugging scripts in MetricBase.
locale: en-US
release: yokohama
product: MetricBase
classification: metricbase
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Managing MetricBase

View the overall health and performance of MetricBase, and debug its triggers and scripts.

## Overview of managing MetricBase

**Parent Topic:**[MetricBase](metricbase.md)

## View MetricBase database status

View the status and health of the connection to your MetricBase database.

### Before you begin

Role required: clotho\_admin

### Procedure

1.  Navigate to **All** &gt; **MetricBase** &gt; **MetricBase Health Dashboard**.

2.  In the list, select **Health**.

3.  View the status of the database connection.

    If the database is offline, contact Customer Service and Support.

4.  Monitor the lag time between your instance and the database by viewing the **MetricBase Lag Statistics** value.

    If the lag time is reported in multiple seconds, contact Customer Service and Support.

5.  Select **Refresh** to view the latest status.


## View MetricBase data usage and efficiency

Monitor the usage and efficiency of your MetricBase time series data.

### Before you begin

Role required: clotho\_admin

### Procedure

1.  Navigate to **All** &gt; **MetricBase** &gt; **MetricBase Health Dashboard**.

2.  In the list, select **Series**.

    The MetricBase Series Information page displays the Total Series Count, which is the total number of series registered in MetricBase.

3.  Determine whether any series aren't being used by calculating the stale series ratio.

    This ratio is the percentage of series that haven't received a value within a specified number of days.

    1.  Enter the number of days \(greater than or equal to 1\) in the **Staleness Time Period** field.

    2.  Select the Refresh icon \(![Refresh icon.](../../virtual-agent/images/refresh-icon.png)\).

    The closer the ratio is to 0%, the fewer unused series there are within the given time period. You determine your own threshold for an acceptable stale series ratio. To lower the ratio, adjust the metric's sampling schedule or remove unused metrics or series. For help with removing a stale series, contact Customer Service and Support.

4.  Determine how efficiently your time series data is used by viewing the **Data Utilization Efficiency** value.

    The value is the percentage of data points per metric that have a non-null value. The closer this value is to 100%, the fewer null data points there are. To increase the efficiency, review each metric to ensure that data is being posted at a similar rate to the first schedule of its retention policy. See [MetricBase retention policies](../reference/metricbase-retention-policies.md) for more information.

5.  Determine how often values are published to MetricBase by viewing the **Average Unutilized Data Gap** value.

    The gap value is the average number of entries between two non-null data points. To decrease the gap value, change the metric's schedule to publish data more often or update the metric's sampling period in its retention policy. See [MetricBase retention policies](../reference/metricbase-retention-policies.md).


## View MetricBase statistics and metrics

You can view the status of the MetricBase database.

### Before you begin

Role required: admin

### Procedure

1.  View the status of the MetricBase instance.

    1.  Navigate to **System Diagnostics** &gt; **Stats** &gt; **Stats**.

    2.  Scroll down to find **MetricBase Statistics**

        ![MetricBase statistics](../image/mb-statistics.png)

2.  View the metrics monitored by MetricBase and statistics about them.

    1.  Click **MetricBase** &gt; **MetricBase Status**

        The MetricBase Status page displays all of the metrics tracked in MB.

        ![List of metrics monitored](../image/mb-status-metrics-monitored.png)

    2.  Click the gear icon.

        The Personalize List Columns dialog box displays.

        ![Select metrics to display.](../image/personalize-list-columns.png)

    3.  Select and move metrics from the **Available** column to the **Selected** column to display the metric and click **OK**.

        The metrics display on the MetricBase Status page.

        ![Metrics](../image/mb-statistics-metrics.png)


## Debug MetricBase

You can display the results of debugging scripts in MetricBase.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Diagnostics** &gt; **Session Debug** &gt; **Debug MetricBase**.

    When the page you are on submits queries to MetricBase, you see the transforms and how long they took on the bottom of the page. Submitting a lot of MetricBase queries may slow down the page load time significantly.

2.  To view a history of the debug script's execution, click **available here**.

3.  Click **Update**.

    Session debug tracking for MetricBase activities starts and the MetricBase Status page displays.


