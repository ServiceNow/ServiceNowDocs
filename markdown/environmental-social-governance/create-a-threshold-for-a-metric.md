---
title: Create a threshold for a metric
description: Create thresholds such as amber threshold and red threshold for metrics and metric definitions. Thresholds refer to predetermined values used to assess the performance of a metric. These thresholds are typically defined based on specific criteria or objectives and serve as reference points to determine whether the measured value or performance meets, exceeds, or falls below the desired level.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Environmental, Social, and Governance Management]
---

# Create a threshold for a metric

Create thresholds such as amber threshold and red threshold for metrics and metric definitions. Thresholds refer to predetermined values used to assess the performance of a metric. These thresholds are typically defined based on specific criteria or objectives and serve as reference points to determine whether the measured value or performance meets, exceeds, or falls below the desired level.

## Before you begin

Role required: en\_esg.metric.admin

## Procedure

1.  Navigate to **All** &gt; **Environmental, Social, and Governance** &gt; **ESG Workspace** &gt; **Metrics**.

2.  Open the quantitative metric definition for which you want to add thresholds.

3.  Select the Thresholds related list.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_xp1_3c5_txb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Threshold type

</td><td>

Type of threshold. The choices are the following.-   Static: A static threshold for a metric or a metric definition refers to a fixed value used as a limit for tracking a metric.
-   Dynamic: Dynamic thresholds are specified in percentages. This means that the percentage variance is calculated based on two factors: direction and the previous data
For more information, see [Thresholds for metrics](../concept/thresholds-for-metrics.md)

</td></tr><tr><td>

Amber threshold

</td><td>

Percentage value that signifies moderate change in the variance of target value.

</td></tr><tr><td>

Valid from

</td><td>

Date the data is valid from.

</td></tr><tr><td>

Target value

</td><td>

Previous data against which the percentage variance is compared.

</td></tr><tr><td>

Red threshold

</td><td>

Percentage value that signifies critical change in the variance of target value.

</td></tr><tr><td>

Valid until

</td><td>

Date the data is valid until.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  To copy the thresholds to the metrics, select **Copy threshold**.


**Parent Topic:**[Configuring GRC: Metrics](../concept/configuring-grc-metrics.md)

