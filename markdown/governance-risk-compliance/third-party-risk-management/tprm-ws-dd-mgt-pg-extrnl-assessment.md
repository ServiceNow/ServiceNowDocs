---
title: Third-party \(external\) risk assessment management
description: After the IRQ process is complete, you send questionnaires and document requests to the third-party contact. You manage the third-party risk assessment by working with the contacts to help ensure that the responses are complete and accurate.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Third-party \(external\) risk assessment management

After the IRQ process is complete, you send questionnaires and document requests to the third-party contact. You manage the third-party risk assessment by working with the contacts to help ensure that the responses are complete and accurate.

## Accessing an external assessment

On the Due diligence management page, select the **DDR** number for any engagement due diligence request and the select the **External assessments** tab. The tab displays the list of all third-party risk assessments \(external due diligence processes\) for the selected engagement request.

![List of third-party risks assessments.](../image/tprm-ws-dd-mgt-tp-assesment.png)

## Working on a third-party risk assessment

For each external risk assessment, the system auto-assigns a unique ID number that starts with the text VRA. A risk assessment can represent the work on an engagement request for a third-party organization or an engagement request for a group within the parent organization. Select a VRA number to work on the risk assessment on the **External assessments** tab.

![Overview of a third-party risk assessment— external due diligence — process.](../image/tprm-ws-dd-mgt-tp-assess-risk-ovw.png)

## Actions on any tab

<table id="table_dld_1dt_fyb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Discuss

</td><td>

Select **Discuss** to send a message to other users. The message is recorded in the **Activity** section of the **Details** tab.

</td></tr><tr><td>

Create

</td><td>

Create an issue or task as describe in the following sections.

</td></tr><tr><td>

Save

</td><td>

Select **Save** to save any change you made to a value on any tab.

</td></tr><tr><td>

Submit to third party

</td><td>

Submit all questionnaires and document requests to the TP contact. The action is recorded in the Activity section on the **Details** tab.

</td></tr><tr><td>

… Delete

</td><td>

Select **Delete** to delete the record of the engagement request.

</td></tr><tr><td>

Adding an attachment

</td><td>

Select **Browse** in the **Attachments** section or select the attachment icon to select and add an attachment.

</td></tr></tbody>
</table>## Working on third-party risk assessments

-   **Risk overview tab on the External assessments page**
    -   The symbols indicate the current state of the external assessment process for the engagement request. See [Life cycle states of a external assessment](../../grc-vendor-risk/concept/tprm-external-assessment-lifecycle.md) for descriptions of the states.

        ![Symbols identify the state of the third-party risk assessment process.](../image/tprm-ws-vra-stage-indicators.png)

    -   **Overview** section: List of assessments that are associated with the engagement.
    -   **Questionnaires and document requests** section: List of questionnaires and document requests for the engagement.
    -   **Fourth-party questionnaires** section: List of questionnaires and document requests for fourth parties and their sub-parties that are associated with the engagement.
    -   **Tracking** section: Count of assessments associated with the third party that are in the **Open**, **Overdue**, and **Closed** status.
-   **Details tab on the External assessments page**
    -   Third-party risk assessment section: General information on the third party plus schedules for the overall assessment and questionnaire due dates from the engagement due diligence request.
    -   The **Compose section** on the **Details** tab enables you to permanently add text to the record. The Activity section is updated with any actions on issues and tasks, submissions to TP contacts, and also with work notes and comments that users add to the record. Add text in the following fields as needed:

        -   **Work notes \(Private\)**: Information about the third-party risk assessment. Work notes are visible only to internal users who are assigned to the process.
        -   **Comments**: Comments about the third-party risk assessment are visible both to internal users and to third-party contacts.
-   **Questionnaire templates tab on the External assessments page**

    The tab lists the questionnaires that the third-party contact will respond to. Select a name to view the details. For more information, see [Create a questionnaire or document request template](../../grc-vendor-risk/task/create-questionnaire-template.md) and [Create a questionnaire or document request template using the Designer](../../grc-vendor-risk/task/create-question-template.md).

    To enable TPR assessors to modify responses, configure the **Allow TPR assessors to modify responses in third-party questionnaires** \[`sn_svdp.allow_assessor_edit`\] system property. You can set the following options:

    -   Enable TPR assessors to answer questions or modify responses \(default\)
    -   Enable TPR assessors to modify responses
    -   Do not enable TPR assessors to answer questions or modify responses
    See [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md).

-   **Document templates tab on the External assessments page**

    The tab lists the requests for documents that the third-party contact should return. The information in the columns helps you to prioritize your work in following up with third-party contact. In particular, the state and percent complete values are key indicators. Select a name to view the details. For more information, see [Create a questionnaire or document request template](../../grc-vendor-risk/task/create-questionnaire-template.md) and [Create a questionnaire or document request template using the Designer](../../grc-vendor-risk/task/create-question-template.md).

-   **Fourth-party templates tab on the External assessments page**

    The tab lists the fourth-party questionnaires that the third-party contact will respond to. Select a name to view the details. For more information, see [Monitoring your fourth-nth parties](../../grc-vendor-risk/concept/tprm-monitor-fourth-parties.md).

-   **Third-party risk areas tab on the External assessments page**

    A risk domain defines the type of risk to assess for a third party. For example, you might want to assess a data-management third party in terms of security risk and a bank in terms of financial risk. Security risk and financial risk are risk domains. Some platform applications refer to risk domains as "risk areas." See [Define a third-party risk domain](../../grc-vendor-risk/task/tprm-risk-domain-define.md).

-   **Issues tab on the External assessments page**

    In an iterative process, before the TPR manager closes an assessment, the TPR manager can generate non-compliance issues and tasks. The TPR manager communicates with the TP contacts and engagement contacts by using comments to close the issues and tasks. The TPR manager can also assign different contacts as needed. See [Create an issue for a third party or engagement](../../grc-vendor-risk/task/tprm-ws-issue-create.md) and [Manage issues](../../grc-vendor-risk/task/tprm-ws-issue-manage.md).

-   **Tasks tab on the External assessments page**

    In an iterative process, before the TPR manager closes an assessment, the TPR manager can generate non-compliance issues and tasks. The TPR manager communicates with the TP contacts and engagement contacts by using comments to close the issues and tasks. The TPR manager can also assign different contacts as needed. See [Create a task for a third party or engagement](../../grc-vendor-risk/task/tprm-ws-task-create.md) and [Manage a task for a third party or engagement](../../grc-vendor-risk/task/tprm-ws-task-manage.md).


-   **[Life cycle states of a external assessment](../../grc-vendor-risk/concept/tprm-external-assessment-lifecycle.md)**  
The process of collecting assessment data from a third party moves between several states. For example, during the **Submitted to third party** state, the third party responds to tasks, issues, and works to complete the questionnaires.
-   **[Assessment metric type form](../../grc-vendor-risk/reference/tprm-create-q-template-form.md)**  
Use the assessment metric type form to capture all the information that you need to create a questionnaire template using the Third-party Risk Management application. As a third-party risk admin, you can create a questionnaire template.
-   **[Create new external assessment template form](../../grc-vendor-risk/reference/create-assess-template-form.md)**  
Use the external assessment template form to capture all the information that you need to create an external assessment template. As a third-party risk manager, you can create an assessment template.
-   **[Create New TPRM SAE questionnaire template form](../../grc-vendor-risk/reference/create-sae-q-template-form.md)**  
Use the Create New TPRM questionnaire template form to capture all the information that you need to create a TPRM SAE questionnaire template using the Smart Assessment template designer. As a third-party risk admin, you can create a questionnaire template.
-   **[Third-party risk assessment form](../../grc-vendor-risk/reference/tprm-create-assessment-form.md)**  
Use the third-party risk assessment form to capture all the information that you need to create an assessment using the Third-party Risk Management application. As a third-party risk assessor or manager, you can create an external assessment.
-   **[Third-party element form](tprm-tpe-form.md)**  
Use the third-party element form to capture all the information that you need to create a third-party element record using the Third-party Risk Management application. As a third-party risk manager, third-party risk assessor, or due diligence request owner, you can create a third-party element record.

**Parent Topic:**[Third-party Risk Management reference](../../grc-vendor-risk/concept/tprm-reference.md)

**Related topics**  


[Life cycle states of a external assessment](../../grc-vendor-risk/concept/tprm-external-assessment-lifecycle.md)

[Define a third-party risk domain](../../grc-vendor-risk/task/tprm-risk-domain-define.md)

[Manage issues](../../grc-vendor-risk/task/tprm-ws-issue-manage.md)

[Manage a task for a third party or engagement](../../grc-vendor-risk/task/tprm-ws-task-manage.md)

[Assessment metric type form](../../grc-vendor-risk/reference/tprm-create-q-template-form.md)

[Third-party risk assessment form](../../grc-vendor-risk/reference/tprm-create-assessment-form.md)

[Third-party element form](tprm-tpe-form.md)

