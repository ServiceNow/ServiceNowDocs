---
title: Thresholds for metrics
description: In the context of metrics, thresholds refer to predetermined values or limits used to assess the performance of a metric. These thresholds are typically defined based on specific criteria or objectives and serve as reference points to determine whether the measured value or performance meets, exceeds, or falls below the desired level.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring GRC: Metrics, GRC: Metrics, Environmental, Social, and Governance Management]
---

# Thresholds for metrics

In the context of metrics, thresholds refer to predetermined values or limits used to assess the performance of a metric. These thresholds are typically defined based on specific criteria or objectives and serve as reference points to determine whether the measured value or performance meets, exceeds, or falls below the desired level.

The three colors of thresholds—red, amber, and green—are commonly used to indicate different levels of performance or status. These colors indicate the status where green signifies the metric is performing well according to expectation, amber signals caution or warning, and red signifies a critical situation. For instance, consider a scenario where you have established a metric definition aimed at decreasing pollution, with the metric direction set to Minimize. In this case, the metric values should be lower than the specified threshold value. This requirement arises from the intention to prevent pollution from increasing and instead promote its reduction. If the metric value is higher than the defined limit, the value would appear in red or amber. Thresholds only apply to quantitative metric definitions.

## Types of threshold

There are two types of threshold for a metric.

-   Static: A static threshold for a metric or a metric definition refers to a fixed value used as a limit for tracking a metric.
-   Dynamic: Dynamic thresholds are specified in percentages. This means that the percentage variance is calculated based on two factors: direction and the previous period data. For example, you want to track electricity consumption, from a particular region and in June 2023, the electricity consumption value is 700 kWh. The direction of the metric and the metric definition is Minimize. This means you want to minimize the consumption, so any increase is considered undesirable. In July 2023, you collect new data and find that the consumption value has increased to 1000 kWh. To evaluate the status of this threshold, you define different thresholds that represent various levels of change. These thresholds are expressed as percentage differences from the previous period's data, in this case, from June 2023. For example, you can set a threshold range of 5% to 10%. If the percentage change between June and July falls within this range, you classify the threshold status as "amber." This means that there has been a moderate level of change, indicating that the metric is deviating from the desired target value, but it's not critical yet. However, if the percentage change in the metric value exceeds or reaches 15%, you classify the threshold status as "red." This increase indicates a significant change that requires immediate attention or corrective action because it deviates greatly from the desired target value.

**Related topics**  


[Create a threshold for a metric](../task/create-a-threshold-for-a-metric.md)

