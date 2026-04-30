---
title: Metric binding
description: After metric data is collected, Metric Intelligence identifies the CIs and the resources to bind the data to.
locale: en-US
release: zurich
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Metric binding

After metric data is collected, Metric Intelligence identifies the CIs and the resources to bind the data to.

The data that is collected on the MID Server is raw and does not relate to any specific CI or resource in the CMDB. To be useful, the data goes through a **normalization** process that uses CMDB identification rules and event rules to uniquely identify CIs, and to map and bind them to the raw data. Raw data can also be [mapped and bound to resources](resource-binding.md), if binding to a CI is successful and if resource binding is configured.

Records for mapping raw data to CIs are automatically generated and remain in effect for a specified length of time determined by the properties:

-   **sa.metric.map.with.ci.expiration.sec**: If the mapping to the CI was found. Set by default to be valid for five days.
-   **sa.metric.map.without.ci.expiration.sec**: If mapping to the CI was not found. Set by default to be valid for 24 hours.

When similar metric data arrives within that time period, the existing mapping is used to match the data to CIs. At the end of the time period, metric-to-CI records expire. Also, a change in the event rules triggers an immediate expiration of the respective metric-to-CI records. Next time that raw metric data arrives, it will be normalized again. When Discovery adds or removes CIs, mappings are adjusted to reflect these changes at the next cycle.

All the information about the recent existing mapping is saved under metric-to-CI records in the sa\_metric\_map table, as shown below. You can access the Metric to CI table by navigating to **All &gt; Event Management &gt; Metrics &gt; Metric to CI**.

![Metric to CI table](../image/sa_metric_map.png "Metric to CI table")

