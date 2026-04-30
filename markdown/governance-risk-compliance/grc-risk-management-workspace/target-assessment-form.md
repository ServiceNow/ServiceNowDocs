---
title: Target assessment form
description: Use the Target Assessment form in the Advanced Risk application to assess the desired future risk level in your organization.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Configure a target assessment, Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Target assessment form

Use the Target Assessment form in the Advanced Risk application to assess the desired future risk level in your organization.

See the following table for a description of the field values.

<table id="table_l35_zwl_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk assessment methodology

</td><td>

Name of the RAM to which this target assessment belongs. This field is automatically set based on the selected RAM.

</td></tr><tr><td>

State

</td><td>

Current state of the assessment type. This field is automatically set to **Draft**.

</td></tr><tr><td>

Calculate based on

</td><td>

Options for calculating the assessment score:-   **Factor responses**: Option to select individual factors for the target assessment.
-   **Factors same as inherent**: Option to copy the assessment contribution, scoring logic, and factors from the inherent assessment.
-   **Factors same as residual**: Option to copy the assessment contribution, scoring logic, and factors from the residual assessment.
-   **Overall assessment**: Option to continue without any factors selection. Assessors can directly provide rating or Annual loss expectancy \(ALE\) for the assessment.

</td></tr><tr><td>

Assessment contribution

</td><td>

Type of factor contribution: -   **Quantitative**
-   **Qualitative**
-   **Both**

 **Note:** If **Factors same as inherent** or **Factors same as residual** is selected in the **Calculate based on** field, then **Assessment contribution** field is automatically set to a value defined in the inherent and residual assessment types. The field can't be modified.

</td></tr><tr><td>

Enable heatmap

</td><td>

Option to enable you to view the heatmap report on the Advanced Risk dashboard. **Note:** This option can be selected only if a minimum of two factors are added to the assessment type.

</td></tr><tr><td>

Copy rating criteria from inherent

</td><td>

Option to copy the qualitative rating criteria from the inherent assessment. This option appears only when the value **Factors same as inherent** is selected from the **Calculate based on** field.

</td></tr><tr><td>

Copy rating criteria from residual

</td><td>

Option to copy the qualitative rating criteria from the residual assessment. This option appears only when the value **Factors same as residual** is selected from the **Calculate based on** field.

</td></tr><tr><td class="sub-head" colspan="2">

Qualitative score

</td></tr><tr><td colspan="2">

This section appears only when the value **Qualitative** or **Both** is selected from the **Assessment contribution** field.

</td></tr><tr><td>

Qualitative scoring logic

</td><td>

Formulae to calculate the qualitative scoring. You can modify the **Qualitative scoring logic** field only when the value **Factor responses** is selected from the **Calculate based on** field. The options are as follows:

-   **Sum**: Sum of the factor responses.
-   **Minimum**: Minimum value of the factor responses.
-   **Maximum**: Maximum value of the factor responses.
-   **Average**: Average value of the factor responses.
-   **Product**: Value derived by multiplying the factor responses.
-   **Weighted average**: Average value of the weighting of factors. This value is then classified as low, medium, or high.
-   **Script**: Use a custom script to calculate the qualitative score. The Script option enables you to create a customized calculation method that aligns with your organization's unique requirements and risk assessment approach. This option is available only to users with the sn\_grc.developer role.

**Note:** Only users with the sn\_grc.developer role can write or modify scripts for assessment types that aren’t published.


</td></tr><tr><td class="sub-head" colspan="2">

Quantitative score

</td></tr><tr><td colspan="2">

This section appears only when the value **Quantitative** or **Both** is selected from the **Assessment contribution** field.

</td></tr><tr><td>

Quantitative scoring logic

</td><td>

Formulae to calculate the quantitative scoring. You can modify the **Quantitative scoring logic** field only when the value **Factor responses** is selected from the **Calculate based on** field. The options are as follows:

-   **Sum**: Sum of the factor responses.
-   **Minimum**: Minimum value of the factor responses.
-   **Maximum**: Maximum value of the factor responses.
-   **Average**: Average value of the factor responses.
-   **Product**: Value that is derived by multiplying the factor responses.
-   **Script**: Use a custom script to calculate the quantitative score. The Script option enables you to create a customized calculation method that aligns with your organization's unique requirements and risk assessment approach.

**Note:** Only users with the sn\_grc.developer role can write or modify scripts for assessment types that aren’t published.


</td></tr><tr><td class="sub-head" colspan="2">

Section Labels

</td></tr><tr><td colspan="2">

This section appears only when the **Configure section terminology** option is selected in the RAM form.

 **Note:** Section label renaming applies only to the advanced risk assessment interface while leaving the terminology used in reports, dashboards, heatmaps, and other areas unchanged.

</td></tr><tr><td>

Title

</td><td>

Option to rename the section title of the assessment type. For example, if you rename Target assessment as Future assessment, the new title will be displayed in all sections where the Target assessment was previously referred.

</td></tr><tr><td>

Score label

</td><td>

Option to rename the qualitative score label in the Scoring section of the assessment form. For example, if you rename Target risk as Future risk, the new score label will be displayed in the scoring section where Target risk was previously referred.

</td></tr><tr><td>

Annual loss expectancy label

</td><td>

Option to rename the quantitative score label in the Scoring section of the assessment form. For example, if you rename Target ALE as Future ALE, the new score label will be displayed in the scoring section where Target ALE was previously referred.

</td></tr><tr><td class="sub-head" colspan="2">

Other Configurations

</td></tr><tr><td>

Assessment is required

</td><td>

Option to make the target assessment either always required or conditionally required based on specific conditions. The options are as follows:-   **Always**: Option to make the target assessment required regardless of any specific conditions.
-   **On specific conditions**: Option to make the target assessment required based on specific conditions using the condition builder.
-   **On specific conditions specified through script**: Option to make the target assessment required using a predefined script or set of instructions. The Script option enables you to create a customized condition that align with your organization's unique requirements and risk assessment approach.

**Note:** Only users with the sn\_grc.developer role can write or modify scripts.


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
</table>**Parent Topic:**[Configure a target assessment](../task/configure-target-assessment.md)

