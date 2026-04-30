---
title: Create a scripted automated factor
description: Create scripted automated factors that use a script to fetch data from ServiceNow records or from external sources. During risk assessment, scripted automated factors automatically calculate and provide the responses for factors.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Create a scripted automated factor

Create scripted automated factors that use a script to fetch data from ServiceNow® records or from external sources. During risk assessment, scripted automated factors automatically calculate and provide the responses for factors.

## Before you begin

Role required: sn\_grc.developer and sn\_risk.admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Administration** &gt; **Automated Scripted Factors**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ycl_dkx_clb"><thead><tr><th>

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
-   **Quantitative**: Provides the losses that can be incurred from a risk in monetary terms. The losses contribute to the annual loss expectancy \(ALE\).
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
-   **Percentage**: The factor response after automatic calculation will be in percentage.


</td></tr><tr><td>

Transform qualitative score

</td><td>

Option to transform the overall group qualitative score based on an interval scale.For example, assume the **User response** field is set to **Percentage**. As the admin, you can transform the percentage value into a qualitative score, such that 0% to 30% is low, 30% to 60% is medium, and 60% and higher is high. In this case, the ratings 1, 2, and 3 can be assigned to low, medium, and high.

 This field appears only when **Qualitative** is selected from the**Factor contribution** field.

</td></tr><tr><td>

State

</td><td>

State of the factor. This field is automatically set to **Draft**.

</td></tr><tr><td>

Qualitative weighting \(%\)

</td><td>

Score contribution or qualitative weight that is given to a factor. This value determines the actual contribution of this factor to the final score. This field appears only when **Qualitative** is selected from the **Factor contribution** field.

</td></tr><tr><td>

Assessment context

</td><td>

Context for which the assessment must be performed. Choices are the following:-   **Risk**: Select this option to perform the assessment for an entity and its associated risk.
-   **Object**: Select this option to perform an assessment on any ServiceNow record. For example, users can perform Exception Risk Assessment or Change Risk Assessment directly on an object.


</td></tr><tr><td>

Description

</td><td>

Brief description about the purpose of the factor and where to use the factor. This description is for the administrator to understand the factor.

</td></tr><tr><td class="sub-head" colspan="2">

Script

</td></tr><tr><td>

Variables

</td><td>

Predefined variables to be used in the **Script** field.

</td></tr><tr><td>

Script

</td><td>

Custom script.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Frequency

</td><td>

Frequency of when factor is run.

</td></tr><tr><td>

Day of the week

</td><td>

Day of the week when the factor is run. This field appears only when the **Frequency** field has **Weekly**.

</td></tr><tr><td>

Day of month

</td><td>

Day of the month when the factor is run. This field appears only when the **Frequency** field has **Monthly**.

</td></tr><tr><td>

Month

</td><td>

Month when the factor is run. This field appears only when the **Frequency** field has **Quarterly**, or **Semi-annually**, **Annually**.

</td></tr><tr><td>

Next run date

</td><td>

Date when the factor is run again. This field is automatically set based on the selections made on the form.

</td></tr></tbody>
</table>4.  Click **Submit**.

5.  Open the factor that you created.

6.  Click **Publish**.


## Result

The factor is published and is ready for use in a Risk Assessment Methodology.

**Parent Topic:**[Perform Advanced Risk Assessment](../concept/use-advanced-risk-assessment.md)

**Related topics**  


[Create an automated factor](configure_automated_factor.md)

