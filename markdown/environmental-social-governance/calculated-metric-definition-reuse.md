---
title: Calculated metric definition form
description: The fields of the calculated metric definition form are explained in this topic.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Create a calculated metric definition, Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
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

Precision

</td><td>

Number of decimal places after the decimal point on a score. This field is automatically set to **0**.

 When the Precision is set to 0, the result is rounded to the nearest whole number. For example, if a metric definition with Precision 0 calculates the values 7 + \(5 / 2\), the result rounds up to 10.

 When the Precision is set to greater than 0, the result is rounded to the nearest decimal point for the given precision. For example, Precision 1 rounds a result of 4.45 as 4.5.

</td></tr><tr><td>

Calendar

</td><td>

Calendar to use for metric aggregation. Only the configured calendar options are available for selection. This field is automatically set to **Standard Calendar**. **Note:** Standard calendar refers to the Gregorian calendar.

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

This field only appears when the **Calculation level** field is set to **Entity**.

</td></tr><tr><td class="sub-head" colspan="2">

Metric Properties

</td></tr><tr><td>

Enterprise Owner Type

</td><td>

Enterprise owner responsible for the calculated metric definition. The choices are as follows:-   **User**
-   **User group**

</td></tr><tr><td>

Enterprise owner

</td><td>

Enterprise owner of the metric definition.

</td></tr><tr><td>

Direction

</td><td>

Direction that you want to see the metric in. The choices are as follows:-   **None**: If you do not want any change in the metric direction, select this option.
-   **Minimize**: If the desired metric direction is downward, select this option. For example, if you want to minimize the carbon emission from the datacenters.
-   **Maximize**: If the desired metric direction is upward, select this option. For example, if you want to maximize the use of energy-efficient resources in your organization.
-   **Milestone**: When the metric direction is not applicable, but the metric is tracked against a milestone, select this option. For example, if your organization has a goal to use 100% renewable energy by the end of 2029, the upcoming date for the goal is considered as a milestone.

</td></tr><tr><td>

Nature

</td><td>

Nature of the calculated metric definition. The choices are as follows:-   **None**:
-   **Leading** \(Predictive\) Metric: Is predictive and helps anticipate future outcomes. In this case, the company may use a leading metric related to GHG emissions, such as the amount of energy consumed per production unit. By tracking energy consumption, the company can predict its future GHG emissions based on the energy sources used and the efficiency of its production processes. This leading metric enables the company to proactively identify areas for improvement and make informed decisions to reduce emissions.
-   **Lagging** \(Measures Impact\) Metric: Measures the impact of past actions or events. In our example, a lagging metric related to GHG emissions could be the total emissions produced by the company in a given year. This metric provides an assessment of the company's historical environmental impact. By monitoring this metric over time, the company can evaluate the effectiveness of its emission reduction efforts and identify areas where further improvements are needed. Lagging metrics help measure the outcomes of past actions and inform future strategies.
-   **Current** metric: Monitors ongoing processes and identifies real-time improvement areas. For GHG emissions, a current metric could be the emissions intensity, which measures the emissions generated per unit of production. By tracking emissions intensity, the company can identify specific areas within its operations that contribute to higher emissions. This metric helps the company identify real-time improvement opportunities, such as optimizing energy usage, implementing energy-efficient technologies, or adopting renewable energy sources.

</td></tr><tr><td>

Group

</td><td>

Area that the metric relates to. For example, the,metric may be related to the area of energy, water emissions, and so on.

</td></tr><tr><td>

Reporting classification

</td><td>

Tag used to categorise the metric.

</td></tr><tr><td>

Subgroup

</td><td>

Subgroup that the metric relates to.

</td></tr><tr><td>

Key metric

</td><td>

Option to indicate if it is a key metric for your business.

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

Users who can view the record.**Note:** By default, the logged in user is added to the list of confidential users.

</td></tr><tr><td>

Allowed groups

</td><td>

Groups that can view the record.

</td></tr></tbody>
</table>**Parent Topic:**[Create a calculated metric definition](../task/create-composite-metric-definition.md)

