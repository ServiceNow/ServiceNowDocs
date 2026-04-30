---
title: Normalized value for an assessment
description: The normalized value is calculated based on a linear equation and the scale definition of the metric. This value can be used for risk assessment.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Metric Result form, Surveys reference, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Normalized value for an assessment

The normalized value is calculated based on a linear equation and the scale definition of the metric. This value can be used for risk assessment.

## Normalized value for any metric

The normalized value is directly proportional to the scale definition of the metric. If the scale definition is low, that is, the lower scale values are better, then `Normalized value = 1.0 – Normalized value`.

For the reporting purpose, use the Metric Result \[asmt\_metric\_result\] table.

`Normalized value = (Input Value - Min value defined in metric) / (Max value defined in metric - Min value defined in metric) * (current metric weight * bias / (sum of all metric weight in the metric category)) * scale_factor`

Bias is the ratio of total metric weight in the category and the sum of valid metric weight in the metric category. While calculating bias, the scripted metrics are excluded.

**Note:**

-   If a metric is skipped when taking the assessment, its weight is excluded when calculating `sum of valid metric weight in the metric category`.
-   The following metric types are excluded in the normalized value calculation:
    -   String
    -   Date
    -   Date/Time
    -   Reference
    -   Attachment
    -   Ranking

For example, consider the following scenario.

Calculate the normalized value for the **Please rate the competency of the technician** metric.

<table id="table_dpr_cyt_zz"><tbody><tr><td>

Input value

</td><td>

3

</td></tr><tr><td>

Minimum value

</td><td>

1

</td></tr><tr><td>

Maximum value

</td><td>

6

</td></tr><tr><td>

Current metric weight

</td><td>

10

</td></tr><tr><td>

Number of metrics in the metric category

</td><td>

6-   4 of type=number
-   1 of type=yes/no
-   1 of type=string \(invalid data type; value cannot be calculated\)

</td></tr><tr><td>

Valid metric weight of each response

</td><td>

10

</td></tr><tr><td>

Scale factor

</td><td>

10

</td></tr></tbody>
</table>`Normalized value = (3 - 1) / (6 - 1) * (10 / (10 + 10 + 10 + 10 + 10)) * 10 = 0.8`

## Normalized value for a multiple selection metric

The normalized value for a multiple selection metric is calculated by using the weight of the metric and the score for each choice of the metric.

In a multiple selection metric, for each choice that should be used for the normalization calculation, define the normalization input value.

`Normalized value = (Score of all choices) * (current metric weight / (sum of valid metric weight in the metric category)) * scale_factor`

Here, score of all choices of the metric is the sum of individual scores of each choice.

-   `Score of each choice in a multiple selection metric= Normalization input of the choice / max value of the metric`
-   `max value of the metric = Sum of the normalization input for all choices of the metric`
-   `min value of the metric is always 0`

For example, consider the following scenario.

Calculate the normalized value for the multiple selection metric, **Please rate the competency of the technician**, with three choices, A, B, and C.

<table id="table_gqq_c1w_3kb"><tbody><tr><td>

Choice A

</td><td>

Normalization input is 1

</td></tr><tr><td>

Choice B

</td><td>

Normalization input is 1

</td></tr><tr><td>

Choice C

</td><td>

Normalization input is 2

</td></tr><tr><td>

Minimum value

</td><td>

0

</td></tr><tr><td>

Maximum value

</td><td>

4

</td></tr><tr><td>

Current metric weight

</td><td>

10

</td></tr><tr><td>

Number of metrics in the metric category

</td><td>

5

</td></tr><tr><td>

Valid metric weight of each metric

</td><td>

10

</td></tr><tr><td>

Scale factor

</td><td>

10

</td></tr></tbody>
</table>If Choice A and B are selected, `Normalized value = ((1 / 4) + (1 / 4)) * (10 / (10 + 10 + 10 + 10 + 10)) * 10 = 1`

## Weighted value for a risk assessment

For a risk assessment, the weighted value from metric results table is calculated as following.

`weighted_value = metric.weight * result.actual_value`

**Parent Topic:**[Metric Result form](../../survey-administration/reference/r_MetricResultFieldNames.md)

