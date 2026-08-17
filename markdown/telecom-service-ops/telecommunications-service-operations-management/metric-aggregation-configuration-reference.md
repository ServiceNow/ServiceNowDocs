---
title: Metric aggregation configuration reference
description: The configuration object passed to the metric aggregation scripted extension point defines what to aggregate, how to aggregate it, and where to publish the result. The parameters that apply depend on the aggregation mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-configuration-reference.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 3
keywords: [metric aggregation configuration, aggregation parameters, metric aggregation, TSOM]
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Metric aggregation configuration reference

The configuration object passed to the metric aggregation scripted extension point defines what to aggregate, how to aggregate it, and where to publish the result. The parameters that apply depend on the aggregation mode.

## Configuration parameters

|Parameter|Type|Applies to mode|Required|Description|
|---------|----|---------------|--------|-----------|
|`mode`|String|Both|Required|Aggregation mode. One of `hierarchy` or `flat`. The mode determines how source resources are selected and where the calculated metric is published. See [Metric aggregation modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-modes.md).|
|`targetCIClass`|String|Hierarchy|Required \(hierarchy\)|CMDB class of the parent or target CI that receives the calculated metric, for example `cmdb_ci_baseband_unit`. The aggregation traverses CMDB relationships downward from each target CI to collect the matching source CIs.|
|`sourceCIClass`|String|Both|Required|CMDB class of the source CIs whose raw metric is aggregated, for example `cmdb_ci_mobile_cell`.|
|`sourceMetric`|String|Both|Required|Name of the raw metric collected on the source CIs that is read as input to the aggregation.|
|`aggregate`|String|Both|Required|Aggregate function applied to the source metric values. One of `avg`, `sum`, `max`, `min`, `count`, or `p95`. The calculated value is stored unrounded, as a raw floating-point number.|
|`calculatedMetricName`|String|Both|Required|Name of the calculated metric that the aggregation produces and publishes.|
|`unit`|String|Both|Optional|Unit label applied to the calculated metric, for example `Mbps`.|
|`level`|Integer|Hierarchy|Optional|Depth limit that bounds how far the CMDB traversal descends from each target CI. Prevents the traversal from following relationships beyond the resources you intend to aggregate. Defaults to `4` and is capped at a maximum of `20`; larger values are silently capped. A value of `0` is not treated as "no traversal" — it falls back to the default of `4`.|
|`rangeStart`|String|Both|Optional|Start of a contiguous range of source resources identified by name, for example `SIM010`. Use with `rangeEnd` to select source CIs by range.|
|`rangeEnd`|String|Both|Optional|End of the contiguous range of source resources identified by name, for example `SIM050`.|
|`filters`|Array|Both|Optional|Field filters that restrict the source CIs to those meeting a condition. Each element is an object with `field`, `operator`, and `value`. See [Filter object](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-configuration-reference.md).|
|`anchorCiSysId`|String|Flat|Required \(flat\)|The `sys_id` of the anchor CI that holds the calculated metric. In flat mode the result is not tied to an existing parent CI, so you specify an anchor CI to hold it.|

## Filter object

Each element of the `filters` array selects source CIs that meet a single field condition.

|Property|Type|Description|
|--------|----|-----------|
|`field`|String|Name of the field on the source CI to evaluate, for example `operational_status`.|
|`operator`|String|Comparison operator applied to the field. One of `=`, `!=`, `>`, `>=`, `<`, `<=`, `CONTAINS`, `STARTSWITH`, or `IN`.|
|`value`|String|Value the field is compared against, for example `1`.|

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

**Related topics**  


[Metric aggregation modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-aggregation-modes.md)

[Configure a metric aggregation job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-metric-aggregation-job.md)

[Metric type IDs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/tsom-metric-type-ids.md)

