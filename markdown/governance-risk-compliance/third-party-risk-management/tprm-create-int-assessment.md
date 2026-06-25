---
title: Create an internal assessment
description: Create an internal assessment as part of a due diligence request or ongoing risk monitoring using Third-party Risk Management. An internal assessment can affect which questionnaires are later sent to the third party or engagement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-create-int-assessment.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Assess third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create an internal assessment

Create an internal assessment as part of a due diligence request or ongoing risk monitoring using Third-party Risk Management. An internal assessment can affect which questionnaires are later sent to the third party or engagement.

## Before you begin

The third-party risk \(TPR\) assessors must contact a team member with the TPR manager role to complete step 5.

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager or sn\_vdr\_risk\_asmt.vendor\_assessor

## About this task

When creating an on-demand internal assessment, TPR managers or TPR assessors can create the assessment and add the questionnaires. TPR managers can submit the assessment and the assigned respondents complete the assessment. You can select multiple respondents at a time and automatically trigger assessments.

**Important:** Smart assessments must be viewed in the Vendor Management Workspace.

## Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Third-party Risk Management** &gt; **Internal Risk Assessments** &gt; **All Assessments**.
    -   **Workspaces** &gt; **Vendor Management Workspace**, select the list icon \[Omitted image "ws-list-icon.png"\] Alt text: and then navigate to **Internal Risk Assessments** &gt; **All Assessments**.
2.  Create an internal assessment by selecting **New** and fill in the form.

    For descriptions of all these fields, see [Create new internal assessment form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/create-int-assess-form.md).

3.  Select **Submit**.

4.  Associate existing questionnaires with the assessment by performing one of the following.

<table id="choicetable_zqw_522_yfc"><thead><tr><th align="left" id="d376819e155">

Option

</th><th align="left" id="d376819e158">

Description

</th></tr></thead><tbody><tr><td id="d376819e164">

**Add a template in the Classic UI**

</td><td>

1.  Navigate to the Questionnaire templates related list.
2.  Select **Edit**, select the questionnaires you want to use, and then select **Save**.


</td></tr><tr><td id="d376819e188">

**Add a template in the Vendor Management Workspace**

</td><td>

1.  Navigate to the Questionnaire Templates tab.
2.  Select **Add**, select the questionnaires you want to use, and then select **Add**.
3.  Select **Save**.


</td></tr></tbody>
</table>    TPR administrators can create questionnaires and associate them with the assessment. For more information, see [Create a questionnaire or document request template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/create-questionnaire-template.md) and [Create a TPRM SAE questionnaire or document request template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/create-sae-q-template.md).

5.  Select **Submit**.

    This step can be completed by TPR managers.

    -   The state of the assessment changes to Awaiting response.
    -   The Respondents receive an email notification that includes a link to the assessment.

## What to do next

The owner assigned to the internal assessment works with the respondents to close the assessment. For information on how to respond to Internal assessments, see [Respond to an internal assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-irq-respond-to.md).

**Related topics**  


[Assessing your third-party risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-assessing-tpr.md)

[Respond to an internal assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-irq-respond-to.md)

[IRQ process management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-dd-mgt-pg-irq-tab.md)

