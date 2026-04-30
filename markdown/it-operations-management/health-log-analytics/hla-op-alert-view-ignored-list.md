---
title: View the list of muted metrics
description: View the list of metrics that were muted so that they no longer generate alerts.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mute an unimportant alert, Assigning higher or lower significance to an alert, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# View the list of muted metrics

View the list of metrics that were muted so that they no longer generate alerts.

## Before you begin

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Log Anomaly Detection** &gt; **Muted Metrics**.

    |Field|Description|
    |-----|-----------|
    |Service instance|Service instance where the muted alert with which the metric is associated appears.|
    |Component|Logical component of the service instance that generated the event. Multiple CIs can sometimes perform the same function.|
    |Pattern text|Text for the metric that is associated with the muted alert.|
    |Metric|Log text or key that represents a meter or gauge value in the data. For example, patterns, raw metrics, keyword, severity, all events metrics.|
    |Created|Date and time when the metric was added to the list.|


**Parent Topic:**[Mute an unimportant alert](hla-op-alert-mute.md)

**Related topics**  


[Mute an unimportant alert](hla-op-alert-mute-sow.md)

[Restore normal importance to an alert metric](hla-op-alert-restore-user-defined-sow.md)

