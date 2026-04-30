---
title: Thresholds in Integrated Risk Management
description: In the context of metrics, thresholds refer to predetermined values or limits used to assess the performance of a metric. These thresholds are typically defined based on specific criteria or objectives and serve as reference points to determine whether the measured value or performance meets, exceeds, or falls below the desired level.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-06"
reading_time_minutes: 2
breadcrumb: [GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Thresholds in Integrated Risk Management

In the context of metrics, thresholds refer to predetermined values or limits used to assess the performance of a metric. These thresholds are typically defined based on specific criteria or objectives and serve as reference points to determine whether the measured value or performance meets, exceeds, or falls below the desired level.

Thresholds use color-coded indicators to signify different levels of performance or status. These colors help users quickly assess metric performance at a glance. While green traditionally signifies the metric is performing well, amber signals caution, and red signifies a critical situation, you can now customize colors for each threshold level to match your organization's monitoring requirements. Risk administrators and Risk managers can define multiple threshold levels and assign unique colors to each level for precise performance monitoring. For example, you can create a metric to monitor the frequency of operational loss events on a monthly basis. Using predefined threshold ranges, you can define when threshold breaches occur, such as when the number of recorded loss events falls between 6 and 10 in a month or exceeds 10 events. Each threshold band can be assigned a unique color to provide visual indicators across dashboards, list pages, and record pages. When the monthly loss event count meets these conditions, the system triggers the configured risk response actions, such as notifying the risk owner or escalating to the operational risk management committee. Thresholds apply only to quantitative metrics, such as the count of realized operational loss events.

## Types of threshold

There are two types of threshold for a metric.

-   Static: A static threshold for a metric or a metric definition refers to a fixed value used as a limit for tracking a metric.
-   Dynamic: Dynamic thresholds are specified in percentages. This means that the percentage variance is calculated based on two factors: direction and the previous data.

    For example, in January 2026, the attrition rate is 12% based on the industry average, indicating a relatively low level of risk. The objective is to minimize attrition risk, so any increase in the metric value is considered undesirable. In February 2026, new metric data is collected, and it shows that the attrition risk metric has deviated by 5%. To evaluate the significance of this increase, you can define different thresholds representing various levels of change. These thresholds are expressed as percentage differences from the previous period's data, in this case, from January 2026. For example, the organization sets a threshold range of 5% to 10%. If the percentage change in the attrition risk metric between June and July falls within this range, the threshold status is classified as "amber." This indicates a moderate level of change, signaling that the metric has deviated from the desired target value but is not yet critical. However, if the percentage change in the attrition risk metric exceeds or reaches 15%, the threshold status is classified as "red." This signifies a significant change that demands immediate attention or corrective action since it deviates greatly from the desired target value. By monitoring these threshold levels, the organization can identify and address the increasing attrition risks promptly, enabling effective risk management.


**Related topics**  


[Create a threshold for a metric definition](../task/t_create-threshold-for-metrics.md)

[Copy thresholds](../task/copy-thresholds-irm.md)

[Customize threshold colors](../task/customize-threshold-colors-irm.md)

