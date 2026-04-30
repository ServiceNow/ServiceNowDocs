---
title: Create an automated factor
description: Create automated factors to automatically fetch data from other data sources such as tables or database views.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Create an automated factor

Create automated factors to automatically fetch data from other data sources such as tables or database views.

## Before you begin

You must have the Governance, Risk, and Compliance Enterprise license.

Role required: sn\_risk.admin

## About this task

Automated factors help automate the risk assessment process. They do not to rely on manual inputs, and they thus reduce subjectivity. All the responses to automated factors are automatically calculated during the assessment.

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Administration** &gt; **Automated Factors**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_prh_qjt_blb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the factor such as `Regulatory Impact`.

</td></tr><tr><td>

Factor contribution

</td><td>

Type of factor contribution. Choices are the following:-   **Qualitative**: Provides a numerical score and then converts the score into a rating.
-   **Quantitative**: Provides the losses that can be incurred in monetary terms. The losses contribute to the annual loss expectancy \(ALE\).
-   **Both**: Assessment type is both qualitative and quantitative.


</td></tr><tr><td>

Display order

</td><td>

Order of questions in the assessment form. This field enables you to set a specific sequence in which the questions must appear.

</td></tr><tr><td>

Response type

</td><td>

Options for users to respond to the factors. Choices are the following:-   **Number**: The factor response after automatic calculation will be a number.
-   **Currency**: The factor response after automatic calculation will be in currency.
-   **Percentage**: The factor response after automatic calculation will be a percentage.


</td></tr><tr><td>

Assessment context

</td><td>

Context where the assessment must be performed. Choices are the following:-   **Risk**: Select this option to perform the assessment for an entity and for an associated risk.
-   **Object**: Select this option to perform an assessment on any ServiceNow record. For example, users can perform Exception Risk Assessment or Change Risk Assessment directly on an object.


</td></tr><tr><td>

State

</td><td>

State of the factor. This field is automatically set to **Draft**.

</td></tr><tr><td>

Qualitative weighting \(%\)

</td><td>

Score contribution or qualitative weight that is given to the factor. This value determines the actual contribution of this factor to the final score. This field appears only when **Qualitative** is selected from the **Factor contribution** field.

</td></tr><tr><td>

Transform qualitative score

</td><td>

Option to transform the overall group qualitative score based on an interval scale.For example, assume the **User response** field is set to **Percentage**. As the admin, you can transform the percentage value into a qualitative score, such that 0% to 30% is low, 30% to 60% is medium, and 60% and higher is high. In this case, the ratings 1, 2, and 3 can be assigned to low, medium, and high.

 This field appears only when **Qualitative** is selected from the**Factor contribution** field.

</td></tr><tr><td>

Collect supporting data

</td><td>

Option for collecting supporting data. If this option is selected, the Supporting Data section appears.

</td></tr><tr><td>

Description

</td><td>

Brief description about the purpose of the factor and where to use the factor. This description is for the administrator to understand the factor.

</td></tr><tr><td class="sub-head" colspan="2">

Data Source

</td></tr><tr><td>

Source

</td><td>

Table or view that is used as the source of the factor.

</td></tr><tr><td class="sub-head" colspan="2">

Filter Criteria

</td></tr><tr><td>

Filter by entity

</td><td>

Option for filtering the source by the risk assessment instance entity.

</td></tr><tr><td>

Entity-mapping field

</td><td>

Field that refers to the Entity table. This field appears only when the **Filter by entity** option is selected.

</td></tr><tr><td>

Filter by risk

</td><td>

Option for filtering the source by the risk of the risk assessment instance.

</td></tr><tr><td>

Risk mapping field

</td><td>

Field that refers to the Risk table. This field appears only when the **Filter by risk** option is selected.

</td></tr><tr><td>

Filter by control

</td><td>

Option for filtering the source by the risk assessment instance control. This option applies only to the individual assessment of controls in the control assessment.

</td></tr><tr><td>

Control mapping field

</td><td>

Field that refers to the Control table. This field appears only when the **Filter by control** option is selected.

</td></tr><tr><td>

Filter by object

</td><td>

Option for filtering the source by the object of the risk assessment instance. This field appears only when you are performing the risk assessment on an object.

</td></tr><tr><td>

Object mapping field

</td><td>

Field that refers to an object in the assessment instance. This field appears only when **Object** is selected from the **Assessment context** field, and when the **Filter by object** option is selected.

</td></tr><tr><td class="sub-head" colspan="2">

Aggregation.

</td></tr><tr><td>

Aggregation type

</td><td>

Formula for aggregating the records that are selected from the table in the **Source** field. Choices are the following:-   **Sum**: Sum of the aggregation column.
-   **Average**: Average value of the aggregation column.
-   **Maximum**: Maximum value of the aggregation column.
-   **Minimum**: Minimum value the aggregation column.
-   **Count**: Count of number of records of the aggregation column.
-   **Count distinct**: Number of unique records of the aggregation column.


</td></tr><tr><td>

Aggregation column

</td><td>

Column that is used for aggregation based on the table selected in the **Source** field.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Frequency

</td><td>

Frequency of when the factor is run.

</td></tr><tr><td>

Day of the week

</td><td>

Day of the week when the factor is run. This field appears only when **Weekly** is selected from the **Frequency** field.

</td></tr><tr><td>

Day of month

</td><td>

Day of the month when the factor is run. This field appears only when **Monthly** is selected from the **Frequency** field.

</td></tr><tr><td>

Month

</td><td>

Month when the factor is run. This field appears only when the **Frequency** field has the values **Quarterly**, **Semi-annually**, or **Annually**.

</td></tr><tr><td>

Next run date

</td><td>

Date when the factor runs again. This field is automatically set based on the selections made on the form.

</td></tr></tbody>
</table>4.  Click the Supporting Data section.

5.  For the data that you want to collect, move the corresponding fields from the Available list to the Selected list.

6.  Click **Submit**.

7.  Open the factor that you created.

8.  Click **Publish**.


## Result

The factor is published and is ready for use in a Risk Assessment Methodology.

**Parent Topic:**[Perform Advanced Risk Assessment](../concept/use-advanced-risk-assessment.md)

**Related topics**  


[Create a scripted automated factor](define-scripted-automated-factor.md)

