---
title: Create a threshold for a metric definition
description: Evaluate the performance of your quantitative metric definition by defining threshold for your metric definitions.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring metrics, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Create a threshold for a metric definition

Evaluate the performance of your quantitative metric definition by defining threshold for your metric definitions.

## Before you begin

Role required: admin

## About this task

After you create a metric definition, you can define threshold limits for a metric and a metric definition to determine the performance of the metric. When the threshold value is breached or crossed, the system notifies the relevant owners. For example, you can create a metric definition to monitor employee attrition and define your target value for the metric, the amber threshold value and the red threshold value for a specified period. Now, consider that you defined your threshold value as 5, and your amber value as 8, and your red value as 10. This means that when there is an attrition of 8 people, the system will notify you about the metric performance as Amber. If your attrition reaches 10, the system will notify you about the metric performance as Red. This notification will enable you to take appropriate actions. You can create more than one threshold for a metric. If a threshold is defined before the metric is created, then the metrics inherit the rules of the threshold. You can create thresholds for all types of metric definitions. In this procedure, automated metric definition is used as an example.

If the threshold is created after the metric definition is created, you can copy the thresholds to the metrics.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace** &gt; **Metrics** &gt; **Metrics**.

2.  Select and open the metric for which you want to define the threshold.

3.  Select the Thresholds related list.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_ddc_1kp_nsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Threshold type

</td><td>

Type of threshold. The choices are the following.-   Static: A static threshold for a metric or a metric definition refers to a fixed value used as a limit for tracking a metric.
-   Dynamic: Dynamic thresholds are specified in percentages. This means that the percentage variance is calculated based on two factors: direction and the previous data
For more information, see [Thresholds for metrics](https://www.servicenow.com/docs/access?context=thresholds-for-metrics&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US).

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
</table>6.  Select **Submit**.

7.  To copy the thresholds to the metrics, select **Copy threshold**.


-   **[Metric Definition Threshold form](../reference/metric-definition-threshold-form-irm.md)**  
Use the Metric Definition Threshold form to define performance limits for a metric and control how the system responds when those limits are reached.

**Parent Topic:**[Configuring metrics](../concept/configuring-irm-metrics.md)

