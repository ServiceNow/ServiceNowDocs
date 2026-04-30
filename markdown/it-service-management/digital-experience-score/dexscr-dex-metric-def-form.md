---
title: Metric definition form
description: Update the scoring details of a metric definition, enable or disable it, or specify whether it contributes to the overall DEX score.
locale: en-US
release: zurich
product: Digital Experience Score
classification: digital-experience-score
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Digital Experience Score, Digital End-User Experience, IT Service Management]
---

# Metric definition form

Update the scoring details of a metric definition, enable or disable it, or specify whether it contributes to the overall DEX score.

For more information, see [Customize metric definitions](../task/dexscr-customize-dex-score-metric-defs.md).

<table id="table_fr4_1dn_jhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contributes to DEX score

</td><td>

Option to determine whether the metric can contribute to the overall DEX score.

</td></tr><tr><td>

Value type

</td><td>

Value type of the metric that can be either qualitative or quantitative, depending on how it’s measured and what type of data it collects.-   Quantitative metrics evaluate scores using numbers. For example, the CPU usage or battery health of a device.
-   Qualitative metrics evaluate scores using descriptive information instead of numbers. For example, the information you collect from surveys can provide details on how employees feel about using a particular device or application.

</td></tr><tr><td>

Active

</td><td>

Option to make the metric definition active. Only active metrics are considered for calculations and aggregations.

</td></tr><tr><td>

Good lower bound

</td><td>

Minimum value for a good metric.For example, let's say the good lower bound for a customer satisfaction metric score is set to 80%. This value means that any score more than 80% is considered good.

</td></tr><tr><td>

Average lower bound

</td><td>

Minimum value for an average metric.For example, let's say the average lower bound for a CPU usage metric score is set to 85 and its upper bound is set to 55. This value means that any score between 85 and 55 is considered average.

</td></tr><tr><td>

Poor lower bound

</td><td>

Minimum value for a poor metric.For example, let's say the poor lower bound for a device crash metric score is set to 5 and its upper bound is set to 2. This value means that any score \(number of times a device crashed\) between 5 and 2 is considered poor.

</td></tr><tr><td>

Max upper bound

</td><td>

Maximum value that is considered as the upper bound for the metric definition.

</td></tr><tr><td>

Weight

</td><td>

Weighted average for the metric that contributes to the overall DEX score.

</td></tr></tbody>
</table>**Parent Topic:**[Digital Experience Score​ reference](../concept/dexscr-dex-score-reference.md)

