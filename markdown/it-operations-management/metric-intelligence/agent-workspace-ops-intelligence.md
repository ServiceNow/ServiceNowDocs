---
title: Metric Explorer
description: Metric Explorer provides an easy-to-navigate interface where service agents can view the health of a CI associated with an alert. Health details for a CI include various metric charts with control bounds, and aggregations in a time period.
locale: en-US
release: yokohama
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Metric Explorer

Metric Explorer provides an easy-to-navigate interface where service agents can view the health of a CI associated with an alert. Health details for a CI include various metric charts with control bounds, and aggregations in a time period.

The set of metric charts that appear for a CI class in Metric Explorer is determined by metric chart configurations in the Metric Dashboard Metadata \[sa\_metric\_dashboard\_metadata\] table. The Metric Dashboard Metadata table is initially populated with configurations for common classes and important metrics for those classes. A user with the admin or evt\_mgmt\_admin role can update the default metric chart configurations in the Metric Dashboard Metadata table.

There can be up to 10 active metric charts configured for a class at any point.

## Chart types

A metric chart that appears in the metric charts form in Metric Explorer can be a **time-series** chart or a **single-score** chart.

-   **Time-series chart**

    ![Time series chart type in Agent Workspace.](../image/time-series-chart.png)

    The time-series chart type is a graph of all data points in the specified time range, for the metrics of the CI associated with the chart. Time-series charts are similar to charts in [Insights Explorer](../task/view-metrics-explorer.md), and depending on settings, show lower and upper bounds.

-   **Single-score chart**

    ![Single score chart type in Agent Workspace.](../image/single-score-chart.png)

    The single-score chart type shows a single number which is an aggregation of the data points in the time series for the metric and CI of the chart. The aggregation is an average of the data points, or the maximum, minimum, or last data point in the time series.


## Templates

The ITOM Service Operations Workspace Metric Explorer template enables metric chart drill-down from Digital Analytics \(DA\) dashboards to Metric Explorer. For details, see [Express list overview](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/now-components/sn-itom-aiops-list/overview) on the ServiceNow® Developer portal.

