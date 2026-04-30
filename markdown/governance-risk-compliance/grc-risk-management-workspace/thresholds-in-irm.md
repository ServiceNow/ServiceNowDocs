---
title: Thresholds in Integrated Risk Management
description: In the context of metrics, thresholds refer to predetermined values or limits used to assess the performance of a metric. These thresholds are typically defined based on specific criteria or objectives and serve as reference points to determine whether the measured value or performance meets, exceeds, or falls below the desired level.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring GRC: Metrics, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Thresholds in Integrated Risk Management

In the context of metrics, thresholds refer to predetermined values or limits used to assess the performance of a metric. These thresholds are typically defined based on specific criteria or objectives and serve as reference points to determine whether the measured value or performance meets, exceeds, or falls below the desired level.

The three colors of thresholds—red, amber, and green—are commonly used to indicate different levels of performance or status. These colors indicate the status where green signifies the metric is performing well according to expectation, amber signals caution or warning, and red signifies a critical situation. For instance, consider a scenario where you have established a metric definition aimed at reducing credit risk, with the metric direction set to Minimize. In this case, the metric values should be lower than the specified threshold value. This requirement arises from the intention to prevent pollution from increasing and instead promote its reduction. If the metric value is higher than the defined limit, the value would appear in red or amber. Thresholds only apply to quantitative metric definitions.

## Types of threshold

There are two types of threshold for a metric.

-   Static: A static threshold for a metric or a metric definition refers to a fixed value used as a limit for tracking a metric.
-   Dynamic: Dynamic thresholds are specified in percentages. This means that the percentage variance is calculated based on two factors: direction and the previous data.

    For example, in June 2023, the attrition rate is 12% based on the industry average, indicating a relatively low level of risk. The objective is to minimize attrition risk, so any increase in the metric value is considered undesirable. In July 2023, new metric data is collected, and it shows that the attrition risk metric has deviated by 5%. To evaluate the significance of this increase, you can define different thresholds representing various levels of change. These thresholds are expressed as percentage differences from the previous period's data, in this case, from June 2023. For example, the organization sets a threshold range of 5% to 10%. If the percentage change in the attrition risk metric between June and July falls within this range, the threshold status is classified as "amber." This indicates a moderate level of change, signaling that the metric has deviated from the desired target value but is not yet critical. However, if the percentage change in the attrition risk metric exceeds or reaches 15%, the threshold status is classified as "red." This signifies a significant change that demands immediate attention or corrective action since it deviates greatly from the desired target value. By monitoring these threshold levels, the organization can identify and address the increasing attrition risks promptly, enabling effective risk management.


For more information, refer to [Create a threshold for a metric definition](../task/t_create-threshold-for-metrics.md).

