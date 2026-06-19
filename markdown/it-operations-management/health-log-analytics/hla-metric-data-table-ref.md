---
title: Metric Data table columns in Health Log Analytics
description: The Metric Data table lists all metrics that Health Log Analytics collects. Use the table to query metrics by log source, integration, source type, and metric type, review anomaly detection statistics, and view metric baselines.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/hla-metric-data-table-ref.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-05-13"
reading_time_minutes: 1
keywords: [Health Log Analytics, HLA, Metric Data table, metric name, metric type, metric class, log source, metric record, meter, gauge]
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Metric Data table columns in Health Log Analytics

The Metric Data table lists all metrics that Health Log Analytics collects. Use the table to query metrics by log source, integration, source type, and metric type, review anomaly detection statistics, and view metric baselines.

For more information about using the Metric Data table, see [View log anomaly metrics in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-metric-data-table.md).

## Column descriptions

Each row in the Metric Data table represents one metric that HLA collects.

|Column|Description|
|------|-----------|
|Metric Name|Unique identifier of the metric being tracked.|
|Service|Service instance associated with the metric.|
|Source|Log source from which the metric originates.|
|Component|Component within the log source that generates the metric.|
|Metric Type|Type of measurement, such as meter or gauge.|
|Dimension|AI Engine metric identifier associated with this record.|
|Subject|Subject identifier that groups related metrics.|
|Class|Metric classification, such as Keyword Metric, Pattern ID Metric, Raw Metric, or All Events Metric.|

**Parent Topic:**[Health Log Analytics reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-reference.md)

