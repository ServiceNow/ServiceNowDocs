---
title: Create an external assessment
description: Create an assessment and initiate the third-party risk assessment life cycle using Third-party Risk Management. An external assessment specifies the details for the third party or engagement and defines the plan for completing the assessment.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Assess third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create an external assessment

Create an assessment and initiate the third-party risk assessment life cycle using Third-party Risk Management. An external assessment specifies the details for the third party or engagement and defines the plan for completing the assessment.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager or sn\_vdr\_risk\_asmt.vendor\_assessor

## About this task

Assessments can be created on-demand or can recur on a specified schedule. When creating an on-demand external assessment, Third-party risk \(TPR\) managers or TPR assessors select the questionnaire template or document request template and the third party. You can select multiple third parties at a time and automatically trigger assessments.

## Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Third-party Risk Management** &gt; **External Risk Assessments** &gt; **All Assessments**.
    -   **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **External Risk Assessments** &gt; **All Assessments**.
    **Important:** Smart assessments must be viewed in the Vendor Management Workspace.

2.  Create an external assessment by selecting **New** and fill in the form.

    For descriptions of all these fields, see [Third-party risk assessment form](../reference/tprm-create-assessment-form.md).

3.  Select **Submit**.

    Additional related lists appear. If you left the **Assessment template** field empty and want to use assessment templates to associate multiple questionnaires or document requests with this assessment, use the Questionnaires or Document Requests related lists.

4.  Associate existing questionnaires or document requests with the assessment, by performing the following steps.

    1.  Open the Questionnaires or Document Requests related list.

    2.  Select Edit, select the questionnaires or document requests to use, and then select Save.

    3.  Repeat for the other type of questions, if needed.

    TPR administrators can create questionnaire or document request templates and associate them with the assessment. For more information, see [Create a questionnaire or document request template](create-questionnaire-template.md).

5.  Select **Submit to third party**.

    **Important:** When the TPR manager or TPR assessor adds a questionnaire to an assessment, they have the option to select or deselect the Include previous responses option on the questionnaire page. The option can’t be changed after the questionnaire is sent to the third party. For more information, see [Create a questionnaire or document request template](create-questionnaire-template.md) and [Assessment metric type form](../reference/tprm-create-q-template-form.md).

    -   The state of the assessment changes to Submitted to third party.
    -   The templates that you selected generate questionnaires or document requests.
    -   If the Include previous responses option is selected for a questionnaire, then previous responses are copied and added to the outgoing questionnaire. The notification in the Third-party portal includes the number, name, and last updated date of the previous assessment that supplied the responses. The notification also includes a link to the assessment.
    -   The primary third-party contact receives an email notification that includes a link to the assessment in the Third-party portal.

        **Note:** When you use the Include previous responses option, responses are copied from the original assessment \(Assessment A\) to the newer assessment \(Assessment B\) one time. Any changes you make to Assessment A afterward won't be reflected in Assessment B. Both assessments remain separate.

6.  When the third-party contact is ready to respond to the assessment, they open the assessment in the Third-party portal.

    **Note:** If your questionnaire is set up to require a signature, the third party or reviewer must save and e-sign the questionnaire or document request before it can be submitted. The signature feature isn’t supported for SAE questionnaires. For more information, see [E-signatures on questionnaires or document requests](../../grc-workspace-vrm/task/tprm-ws-approve-with-e-sig.md).

7.  The TPR assessor moves the state of the assessment to Generating Observations.

    During this time, the TPR assessor can navigate to the Risk overview tab, in the Questionnaires and document requests section, select the **Name** or **Questionnaire instance** to view the responses. In the classic engine they can provide comments or change responses, as necessary.

    For any problems that arise, the TPR assessor creates an issue to track the remediation process \(Finalizing with third party\).

8.  The TPR assessor moves the assessment to the Closed state.


## What to do next

The TPR assessor works through the third-party portal with the third party to close the assessment.

**Related topics**  


[Assessing your third-party risk](../concept/tprm-assessing-tpr.md)

[Review responses to external questionnaires](../../grc-workspace-vrm/task/tprm-ws-assessment-rvw-response.md)

