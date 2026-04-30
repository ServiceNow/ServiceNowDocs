---
title: Risk Assessment Methodology form
description: Use the Risk Assessment Methodology form in the Advanced Risk application to specify the types of risk assessments and the entities on which the risk assessment is performed.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-01-15"
reading_time_minutes: 6
breadcrumb: [Configure a risk assessment methodology, Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Risk Assessment Methodology form

Use the Risk Assessment Methodology form in the Advanced Risk application to specify the types of risk assessments and the entities on which the risk assessment is performed.

See the following table for a description of the field values.

<table id="table_l35_zwl_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the risk assessment methodology \(RAM\). For example, Organizational risk assessment.

</td></tr><tr><td>

Domain area

</td><td>

Domain area of the RAM. This field is automatically set to **IRM**.

</td></tr><tr><td>

State

</td><td>

State of the RAM. This field is automatically set to **Draft**.

</td></tr><tr><td class="sub-head" colspan="2">

Assessment Context

</td></tr><tr><td>

Assess

</td><td>

Assessment context that you can select:-   **Risk**: Performs the assessment for an entity and the risk statement that is related to it.
-   **Object**: Performs an assessment on any ServiceNow record. For example, users can perform an Exception Risk Assessment or a Change Risk Assessment directly on those respective tables.

</td></tr><tr><td>

Applicable entity classes

</td><td>

All entity classes that the RAM applies to, such as the business services, assets, or business applications. This field appears only when **Risk** is selected from **Assess**.

</td></tr><tr><td>

Applicable Record Types

</td><td>

Tables on which you want to perform the assessment. You can select multiple tables and associate them to the RAM. This field appears only when **Object** is selected from **Assess**.**Note:** You can add multiple objects or tables to a published RAM, but can’t remove them after the RAM is published.

</td></tr><tr><td class="sub-head" colspan="2">

Workflows

</td></tr><tr><td>

Inherent risk

</td><td>

Option for assessing an inherent risk.

</td></tr><tr><td>

Control effectiveness

</td><td>

Option for assessing the control effectiveness.

</td></tr><tr><td>

Enable risk response

</td><td>

Option to enable the **Risk Response** tab on the risk assessment. This option appears only when **Risk** is selected from **Assess**.

</td></tr><tr><td>

Residual risk

</td><td>

Option for assessing a residual risk.

</td></tr><tr><td>

Target risk

</td><td>

Option for assessing a target risk.

</td></tr><tr><td class="sub-head" colspan="2">

Rollup Configurations

</td></tr><tr><td colspan="2">

This section appears only when **Risk** is selected from **Assess**.

</td></tr><tr><td>

Calculate ALE based on

</td><td>

Formula that you can select for calculating the annual loss expectancy \(ALE\):-   **Sum**
-   **Average**
-   **Maximum**
-   **Minimum**

</td></tr><tr><td>

Calculate score based on

</td><td>

Formula that you can select for calculating the score:-   **Average**
-   **Maximum**
-   **Minimum**

</td></tr><tr><td class="sub-head" colspan="2">

Risk Response Configurations

</td></tr><tr><td colspan="2">

This section appears only when **Risk** is selected from **Assess**.

</td></tr><tr><td>

Enable risk response task workflow

</td><td>

Option to enable users to create, delete, remove, edit, and link risk response tasks within an assessment.

</td></tr><tr><td>

Allow single risk response

</td><td>

Option to make the risk response selection a single select in the risk assessment form. For example, the options could be "Accept," "Avoid," "Mitigate," or "Transfer." With a single select, assessors can choose only one of these options to indicate the risk response strategy.**Note:** This option can only be enabled when there are no ongoing assessments.

</td></tr><tr><td>

Allow issue linking with risk assessment

</td><td>

Option to create an issue or link an existing open issue with the risk assessment.

</td></tr><tr><td>

Risk response is required

</td><td>

Option to make a risk response as required: -   **None**: No risk response is required.
-   **Always**: Mandate a risk response always.
-   **On specific conditions**: Mandate a risk response based on specific conditions using the condition builder.
-   **On specific conditions defined using script**: Mandate a risk response under specific conditions using a predefined script or set of instructions.

</td></tr><tr><td class="sub-head" colspan="2">

Business Rules and Validations

</td></tr><tr><td>

Final comment is required

</td><td>

Option to make the final comments as required. Final comments provide better transparency and enable risk owners to communicate the action plan if there’s a breach of appetite or tolerance. The options are as follows: -   **None**: No final comment is required.
-   **Always**: Mandate final comments always.
-   **On breach of appetite**: Mandate final comments on the breach of appetite.
-   **On breach of tolerance**: Mandate final comments on the breach of tolerance.

 This field appears only when **Risk** is selected from **Assess**.

</td></tr><tr><td>

Automatically create issue

</td><td>

Option to create issues automatically. This field appears only when **Risk** is selected from **Assess**. -   **None**: Enables you not to create issues automatically.
-   **On breach of appetite**: Creates issues automatically on the breach of appetite.
-   **On breach of tolerance**: Creates issues automatically on the breach of tolerance.

 **Note:** The issues are created only after the risk assessment is approved and moved to the published state.

</td></tr><tr><td>

Residual score is lower than inherent

</td><td>

Option to validate that the qualitative residual score is lower than the inherent score. **Note:** This option appears only when the residual risk assessment is enabled.

</td></tr><tr><td class="sub-head" colspan="2">

Reference Information

</td></tr><tr><td colspan="2">

This section appears only when **Risk** is selected from **Assess**. Enabling these options shows the reference information in the risk assessment instance.

</td></tr><tr><td>

Show related risk events

</td><td>

Option for showing the related risk events on the risk assessment.

</td></tr><tr><td>

Show related risk indicators

</td><td>

Option for showing the related risk indicators on the risk assessment.

</td></tr><tr><td>

Show open issues

</td><td>

Option for showing the open issues on the risk assessment.

</td></tr><tr><td>

Show previous assessment

</td><td>

Option for showing the previous assessment on the risk assessment. This option helps the risk assessor to refer to the previous assessment and analyze the details of that assessment before taking another assessment.

</td></tr><tr><td class="sub-head" colspan="2">

Other Configurations

</td></tr><tr><td>

Advanced reminder \(days\)

</td><td>

Based on the due date of the risk assessment, this field is the number of days before a notification is sent to the assessor. For example, if you enter 3 in this field, then the assessor gets a reminder notification three days before the due date.

</td></tr><tr><td>

Overdue reminder \(days\)

</td><td>

Based on the due date of the risk assessment, this field is the number of days after this date that reminder emails are sent. For example, assume you enter 5 in this field. Then for five days after the due date is over, the assessor keeps receiving reminder emails that the due date is over. On the sixth day, an email notification is sent to the assessor and to the assessor's manager.

</td></tr><tr><td>

Risk identification

</td><td>

Method to identify risks in the risk assessment scope:-   **None**
-   **From Library**: Identifies risks from the library on the risk assessment.
-   **Ad-hoc**: Identifies a risk that is not in the library.
-   **From Library and Ad-hoc**: Creates risks as well as adds risks from the library.

</td></tr><tr><td>

Group factor comments

</td><td>

Option to enable group factor comments in the risk assessment form.

</td></tr><tr><td>

Copy previous responses

</td><td>

Option to copy the factor responses and comments whenever a reassessment is performed.

</td></tr><tr><td>

Allow override of results

</td><td>

Option to override the computed scores and the ALE during risk assessment.

</td></tr><tr><td>

Configure section terminology

</td><td>

Option to configure section labels for inherent, control, residual, and target assessments. After you select this option, you can configure the title, score label, and annual loss expectancy label for each assessment type.**Note:** Section label renaming applies only to the advanced risk assessment interface while leaving the terminology used in reports, dashboards, heatmaps, and other areas unchanged.

</td></tr><tr><td>

Update assessment results to source record

</td><td>

Option to copy the assessment results to the source record on which the assessment is performed. You can define the assessment result mapping for the applicable record types in the individual assessment types. This field appears only when **Object** is selected from **Assess**.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td colspan="2">

This section appears only when **Object** is selected from **Assess**.

</td></tr><tr><td>

Reassessment frequency

</td><td>

Option of how often the reassessment is performed:-   **None**
-   **Weekly**
-   **Monthly**
-   **Quarterly**
-   **Semi-annually**
-   **Annually**

</td></tr><tr><td>

Days to overdue

</td><td>

Based on the due date of the risk assessment, this field is the number of days after which an assessment is considered overdue.

</td></tr></tbody>
</table>**Parent Topic:**[Configure a risk assessment methodology](../task/configure-ram.md)

