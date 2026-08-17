---
title: Metric aggregation scripted extension
description: You can define custom KPI calculations on top of raw metrics collected from source systems. Configurable formulas combine, aggregate, and label metrics without requiring code changes to the platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-scripted-extension.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Performance management: Metric collection, Telecom Assurance, Explore, Telecommunications Service Operations Management]
---

# Metric aggregation scripted extension

You can define custom KPI calculations on top of raw metrics collected from source systems. Configurable formulas combine, aggregate, and label metrics without requiring code changes to the platform.

By default, TSOM Assurance collects raw metrics from pull connectors and publishes them as-is. The metric aggregation scripted extension provides an extension point on the aggregation script, allowing you to implement custom logic that derives KPIs from those raw metrics. One or more KPIs can be calculated from a single metric value, and KPI definitions can be added, updated, or deleted on demand without redeployment.

## Key capabilities

-   **Configurable formulas**

    Define KPIs using mathematical expressions that combine one or more raw or already-transformed metrics. Formulas are vendor-agnostic and can be conditioned on resource attributes such as vendor or software version.

-   **Temporal aggregation**

    Apply aggregation operators over a configured time period to produce a single derived value per metric. Supported operators are `avg`, `max`, `min`, and `p95`. Supported periods are 5 minutes, 15 minutes, and 1 hour.

-   **Spatial aggregation**

    Aggregate the same KPI or metric across multiple resources that match a filter criterion based on metric or resource attributes. The supported aggregate functions are `avg`, `sum`, `max`, `min`, `count`, and `p95`.

-   **User-defined labels**

    Attach custom labels to calculated KPIs to support downstream categorization, routing, or display logic.

-   **Formula error handling**

    When a formula can't be evaluated \(for example, due to a division by zero or missing input metric\), the system generates an error code for that KPI. The system does not discard the value without notification.


## Implementation

The extension point is implemented using the **sn\_tsom\_em\_conns.TSOMMetricAggregatorSEP** scripted extension point. To create a custom implementation, navigate to **All** &gt; **System Scripted Extension Points** &gt; **Scripted Extension Points** and search for **sn\_tsom\_em\_conns.TSOMMetricAggregatorSEP**. Select **Create implementation** and define your KPI formulas in the script body.

KPI definitions, including formulas and resource attribute filters, can be configured and managed independently. Add, update, or delete definitions to adapt KPI coverage as your network environment changes.

