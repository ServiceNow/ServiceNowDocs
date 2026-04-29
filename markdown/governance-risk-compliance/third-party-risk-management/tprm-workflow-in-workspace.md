---
title: Due diligence workflow
description: The Third-party risk management \(TPRM\) processes provide a consistent framework for your third-party risk management program. You can customize the workflow processes to meet your organization's needs.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Explore, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Due diligence workflow

The Third-party risk management \(TPRM\) processes provide a consistent framework for your third-party risk management program. You can customize the workflow processes to meet your organization's needs.

## Processes in the due diligence workflow

Each task in a process must be completed before the next task can be started. The roles of the users that perform the various tasks are described in [Roles in Third-party Risk Management](../../grc-vendor-risk-implementation/reference/tprm-roles.md). The following diagram describes the due diligence workflow.

![Infographic that shows where the processes in the due diligence workflow are performed. For the text description, refer to the workflow steps that follow.](../image/mmasset0020705-due-diligence-workflow-horizontal.png "Due diligence workflow")

-   **Request process: Ask to start a new engagement, reassess, or offboard an existing one**

    1.  An employee at your organization requests due diligence for a third-party engagement.
        1.  The employee logs in to Employee Center on their instance. They open the due diligence request form and specify the name of the third party and the reason for the request:

            -   Onboard a new engagement
            -   Reassess a risk for an existing engagement
            -   Reassess an existing engagement to prepare for a contract renewal
            -   Offboard an engagement with due diligence
            -   Offboard an engagement with no due diligence
            **Note:** When offboarding an engagement with no due diligence the TP element collection and Due diligence process are not applicable.

        2.  The employee provides details about the third party and engagement. The information includes the product or service that should be assessed in this engagement, the user who will respond to the Inherent Risk Questionnaire assessor \(IRQ\), and the third-party \(TP\) contact or engagement contact who will respond to the external questionnaires.
        3.  At any time, an external risk intelligence provider might update the risk data for the third party because a Third-party risk \(TPR\) manager might have integrated the services of a risk intelligence provider while configuring the application.
        4.  The employee submits the form.
        5.  The system sends out an email notification to the employee who made the request.
        6.  The system sends an email notification to the Due diligence request assignment group. A member of the group can assign a TPR manager or TPR assessor to act as the owner of the request. This action triggers a task for the TPR manager.
    2.  The TPR manager scopes the request, updates it as needed, and then approves or rejects it.
        1.  The TPR manager logs in to the Vendor Management Workspace and navigates to the due diligence management page, where they review and update the request:
            -   The TPR manager reviews the person who was suggested as the IRQ assessor. If needed, they can specify a different person as the IRQ assessor.
            -   The TPR manager can start a discussion with the requester and other users by selecting **Discuss**. The message is recorded in the Activity section of the **Details** tab.
        2.  The TPR manager either rejects or approves the request. If the TPR manager accepts the request, the IRQ process starts.

    **Note:** TPR assessors can create recurring third-party assessments to reassess a risk on a regular schedule. For more information, see [Configure a risk assessment to recur on a schedule](../../grc-vendor-risk/task/define-repeating-vend-assess.md) and [Event-driven management — automate assessment processes](../task/tprm-event-drvn-mgt-rule-create.md).

-   **IRQ process: Scope the risk**

    1.  The TPR manager reviews and approves the IRQ.
        1.  In the Vendor Management Workspace, the TPR manager reviews and approves the IRQ from a list on the system.

            The TPR administrator can create custom IRQs for an organization. The content of each IRQ is created and maintained by the person responsible for the business area, geography, or third party. To define an IRQ, the TPR administrator adds sample questions to a questionnaire template and modifies them as needed. The sample questions are provided in the base system. Defining an IRQ is a no-code process.

            **Tip:** The TPR manager can use the answer to a question in an IRQ to determine the questionnaires that are sent to the third party that is being assessed. This feature is available only if the Third-party Risk Management application has been activated.

            For more information, see [Set up internal questionnaire responses to automatically attach external questionnaires to assessments](../task/tprm-setup-eq-irq.md).

        2.  The TPR manager either rejects the due diligence request or approves it. When the request is approved, the system sends the IRQ to the IRQ assessor, which is an internal stakeholder at an organization.
        3.  The IRQ assessor is notified of the IRQ both by email and by a new task in their queue.

            **Note:** The system can also auto-send third-party risk assessments when changes to a risk score occur.

    2.  Internal users respond to the IRQ:
        1.  In the Employee Center, any user interested in the engagement opens and responds to the IRQ.

            Several answers generate further clarifying questions. The answers can determine which external questionnaires are auto-generated and added to the sets for the TP and engagement contact.

            For example, if an IRQ assessor responds that the third party interacts with government officials as part of the engagement, an anti-bribery questionnaire appropriate to the third party's country is included \(ABAC in the USA or FCBA in the EU\).

        2.  The IRQ assessor submits the completed IRQ. This action triggers a task for the TPR manager.
    3.  The internal stakeholders \(third-party assessment reviewer, TPR assessor, TPR approver, TPR manager, or TPR administrator\) review the IRQ responses:
        1.  In the Vendor Management Workspace, the users review the IRQ responses.
        2.  The TPR manager might ask the IRQ assessor for clarification and then either rejects or approves the IRQ responses.
        3.  If an internal stakeholder user approves the IRQ responses, they move to the next process by closing the engagement request.
    **Note:** After the IRQ process enters the IRQ in progress state, you can request risk intelligence reports associated with your due diligence request. For more information, see [Using risk intelligence reports and scores](../../grc-vendor-risk/concept/tprm-riskintel-using.md) and [Request a risk intelligence report associated with a due diligence request](../../grc-vendor-risk/task/tprm-riskintel-request-dd.md).

-   **TP element collection process: Collect third-party element information \(Optional\)**
    1.  The TPR manager or due diligence request owner starts the third-party element collection.
        1.  In the Vendor Management Workspace, if third-party elements are needed the TPR manager or owner selects **Start collection** and a collection task is created.
        2.  The TPR manager or owner navigates to the collection task tab and assigns the relevant third-party element collection questionnaires to the external assessment.

            **Note:** As part of the base system, sample questionnaires for collection and assessment are available for third-party elements classified as a Facility, Principal, Products, or Other.

        3.  The TPR manager or owner reviews and approves the questionnaires and they're sent to the third party.
    2.  The system sends out an email notification to persons at the third party. The messages notify the third-party contact to respond to the third-party element collection questionnaires.
    3.  In the Third-party portal, the third-party contacts either respond to the questionnaires directly or assign the tasks to other contacts at the organization.

    4.  The third-party contact returns the completed questionnaires.
    5.  The system changes the state of the assessment to **Responses received** and sends alerts to the TPR manager and owner.
    6.  In the Vendor Management Workspace, the TPR manager or owner opens the questionnaires and verifies all the required information was provided.
    7.  The TPR manager or owner then navigates to the list of third-party elements and manually creates a third-party element record for each set of responses in the questionnaire.
    8.  After all third-party elements are created, the TPR manager or owner closes the assessment.
    9.  The system changes the state of the request to **Collection in review**.
    10. The internal stakeholders \(TPR assessor, TPR approver, TPR manager, or TPR administrator\) review and approve the element records.
    11. In the Vendor Management Workspace, the TPR manager or owner opens the engagement and manually adds elements to the **Engagement elements** tab.
    12. After all third-party elements are assigned to an engagement, you can start the due diligence process.
-   **Due diligence process: Collect information to generate a risk score**

    1.  Either one of the following processes results in the selection of external due diligence questionnaires:
        -   In the Vendor Management Workspace, the TPR manager selects the questionnaires that the TP and engagement contacts respond to.
        -   The system auto-selects the questionnaires according to the configurations set to make the selections. For more information on how to configure external questionnaires to be selected based on internal questionnaire responses, see [Set up internal questionnaire responses to automatically attach external questionnaires to assessments](../task/tprm-setup-eq-irq.md).
        -   The system auto-selects the questionnaires according to the business rules that were defined to make the selections.
    2.  Regardless of the selection method that you used in step 1, two external due diligence questionnaires are selected:

        -   One set collects information on the third-party organization. The TP contact responds to that questionnaire.
        -   The other set collects information on the business unit within the third-party organization that is the subject of the engagement. The engagement contact \(as specified in the due diligence request\) responds to that questionnaire.
        **Note:** If you completed the optional TP element collection process, a questionnaire must be selected and assigned as part of an assessment for each third-party element you created. The third-party element questionnaires are completed by the engagement contact.

    3.  In the Vendor Management Workspace, the TPR manager reviews the auto-selected questionnaires that the TP and engagement contacts respond to. The TPR manager validates or modifies the selections and then approves the set of questionnaires. For more information on creating external assessments, see [Create an external assessment](../../grc-vendor-risk/task/tprm-create-assessment.md).
    4.  The system sends out an email notification to persons at the third party. The messages notify the TP contact and engagement contact to respond to the external questionnaires.

        **Note:** Do not make any changes to a questionnaire template after it's already in use, you can duplicate the template instead by making a copy. If you make any changes to a questionnaire after it's been sent out as part of an external assessment, those updates won't show up in the questionnaire displayed in the third-party portal. For more information, see [Create a questionnaire or document request template](../../grc-vendor-risk/task/create-questionnaire-template.md) and [Create a questionnaire or document request template using the Designer](../../grc-vendor-risk/task/create-question-template.md).

    5.  In the Third-party portal, the TP and engagement contacts either respond to the questionnaires directly or assign the tasks to other contacts at the third-party organization.

        **Note:** The Third-party portal is fully isolated from your organization's instance.

        In an iterative process, before the TPR manager closes an assessment, the TPR manager can generate non-compliance issues and tasks. The TPR manager communicates with the TP contacts and engagement contacts by using comments to close the issues and tasks. The TPR manager can also assign different contacts as needed. For more information, see [Manage issues](../../grc-vendor-risk/task/tprm-ws-issue-manage.md).

    6.  The TP contact and engagement contact return the completed questionnaires.
    7.  The system changes the state of the request to **Ready for TPRM approval** and sends alerts to TPR managers.
    8.  In the Vendor Management Workspace, the TPR manager validates that the questionnaires are received, complete, and signed if necessary, and then closes the assessment phase to start the approval process.
    **Note:** If the third-party risk manager or owner selects the **Skip contract risk process** option during the due diligence process, the assigned contract negotiator isn't notified and the Contract risk process state is skipped. An approver and owner can update the **Skip contract risk process** selection until the approval process completes. For more information about this process, see [Due diligence request process management](../reference/tprm-ws-dd-mgt-pg-details-tab.md).

-   **Approval process: Internal stakeholder analyzes each aspect of risk**

    All internal stakeholders \(approvers\) review the questionnaire responses and supporting documents from the third-party and engagement contacts. If the responses are good, one or more approvers approves and then closes the DD request. If a contract will be prepared, the approved request moves to the Contract Risk process.

    -   Approvers can approve or reject the request and then close it.
    -   Closing the request moves it either to the contract risk process, or if no contract is involved, the engagement starts.
-   **Contract Risk process**

    After approval, all due diligence information can be made available for the contract negotiator. By using the Vendor Management Workspace, the contract negotiator accesses all the data that is generated during the preceding processes to design and settle the contract:

    -   The contract negotiator can skip the contract risk process if a contract is no longer required.
    -   The contract negotiator can request additional due diligence if it's required.
    -   If the contract negotiator successfully executes a contract with the third party, they can upload it and specify the contract is executed to automatically notify all the key stakeholders.
    -   The contract negotiator can specify that the contract isn't executed, and the third party won't be engaged for business.
    -   The contract negotiator can specify that the contract is terminated, and the third party won't be engaged for business.

**Note:** Starting with version 19.1.x of the Third-party Risk Management application, the tiering questionnaire and external assessment reminders workflows are deprecated and migrated to Workflow Studio. If you have customized these workflows, they won't be deprecated or migrated as part of this change.

