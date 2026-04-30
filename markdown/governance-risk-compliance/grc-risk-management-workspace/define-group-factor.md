---
title: Create a group factor
description: Create group factors to evaluate and assess risks on a risk assessment instance.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Create a group factor

Create group factors to evaluate and assess risks on a risk assessment instance.

## Before you begin

Role required: sn\_risk.admin

## About this task

Group factors contribute to either a numerical risk score or to the Annual Loss Expectancy \(ALE\). You can group multiple factor responses into one group factor that can be used for reporting. The score of a group factor is computed based on the scores of its associated factors.

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Administration** &gt; **Group Factors**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_l35_zwl_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the factor such as `Organizational impact`.

</td></tr><tr><td>

Factor contribution

</td><td>

Type of factor contribution. Choices are the following:-   **Qualitative**: Provides a numerical score and then converts the score into a rating.
-   **Quantitative**: Provides the losses that are incurred from a risk in monetary terms. The losses contribute to the ALE.
-   **Both**: Assessment type is both qualitative and quantitative.


</td></tr><tr><td>

Display order

</td><td>

Order of questions in the assessment form. This field enables you to set a specific sequence in which the questions must appear.

</td></tr><tr><td>

State

</td><td>

State of the factor. This field is automatically set to **Default**.

</td></tr><tr><td>

Qualitative weighting \(%\)

</td><td>

Score contribution or qualitative weight that is given to the factor. This value determines the actual contribution of this factor to the final score. This value is a percentage. This field appears only when **Qualitative** is selected from the **Factor contribution** field.

</td></tr><tr><td>

Description

</td><td>

Brief description about the purpose of the factor and where to use the factor. This description is for the administrator to understand the factor.

</td></tr><tr><td class="sub-head" colspan="2">

Qualitative Score

</td></tr><tr><td colspan="2">

This section appears only when **Qualitative** is selected from the **Factor contribution** field.

</td></tr><tr><td>

Formula for qualitative score

</td><td>

Formula for calculating the overall qualitative risk score. Choices are the following:-   **Sum**: Sum of the factor responses.
-   **Minimum**: Minimum value of the factor responses.
-   **Maximum**: Maximum value of the factor responses.
-   **Average**: Average value of the factor responses.
-   **Product**: Value derived by multiplying the factor responses.
-   **Weighted average**: Average value of the weighting of factors.
-   **Script**: User-defined formula to calculate the score. This option is available only to users with the sn\_grc.developer role.


</td></tr><tr><td>

Transform qualitative score

</td><td>

Option to transform the overall group qualitative score based on an interval scale.For example, assume the **User response** field is set to **Percentage**. As the admin, you can transform the percentage value into a qualitative score, such that 0% to 30% is low, 30% to 60% is medium, and 60% and higher is high. In this case, the ratings 1, 2, and 3 can be assigned to low, medium, and high.

 This field appears only when **Qualitative** is selected from the **Factor contribution** field.

</td></tr><tr><td class="sub-head" colspan="2">

Quantitative Score

</td></tr><tr><td colspan="2">

This section appears only when **Quantitative** is selected from **Factor contribution** field.

</td></tr><tr><td>

Formula for quantitative score

</td><td>

Formula for calculating the overall qualitative risk score. Choices are the following:-   **Sum**: Sum of the factor responses.
-   **Minimum**: Minimum value of the factor responses.
-   **Maximum**: Maximum value of the factor responses.
-   **Average**: Average value of the factor responses.
-   **Product**: Value derived by multiplying the factor responses.
-   **Script**: User-defined formula to calculate the score. This option is available only to users with the sn\_grc.developer role.


</td></tr></tbody>
</table>4.  Select **Save**.

5.  In the Factors related list, click **Edit** and add the required factors.

6.  Select **Save**.

7.  Select the Qualitative Transformation Criteria related list.

8.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Lower limit of range|Value that is the lower limit of a range of values. For example, for the first range of 0% to 30%, the lower limit is 0. For the second range of 31% to 60%, the lower range is 31.|
    |Score|Value that must be used as the score if the value is within the range defined in the **Lower limit of range** field. For example, for the lower limit 0, the score can be 1. For the lower limit 31, the score can be 2.|

9.  Select **Submit.**

10. Open the factor that you created.

11. Select **Publish**.


## Result

The factor is published and is ready for use in a Risk Assessment Methodology.

-   **[Scoring logic for predefined formulas for group factors](../reference/scoring-logic-group-factors.md)**  
Group factors have multiple predefined formulae and each of them has a specific contribution to the scoring logic.

**Parent Topic:**[Perform Advanced Risk Assessment](../concept/use-advanced-risk-assessment.md)

