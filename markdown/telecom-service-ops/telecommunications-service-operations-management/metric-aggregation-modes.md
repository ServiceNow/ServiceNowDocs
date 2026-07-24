---
title: Metric aggregation modes
description: Metric aggregation rolls up raw metrics collected from individual network resources into calculated metrics on parent or anchor configuration items \(CIs\). The aggregation mode determines how source resources are selected and where the aggregated result is published.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-modes.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 3
keywords: [metric aggregation, hierarchy mode, flat mode, TSOM]
breadcrumb: [Performance management: Metric collection, Telecom Assurance, Explore, Telecommunications Service Operations Management]
---

# Metric aggregation modes

Metric aggregation rolls up raw metrics collected from individual network resources into calculated metrics on parent or anchor configuration items \(CIs\). The aggregation mode determines how source resources are selected and where the aggregated result is published.

By default, a pull connector collects raw metrics and publishes one value per network resource, such as a single metric value for each mobile cell. There is no built-in way to combine those per-resource values into a higher-level metric.

Metric aggregation addresses this gap. It reads the raw metric values for a set of related resources, applies an aggregate function such as average, maximum, or minimum, and publishes a calculated metric so that the result can be viewed at a higher level of the network. An aggregation runs as a scheduled job that calls the metric aggregation scripted extension point.

## Key benefits

Metric aggregation provides the following benefits:

-   View metrics at higher levels of the network, such as per Baseband Unit \(BBU\) or per Network Site, instead of only per cell.
-   Aggregate metrics across a defined range of resources, such as a range of SIM cards.
-   Define new aggregations without changing product code by configuring scheduled jobs that call a scripted extension point.

## How it works

Each aggregation runs in one of two modes. The mode determines how source resources are selected and where the calculated metric is published.

-   **Hierarchy mode**

    The aggregation traverses configuration management database \(CMDB\) relationships downward from each target CI to collect the matching source CIs, then writes one calculated metric onto each target CI. Use hierarchy mode to roll per-cell metrics up to each parent resource, such as per Baseband Unit or per Network Site.

-   **Flat mode**

    The aggregation selects source CIs directly, optionally filtered by a name range or by field values, and writes a single calculated metric onto one anchor CI. Use flat mode for range-based or fleet-wide metrics where no single parent CI exists to hold the result.


A range identifies a contiguous set of resources by name, such as a range of SIM cards. You can also apply field filters so that only resources meeting a condition are included in the aggregation, for example only resources whose operational status indicates that they are active.

An aggregation runs one of the following functions, set through the `aggregate` parameter: average \(`avg`\), sum \(`sum`\), maximum \(`max`\), minimum \(`min`\), count \(`count`\), and the 95th percentile \(`p95`\).

After an aggregation run produces a calculated metric, the metric base framework raises an event to bind the metric to a CI. After the metric-to-CI binding completes, the calculated metric is stored in the metric base \(Clotho\) against the bound CI and becomes available to view.

## Considerations

Consider the following when you plan an aggregation:

-   In hierarchy mode, a depth limit bounds how far the traversal descends through the CMDB. The depth limit helps prevent the traversal from following relationships beyond the resources you intend to aggregate.
-   In flat mode, the calculated metric is not tied to an existing parent CI, so you specify an anchor CI to hold the result.
-   An aggregation runs on the schedule defined for its scheduled job. Calculated metrics appear after the next successful run and metric-to-CI binding.

**Related topics**  


[Configure a metric aggregation job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-metric-aggregation-job.md)

[Create a custom metric aggregation implementation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/create-custom-metric-aggregation-implementation.md)

[Metric aggregation configuration reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-configuration-reference.md)

[Metric aggregation scripted extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-scripted-extension.md)

[Metric-to-CI binding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-to-ci-binding-tsom-sgc.md)

[MPN data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/mpn-data-model.md)

