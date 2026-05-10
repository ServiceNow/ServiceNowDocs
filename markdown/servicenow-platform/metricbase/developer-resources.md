---
title: Developer resources
description: Developers can use JavaScript or REST APIs to insert and retrieve time-series data from the MetricBase database and to run transforms on the data. The transformations enable you to visualize time-series data in a variety of ways.
locale: en-US
release: australia
product: MetricBase
classification: metricbase
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Developer resources

Developers can use JavaScript or REST APIs to insert and retrieve time-series data from the MetricBase database and to run transforms on the data. The transformations enable you to visualize time-series data in a variety of ways.

## REST APIs

For information about the MetricBase REST APIs that return time-series data from the MetricBase database, see [MetricBase Time Series API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/Clotho-Time-Series-API.md).

## JavaScript APIs

For information about the MetricBase JavaScript APIs that return time-series data from the MetricBase database, see:

-   [Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/ClientScopedAPI.md) — Execute transforms on the MetricBase database and receive the results.
-   [Data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/DataScopedAPI.md) — Return the object that contains the result of a transform.
-   [DataBuilder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/DataBuilderScopedAPI.md) — Create a series of data points for a metric.
-   [Transformer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/TransformerScopedAPI.md) — Manipulate time-series data to prepare the data for evaluation and analysis.
-   [TransformPart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/TransformPartScopedAPI.md) — Specify details of the transform to be done.
-   [TransformResult](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/TransformResultScopedAPI.md) — Return the object that contains the result of the transformation.

## Transformations

For more information about MetricBase time-series data transformations, see [MetricBase transforms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/metricbase-transforms.md).

## Data Explorer

Experiment and get familiar with the JavaScript APIs by using the [MetricBase Data Explorer](../task/metricbase-data-explorer.md) that comes with the MetricBase Demo.

**Parent Topic:**[MetricBase reference](reference-metricbase.md)

**Related topics**  


[Domain separation and MetricBase](domain-separation-metricbase.md)

[MetricBase roles](../reference/metricbase-roles.md#)

