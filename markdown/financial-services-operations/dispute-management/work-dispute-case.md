---
title: Managing disputes without network integration
description: Work on a dispute case to review case information, ensure that any outstanding tasks are completed, and resolve the service request.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Managing disputes without network integration

Work on a dispute case to review case information, ensure that any outstanding tasks are completed, and resolve the service request.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

When a customer requires resolution of a dispute, there are three ways a case is raised:

-   A contributor initiates a case on behalf of the customer through the workspace and provides dispute transaction details, triggering a workflow for the transaction. For more information, see [Initiate a dispute](create-case-with-intake-workspace.md#).
-   A customer files a dispute through their financial institution's customer portal. For more information, see [Create a dispute case with Dispute Intake in Portal](../concept/creating-an-onboarding-case-with-dispute-playbook-for-portal.md).
-   As an agent, you can also create a dispute case through the agent workspace as needed.

Once the dispute case is created and assigned to you, you can review the submitted details, make updates as necessary, then submit the case for investigation.

Throughout the workflow, dispute agents complete their assigned tasks, and the statuses of tasks associated with the case update. Depending on the task updates, a workflow might have additional or fewer tasks. If there is more than one disputed transactions associated with a case, the case remains open until the workflows for each transaction are completed and closed.

Work through the activities and tasks required to research and complete the request. Tasks in the playbook activities are also available in the **Tasks** tab of the case.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Use the activities and tasks under the following playbook stages to fulfill the request and resolve the case:

    -   **Initiate** - This stage is active when a case is created by the dispute agent. If the case is submitted through the contributor workspace or the customer dispute portal, the provided details are displayed and all activities are marked as complete.

        This stage enables you to enter dispute information, upload documents, fill out the dispute questionnaire, and submit the case.

    -   **Review** - This stage is active if a case is submitted through the contributor workspace or the customer dispute portal.

        This stage includes details to review a submitted case, including the selected transactions and reasons for dispute. You can also answer additional questions to provide more information, and modify responses for accuracy.

    -   **Processing**- This stage is active after a dispute case is submitted, each disputed transaction is displayed in a workspace as tasks. Each dispute transaction progresses through these stages: **Investigate**, **Chargeback**, and **Closure**.
        -   **Investigation**- This stage enables you to determine the recovery option, write off a transaction amount, provide immediate final credit, trigger a pre-dispute collaboration, initiate provisional credit, determine reverse provisional credit, and investigate the transaction.
        -   **Chargeback**- This stage enables you to report fraud, initiate chargeback, and review merchant representment.

    -   **Closure** - After you complete all the activities for the case, you can select the resolution code and enter resolution notes to close the case.
    Any tasks generated during playbook activities appear in the **Tasks** tab of the case.

7.  Close the task from the task form.

    |Case/Dispute activity|Action|
    |---------------------|------|
    |**To submit a dispute case**|In the case playbook, select **Submit**.|
    |**    -   To close investigation tasks
    -   To close chargeback tasks
**|In the task form, select **Close** to close the task.|


## Result

The tasks update to Closed Complete.

-   **[Investigating a dispute](investigate-a-dispute.md)**  
Complete tasks such as determining a recovery option, writing off a disputed transaction amount, and provide immediate final credit, notify the merchant, initiate provisional credit, determine reversal of provisional credit, and investigate the transaction.
-   **[Initiating a chargeback](initiate-a-chargeback.md)**  
Complete tasks such as initiating a chargeback, providing credit to a customer, and refunding a merchant.

**Parent Topic:**[Managing Disputes](../concept/managing-disputes.md)

