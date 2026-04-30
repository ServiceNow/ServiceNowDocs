---
title: Automate actions upon risk intelligence updates
description: A provider-based submission rule is a set of conditions and actions. In a rule, you can specify that an update to a rating from a risk intelligence provider is the condition that triggers the action that is specified in the rule. The action might be to create and send a third-party risk assessment, issue, task, or email.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Scores from risk intelligence providers, Integrate, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Automate actions upon risk intelligence updates

A provider-based submission rule is a set of conditions and actions. In a rule, you can specify that an update to a rating from a risk intelligence provider is the condition that triggers the action that is specified in the rule. The action might be to create and send a third-party risk assessment, issue, task, or email.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer

## About this task

When you enter a rating from a risk intelligence provider, the system normalizes the value to convert it to the appropriate TPRM rating. When you enter a score from a risk intelligence provider, the TPRM generates both a normalized rating and a normalized numerical score.

Follow this procedure to define a rule to perform an action when a provider sends an updated rating or score.

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Assessment Submission Rules** &gt; **Provider-based Submission**.

2.  Select **New** and then fill in the form.

<table id="table_epy_qrq_f5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider service

</td><td>

Select the scoring service from the risk intelligence provider that is associated with the rule.

</td></tr><tr><td>

Order

</td><td>

Enter the execution order for the rule. If multiple rules are defined for the same risk intelligence provider, only the rule with the lowest **Order** value is executed.

</td></tr><tr><td>

Name

</td><td>

Auto-generated name of the rule.

</td></tr><tr><td>

-   Change type
-   Extent of change
-   Normalized percentage/Normalized score/Normalized risk rating


</td><td>

Select the basis for the external score change that should trigger the rule and the extent of change, as follows:

-   If Change type = Normalized percentage, select **Increased risk by** or **Decreased risk by**, and the percentage in the **Normalized percentage** field.
-   If Change type = Normalized score, select **Increased risk by**, **Decreased risk by**, or **Threshold**, and a score in the **Normalized score** field.
-   If Change type = Normalized rating, enter a risk rating threshold that will trigger the rule in the **Normalized risk rating** field.


</td></tr></tbody>
</table>3.  Select the **Apply to third parties** tab.

    1.  Use the [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) to define conditions for identifying the third parties to be affected by the rule.

    2.  Select **Submit**.

4.  Select the **Rule Actions** tab, fill in the fields, and then select **Submit**.

    ![Options on the Rule Actions tab.](../image/prov-based-submission-rule-actions.png)

<table id="table_btn_fkf_4mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create assessment

</td><td>

Select this check box to create an assessment for the third parties identified on the **Apply to third parties** tab. If you also select the **Auto submit to third party** check box, the assessment is automatically sent to the third parties when the rule is triggered.

</td></tr><tr><td>

Create issue

</td><td>

Select this check box to create an issue for the third parties identified on the **Apply to third parties** tab. If you also select the **Auto submit to third party** check box, and you have selected a template from the **Issue template** field, the issues are auto-generated for the third parties when the rule is triggered.**Note:** To enable to auto-generation, you must verify that the following three fields are completed when the issue is created:

-   **Vendor**
-   **Recommendation** \(on the **Recommendations** tab\)
-   **Explanation** \(on the **Recommendations** tab\)


</td></tr><tr><td>

Create task

</td><td>

Select this check box to create a task for the third parties identified on the **Apply to third parties** tab.

 If you also select the **Auto submit to third party** check box, and you have selected a template from the **Task template** field, the tasks are automatically created for the third parties when the rule is triggered.

</td></tr><tr><td>

Assessment template

</td><td>

If you selected the **Create assessment** check box, select the assessment template to be used to create the assessments.

</td></tr><tr><td>

Issue template

</td><td>

If you selected the **Create issue** check box, you can optionally select an issue template to be used to create an issue for the third parties identified on the **Apply to Vendors** tab.

 If you also select the **Auto submit to third party** check box, you must select an issue template in order to automatically create an issue when the rule is triggered.

</td></tr><tr><td>

Task template

</td><td>

If you selected the **Create task** check box, you can optionally select a task template to be used to create a task for the third parties identified on the **Apply to Vendors** tab.

 If you also select the **Auto submit to third party** check box, you must select a task template in order to automatically create a task when the rule is triggered.

</td></tr><tr><td>

Auto submit to third party

</td><td>

Automatically submit assessments, issues, and/or tasks to the third parties identified on the **Apply to third parties** tab as described in the preceding field descriptions.

</td></tr><tr><td>

Send email/Recipients

</td><td>

When the rule is triggered, users with the TPR manager role receive an email notification. Select **Send email** and specify **Recipients** to send the email notification to other individuals.

</td></tr></tbody>
</table>
**Parent Topic:**[Integrating scores from risk intelligence providers](../concept/tprm-riskintelprvdr-overview.md)

