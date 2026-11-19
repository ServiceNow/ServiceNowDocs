---
title: View log anomaly metrics in Health Log Analytics
description: View and query all metrics that Health Log Analytics tracks from a single location.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/health-log-analytics/hla-metric-data-table.html
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 1
keywords: [Health Log Analytics, HLA, all metrics, log anomaly metrics, anomaly detection, log source, integration, source type, pattern metrics, custom metrics, raw metrics]
breadcrumb: [Administer HLA, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# View log anomaly metrics in Health Log Analytics

View and query all metrics that Health Log Analytics tracks from a single location.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

The Metric Data table provides a centralized view of every metric that HLA collects and monitors. It includes pattern metrics, custom metrics, and raw metrics. Use the table for the following tasks:

-   Query metrics by log source, integration, source type, and metric type to narrow down which metrics HLA is tracking for a data input or environment.
-   Review anomaly detection statistics to see how often HLA detects anomalies for a given metric.
-   View metric baselines to understand what HLA records as normal behavior.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Log Anomaly Detection** &gt; **All Metrics**.

    The **Metric Data** table displays a record for each metric that HLA is collecting. For a description of the columns in the table, see [Metric Data table columns in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-metric-data-table-ref.md).

2.  Filter the table by log source, integration, source type, or metric type.

    Filtering enables you to narrow the results to the metrics relevant to a specific data input or environment.

3.  Select a metric record to view its details.


**Parent Topic:**[Administering Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-administer.md)

