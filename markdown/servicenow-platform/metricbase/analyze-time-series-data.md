---
title: Retrieving MetricBase data using REST and JavaScript
description: Use JavaScript or REST APIs to insert and retrieve time-series data from the MetricBase database and to run transforms on the data. The transformations enable you to visualize time-series data in a variety of ways.
locale: en-US
release: xanadu
product: MetricBase
classification: metricbase
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Accessing MetricBase data, Defining and collecting MetricBase data, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Retrieving MetricBase data using REST and JavaScript

Use JavaScript or REST APIs to insert and retrieve time-series data from the MetricBase database and to run transforms on the data. The transformations enable you to visualize time-series data in a variety of ways.

For more information about MetricBase time-series data transformations, see [MetricBase transforms](https://www.servicenow.com/docs/access?context=metricbase-transforms&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

## Using REST

For information about the MetricBase REST APIs that return time-series data from the MetricBase database, see [MetricBase Time Series API](https://www.servicenow.com/docs/access?context=Clotho-Time-Series-API&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

## Using JavaScript

For information about the MetricBase JavaScript APIs that return time-series data from the MetricBase database, see:

-   [Client](https://www.servicenow.com/docs/access?context=ClientScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) — Execute transforms on the MetricBase database and receive the results.
-   [Data](https://www.servicenow.com/docs/access?context=DataScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) — Return the object that contains the result of a transform.
-   [DataBuilder](https://www.servicenow.com/docs/access?context=DataBuilderScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) — Create a series of data points for a metric.
-   [Transformer](https://www.servicenow.com/docs/access?context=TransformerScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) — Manipulate time-series data to prepare the data for evaluation and analysis.
-   [TransformPart](https://www.servicenow.com/docs/access?context=TransformPartScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) — Specify details of the transform to be done.
-   [TransformResult](https://www.servicenow.com/docs/access?context=TransformResultScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) — Return the object that contains the result of the transformation.

Experiment and get familiar with the JavaScript APIs by using the [MetricBase Data Explorer](../task/metricbase-data-explorer.md) that comes with the MetricBase Demo.

