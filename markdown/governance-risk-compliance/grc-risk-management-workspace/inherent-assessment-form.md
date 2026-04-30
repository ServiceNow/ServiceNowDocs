---
title: Inherent Assessment form
description: Use the Inherent Assessment form in the Advanced Risk application to assess the inherent risks in your organization.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure an inherent assessment, Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Inherent Assessment form

Use the Inherent Assessment form in the Advanced Risk application to assess the inherent risks in your organization.

See the following table for a description of the field values.

<table id="table_l35_zwl_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk assessment methodology

</td><td>

Selected RAM. This field is automatically set based on your RAM.

</td></tr><tr><td>

State

</td><td>

State of the RAM. This field is automatically set to **Draft**.

</td></tr><tr><td>

Calculate based on

</td><td>

Option for calculating the assessment score that is based on factor responses.

</td></tr><tr><td>

Assessment contribution

</td><td>

Type of factor contribution:-   **Qualitative**: Provides a numerical score and then converts the score into a rating. Selecting this option ensures that only qualitative factors are available for adding.
-   **Quantitative**: Provides the losses that can be incurred in monetary terms. The losses contribute to the annual loss expectancy \(ALE\). Selecting this option ensures that only quantitative factors are available for adding.
-   **Both**: Provides both the qualitative and quantitative assessment type.

</td></tr><tr><td>

Enable heatmap

</td><td>

Option to enable the heatmap report on the Advanced Risk dashboard. **Note:** You can select this option only if a minimum of two factors are added to the assessment type. Selecting this option makes the Heatmap Configuration section and the Heatmap Colors related list appear on the form.

</td></tr><tr><td class="sub-head" colspan="2">

Qualitative Score

</td></tr><tr><td colspan="2">

This section appears only when **Qualitative** is selected from the **Assessment contribution** field.

</td></tr><tr><td>

Qualitative scoring logic

</td><td>

Formula that you can use to calculate the scoring logic:-   **Sum**: Sum of the factor responses.
-   **Minimum**: Minimum value of the factor responses.
-   **Maximum**: Maximum value of the factor responses.
-   **Average**: Average value of the factor responses.
-   **Product**: Value that is derived by multiplying the factor responses.
-   **Weighted average**: Average value of the weighting of factors. This value is then classified as low, medium, or high.
-   **Script**: User-defined formula to calculate the score. This option is available only to users with the sn\_grc.developer role.

</td></tr><tr><td class="sub-head" colspan="2">

Quantitative Score

</td></tr><tr><td colspan="2">

This section appears only when **Quantitative** is selected from the **Assessment contribution** field.

</td></tr><tr><td>

Quantitative scoring logic

</td><td>

Formula that you can use to calculate the scoring logic:-   **Sum**: Sum of the factor responses.
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

Option to rename the section title of the assessment type. For example, if you rename Inherent assessment as Gross assessment, the new title will be displayed in all sections where the Inherent assessment was previously referred.

</td></tr><tr><td>

Score label

</td><td>

Option to rename the qualitative score label in the Scoring section of the assessment form. For example, if you rename Inherent risk as Gross risk, the new score label will be displayed in the scoring section where Inherent risk was previously referred.

</td></tr><tr><td>

Annual loss expectancy label

</td><td>

Option to rename the quantitative score label in the Scoring section of the assessment form. For example, if you rename Inherent ALE as Gross ALE, the new score label will be displayed in the scoring section where Inherent ALE was previously referred.

</td></tr><tr><td class="sub-head" colspan="2">

Heatmap Configuration

</td></tr><tr><td colspan="2">

This section appears only when the **Enable heatmap** option is selected.

</td></tr><tr><td>

Factor for X-axis

</td><td>

Factor that appears on the X-axis of the heatmap.**Note:** Only qualitative factors of the type **Choice** or factors with the transformation criteria can be selected. For more information, see [Transformation criteria](../concept/transformation-criteria.md).

</td></tr><tr><td>

Factor for Y-axis

</td><td>

Factor that appears on the Y-axis of the heatmap.**Note:** Only qualitative factors of the type **Choice** or with the transformation criteria can be selected. For more information, see [Transformation criteria](../concept/transformation-criteria.md).

</td></tr></tbody>
</table>**Parent Topic:**[Configure an inherent assessment](../task/configure-inherent-assessment.md)

