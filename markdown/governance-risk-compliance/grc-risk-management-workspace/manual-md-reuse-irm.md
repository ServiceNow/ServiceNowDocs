---
title: Create New Metric Definition form
description: Detailed explanation of the fields on the manual metric definition form.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Create a manual metric definition, Configuring metrics, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Create New Metric Definition form

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

Unit

</td><td>

Unit for the manual metric definition.

</td></tr><tr><td>

Aggregation method

</td><td>

Method used to calculate the metric data for all the entities. For example, if you have a metric that you want to measure for multiple entities such as people, departments, or regions. You want to know how to calculate the scores for each entity into a single score that represents the overall performance. Your choice of aggregation method depends on your goal of metric collection. For example, if you’re interested in overall performance and want to account for differences in scale or size between entities, the sum or average is more appropriate. If you’re interested in identifying the best-performing entity, the maximum may be more appropriate, while if you’re interested in identifying the worst-performing entity, the minimum may be more appropriate. The aggregation happens across time periods based on the frequency defined in the metric definition. If the frequency is monthly, the calculation takes place every month. The four choices for aggregation methods are as follows:-   **Sum**: The metric data for all entities are added together to create a single score.
-   **Average**: The metric data for all entities are averaged to create a single score.
-   **Maximum**: The highest metric data among all entities is used as the single score.
-   **Minimum**: The lowest metric data among all entities is used as the single score.

</td></tr><tr><td>

Precision

</td><td>

Number of decimal places after the decimal point on a score. This field is automatically set to **0**.

 When the Precision is set to 0, the result is rounded to the nearest whole number. For example, if a metric definition with Precision 0 calculates the values 7 + \(5 / 2\), the result rounds up to 10.

 When the Precision is set to greater than 0, the result is rounded to the nearest decimal point for the given precision. For example, Precision 1 rounds a result of 4.45 as 4.5.

</td></tr><tr><td>

Class

</td><td>

Class to which the metric definition belongs. The choices are as follows:-   **KPI**: Indicates how well the risk exposure is managed against objectives. Use this option to add entities and additional entities to the metric definition.
-   **KRI**: Indicates the amount of exposure to a given risk or set of risks. Use this option to add risks and risk statements to the metric definition. This option is available if the Advanced Risk plugin is activated.
-   **KCI**: Indicates the effectiveness of any controls that have been implemented to reduce or mitigate a given risk exposure. Use this option to add controls and control objectives to the metric definition. This option is available if the Policy and Compliance Management plugin is activated.

**Important:** This field appears only when the metric definition is created from the IRM suite of applications. It doesn’t appear for Operational Sustainability Management.

</td></tr><tr><td>

Calendar

</td><td>

Calendar to use for metric aggregation. Only the configured calendar options are available for selection. This field is automatically set to **Standard Calendar**. **Note:** Standard calendar refers to the Gregorian calendar.

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

Type of the data owner assignment for the metrics within the metric definition. The choices are as follows:-   **Simple**: The system assigns the specified Data owner or Data owner group to the Metric.
-   **Advanced**: The system assigns a Data owner based on the assignment configuration. Risk admins \[sn\_risk.admin\] can set assignment configurations to dynamically assign data owners. For more information on creating assignment configurations, see [Create an assignment configuration](../task/create-assign-config-mmd-irm.md) and [Assignment Configuration New Record](../../grc-common/reference/assignment-configuration-new-record.md).

**Note:** This is available if you have the GRC: Approver Configurator application installed. For more information see, [Using Approver Configurator for setting up approvals](../../grc-common/concept/approval-configuration.md).


</td></tr><tr><td>

Data owner type

</td><td>

Type of the data owner responsible for the manual metric definition. The choices are as follows:-   **User**
-   **User group**

</td></tr><tr><td>

Data owner

</td><td>

Data owner responsible for the manual metric definition.**Note:** If you selected the advanced option for **Data owner assignment type**, this will be the assigned data owner if the assignment configuration doesn’t return any results.

</td></tr><tr><td>

Result type

</td><td>

The format that you want to be available for responses in assigned metric data tasks. This applies to responses and overridden responses.-   **Text**: Users can enter a plain text response.
-   **HTML**: Users can enter HTML code as a response.
-   **Choice**: Users can select a choice from a list.

This field appears when the **Category** field is set to **Qualitative**.

</td></tr><tr><td>

Choice table

</td><td>

Table the choices are being populated from. This field appears when the **Result type** field is set to **Choice**.

</td></tr><tr><td>

Choice field

</td><td>

Field and its values from the selected table that are displayed for each choice. This field appears when the **Result type** field is set to **Choice**.

</td></tr><tr><td>

Choice condition

</td><td>

Option to only show certain fields or certain values within the Choice field under set conditions. Select **Set conditions** to open the condition builder. This field appears when the **Result type** field is set to **Choice**.

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

**Note:** This field appears only when the **Approval required** option is selected.

</td></tr><tr><td>

Approver

</td><td>

User or group that is responsible approving the metric definition.**Note:** This field appears only when the **Approval required** option is selected.

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
-   **Minimize**: If the desired metric direction is downward or descending, select this option. For example, minimize the number of risks assessments that remain open beyond their due date.
-   **Maximize**: If the desired metric direction is upward or ascending, select this option. For example, you want to maximize the number of critical controls.
-   **Milestone**: Option to select when the metric direction is not applicable, but the metric is tracked against a milestone. For example, if your organization has a goal to complete all the risk assessments for an entity by the end of the month, the upcoming date for the goal is considered as a milestone.

**Note:** Thresholds can be set for all directions excluding **Milestone**. For more information on creating thresholds, see [Create a threshold for a metric definition](../task/t_create-threshold-for-metrics.md).

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

Nature of the manual metric definition. The choices are as follows:-   **Leading**: A leading metric is predictive and helps anticipate future risk outcomes. For example, an organization may use a leading metric such as the percentage increase in control failures within critical processes. By monitoring early signs of control degradation, the organization can predict a potential rise in operational or compliance risk. Tracking this metric enables risk teams to proactively identify emerging risk exposure and take preventive actions before the risk materializes or exceeds defined risk tolerance.
-   **Lagging**: A lagging metric measures the impact of past risk events or actions. For example, a lagging metric could be the number of risk events that resulted in financial loss or regulatory penalties during a reporting period. This metric provides visibility into the organization’s historical risk impact. By tracking this metric over time, risk teams can assess how effective past risk mitigation and control efforts have been and identify patterns that require corrective action. Lagging metrics help evaluate outcomes after risks have materialized and support improvements to future risk strategies.
-   **Current**: A current metric monitors active risk exposure across operations. For example, the number of active operational risks rated as high or very high helps organizations understand their present risk posture. Monitoring this metric enables risk owners to focus on high-exposure areas and initiate mitigation actions in real time.

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
</table>**Parent Topic:**[Create a manual metric definition](../task/t_create-manual-metric-definition.md)

