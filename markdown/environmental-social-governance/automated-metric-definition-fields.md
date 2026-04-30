---
title: Automated metric definition fields
description: The fields of the automated metric definition form are explained in this topic.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Create an automated metric definition, Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Automated metric definition fields

The fields of the automated metric definition form are explained in this topic.

<table id="table-create-metric"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Basic details

</td></tr><tr><td>

Name

</td><td>

Name of the automated metric definition. For example, `Number of incidents`.

</td></tr><tr><td>

Active

</td><td>

Option to mark the automated metric definition as active. When enabled, the metric definition becomes active and ready for use.

</td></tr><tr><td>

Description

</td><td>

Brief description of the automated metric definition.

</td></tr><tr><td>

Unit

</td><td>

Unit for the automated metric definition. You can define the units in which the data is shown.

</td></tr><tr><td>

Aggregation method

</td><td>

The Aggregation method refers to the method used to calculate the metric data for all the entities. For example, if you have a metric that you want to measure for multiple entities such as people, departments, or regions, you might want to know how to calculate the data for each entity into a single score that represents the overall performance. Your choice of aggregation method depends on your goal of metric collection. For example, if you are interested in overall performance and want to account for differences in scale or size between entities, the sum or average may be more appropriate. If you are interested in identifying the best-performing entity, the maximum may be more appropriate, while if you are interested in identifying the worst-performing entity, the minimum may be more appropriate. The aggregation happens across time periods based on the frequency defined in the metric definition. If the frequency is monthly, the calculation will take place every month. The four choices for aggregation methods are as follows:-   **Sum**: The metric data for all entities are added together to create a single score.
-   **Average**: The metric data for all entities are averaged to create a single score.
-   **Maximum**: The highest metric data among all entities is used as the single score.
-   **Minimum**: The lowest metric data among all entities is used as the single score.

</td></tr><tr><td>

Class

</td><td>

Class to which the metric definition belongs. The choices are as follows:-   **KPI**: Indicates how well the risk exposure is managed against objectives. Use this option to add entities and additional entities to the metric definition.
-   **KRI**: Indicates the amount of exposure to a given risk or set of risks. Use this option to add risks and risk statements to the metric definition. This option is available if the Advanced Risk plugin is activated.
-   **KCI**: Indicates the effectiveness of any controls that have been implemented to reduce or mitigate a given risk exposure. Use this option to add controls and control objectives to the metric definition. This option is available if the Policy and Compliance Management plugin is activated.

**Important:** This field appears only when the metric definition is created from the IRM suite of applications. It does not appear for Operational Sustainability Management.

</td></tr><tr><td>

Precision

</td><td>

Number of decimal places after the decimal point on a score.

 When an indicator has a Precision of 0, the indicator rounds the result to the nearest whole number. For example, if an indicator with Precision 0 calculates the values 7 + \(5 / 2\), the indicator rounds the result up to 10.

 When an indicator has a Precision greater than 0, the indicator rounds to the nearest decimal point for the given precision. For example, an indicator with Precision 1 rounds a result of 4.45 as 4.5.

</td></tr><tr><td>

Calendar

</td><td>

Calendar to use for metric aggregation. Only the configured calendar options are available for selection. This field is automatically set to **Standard Calendar**. **Note:** Standard calendar refers to the Gregorian calendar.

</td></tr><tr><td>

Frequency

</td><td>

Collection frequency with which the metric is executed. Indicates how often the metric definition should collect the data. The choices are as follows:-   **Daily**
-   **Weekly**
-   **Monthly**
-   **Quarterly**
-   **Semi-annually**
-   **Annually**

</td></tr><tr><td>

First run date

</td><td>

Start date for the collection frequency schedule for the automated metric definition.

</td></tr><tr><td class="sub-head" colspan="2">

Data collection

</td></tr><tr><td>

Method Type

</td><td>

Type of automated metric. The choices are as follows:-   **Basic**: Indicates using aggregation methods such as sum, average, maximum, minimum, and count distinct.
-   **Scripted**: Indicates using a script to collect the data. This option can be used when, for example, you want to collect data from multiple tables.
-   **External Source**: Indicates that the data will be collected from external sources. For example, if you want to source data about the number of employees in your organization and their gender ratio, you can obtain the information from an external source such as Workday which is an application that stores human resources data.

 **Note:** If you select **Scripted**, you must save the form and select **Add script** to add your script. Only users with the sn\_grc\_metric.developer role can add scripts.

</td></tr><tr><td>

Table

</td><td>

Table from which data is obtained for the metrics. This field only appears if the **Method Type** field is set to **Basic**.

</td></tr><tr><td>

Criteria

</td><td>

Condition for the record from which data is collected. Build a filter by adding conditions that contain a field, operator, and values and then click **Set**. For example, you can build a condition that you want to collect data for only those incidents the due date for which is in the current month.**Note:** Select a value for the **Table** field before modifying this field.

</td></tr><tr><td>

Aggregate

</td><td>

Method or the calculation used to aggregate the data from the chosen table. When an option is selected in the **Aggregate** field, a new **Aggregation Field** is displayed next to the **Aggregate** field. The **Aggregation Field** displays the selected record. The choices for the **Aggregate** field are as follows:

 -   **Count**: Count of the number of records that are obtained from the chosen table. For example, if you want a count of the incidents, you can select this option.

**Note:** The **Aggregation Field** is not displayed when **Count** is selected.

-   **Sum**: Sum of the column that is selected in the **Aggregation Field**.
-   **Average**: Average of the values of the column that is selected in the **Aggregation Field**.
-   **Maximum**: Maximum of the values of column that is selected in the **Aggregation Field**.
-   **Minimum**: Minimum of the values of the column that is selected in the **Aggregation Field**.
-   **Count Distinct**: Number of groups in the result set that is grouped by the **Aggregation Field**.

</td></tr><tr><td>

Table field

</td><td>

Column or field of the table that is selected in the **Table** field. For example, you can select the **Caller** column in the Incident table. This selection enables you to understand that which callers are associated with the Incident table and compare them with the callers of your entities.**Note:** Select a table before modifying this field.

</td></tr><tr><td>

Aggregation field

</td><td>

Column or field from the table that is selected in the **Table** field on which the aggregation must be performed.**Note:** This field does not appear if **Count** is selected in the **Aggregate** field.

</td></tr><tr><td>

Entity field

</td><td>

Column or field from the entity table. The entities are matched based on the field selected in the **Table field** and the field selected in the **Entity field**. This field is automatically set to **Applies to record**. In the context of the Incident table in this procedure, this field enables you to compare, for example, which particular incident has been logged by which caller.

</td></tr><tr><td>

Create metric data task

</td><td>

Option to mark the creation of metric data task.

</td></tr><tr><td>

Data owner assignment type

</td><td>

Type of the data owner assignment for the metrics within the metric definition. The choices are as follows:-   **Simple**

The system assigns the specified Data owner or Data owner group to the Metric.

-   **Advanced**

The system assigns a Data owner based on the assignment configuration. ESG admins \[sn\_esg.admin\] or Risk admins \[sn\_risk.admin\] can set assignment configurations to dynamically assign data owners. For more information on creating assignment configurations see, [Create an assignment configuration](../task/create-assign-config-mmd.md) and [Assignment Configuration New Record](https://www.servicenow.com/docs/access?context=assignment-configuration-new-record&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US).

**Note:** This is available if you have the GRC: Approver Configurator application installed. For more information see, [Using Approver Configurator for setting up approvals](https://www.servicenow.com/docs/access?context=approval-configuration&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US).


</td></tr><tr><td>

Data owner type

</td><td>

Type of the data owner responsible for the metric definition. The choices are as follows:-   **User**
-   **User group**

</td></tr><tr><td>

Data owner

</td><td>

Data owner responsible for the metric definition. Select a data owner from the list.**Note:** If you selected the advanced option for **Data owner assignment type**, this will be the assigned data owner if the assignment configuration doesn’t return any results.

</td></tr><tr><td>

Instructions

</td><td>

Instructions for the data owner.

</td></tr><tr><td>

Collect supporting data

</td><td>

Option to enable collection for supporting data.**Note:** Collected supporting data is automatically deleted after a certain period, with the retention time varying according to the data frequency.

-   Daily: After 30 days
-   Weekly: After 30 days
-   Monthly: After 3 months
-   Quarterly: After 3 quarters
-   Semiannually: After 3 semi-annual periods
-   Yearly: After 3 years

</td></tr><tr><td>

Supporting data fields

</td><td>

Specifies the data fields to be shown in the supporting data.**Note:** For optimal performance, please limit your selection to 4-5 fields if your data is extensive. Selecting more fields may result in performance issues.

</td></tr><tr><td>

Approval required

</td><td>

Option to indicate if an approval is required for the metric definition.**Note:** When the **Approval required** option is enabled, the **Approver type** and **Approver** fields are displayed.

</td></tr><tr><td>

Approver type

</td><td>

Specifies the type of approver for the metric definition. The choices are as follows:-   **User**
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

Method used to determine if the data is collected manually or in an automated manner. The choices are as follows:-   **Automated**
-   **Manual**

 Select **Automated** because the procedure is to create an automated metric definition.

</td></tr><tr><td>

Enterprise Owner Type

</td><td>

Type of enterprise owner who is responsible for the automated metric definition. The choices are as follows:-   **User**
-   **User group**

</td></tr><tr><td>

Direction

</td><td>

Direction that you want to see the metric in. The choices are as follows:-   **None**: If you don’t want any change in the metric direction, select this option.
-   **Minimize**: If the desired metric direction is downward or descending, select this option. For example, you want to minimize the fuel consumption.
-   **Maximize**: If the desired metric direction is upward or ascending, select this option. For example, you want to maximize the use of natural resources in your organization.
-   **Milestone**: When the metric direction isn’t applicable, but the metric is tracked against a milestone, select this option. For example, if your organization is going to launch a new renewable energy product in the market, the upcoming launch date is considered as a milestone.

</td></tr><tr><td>

Group

</td><td>

Area that the metric relates to. For example, the metric may be related to the area of gender diversity, energy, water consumption, or may be related to Scope 3 emissions, and so on.

</td></tr><tr><td>

Reporting classification

</td><td>

Tag used to categorise the metric.

</td></tr><tr><td>

Enterprise owner

</td><td>

User who is the owner of the metric and is responsible for the metric. For example, for a metric such as revenue collection, the vice president or the general manager of the business unit could be the enterprise owner.

</td></tr><tr><td>

Nature

</td><td>

Nature of the automated metric definition. The choices are as follows:-   **None**: If you don’t want any change in the metric direction, select this option.
-   **Leading** \(Predictive\) Metric: Is predictive and helps anticipate future outcomes. In this case, the company may use a leading metric related to GHG emissions, such as the amount of energy consumed per production unit. By tracking energy consumption, the company can predict its future GHG emissions based on the energy sources used and the efficiency of its production processes. This leading metric enables the company to proactively identify areas for improvement and make informed decisions to reduce emissions.
-   **Lagging** \(Measures Impact\) Metric: Measures the impact of past actions or events. In our example, a lagging metric related to GHG emissions could be the total emissions produced by the company in a given year. This metric provides an assessment of the company's historical environmental impact. By monitoring this metric over time, the company can evaluate the effectiveness of its emission reduction efforts and identify areas where further improvements are needed. Lagging metrics help measure the outcomes of past actions and inform future strategies.
-   **Current** metric: Monitors ongoing processes and identifies real-time improvement areas. For GHG emissions, a current metric could be the emissions intensity, which measures the emissions generated per unit of production. By tracking emissions intensity, the company can identify specific areas within its operations that contribute to higher emissions. This metric helps the company identify real-time improvement opportunities, such as optimizing energy usage, implementing energy-efficient technologies, or adopting renewable energy sources.

</td></tr><tr><td>

Subgroup

</td><td>

Subgroup that the metric relates to.

</td></tr><tr><td>

Key metric

</td><td>

Option to indicate if the metric is a key metric for your business.

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

Users who can view the record.**Note:** By default, the logged in user is added to the list of confidential users.

</td></tr><tr><td>

Allowed groups

</td><td>

Groups that can view the record.

</td></tr></tbody>
</table>**Parent Topic:**[Create an automated metric definition](../task/create-metric-definition.md)

