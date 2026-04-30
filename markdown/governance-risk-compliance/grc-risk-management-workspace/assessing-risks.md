---
title: Assess risks and objects on an assessment instance
description: Assess the risks that you have configured and reassign the risks to relevant approvers.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Assess risks and objects on an assessment instance

Assess the risks that you have configured and reassign the risks to relevant approvers.

## Before you begin

Role required: sn\_grc.business\_user

**Note:** You must manually assign the advanced risk assessment roles to the sn\_grc.business\_user role. To understand how you can adjust granting of roles and groups, see the [How to adjust granting of roles and groups to use background jobs \[KB0963693\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0963693) article in the Now Support Knowledge Base.

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Risk Assessment Tasks** &gt; **My Tasks**.

    The assessment is in the **Ready to assess** state.

2.  To begin the assessment, click **Assess**.

    The work flow moves to the first risk assessment type. If a particular assessment type is not configured, then that section does not appear on the form.

3.  To reassign an assessment, click **Reassign** and enter the name of the person who you want to reassign the assessment to.

4.  Click the Inherent Assessment section and answer the questions on the form.

    1.  Right-click and save the form.

    2.  To move to the next assessment, click **Inherent Assessment** and fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Results|
        |Computed inherent risk|Inherent risk score.|
        |Override computed score|Option to override the computed inherent score.|
        |Computed inherent ALE|Computed inherent ALE of the risk. The ALE is calculated based on the inherent assessment factors.|
        |Override inherent risk|Value that was configured in the RAM form to override the computed inherent risk score. This field is available only when the **Override computed score** option is selected.|
        |Override inherent ALE|Value that overrides the computed inherent risk score. The value is used for rollup.|
        |Comments|Additional information that provides more details for the risk assessment approver. Users must enter a reason for overriding the computed score. This field is required when the **Override computed score** option is selected.|

    3.  If necessary, add comments in the **Comments** column.

    4.  Click **Save and calculate**.

5.  To perform control assessment, click **Perform control assessment** and do the following.

    1.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Results|
        |Computed control effectiveness|Control effectiveness score.|
        |Override computed score|Option for overriding the computed control effectiveness score.|
        |Comments|Additional information that provides more details for the risk assessment approver. This field is required when the **Override computed score** option is selected.|

        **Note:** If you have selected **Individual assessment of controls** in the **Calculate based on** field in the Control Assessment form, then you can create controls from the library, add existing controls, add new controls, or remove existing controls. Use guidance text for assistance in answering the factors. To determine if the control is compliant, see the Status column.

    2.  To create, add, or remove controls, perform one of the following actions:

<table id="table_cmb_4vc_h4b"><thead><tr><th>

Choice

</th><th>

Action

</th></tr></thead><tbody><tr><td>

To create controls from the library

</td><td>

1.  Click **Create From Library** from the Choose Controls window.
2.  Select the necessary control objectives.
3.  Click **Add controls**.


</td></tr><tr><td>

To add an existing control

</td><td>

1.  Click **Add**.
2.  Select the controls.
3.  Click **Add controls**.


</td></tr><tr><td>

To create a new control

</td><td>

1.  Fill in the fields in the New Control window.
2.  Click **Submit**.


</td></tr><tr><td>

To remove any control

</td><td>

1.  Click **Remove** from the Choose Controls window.
2.  Select the controls that you want to remove.
3.  Click **Remove controls**.


</td></tr></tbody>
</table>        If the risk has default controls, then those controls are automatically added to the control assessment.

    3.  If you do not have any controls that are associated with the risk or object that you must assess, then select the **No mitigating controls to assess** option.

        If you choose not to assess the mitigating controls, then the residual risks are by default marked as not applicable in the residual assessment stage. However, if a risk has associated mitigating controls, then the users do not see the **No mitigating controls to assess** option.

    4.  If you opt out of assessing controls, enter a justification in the **Comments** field.

    5.  Click **Save and calculate**.

6.  To move to the next assessment, click **Perform residual assessment** and do the following.

    1.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Results|
        |Computed residual risk|Residual risk score.|
        |Comments|Additional information that provides more details for the risk assessment approver. This field is required when the **Override computed score** option is selected.|

        **Note:** You can add existing controls and new controls during this stage. You can also remove controls that you might have wrongly added. The factors that appear for residual assessment are the factors that you have configured in the factor form. The answers that you provide for these factors determine the control assessment score. The score is based on the qualitative weight, qualitative score, and quantitative score.

    2.  If you want to assess a residual risk but you have opted not to assess mitigating controls, then clear the **Residual risk not applicable** field.

        If you do not want to assess a residual risk, then do not change the field.

    3.  Right-click and save the form.

7.  To move to the next state and respond to the risks that you have assessed, click **Respond**.

    1.  In the **Risk Response** tab, click **Risk response** and select one or more risk responses from the following options:

        -   **None**: Do not select any response for the risk.
        -   **Accept**: Accept and acknowledge the risk.
        -   **Avoid**: Eliminate the risk or its impact.
        -   **Mitigate**: Lessen the impact or probability of the risk.
        -   **Transfer**: Transfer the responsibility to a third party.
    2.  Right-click and save the form.

    If multiple risk responses are selected, risk response tasks are created.

8.  Click the Risk Response task related list, assign the task to an appropriate user, and right-click to save the form.

    This related list only appears when the **Enable risk response** option is selected by the risk administrator during the RAM configuration.

9.  In the **Comments** field, enter comments.

10. To view the activities for this assessment, click **Activity Journal**.

11. To finish your assessment and send it for approval, click **Save** and then click **Request Approval**.

    The approver that you have selected in the risk assessment scope gets an email notification to approve or reject the risk assessment instance. If there are no approvers, the risk assessment instance moves to the Monitor state.


## What to do next

To view the summary of the assessment, click **Assessment Summary**.

**Parent Topic:**[Perform Advanced Risk Assessment](../concept/use-advanced-risk-assessment.md)

