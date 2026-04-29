---
title: Disable a metric for a CI
description: Metric Intelligence can be configured to collect significant amounts of data, some of which might not be necessary. To improve performance, you can disable a specific metric for a specific CI to stop processing data related to the specified metric and CI.
locale: en-US
release: australia
product: Metric Intelligence
classification: metric-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Optimizing Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Disable a metric for a CI

Metric Intelligence can be configured to collect significant amounts of data, some of which might not be necessary. To improve performance, you can disable a specific metric for a specific CI to stop processing data related to the specified metric and CI.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

**Note:** The **Active** setting \(true or false\) for a source metric in the Monitoring System Metric Types \[sa\_source\_metric\_type\] table takes precedence over the setting for the corresponding metric in the Metric To CI Mappings \[sa\_metric\_map\] table. If a source metric type in the Monitoring System Metric Types \[sa\_source\_metric\_type\] table is disabled, all records related to the corresponding metrics are removed from the Metric To CI Mappings \[sa\_metric\_map\] table.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Anomaly Detection** &gt; **Metric to CI**.

2.  Locate the record for the metric/CI that you want to disable, and set its **Active** column to **false**.


**Parent Topic:**[Optimizing Metric Intelligence](../../metric-intelligence/concept/optimizing-metric-intelligence.md)

