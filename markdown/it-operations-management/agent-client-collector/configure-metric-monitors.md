---
title: Choose and configure metrics to monitor
description: Metric Intelligence uses data sources that can be monitoring hundreds of metrics for all CIs. Choose for each data source type which details are important for which CIs, and then activate or deactivate the respective monitor type to control the amount of data that is being processed.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Choose and configure metrics to monitor

Metric Intelligence uses data sources that can be monitoring hundreds of metrics for all CIs. Choose for each data source type which details are important for which CIs, and then activate or deactivate the respective monitor type to control the amount of data that is being processed.

## Before you begin

See [Get started with Metric Intelligence](get-started-metrics.md) for the high level steps of setting up Metric Intelligence.

Role required: evt\_mgmt\_admin

## About this task

The SCOM data source, available by default, collects about 400 metric types from discovered devices such as '% Available Memory' and '% of Free Space'. Processing data from all metric types can overload the system and impact performance. It might be necessary to deactivate selected metric types for selected CIs to reduce that load.

The overall number of metrics that can be processed, depends on the number of MID Servers and their hardware configuration. For details about hardware requirements and metrics scalability, see [MID Server and MID Server distributed cluster for Metric Intelligence](../concept/ops-intelligence-mid-server.md).

**Note:** The **Active** setting \(true or false\) for a metric in the Monitoring System Metric Types \[sa\_source\_metric\_type\] table takes precedence over the setting for the corresponding metric in the Metric To CI Mappings \[sa\_metric\_map\] table. If a metric type in the Monitoring System Metric Types \[sa\_source\_metric\_type\] table is disabled, all records related to the corresponding metrics are removed from the Metric To CI Mappings \[sa\_metric\_map\] table.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Metrics** &gt; **Metric Types**.

    The **Monitoring System Metric Types** displays the metric types that are being collected per data source, per CI type.

2.  Review the **Monitoring System Metric Types** list, and set the value in the **Active** column to **false** or **true**, as necessary.

<table id="table_cyy_2c4_vw"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

Data source monitoring the metric type.

</td></tr><tr><td>

Source Metric Type

</td><td>

Metric such as '% Free Space' that is being monitored for the CI type.

</td></tr><tr><td>

Anomaly Detection Action Level

</td><td>

The level of anomaly detection processing and analysis applied to CIs and metrics. The available options are: -   **Metrics Only**: Only gather metrics from the data source without any further processing.
-   **Bounds**: Includes the Metrics Only processing level, and also creates a statistical model and shows bounds in Insights Explorer.
-   **Anomaly Scores**: Includes the Bounds processing level, and also calculates and displays anomaly scores.
-   **Anomaly Alerts**: Includes the Anomaly Scores processing level, and also creates anomaly alerts, as applicable.
-   **IT Alerts**: Includes the Anomaly Alerts processing level, and also creates IT alerts which are based on anomaly alerts, as applicable.


</td></tr><tr><td>

Monitored Object Type

</td><td>

CI type that is being monitored.

</td></tr><tr><td>

Active

</td><td>

Determines whether the metric data is processed by Event Management alert aggregation and RCA metrics.

</td></tr><tr><td>

Unit

</td><td>

Unit type that is associated with the source metric type, displayed in the Metric Intelligence reports.

</td></tr></tbody>
</table>
