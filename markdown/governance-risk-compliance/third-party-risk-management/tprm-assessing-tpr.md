---
title: Assessing your third-party risk
description: Use Third-party Risk Management to identify and assess potential risks that are associated with your third-party relationships. The information gathered from internal questionnaires, external questionnaires, and documentation requests helps you to understand the third party's risk profile, determine the appropriate risk mitigation strategies, and determine whether the third party or engagement meets all necessary compliance requirements.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 14
breadcrumb: [Third-party Risk Management, Governance, Risk, and Compliance]
---

# Assessing your third-party risk

Use Third-party Risk Management to identify and assess potential risks that are associated with your third-party relationships. The information gathered from internal questionnaires, external questionnaires, and documentation requests helps you to understand the third party's risk profile, determine the appropriate risk mitigation strategies, and determine whether the third party or engagement meets all necessary compliance requirements.

## Responding to questionnaires

The following processes outline the timing and methods for responding to internal and external questionnaires:

-   **Inherent Risk Questionnaire \(IRQ\) process**

    The following infographic shows the IRQ process.

    ![Infographic that shows the IRQ process in the due diligence workflow. For the text description, refer to the process steps that follows.](../../grc-workspace-vrm/image/mmasset0020741-IRQ-process-landing.png)

    The following are the steps of the IRQ process.

    1.  After the due diligence request is approved by the Third-party risk \(TPR\) manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] or TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] that has been assigned as the owner of the due diligence request, they select an IRQ and attach it to an internal assessment.
    2.  The system sends out an email notification to the employee that has been assigned as the IRQ assessor \[snc\_internal\].
    3.  The IRQ assessor completes the internal assessment by responding to the IRQ.
    4.  After the IRQ assessor submits their responses and the TPR manager or owner reviews and closes the IRQ, the due diligence request state updates from IRQ in progress to IRQ in review.
    **Note:** Don’t change a questionnaire template after it has been sent out as part of an internal assessment. Instead, duplicate the template by making a copy and make your changes in the new copy. If you update a questionnaire after it has been sent out, the changes won't appear in the version shown to the IRQ assessor. To send an updated version, you must cancel the existing questionnaire by deassociating it from the internal assessment and then add the questionnaire using the updated template. For more information, see [Create a questionnaire or document request template](../task/create-questionnaire-template.md), [Create a questionnaire or document request template using the Designer](../task/create-question-template.md), [Create a TPRM SAE questionnaire or document request template](../task/create-sae-q-template.md).

    Based on the information gathered, the TPR manager and their team assess the potential risks that are associated with the engagement. They evaluate factors such as the financial stability, the operational capacity, the adherence to quality standards, the compliance with regulations, and the third party's ability to meet delivery timelines. This assessment helps the team to understand the third party's risk profile and to determine the appropriate risk mitigation strategies.

    For more information about IRQs or internal assessments, see [Create an internal assessment](../task/tprm-create-int-assessment.md) and [Respond to an internal assessment](../../grc-workspace-vrm/task/tprm-irq-respond-to.md).

-   **Third-party \(TP\) element collection process: Collect TP element information**

    The following infographic shows the TP element collection process.

    ![Infographic that shows the TP element collection process in the due diligence workflow. For the text description, refer to the process steps that follow.](../../grc-workspace-vrm/image/mmasset0020761-TP-element-process-vertical.png)

    The following are the steps of the TP element collection process.

    1.  After your due diligence request has completed the IRQ process, if TP elements are needed, the TPR manager or due diligence request owner selects **Start collection** and a collection task is created.
    2.  The TPR manager or owner assigns TP element questionnaires to an external assessment for collecting elements and sends that assessment to a third-party engagement to collect required information for TP elements.
    3.  The system sends out an email notification to the third-party engagement contact that has been assigned the TP element questionnaire.
    4.  After the third-party engagement contact submits their responses, the TPR manager or owner reviews and verifies all the required information was provided in the questionnaires.
    5.  The TPR manager or owner then navigates to the list of third-party elements and manually creates a third-party element record for each set of responses in each questionnaire.

        For more information, see [Create a third-party element record](../task/tprm-tp-element-create.md).

    6.  After all TP elements are created, the TPR manager or owner closes the collection task assessment. The system changes the state of the request from Collection in progress to Collection in review.
    7.  The internal stakeholders \(TPR assessor, TPR approver, TPR manager, or TPR administrator\) review and approve the element records.
    This is an optional process for collecting TP elements and assigning them to engagements so that they can be assessed as part of the overall due diligence workflow. For more information on TP elements, see [Monitoring third-party elements](tprm-monitor-tp-elements.md).

-   **Due diligence process: Compliance verification**

    The following infographic shows the due diligence process.

    ![Infographic that shows the due diligence process in the due diligence workflow. For the text description, refer to the process steps that follows.](../../grc-workspace-vrm/image/mmasset0020742-due-diligence-process-vertical.png)

    The following are the steps of the Due diligence process.

    1.  After the IRQ process or TP element collection process is completed, the TPR manager or owner selects questionnaires and requests for documentation to attach to external assessments for sending to the third party or engagement. For more information on creating assessments, see [Create an external assessment](../task/tprm-create-assessment.md) and [Third-party risk assessment form](../reference/tprm-create-assessment-form.md).

        **Note:** If you completed the optional TP element collection process, a questionnaire must be selected and assigned as part of an assessment for each third-party element you created. The TP element questionnaires are completed by the engagement contact.

    2.  The system sends out an email notification to the third-party and engagement contact that has been assigned each assessment.

        **Note:** Don’t change a questionnaire template after it has been sent out as part of an external assessment. Instead, duplicate the template by making a copy and make your changes in the new copy. If you update a questionnaire after it has been sent out, the changes won't appear in the version shown in the third-party portal. To send an updated version, you must cancel the existing questionnaire by deassociating it from the external assessment and then add the questionnaire using the updated template. For more information, see [Create a questionnaire or document request template](../task/create-questionnaire-template.md), [Create a questionnaire or document request template using the Designer](../task/create-question-template.md), [Create a TPRM SAE questionnaire or document request template](../task/create-sae-q-template.md).

    3.  After the third-party and engagement contacts submit their responses, the TPR manager or owner reviews and verifies all the required information was provided in the assessments. Issues and tasks are created if remediation or additional information is required.
    4.  The TPR manager or owner approves and closes each assessment.
    The TPR manager can develop assessment templates to simplify and automate the process of determining which questionnaires and document requests to send to a third party of this type. The TPR administrator can define questionnaire templates, document request templates, and then the TPR manager can group them into an assessment template. Your organization can reuse the template to send the questionnaires and document requests to similar third parties in future assessments. For more information about templates, see [Create an external assessment template](../task/create-vendor-risk-assess-temp.md), [Create a questionnaire or document request template](../task/create-questionnaire-template.md), and [Create a questionnaire or document request template using the Designer](../task/create-question-template.md).

    The TPR manager and their team use the third party's responses and internal analysis to determine whether the third party meets all the necessary compliance requirements. These requirements could include verifying the third party's compliance with applicable laws and regulations, such as environmental regulations, labor laws, and anti-corruption policies.

    **Note:** The third-party risk assessor, manager, or admin can answer questions, modify responses, and submit external questionnaires on behalf of third parties or engagements. For more information, see [Respond to a questionnaire for a third party or engagement](../task/tprm-respond-for-tp.md).

    Due to the sensitive nature of the items involved, the TPR manager and their team evaluate the third party's data security and privacy practices. They assess the third party's information security measures, data protection policies, access controls, and vulnerability management processes. If the third party has access to proprietary information or customer data, they might require the third party to undergo a cybersecurity audit or provide evidence of their data protection measures.

    For more information about reviewing responses, see [Review responses to external questionnaires](../../grc-workspace-vrm/task/tprm-ws-assessment-rvw-response.md).

    **Note:** Your TPR assessor can export received or returned questionnaires to Microsoft Excel spreadsheets. This option enables your organization to use the spreadsheet environment to review the questions and answers. For more information about exporting questionnaire responses, see [Export questionnaire responses to a spreadsheet](../task/export-q-and-a-to-excel.md).


## Pre-populate questionnaires with responses

The TPR manager or TPR assessor can pre-populate questionnaires for third parties and engagements with responses from complete questionnaires associated with the same third party. After sending out the assessment, the questionnaire is pre-populated with all responses from the most recent completed version of that questionnaire, regardless of whether the original associated assessment is completed. This is helpful for questionnaires where responses are expected to remain consistent, expediting the process and enabling third-party contacts to review and update responses only if necessary. For more information on creating assessments, see [Create an external assessment](../task/tprm-create-assessment.md).

**Important:** When the TPR manager or TPR assessor adds a questionnaire to an assessment, they have the option to select or deselect the Include previous responses option on the questionnaire page. The option can’t be changed after the questionnaire is sent to the third party. For more information, see [Create a questionnaire or document request template](../task/create-questionnaire-template.md) and [Assessment metric type form](../reference/tprm-create-q-template-form.md).

When a third-party or engagement contact opens a pre-populated questionnaire in the Third-party portal, they receive a notification that the responses were copied from an earlier questionnaire. The notification includes a link to the assessment that supplied the responses and its last updated date as shown in the following example.

![Notification that the responses are copied from an earlier questionnaire.](../image/tprm-pre-populate-q-aire.png)

Limitations:

-   Some question types and their responses can’t be pre-populated such as the attachment, duration, and signature question types. These question responses remain blank and previous responses aren’t included.
-   Responses are copied from the original assessment \(Assessment A\) to the newer assessment \(Assessment B\) one time. This copying occurs when Assessment B is submitted to a third party or an engagement. Any changes you make to Assessment A afterward won't be reflected in Assessment B. Both assessments remain separate.

## Issues and tasks

The role of TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] is required to create and manage both tasks and issues.

The TPR manager, TPR assessor, or contract negotiator can create tasks to help ensure that a team member or the third-party contact responds to concerns about the questionnaire responses or requested documents. They can manage existing tasks to verify that the assigned team member or third-party contact responds to a task and updates it as needed. For more information about creating and managing issues, see [Create a task for a third party or engagement](../task/tprm-ws-task-create.md) and [Manage a task for a third party or engagement](../task/tprm-ws-task-manage.md).

The TPR manager, TPR assessor, or contract negotiator can create an issue to help ensure the teams concerns about a third party or engagement are remediated. They can also manage the existing issues to verify that they’re understood, shared with the correct persons, and are acted on as needed. For more information about creating and managing tasks, see [Create an issue for a third party or engagement](../task/tprm-ws-issue-create.md) and [Manage issues](../task/tprm-ws-issue-manage.md).

## Additional assessment actions

The TPR manager, due-diligence request owner, or contract negotiator may need to reopen an assessment because there’s new information available that impacts the engagement or some other change has occurred. For more information, see [Why you conduct due diligence](vrm-due-diligence-why.md).

If the TPR manager, due-diligence request owner, or contract negotiator must gather more information from an engagement, they can send out an additional questionnaire or document request by reopening an assessment and doing the following actions:

1.  Navigate to the Due diligence request record page by selecting the relevant **DDR** number.
2.  View the related third-party risk assessment by selecting the **VRA** number on the **External assessments** tab.
3.  Select **Re-open**.

The due diligence request state updates from Ready for TPRM approval to Due diligence. The TPR manager, owner, or contract negotiator can request questionnaires and document requests as needed. For more information, see [Reopen an assessment](../task/trpm-reopen-assessment.md).

If the TPR manager, due-diligence request owner, or contract negotiator doesn’t require an assessment for an ongoing engagement or requires a quick close for onboarding or renewing an engagement, they can cancel an assessment by doing the following actions:

1.  Navigate to the Due diligence request record page by selecting the relevant **DDR** number.
2.  View the related third-party risk assessment by selecting the **VRA** number on the **External assessments** tab.
3.  Select **Cancel**.

Even if one or all assessments are canceled, the due diligence request proceeds to the Approval process.

