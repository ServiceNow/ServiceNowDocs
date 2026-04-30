---
title: Defining and collecting MetricBase data
description: Store time-series summaries of much larger data collections.
locale: en-US
release: xanadu
product: MetricBase
classification: metricbase
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Defining and collecting MetricBase data

Store time-series summaries of much larger data collections.

## Overview of creating a time-series definition

In MetricBase, you specify the metric that you want to store and how often to collect it. You can also determine how long to store it in the MetricBase database. Then, you send the data from an instance to the MetricBase server at the rate that you define using MetricBase REST or JavaScript APIs. In this way, you can monitor a much larger data collection with MetricBase summaries of it.

MetricBase collects the metrics of how often you send data and what the aggregation of that data is, for example, maximum, minimum, average, or last. This data is called time-series data. For example, if you collect drone speeds on an instance, you can send the average drone speed for every two minutes to the MetricBase database. You can also collect altitude and battery life. MetricBase stores each metric as a column in its database.

![MetricBase and instance relationship](../image/mb-glide-relationship.png "Sending information from an instance to a MetricBase server")

## Retention policy schedules

Retention policy schedules specify how long MetricBase stores the time-series data in the MetricBase database. You can create, edit, and delete retention policy schedules. To create, edit, or delete retention policy schedules, navigate to **MetricBase** &gt; **Retention Policy Schedules**.

When creating a retention policy schedule, the following limitations apply:

-   Maximum retention duration: 26 months \(794 days\)
-   Maximum sampling period: 1 day
-   Maximum data points \(calculated as retention duration \* sampling period\): 160,000 data points

In addition, the retention duration must be a multiple of the sampling period.

## Retention policies

Retention policies include multiple retention schedules with coarser granularity the longer that the data is kept. For example, the Coarse retention policy stores sampled data every:

-   Hour for one week \(7 Days per 1-hour period\)
-   Two hours for one month \(31 days per 2-hour period\)
-   Day for 13 months \(397 Days per 1-day period\)

In this policy, the specified metric is measured every hour for the first 7 days. It is then measured every other hour for the next 31 days, and once a day for the next 397 days. MetricBase deletes data that is older than 435 days.

To see the list of all supported retention policies, navigate to **MetricBase** &gt; **Retention Policies**.

