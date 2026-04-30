---
title: Thresholds for metrics
description: In the context of metrics, thresholds refer to predetermined values or limits used to assess the performance of a metric. These thresholds are typically defined based on specific criteria or objectives and serve as reference points to determine whether the measured value or performance meets, exceeds, or falls below the desired level.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Thresholds for metrics

In the context of metrics, thresholds refer to predetermined values or limits used to assess the performance of a metric. These thresholds are typically defined based on specific criteria or objectives and serve as reference points to determine whether the measured value or performance meets, exceeds, or falls below the desired level.

Thresholds use color-coded indicators to signify different levels of performance or status. These colors help users quickly assess metric performance at a glance. While green traditionally signifies the metric is performing well, amber signals caution, and red signifies a critical situation, you can now customize colors for each threshold level to match your organization's monitoring requirements. ESG administrators, ESG program managers, and ESG metrics managers can define multiple threshold levels and assign unique colors to each level for precise performance monitoring. For example, you can create a threshold to monitor pollution levels. Using the condition builder, you can define when threshold breaches occur, such as when pollution values exceed 100 units or fall between 50 and 75 units. Each threshold level can be assigned a unique color to provide visual indicators in dashboards, list pages, and record pages. When pollution data meets these conditions, the system triggers configured actions. Thresholds only apply to quantitative metrics.

## Types of thresholds

The two types of threshold for a metric are static and dynamic:

-   Static: A static threshold for a metric or a metric definition refers to a fixed value used as a limit for tracking a metric.
-   Dynamic: Dynamic thresholds are specified in percentages and calculate variance based on previous period data. For example, if you track electricity consumption and the value in January 2026 is 700 kWh, you can define threshold conditions to monitor changes in subsequent periods. Using the condition builder, you can specify conditions such as "percentage change is between 5% and 10%" or "percentage change exceeds 15%." Each threshold level is assigned a unique color to provide visual indicators. When February 2026 data is collected and the percentage change from January falls within your defined conditions, the system displays the corresponding color indicator and triggers any configured actions such as sending notifications or creating issues. 

**Related topics**  


[Create a threshold for a metric](../task/create-a-threshold-for-a-metric.md)

[Copy a threshold](../task/copy-thresholds.md)

