---
title: Manual metric definition fields
description: Detailed explanation of the fields on the manual metric definition form.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Create a manual metric definition, Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Manual metric definition fields

Detailed explanation of the fields on the manual metric definition form.

<table id="table_lrv_yw4_brb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Basic details

</td></tr><tr><td>

Name

</td><td>

Name of the manual metric definition. For example, `Number of incidents`.

</td></tr><tr><td>

Active

</td><td>

Option to mark the manual metric definition as active.

</td></tr><tr><td>

Description

</td><td>

Brief description of the manual metric definition.

</td></tr><tr><td>

Category

</td><td>

Category of the metrics data. The choices are as follows:-   **Qualitative**: Qualitative data is intangible and non-numerical in nature. It’s defined by the characteristics of a process or business activity.
-   **Quantitative**: Quantitative data is tangible and numerical in nature. It’s defined by the numbers or key performance indicators.

**Note:** This fields **Nature**, **Direction**, **Precision**, and **Unit** are only displayed only when the category of the manual metric definition is **Quantitative**.

</td></tr><tr><td>

Calendar

</td><td>

Calendar to use for metric aggregation. Only the configured calendar options are available for selection. This field is automatically set to **Standard Calendar**. **Note:** Standard calendar refers to the Gregorian calendar.

</td></tr><tr><td>

Aggregation method

</td><td>

Method used to calculate the metric data for all the entities. For example, if you have a metric that you want to measure for multiple entities such as people, departments, or regions, you might want to know how to calculate the scores for each entity into a single score that represents the overall performance. Your choice of aggregation method depends on your goal of metric collection. For example, if you’re interested in overall performance and want to account for differences in scale or size between entities, the sum or average may be more appropriate. If you’re interested in identifying the best-performing entity, the maximum may be more appropriate, while if you’re interested in identifying the worst-performing entity, the minimum may be more appropriate. The aggregation happens across time periods based on the frequency defined in the metric definition. If the frequency is monthly, the calculation takes place every month. The four choices for aggregation methods are as follows:-   **Sum**: The metric data for all entities are added together to create a single score.
-   **Average**: The metric data for all entities are averaged to create a single score.
-   **Maximum**: The highest metric data among all entities is used as the single score.
-   **Minimum**: The lowest metric data among all entities is used as the single score.

</td></tr><tr><td>

Unit

</td><td>

Unit for the manual metric definition.

</td></tr><tr><td>

Precision

</td><td>

Number of decimal places after the decimal point on a score. This field is automatically set to **0**.

 When the Precision is set to 0, the result is rounded to the nearest whole number. For example, if a metric definition with Precision 0 calculates the values 7 + \(5 / 2\), the result rounds up to 10.

 When the Precision is set to greater than 0, the result is rounded to the nearest decimal point for the given precision. For example, Precision 1 rounds a result of 4.45 as 4.5.

</td></tr><tr><td>

Frequency

</td><td>

Frequency at which the metric definition should collect the scores. The choices are as follows:-   **Daily**
-   **Weekly**
-   **Monthly**
-   **Quarterly**
-   **Semi-annually**
-   **Annually**

</td></tr><tr><td>

First run date

</td><td>

Start date of the metric definition execution for the collection of data according to the frequency.

</td></tr><tr><td class="sub-head" colspan="2">

Data collection

</td></tr><tr><td>

Data owner assignment type

</td><td>

Type of the data owner assignment for the metrics within the metric definition. The choices are as follows:-   **Simple**

The system assigns the specified Data owner or Data owner group to the Metric.

-   **Advanced**

The system assigns a Data owner based on the assignment configuration. ESG admins \[sn\_esg.admin\] or Risk admins \[sn\_risk.admin\] can set assignment configurations to dynamically assign data owners. For more information on creating assignment configurations see, [Create an assignment configuration](../task/create-assign-config-mmd.md) and Assignment Configuration New Record.

**Note:** This is available if you have the GRC: Approver Configurator application installed. For more information see, Using Approver Configurator for setting up approvals.


</td></tr><tr><td>

Data owner type

</td><td>

Type of the data owner responsible for the manual metric definition. The choices are as follows:-   **User**
-   **User group**

</td></tr><tr><td>

Data owner

</td><td>

Data owner responsible for the manual metric definition. Select a data owner from the list.**Note:** If you selected the advanced option for **Data owner assignment type**, this will be the assigned data owner if the assignment configuration doesn’t return any results.

</td></tr><tr><td>

Result type

</td><td>

The format that you want to be available for responses in assigned metric data tasks. This applies to responses and overridden responses.-   Text: Users can enter a plain text response.
-   HTML: Users can enter HTML code as a response.
-   Choice: Users can select a choice from a list.

This field appears when the **Category** field is set to **Qualitative**.

</td></tr><tr><td>

Choice table

</td><td>

Table the choices are being populated from. This field appears when the **Category** field is set to **Qualitative**.

</td></tr><tr><td>

Choice field

</td><td>

Field and its values from the selected table that are displayed for each choice. This field appears when the **Category** field is set to **Qualitative**.

</td></tr><tr><td>

Choice condition

</td><td>

Option to only show certain fields or certain values within the Choice field under set conditions. Select **Set conditions** to open the condition builder. This field appears when the **Category** field is set to **Qualitative**.

</td></tr><tr><td>

Instructions

</td><td>

Instructions for the data owner. Method of collection for the manual metric definition.

</td></tr><tr><td>

Approval required

</td><td>

Option to indicate if an approval is required for the manual metric definition.**Note:** When the **Approval required** option is enabled, the **Approver type** and **Approver** fields are displayed.

</td></tr><tr><td>

Approver type

</td><td>

Type of the approver of the metric definition. The choices are as follows:-   **User**
-   **User group**

**Note:** This field appears only when the Metric approval property is set to **Simple**. For more information see, [Components installed with Operational Sustainability Management \(formerly ESG Management\)](../../esg-management-reporting/reference/components-installed-with-esg.md).

</td></tr><tr><td>

Approver

</td><td>

Approver user or approver group that is responsible to approve the metric definition. The choices are as follows:-   **Approver**: Displayed when the User option is selected.
-   **Approver group**: Displayed when the User option is selected.

**Note:** This field appears only when the Metric approval property is set to **Simple**. For more information see, [Components installed with Operational Sustainability Management \(formerly ESG Management\)](../../esg-management-reporting/reference/components-installed-with-esg.md).

</td></tr><tr><td class="sub-head" colspan="2">

Metric Properties

</td></tr><tr><td>

Type

</td><td>

Method used to determine if the score is collected manually or in an automated manner. The choices are as follows:-   **Automated**
-   **Manual**

 Select **Manual**.

</td></tr><tr><td>

Enterprise Owner Type

</td><td>

Type of enterprise owner responsible for the manual metric definition. The choices are as follows:-   **User**
-   **User group**

</td></tr><tr><td>

Direction

</td><td>

Direction that you want to see the metric in. The choices are as follows:-   **None**: If you don’t want any change in the metric direction, select this option.
-   **Minimize**: If the desired metric direction is downward, select this option.
-   **Maximize**: If the desired metric direction is upward, select this option.
-   **Milestone**: When the metric direction isn’t applicable, but the metric is tracked against a milestone, select this option.

**Note:** Thresholds can be set for all directions excluding **Milestone**. For more information on creating thresholds, see [Create a threshold for a metric](../task/create-a-threshold-for-a-metric.md)

</td></tr><tr><td>

Group

</td><td>

Area that the metric relates to.

</td></tr><tr><td>

Reporting classification

</td><td>

Tag used to categorize the metric.

</td></tr><tr><td>

Due date offset

</td><td>

Number of days after the schedule end date when the metric data task becomes overdue. For example, if the frequency of a metric definition is monthly and if you enter `15` in this field, then the due date for metric data task will be overdue 15 days after the month ends.

</td></tr><tr><td>

Enterprise owner

</td><td>

Enterprise owner of the manual metric definition.

</td></tr><tr><td>

Nature

</td><td>

Nature of the manual metric definition. The choices are as follows:-   **None**: If you don’t want any change in the metric direction, select this option.
-   **Leading** \(Predictive\) Metric: Is predictive and helps anticipate future outcomes. In this case, the company may use a leading metric related to GHG emissions, such as the amount of energy consumed per production unit. By tracking energy consumption, the company can predict its future GHG emissions based on the energy sources used and the efficiency of its production processes. This leading metric enables the company to proactively identify areas for improvement and make informed decisions to reduce emissions.
-   **Lagging** \(Measures Impact\) Metric: Measures the impact of past actions or events. In the example, a lagging metric related to GHG emissions could be the total emissions produced by the company in a given year. This metric provides an assessment of the company's historical sustainability impact. By monitoring this metric over time, the company can evaluate the effectiveness of its emission reduction efforts and identify areas where further improvements are needed. Lagging metrics help measure the outcomes of past actions and inform future strategies.
-   **Current** metric: Monitors ongoing processes and identifies real-time improvement areas. For GHG emissions, a current metric could be the emissions intensity, which measures the emissions generated per unit of production. By tracking emissions intensity, the company can identify specific areas within its operations that contribute to higher emissions. This metric helps the company identify real-time improvement opportunities, such as optimizing energy usage, implementing energy-efficient technologies, or adopting renewable energy sources.

</td></tr><tr><td>

Subgroup

</td><td>

Subgroup that the metric relates to

</td></tr><tr><td>

Key metric

</td><td>

Option to indicate if it’s a key metric for your business.

</td></tr><tr><td class="sub-head" colspan="2">

Confidentiality

</td></tr><tr><td colspan="2">

**Note:** This section only appears when:

-   The **sn\_grc.enable\_record\_confidentiality** property is enabled under GRC properties.
-   The record is in **Draft** state.

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
</table>**Parent Topic:**[Create a manual metric definition](../task/create-manual-metric-definition.md)

