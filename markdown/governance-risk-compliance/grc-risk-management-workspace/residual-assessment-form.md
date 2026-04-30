---
title: Residual Assessment form
description: Use the Residual Assessment form in the Advanced Risk application to assess the residual risks in your organization.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure a residual assessment, Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Residual Assessment form

Use the Residual Assessment form in the Advanced Risk application to assess the residual risks in your organization.

See the following table for a description of the field values.

<table id="table_l35_zwl_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk assessment methodology

</td><td>

Name of the RAM. This field is automatically set based on the selected RAM.

</td></tr><tr><td>

Calculate based on

</td><td>

Options for calculating the assessment score:-   **Inherent risk and control effectiveness**: Makes the assessment qualitative. The comparison between inherent and control effectiveness is always qualitative.
-   **Factor responses**: Bases the residual factors' calculation on responses to manual factors.

</td></tr><tr><td>

Assessment contribution

</td><td>

Type of factor contribution: -   **Quantitative**
-   **Qualitative**
-   **Both**

 If **Inherent risk and control effectiveness** is selected in the **Calculate based on** field, then this field is automatically set to **Qualitative**. The field can't be modified.

</td></tr><tr><td>

Factors same as inherent

</td><td>

Option to automatically copy the assessment contribution, qualitative scoring logic, factors, and qualitative rating criteria from the inherent assessment. **Note:** This option appears only when the **Calculate based on field** field has the **Factor responses** value.

</td></tr><tr><td>

Enable heatmap

</td><td>

Option to enable you to view the heatmap report on the Advanced Risk dashboard. **Note:** This option can be selected only if a minimum of two factors are added to the assessment type.

</td></tr><tr><td class="sub-head" colspan="2">

Qualitative score

</td></tr><tr><td>

Qualitative scoring logic

</td><td>

Scoring logic to be used. The options for this field change based on the option that is selected in the **Calculate based on** field. When the **Calculate based on** field has **Inherent risk and control effectiveness**, the options are as follows:

-   **Lookup matrix between inherent assessment and control effectiveness**: Generates a matrix between the inherent assessment and control effectiveness assessment. It performs a Cartesian product to generate scores. You can view the matrix in the Matrix related list. For example, if the inherent risk is high and the control effectiveness is low, then the residual risk is also high.
-   **Inherent score-control effectiveness score**: Provides the difference between the inherent score and the control effectiveness score.
-   **Inherent score/control effectiveness score**: Provides the value that is derived by dividing the inherent score by the control effectiveness score.
-   **Script**: Use a custom script to calculate the qualitative score. The Script option enables you to create a customized calculation method that aligns with your organization's unique requirements and risk assessment approach.

**Note:** You can write or modify scripts only for assessment types that aren’t published.


 When the **Calculate based on** field has **Factor responses**, the options are as follows:

-   **Sum**: Sum of the factor responses.
-   **Minimum**: Minimum value of the factor responses.
-   **Maximum**: Maximum value of the factor responses.
-   **Average**: Average value of the factor responses.
-   **Product**: Value derived by multiplying the factor responses.
-   **Weighted average**: Average value of the weighting of factors. This value is then classified as low, medium, or high.
-   **Script**: User-defined formula to calculate the score. This option is available only to users with the sn\_grc.developer role.

</td></tr><tr><td class="sub-head" colspan="2">

Quantitative score

</td></tr><tr><td colspan="2">

This section appears only when the value **Quantitative** is selected from the **Factor contribution** field.

</td></tr><tr><td>

Quantitative scoring logic

</td><td>

Scoring logic to be used:-   **Sum**: Sum of the factor responses.
-   **Minimum**: Minimum value of the factor responses.
-   **Maximum**: Maximum value of the factor responses.
-   **Average**: Average value of the factor responses.
-   **Product**: Value that is derived by multiplying the factor responses.
-   **Script**: User-defined formula to calculate the score. This option is available only to users with the sn\_grc.developer role.

</td></tr><tr><td class="sub-head" colspan="2">

Section Labels

</td></tr><tr><td colspan="2">

This section appears only when **Configure section terminology** is selected in the RAM form.

 **Note:** Section label renaming applies only to the advanced risk assessment interface while leaving the terminology used in reports, dashboards, heatmaps, and other areas unchanged.

</td></tr><tr><td>

Title

</td><td>

Option to rename the section title of the assessment type. For example, if you rename Residual assessment as Net assessment, the new title will be displayed in all sections where the Residual assessment was previously referred.

</td></tr><tr><td>

Score label

</td><td>

Option to rename the qualitative score label in the Scoring section of the assessment form. For example, if you rename Residual risk as Net risk, the new score label will be displayed in the scoring section where Residual risk was previously referred.

</td></tr><tr><td>

Annual loss expectancy label

</td><td>

Option to rename the quantitative score label in the Scoring section of the assessment form. For example, if you rename Residual ALE as Net ALE, the new score label will be displayed in the scoring section where Residual ALE was previously referred.

</td></tr><tr><td class="sub-head" colspan="2">

Heatmap Configuration

</td></tr><tr><td colspan="2">

This section appears only when the **Enable heatmap** option is selected.

</td></tr><tr><td>

Factor for X-axis

</td><td>

Factor that appears on the X-axis of the heatmap. **Note:** Only the qualitative factors of type **Choice** or factors with the transformation criteria can be selected. For more information, see [Transformation criteria](../concept/transformation-criteria.md).

</td></tr><tr><td>

Factor for Y-axis

</td><td>

Factor that appears on the Y-axis of the heatmap. **Note:** Only the qualitative factors of type **Choice** or with the transformation criteria can be selected. For more information, see [Transformation criteria](../concept/transformation-criteria.md).

</td></tr></tbody>
</table>**Parent Topic:**[Configure a residual assessment](../task/configure-residual-assessment.md)

