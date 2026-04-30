---
title: MetricBase retention policy schedules
description: Specify how long MetricBase stores the time-series data in the MetricBase database.
locale: en-US
release: zurich
product: MetricBase
classification: metricbase
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Define and collect data, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MetricBase retention policy schedules

Specify how long MetricBase stores the time-series data in the MetricBase database.

To create, edit, or delete retention policy schedules, navigate to **MetricBase** &gt; **Retention Policy Schedules**.

When creating a retention policy schedule, the following limitations apply:

-   Maximum retention duration: 26 months \(794 days\)
-   Maximum sampling period: 1 day
-   Maximum data points \(calculated as retention duration \* sampling period\): 160,000 data points

In addition, the retention duration must be a multiple of the sampling period.

