---
title: Defining and collecting MetricBase data
description: Store time-series summaries of much larger data collections.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/metricbase/collecting-metricbase-data.html
release: zurich
product: MetricBase
classification: metricbase
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Defining and collecting MetricBase data

Store time-series summaries of much larger data collections.

## Overview of creating a time-series definition

In MetricBase, you specify the metric that you want to store and how often to collect it. You can also determine how long to store it in the MetricBase database. Then, you send the data from an instance to the MetricBase server at the rate that you define using MetricBase REST or JavaScript APIs. In this way, you can monitor a much larger data collection with MetricBase summaries of it.

MetricBase collects the metrics of how often you send data and what the aggregation of that data is, for example, maximum, minimum, average, or last. This data is called time-series data. For example, if you collect drone speeds on an instance, you can send the average drone speed for every two minutes to the MetricBase database. You can also collect altitude and battery life. MetricBase stores each metric as a column in its database.

\[Omitted image "mb-glide-relationship.png"\] Alt text: MetricBase and instance relationship

-   [Create a time-series definition in MetricBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/metricbase/set-up-data-monitoring.md)

    Specify the metric that you want to store, how often to collect it, and how long to store it in MetricBase.

-   [MetricBase retention policy schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/metricbase/metricbase-retention-policy-schedules.md)

    Specify how long MetricBase stores the time-series data in the MetricBase database.

-   [MetricBase retention policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/metricbase/metricbase-retention-policies.md)

    Retain data in MetricBase according to retention policies.

-   [Accessing MetricBase data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/metricbase/accessing-metricbase-data.md)

    Access the time-series data that you sent to the MetricBase database in the way that is convenient to you.

-   [Detecting anomalies in MetricBase data using predictive models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/metricbase/metricbase-predictive-models.md)

    Distinguish normal data from anomalous data using predictive models.


