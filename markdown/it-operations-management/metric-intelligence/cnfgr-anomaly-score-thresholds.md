---
title: Configure anomaly score thresholds
description: Metric Intelligence scores anomalies on a range 0-10. This range is broken down to the five levels of event severities, each represented by a different color in the Insights Explorer and in the Anomaly Map. You can configure the anomaly score threshold for each level of severity.
locale: en-US
release: zurich
product: Metric Intelligence
classification: metric-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Optimizing Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Configure anomaly score thresholds

Metric Intelligence scores anomalies on a range 0-10. This range is broken down to the five levels of event severities, each represented by a different color in the Insights Explorer and in the Anomaly Map. You can configure the anomaly score threshold for each level of severity.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Anomaly score thresholds are defined in the table Anomaly Score to Event Severity Map \[sa\_metric\_anomaly\_score\_to\_event\_severity\_map\]. For example, by default, anomaly scores from 8 through 9 are severity 2 \(Major\), and are displayed by dark orange color in the Insights Explorer and in the Anomaly Map.

For information on the event severities that each number corresponds to, see [Event severities](../../agent-client-collector/reference/event-severities.md).

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Anomaly Detection** &gt; **Anomaly Score to Severity Mapping**.

2.  In the **Metric Anomaly Score to Event Severity Maps** list view, double-click the event severity that you want to modify.

3.  Modify the range of anomaly scores that map to the respective event severity.

4.  Click **Update**.


**Parent Topic:**[Optimizing Metric Intelligence](../../metric-intelligence/concept/optimizing-metric-intelligence.md)

