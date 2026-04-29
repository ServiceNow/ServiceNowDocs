---
title: Create a manual factor
description: Create manual factors to evaluate and assess risks on a risk assessment instance.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Create a manual factor

Create manual factors to evaluate and assess risks on a risk assessment instance.

## Before you begin

Role required: sn\_risk.admin

## About this task

Manual factors need human responses. You can create manual factors and associate them with various assessment types, such as an inherent assessment, control assessment, or residual assessment.

**Note:** You can only delete a factor if there are no Risk assessment methodologies \(RAMs\) associated with the factor.

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Administration** &gt; **Manual Factors**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_fgf_ccl_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the factor such as `Reputational impact`.

</td></tr><tr><td>

State

</td><td>

State of the factor. This field is automatically set to **Draft**.

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

User response

</td><td>

Option for users to respond to the factors. Choices are the following:-   **Choice**: Users can create choices such as low, medium, and high alongside their respective scores.

**Note:** Selecting this option displays the Choices related list. Save the form to see the Choices related list.

-   **Number**: Users can enter a number in response to a factor.
-   **Text**: Users can enter text in response to a factor. This option does not contribute to the score, and it is used as guidance or as a data collection method.
-   **Currency**: Users can enter currency in response to a factor.
-   **Percentage**: Users can enter a percentage in response to a factor.


</td></tr><tr><td>

Control type

</td><td>

Option to modify the layout of factor choices on the risk assessment form. Choices are as follows:-   **Radio**: Displays the factor choices in radio buttons.
-   **Drop-down**: Displays the factor choices in a drop-down list.
This field appears only when **Choice** is selected from the **User response** field.

</td></tr><tr><td>

Control layout

</td><td>

Option to display the factor choices in vertical or horizontal layout.This field appears only when **Radio** is selected from the **Control type** field.

</td></tr><tr><td>

Transform qualitative score

</td><td>

Option to transform the overall group qualitative score based on an interval scale.For example, assume the **User response** field is set to **Percentage**. As the admin, you can transform the percentage value into a qualitative score, such that 0% to 30% is low, 30% to 60% is medium, and 60% and higher is high. In this case, the ratings 1, 2, and 3 can be assigned to low, medium, and high.

 This field appears only when **Qualitative** is selected from the **Factor contribution** field.

</td></tr><tr><td>

Qualitative weighting \(%\)

</td><td>

Score contribution or qualitative weight that is given to the factor. This value determines the actual contribution of this factor to the final score. This value is a percentage. This field appears only when **Qualitative** is selected from the **Factor contribution** field.

</td></tr><tr><td>

Mandatory response

</td><td>

Option for making the responses mandatory.

</td></tr><tr><td>

Description

</td><td>

Brief description about the purpose of the factor and where to use the factor. This description is for the administrator to understand the factor.

</td></tr><tr><td>

Guidance text

</td><td>

Guidance on how to respond to the factor. If the risk assessor does not understand the factor's question, then this field can help explain the question. For example, if the assessor wants to understand a question about the financial impact of losing a high value asset, the assessor can get guidance from this field.

</td></tr></tbody>
</table>4.  Click **Save**.

5.  Click the Qualitative Transformation Criteria related list.

    **Note:** This related list appears only when you select the **Transform qualitative score** option.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Lower limit of range|Value that is the lower limit of a range of values. For example, for the first range of 0% to 30%, the lower limit is 0. For the second range of 31% to 60%, the lower range is 31.|
    |Score|Value that must be used as the score if the value is within the range defined in the **Lower limit of range** field. For example, for the lower limit 0, the score can be 1. For the lower limit 31, the score can be 2.|

7.  Click **Submit**.

8.  Open the factor that you created.

9.  Click **Publish**.


## Result

The factor is published and is ready for use in a Risk Assessment Methodology.

**Parent Topic:**[Perform Advanced Risk Assessment](../concept/use-advanced-risk-assessment.md)

