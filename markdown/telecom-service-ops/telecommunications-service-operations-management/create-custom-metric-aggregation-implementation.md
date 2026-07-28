---
title: Create a custom metric aggregation implementation
description: Create a custom implementation of the metric aggregation scripted extension point when the default aggregation modes don't cover a calculation you need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/create-custom-metric-aggregation-implementation.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-07-28"
reading_time_minutes: 1
keywords: [custom metric aggregation, scripted extension point, TSOMMetricAggregator, TSOM]
breadcrumb: [Configure Telecom Assurance, Configure, Telecommunications Service Operations Management]
---

# Create a custom metric aggregation implementation

Create a custom implementation of the metric aggregation scripted extension point when the default aggregation modes don't cover a calculation you need.

## Before you begin

Role required: tsom\_visibility\_admin

## About this task

The metric aggregation scripted extension point includes a default implementation that covers the standard aggregation modes. If the default implementation doesn't cover the aggregation you need, create your own implementation of the extension point. Your implementation runs without requiring a product change.

## Procedure

1.  Navigate to **All** &gt; **System Scripted Extension Points** &gt; **Scripted Extension Points**.

2.  Search for `TSOMMetricAggregator`.

3.  Select **Create implementation**.

4.  In the **Script** field, define your aggregation logic.

    Provide the aggregation configuration that your implementation uses, following the same configuration structure as the default aggregation modes.

5.  In the **Order** field, set the execution priority for your implementation.

6.  Select **Submit**.


## Result

Your custom implementation is active. A scheduled job that calls the metric aggregation scripted extension point runs your implementation along with the other registered implementations.

**Parent Topic:**[Configure Telecom Assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-fault-management.md)

**Related topics**  


[Metric aggregation modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-modes.md)

[Configure a metric aggregation job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-metric-aggregation-job.md)

[Metric aggregation configuration reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-configuration-reference.md)

[Metric aggregation scripted extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-scripted-extension.md)

