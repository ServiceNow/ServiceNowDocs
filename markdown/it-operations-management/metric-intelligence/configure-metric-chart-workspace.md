---
title: Configure metric charts for Agent Workspace
description: Configure the set of Metric Intelligence metric charts, chart types, and other chart characteristics, that appear in Agent Workspace.
locale: en-US
release: yokohama
product: Metric Intelligence
classification: metric-intelligence
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Optimizing Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Configure metric charts for Agent Workspace

Configure the set of Metric Intelligence metric charts, chart types, and other chart characteristics, that appear in Agent Workspace.

## Before you begin

Role required: admin or evt\_mgmt\_admin

## About this task

Up to 10 metric charts for a class can be configured to appear in the Metric Intelligence metric charts form in Agent Workspace. Metric chart configurations are stored in the Metric Dashboard Metadata \[sa\_metric\_dashboard\_metadata\] table, determining which metric charts appear for a CI that is associated with an alert. By default, the Metric Dashboard Metadata contains pre-configured metric charts for several classes.

If [resource binding](../concept/resource-binding.md) is enabled and you specify a **Resource Type** in the metric chart configuration, then all the resources for the CI are included in the chart. The class table for the resource class \(such as **ci\_resource\_metric\_extension**\) that you specify is used for retrieving all the resources for the CI. Then, for each point in time in the data series, the values of resources are aggregated into a single data point which is the average of the metric values of all resources for that point of time.

|Chart type|Resources|Aggregation|
|----------|---------|-----------|
|Time\_Series|No|No aggregation|
|Time\_Series|Yes|Resources are averaged per data point.|
|Single\_Score|No|Data points are aggregated according to the **Chart Aggregate** setting.|
|Single\_Score|Yes|Resources are averaged per data point and then data points are aggregated according to the **Chart Aggregate** setting.|

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Metrics View Configuration**.

2.  In the Metric Dashboard Metadatas \(Dashboard Metadata\) list view, select an existing configuration or click **New**.

3.  Fill out the Metric Dashboard Metadata form.

<table id="table_svv_jry_lhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Include the chart on the Metric Intelligence charts form in Agent Workspace.

</td></tr><tr><td>

Resource Type

</td><td>

Resource class associated with the CI and for which to retrieve and aggregate all resources.

</td></tr><tr><td>

Configuration Item Type

</td><td>

CI class that the chart applies to such as **cmdb\_ci\_metric\_extension**.

</td></tr><tr><td>

Chart Aggregate

</td><td>

Type of aggregation that is applied for single-score charts. Aggregation can be the average of the data points in the time series. Or, the minimum, maximum, or the last data point in the time series.

</td></tr><tr><td>

Source Metric Type

</td><td>

Metric such as '% Free Space' that is being monitored for the CI type.

</td></tr><tr><td>

Order

</td><td>

Order in which the metric chart appears within all metric charts specified for the class.

 For proper appearance and alignment, all single-score charts always appear after any time-series charts, regardless of order settings.

</td></tr><tr><td>

Chart Type

</td><td>

-   Time\_Series: Charts all the data points in the time series for the metric and CI of the chart.
-   Single\_Score: A single number which is the aggregation of all data points in the time series for the metric and CI of the chart. Aggregation is determined by the setting of **Chart Aggregate**.


</td></tr></tbody>
</table>
**Parent Topic:**[Optimizing Metric Intelligence](../../metric-intelligence/concept/optimizing-metric-intelligence.md)

