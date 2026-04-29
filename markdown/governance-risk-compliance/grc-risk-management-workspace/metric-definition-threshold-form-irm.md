---
title: Metric Definition Threshold form
description: Use the Metric Definition Threshold form to define performance limits for a metric and control how the system responds when those limits are reached.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a threshold for a metric definition, Configuring metrics, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Metric Definition Threshold form

Use the Metric Definition Threshold form to define performance limits for a metric and control how the system responds when those limits are reached.

<table id="table_xp1_3c5_txb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the threshold.

</td></tr><tr><td>

Metric

</td><td>

Metric to which the threshold applies. This field is pre-populated based on the metric you opened.

</td></tr><tr><td>

Threshold type

</td><td>

Type of threshold. The available options are:-   **Static**: A fixed value used as a limit for tracking a metric.
-   **Dynamic**: Percentage-based thresholds where variance is calculated based on metric direction and previous period data.

For more information, see [Thresholds in Integrated Risk Management](../concept/thresholds-in-irm.md).

</td></tr><tr><td>

Color

</td><td>

Color that represents this threshold level. The available color list can be customized, and each threshold level must have a unique color.

</td></tr><tr><td>

Valid from

</td><td>

Date from which the threshold configuration is valid.

</td></tr><tr><td>

Valid until

</td><td>

Date until the threshold configuration is valid.

</td></tr><tr><td>

Active

</td><td>

Option that Indicates whether the threshold is active.

</td></tr><tr><td>

Enable threshold breach monitoring

</td><td>

Option that indicates whether the system monitors and immediately triggers actions when the threshold is breached.

</td></tr><tr><td>

Condition

</td><td>

Conditions that determine when the threshold applies.

</td></tr><tr><td>

Actions

</td><td>

Actions to execute when the threshold is exceeded. Available actions include Send email and create issue.

</td></tr></tbody>
</table>**Parent Topic:**[Create a threshold for a metric definition](../task/t_create-threshold-for-metrics.md)

