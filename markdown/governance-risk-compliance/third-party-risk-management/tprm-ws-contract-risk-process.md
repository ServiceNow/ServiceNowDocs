---
title: Managing the contract risk process
description: Protect your organization's interests, as the Third-party risk contract negotiator, often the corporate counsel, by incorporating specific contractual provisions so that you can address the risks identified using the Third-party Risk Management application.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Third-party Risk Management, Governance, Risk, and Compliance]
---

# Managing the contract risk process

Protect your organization's interests, as the Third-party risk contract negotiator, often the corporate counsel, by incorporating specific contractual provisions so that you can address the risks identified using the Third-party Risk Management application.

If a contract is being negotiated with the engagement or third party, the due diligence request enters the Contract risk process state after all approvals have been processed. If you’re the assigned contract negotiator, you're notified through an automated email when all the approvals have been processed.

The following infographic shows the contract risk process.

![Infographic that shows the approval process in the due diligence workflow. For the text description, refer to the text that follows.](../../grc-workspace-vrm/image/mmasset0020744-contract-risk-process-horizontal.png)

**Note:** The \[sn\_vdr\_risk\_asmt.contract\_negotiator\] role is required and your contract negotiator performs all actions by using the Vendor Management Workspace or VRM Classic user interface.

You can view all pending **Due diligence requests for Negotiator**, **Tasks**, and **Issues** by navigating to the Task page.

To view the Task page, select **Workspaces** &gt; **Vendor Management Workspace**, and then select the tasks icon ![](../../grc-workspace-vrm/image/icon-tprm-ws-tasks.png).

To view your assigned requests, select **Due diligence requests for Negotiator**.

To view **Due diligence requests for Negotiator** in the VRM Classic user interface, select **All** &gt; **Self-Service** &gt; **Third-party Risk Management** &gt; **Due Diligence Requests** &gt; **My Requests in Contract Process**

From this view, you can accomplish the following tasks:

-   Review the internal questionnaire responses.

    Navigate to the Due diligence request record page by selecting the Due Diligence Request \(DDR\) number. You can view the related internal questionnaire responses by selecting the Internal assessment \(INA\) number on the **Internal assessments** tab. For more information, see [IRQ process management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-irq-tab.md).

-   Review the risk intelligence scores.

    Navigate to the Due diligence request record page by selecting the DDR number. You can view the related risk intelligence scores by selecting the **Risk intelligence scores** tab. For more information, see [Viewing risk intelligence scores](../../grc-workspace-vrm/reference/tprm-ws-tab-risk-intel-scores.md).

-   Review the external questionnaire responses and supporting documents.

    Navigate to the Due diligence request record page by selecting the DDR number. View the related external questionnaire responses and supporting documents by selecting the Third-party risk assessment \(VRA\) number on the **External assessments** tab. For more information, see [Third-party \(external\) risk assessment management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-extrnl-assessment.md).


**Note:** To learn more about the processes in the due diligence workflow, see [Due diligence workflow](../../grc-workspace-vrm/concept/tprm-workflow-in-workspace.md) for more information.

-   **Contract Risk process \(Only if the engagement is contracted\)**

    If the engagement includes a contract, as the contract negotiator, you prepare the contract and do the following actions:

    1.  Access all data that is generated during the Request, IRQ, Due Diligence, and Approval processes to design and settle the contract and assess the following items:
        -   Initial Inherent Risk Questionnaire \(IRQ\) responses and comments by the Third-party risk assessor. For more information, see [IRQ process management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-irq-tab.md).
        -   Risk data from the risk intelligence providers. For more information, see [Viewing risk intelligence scores](../../grc-workspace-vrm/reference/tprm-ws-tab-risk-intel-scores.md).
        -   Responses to third-party questionnaires and engagement questionnaires. For more information, see [Third-party \(external\) risk assessment management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-extrnl-assessment.md).
        -   Issues and tasks for the third-party contacts that were assigned to you by the Third-party risk manager. Assigned issues and tasks are listed on the tasks page.
    2.  After the contract is fully signed by all parties \(executed\), attach the contract and activate the engagement by selecting **Contract executed** and then complete the following actions from the **Details** tab on the due diligence request record page:
        1.  Set the **Contract start date** for the engagement.
        2.  Set the **Contract start date** for the third party if not set previously.
        3.  Set the **Contract expiration date** for the engagement to the requested end date.
        4.  Update the due diligence request's state from Contract risk process to Engagement contract executed.
    After the contract is executed, the **Contract start date** and **Contract expiration date** fields are read-only and available to view from the **Details** tab for the third party and engagement in the Vendor Management Workspace.

    **Note:** After opening an assigned task, select **Browse** in the **Attachments** section to select and add a contract. If you want the contract to appear in the Documents related list, select **Documents** and on the Documents page select **New** to add a new contract document or **Link Documents** to attach an existing contract document. For more information about the Document Management system, see [Document Management system in Third-party Risk Management](tprm-dms.md).


Follow the same process in step 2 to activate an engagement for due diligence requests, onboard an engagement, and reassess an engagement for contract renewal.

-   **Contract Risk process \(contract is skipped\)**

    If the engagement doesn’t require a contract, you can skip the contract by selecting **Skip contract** from the **Details** tab on the due diligence request record page.

    The following changes take place:

    1.  The **Contract start date** is changed to **Engagement start date**.
    2.  The **Contract end date** is changed to **Engagement expiration date**.
    3.  A required **Justification** field appears. Enter an explanation for skipping the contract.
    4.  The due diligence request's state is updated from Contract risk process to Contract risk process skipped.
    5.  After the owner closes the request, the engagement is **Active**.

**Note:** Skipping in this context is a way of intentionally not participating in the contract risk process that was initially scheduled or expected.

The following examples show the contract start and expiration date before and after you select the skip contract risk process.

![Contract start and expiration date before you select the skip contract risk process.](../image/before-click-skip.png "Example of the view before selecting the skip contract risk process")

![Engagement start and expiration date after you select the skip contract risk process.](../image/after-click-skip.png "Example of the view after selecting the skip contract risk process")

**Note:** If the third-party risk manager or owner selects the **Skip contract risk process** option during the due diligence process, the assigned contract negotiator isn’t notified and the Contract risk process state is skipped. An approver and owner can update the **Skip contract risk process** selection up until the approval process is completed. For more information about this process, see [Due diligence request process management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-details-tab.md).

The following example shows the available selections and where the required justification box appears.

![Selections and required justification field.](../image/contract-justification.png "Example of available selections and required justification")

-   **Contract Risk process \(Not contracted, onboarding engagement is rejected\)**

    If an issue can't be resolved or the due diligence request is canceled, you can reject the engagement by selecting **Not contracted** from the **Details** tab on the due diligence request record page.

    The following actions take place:

    1.  A required **Justification** field appears. You must enter an explanation for rejecting the engagement.
    2.  The due diligence request's state is updated from Contract risk process to Not contracted.
    3.  After the owner closes the request, the due diligence request changes from Not contracted to Rejected.
    4.  All stakeholders are notified that the engagement isn’t contracted and onboarding is rejected.
    The owner can reopen the request and the due diligence request's state will update to the Ready for TPRM approval state.


-   **Contract Risk process \(Contract terminated\)**

    When the engagement is being offboarded and a contract is no longer required, you can approve the termination of the contract by selecting **Contract terminated**. The following actions then take place:

    1.  The due diligence request's state is updated from Contract risk process to Contract terminated.
    2.  The **Termination date** is updated with the current date.

-   **Contract Risk process \(Contract not terminated\)**

    If the engagement is being offboarded \(relationship terminated\) and the contract can’t be terminated, you can reject the request by selecting **Contract not terminated** from the **Details** tab on the due diligence request record page.

    The following actions then take place:

    1.  A required **Justification** field appears. You must enter an explanation for rejecting the request.
    2.  The due diligence request's state is updated from Contract risk process to Contract not terminated.
    3.  After the owner closes the request, the engagement is **Rejected** and all stakeholders are notified that the contract isn’t terminated.

-   **Contract Risk process \(Contract not renewed\)**

    If the engagement is being reviewed for renewal and the contract can’t be renewed, you can reject the engagement by selecting **Contract not renewed**.

    The following actions then take place:

    1.  A required **Justification** field appears. You enter an explanation for rejecting the engagement.
    2.  The due diligence request's state is updated from Contract risk process to Contract not renewed.
    3.  After the owner closes the request, the engagement is **Rejected** and all stakeholders are notified that the contract isn’t renewed.

-   **Contract Risk process \(Request additional due diligence\)**

    If you require additional due diligence, you can reject the engagement by selecting **Request additional due diligence** from the **Details** tab on the due diligence request record page.

    The following actions then take place:

    1.  A required **Justification** field appears. You must enter an explanation for requesting additional due diligence.
    2.  The due diligence request's state is updated from Contract risk process to Due diligence.
    3.  After the owner closes the request, it’s updated to the Due diligence process state and all stakeholders are notified that the engagement requires additional due diligence.
    4.  Either you, as the contract negotiator, or the owner can reopen the assessment and attach a new questionnaire to restart the process.

After the contract risk process is completed, the owner receives an email notification. Only the Third-party risk manager or owner can close a due diligence request.

**Note:** For more information on viewing contracts associated with due diligence requests, see [Accessing DD requests that are in the contract risk process](../../grc-workspace-vrm/concept/tprm-ws-dd-mgt-pg-contract-risk.md).

