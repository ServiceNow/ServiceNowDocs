---
title: Retrieving MetricBase data using REST and JavaScript
description: Use JavaScript or REST APIs to insert and retrieve time-series data from the MetricBase database and to run transforms on the data. The transformations enable you to visualize time-series data in a variety of ways.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/metricbase/analyze-time-series-data.html
release: zurich
product: MetricBase
classification: metricbase
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Accessing data, Define and collect data, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Retrieving MetricBase data using REST and JavaScript

Use JavaScript or REST APIs to insert and retrieve time-series data from the MetricBase database and to run transforms on the data. The transformations enable you to visualize time-series data in a variety of ways.

For more information about MetricBase time-series data transformations, see [MetricBase transforms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/reporting/metricbase-transforms.md).

## Using REST

For information about the MetricBase REST APIs that return time-series data from the MetricBase database, see [MetricBase Time Series API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/rest-apis/Clotho-Time-Series-API.md).

## Using JavaScript

For information about the MetricBase JavaScript APIs that return time-series data from the MetricBase database, see:

-   [Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/ClientScopedAPI.md) — Execute transforms on the MetricBase database and receive the results.
-   [Data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/DataScopedAPI.md) — Return the object that contains the result of a transform.
-   [DataBuilder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/DataBuilderScopedAPI.md) — Create a series of data points for a metric.
-   [Transformer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/TransformerScopedAPI.md) — Manipulate time-series data to prepare the data for evaluation and analysis.
-   [TransformPart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/TransformPartScopedAPI.md) — Specify details of the transform to be done.
-   [TransformResult](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/TransformResultScopedAPI.md) — Return the object that contains the result of the transformation.

Experiment and get familiar with the JavaScript APIs by using the [MetricBase Data Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/metricbase/metricbase-data-explorer.md) that comes with the MetricBase Demo.

