---
title: Calculated metric definition form
description: The fields of the calculated metric definition form are explained in this topic.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Create a calculated metric definition, Configure, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Calculated metric definition form

The fields of the calculated metric definition form are explained in this topic.

<table id="table_calculated-md-reuse"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Basic details

</td></tr><tr><td>

Name

</td><td>

Name of the calculated metric definition. For example, `Number of employees`.

</td></tr><tr><td>

Active

</td><td>

Option to mark the calculated metric definition as active.

</td></tr><tr><td>

Description

</td><td>

Brief description of the calculated metric definition.

</td></tr><tr><td>

Unit

</td><td>

Unit for the metric definition. You can define the units in which the scores are shown. The most commonly used units are provided by default.

</td></tr><tr><td>

Calendar

</td><td>

Calendar to use for metric aggregation. Only the configured calendar options are available for selection. This field is automatically set to **Standard Calendar**. **Note:** Standard calendar refers to the Gregorian calendar.

</td></tr><tr><td>

Precision

</td><td>

Number of decimal places after the decimal point on a score. This field is automatically set to **0**.

 When the Precision is set to 0, the result is rounded to the nearest whole number. For example, if a metric definition with Precision 0 calculates the values 7 + \(5 / 2\), the result rounds up to 10.

 When the Precision is set to greater than 0, the result is rounded to the nearest decimal point for the given precision. For example, Precision 1 rounds a result of 4.45 as 4.5.

</td></tr><tr><td>

Frequency

</td><td>

Frequency for the calculated metric definition. This field indicates how often the metric definition should roll up the scores. The choices are as follows:-   **Daily**
-   **Weekly**
-   **Monthly**
-   **Quarterly**
-   **Semi-annually**
-   **Annually**

</td></tr><tr><td class="sub-head" colspan="2">

Calculation

</td></tr><tr><td>

Calculation level

</td><td>

Level at which the calculation is performed. The choices are as follows:-   **Metric definition**: If you calculate the data at the metric definition level, then the data across all child metric definitions or child metrics is used for calculation.
-   **Entity**: If you calculate data at the entity level and specify the calculation method using the formula builder, then the common entities across all the child metric definitions are matched and the data is calculated for each entity. To aggregate the data to get an overall score at the metric definition level, select **Entity**.

</td></tr><tr><td>

Aggregation method

</td><td>

Method to aggregate the metric score at the entity level. The choices are as follows:-   **None**
-   **Sum**
-   **Average**
-   **Maximum**
-   **Minimum**

This field appears only when the **Calculation level** field is set to **Entity**.

</td></tr><tr><td class="sub-head" colspan="2">

Metric Properties

</td></tr><tr><td>

Enterprise Owner Type

</td><td>

Type of enterprise owner responsible for the calculated metric definition. The available options are:-   **User**
-   **User group**

</td></tr><tr><td>

Enterprise owner

</td><td>

Individual responsible for the metric definition.**Note:** This field appears only when the **Enterprise Owner Type** field is set to **User**.

</td></tr><tr><td>

Enterprise owner group

</td><td>

Group responsible for the metric definition.**Note:** This field appears only when the **Enterprise Owner Type** field is set to **User group**.

</td></tr><tr><td>

Direction

</td><td>

Direction that you want to see the metric in. The choices are as follows:-   **None**: If you don’t want any change in the metric direction, select this option.
-   **Minimize**: If the desired metric direction is downward or descending, select this option. For example, minimize the number of risks assessments that remain open beyond their due date.
-   **Maximize**: If the desired metric direction is upward or ascending, select this option. For example, you want to maximize the number of critical controls.
-   **Milestone**: Option to select when the metric direction is not applicable, but the metric is tracked against a milestone. For example, if your organization has a goal to complete all the risk assessments for an entity by the end of the month, the upcoming date for the goal is considered as a milestone.

**Note:** Thresholds can be set for all directions excluding **Milestone**. For more information on creating thresholds, see [Create a threshold for a metric](../task/t_create-threshold-for-metrics.md).

</td></tr><tr><td>

Nature

</td><td>

Nature of the manual metric definition. The choices are as follows:-   **Leading**: A leading metric is predictive and helps anticipate future risk outcomes. For example, an organization may use a leading metric such as the percentage increase in control failures within critical processes. By monitoring early signs of control degradation, the organization can predict a potential rise in operational or compliance risk. Tracking this metric enables risk teams to proactively identify emerging risk exposure and take preventive actions before the risk materializes or exceeds defined risk tolerance.
-   **Lagging**: A lagging metric measures the impact of past risk events or actions. For example, a lagging metric could be the number of risk events that resulted in financial loss or regulatory penalties during a reporting period. This metric provides visibility into the organization’s historical risk impact. By tracking this metric over time, risk teams can assess how effective past risk mitigation and control efforts have been and identify patterns that require corrective action. Lagging metrics help evaluate outcomes after risks have materialized and support improvements to future risk strategies.
-   **Current**: A current metric monitors active risk exposure across operations. For example, the number of active operational risks rated as high or very high helps organizations understand their present risk posture. Monitoring this metric enables risk owners to focus on high-exposure areas and initiate mitigation actions in real time.

</td></tr><tr><td>

Group

</td><td>

Area that the metric relates to. For example, the metric may be related to the stress indicators, failure indicators, and so on.

</td></tr><tr><td>

Reporting classification

</td><td>

Tag used to categorize the metric.

</td></tr><tr><td>

Subgroup

</td><td>

Subgroup that the metric relates to.

</td></tr><tr><td>

Key metric

</td><td>

Option to indicate if it’s a key metric for your business.

</td></tr><tr><td class="sub-head" colspan="2">

Confidentiality

</td></tr><tr><td colspan="2">

**Note:** This section only appears if the following situations are true:

-   The **sn\_grc.enable\_record\_confidentiality** property is enabled under GRC properties.
-   The record is in Draft state.

</td></tr><tr><td>

Confidential

</td><td>

Option to mark the record as confidential.

</td></tr><tr><td>

Allowed users

</td><td>

Users who can view the record.**Note:** By default, the logged-in user is added to the list of confidential users.

</td></tr><tr><td>

Allowed groups

</td><td>

Groups that can view the record.

</td></tr></tbody>
</table>**Parent Topic:**[Create a calculated metric definition](../task/t_create-composite-metric-definition.md)

