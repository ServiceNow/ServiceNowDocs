---
title: Control Assessment form
description: Use the Control Assessment form in the Advanced Risk application to assess the effectiveness of controls in mitigating risks.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure a control effectiveness assessment, Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Control Assessment form

Use the Control Assessment form in the Advanced Risk application to assess the effectiveness of controls in mitigating risks.

See the following table for a description of the field values.

<table id="table_l35_zwl_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk assessment methodology

</td><td>

Name of the risk assessment methodology used for control assessment. This field is automatically set based on your RAM.

</td></tr><tr><td>

State

</td><td>

State of the RAM. This field is automatically set to **Draft**.

</td></tr><tr><td>

Assessment contribution

</td><td>

Type of factor contribution. This field is automatically set to **Qualitative contribution**.

</td></tr><tr><td>

Calculate based on

</td><td>

Option to assess the types of control. Choices are the following:-   **Control environment assessment**: Select this option if you don’t want to assess individual controls, but instead want to assess the overall effectiveness of the control environment.
-   **Individual assessment of controls**: Select this option if you want to perform assessment for individual controls. For example, you can select the risk of employees accepting bribes and then assess each existing control to mitigate the risk of bribery. This option is available only when the Policy and Compliance Management \(com.sn\_compliance\) plugin is activated.

</td></tr><tr><td>

Control identification

</td><td>

Option to decide how to identify the controls in the risk assessment instance. The choices are the following:-   **None**
-   **From Library**: Use this option when you want to identify controls from the library on the risk assessment instance.
-   **Ad-hoc**: Use this option when you want to identify new controls on the risk assessment instance.
-   **From Library and Ad-hoc**: Use this option when you want to identify controls from the library as well as identify new controls.

 This field appears only when the **Calculate based on** field has the value **Individual assessment of controls**.

</td></tr><tr><td>

Factor for overall effectiveness

</td><td>

Manual, automated, or group factors to assess controls. This field appears only when the option **Individual assessment of controls** is selected from the **Calculate based on** field. Only qualitative factors or factors with the option to transform the qualitative score will be displayed in this field.

</td></tr><tr><td>

Qualitative scoring logic

</td><td>

Formula for calculating the scoring logic. Choices are the following:-   **Sum**: Sum of the factor responses.
-   **Minimum**: Minimum value of the factor responses.
-   **Maximum**: Maximum value of the factor responses.
-   **Average**: Average value of the factor responses.
-   **Product**: Value derived by multiplying the factor responses.
-   **Weighted average**: Average value of the weighting of factors. This value is then classified as low, medium, or high. When this option is selected, the control weight is fetched from the control form.
-   **Script**: User-defined formula to calculate the score. This option is available only to users with the sn\_grc.developer role.

</td></tr><tr><td>

Qualitative script variables

</td><td>

Format of the script and the variables used in the script. This field is available only when **Script** is selected from the **Qualitative scoring logic** field.

</td></tr><tr><td>

Qualitative script

</td><td>

User-defined script to compute the scoring logic. This field enables you to have more control over the score computation.

</td></tr><tr><td class="sub-head" colspan="2">

Section Labels

</td></tr><tr><td colspan="2">

This section appears only when **Configure section terminology** is selected in the RAM form.

 **Note:** Section label renaming applies only to the advanced risk assessment interface while leaving the terminology used in reports, dashboards, heatmaps, and other areas unchanged.

</td></tr><tr><td>

Title

</td><td>

Option to rename the section title of the assessment type. For example, if you rename Control assessment as Preventive assessment, the new title will be displayed in all sections where the Control assessment was previously referred.

</td></tr><tr><td>

Score label

</td><td>

Option to rename the qualitative score label in the Scoring section of the assessment form. For example, if you rename Control risk as Preventive risk, the new score label will be displayed in the scoring section where Control risk was previously referred.

</td></tr></tbody>
</table>**Parent Topic:**[Configure a control effectiveness assessment](../task/configure-control-assess.md)

