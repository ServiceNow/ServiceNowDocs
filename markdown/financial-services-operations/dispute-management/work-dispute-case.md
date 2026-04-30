---
title: Working on a dispute case
description: Work on a card dispute case to review case information, ensure that any outstanding tasks are completed, and resolve the service request.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Working on a dispute case

Work on a card dispute case to review case information, ensure that any outstanding tasks are completed, and resolve the service request.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

When a customer requires resolution of a dispute, there are two ways a case is raised:

-   An agent initiates a case and provides dispute transaction details, triggering a workflow for the transaction.
-   A customer files a dispute through their financial institution's customer portal. \(See [Managing dispute intake in portal](../concept/dispute-playbook-for-portal.md) for more information.\) The dispute agent assigned to the case then reviews the submitted details, makes updates as necessary, then submits the case for investigation.

Throughout the workflow, dispute agents complete their assigned tasks, and the statuses of tasks associated with the case update. Depending on the task updates, a workflow might have additional or fewer tasks. If there are more than one disputed transactions associated with a case, the case remains open until the workflows for each transaction are completed and closed.

Use the case playbook that provides the activities and tasks required to research and complete the request. Tasks in the playbook activities are also available in the **Tasks** tab of the case.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![Lists icon.](../../../use/reporting/image/inline-data-vis-list.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

    The case playbook guides an agent through the steps that are involved in resolving a case.

6.  Use the activities and tasks under the following playbook stages to fulfill the request and resolve the case:

    -   **Initiate** - This stage is active, if a case was created by the dispute agent. If the case is submitted through the customer dispute portal, details provided by the customer are displayed and all activities are marked as complete.

        This stage enables you to enter dispute information, upload documents, fill out the dispute questionnaire, and submit the case.

    -   **Review** - This stage is active if a case is submitted through a customer dispute portal, .

        This stage includes details to review a submitted case, including the selected transactions and reasons for dispute. You can also answer additional questions to provide more information, and modify responses for accuracy.

    -   **Investigation** - This stage enables you to determine the recovery option, write off a transaction amount, provide immediate final credit, trigger a pre-dispute collaboration, initiate provisional credit, determine reverse provisional credit, and investigate the transaction.
    -   **Chargeback** - This stage enables you to report fraud, initiate chargeback, and review merchant representment evidence.
    -   **Closure** - After you complete all the activities for the case, you can select the resolution code and resolution notes to mark the cased to closure.
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

-   **[Initiate a dispute](initiating-dispute.md#)**  
Begin a dispute case in Financial Services Card Operations for a transaction associated with a card account. You can enter dispute information, fill out the dispute questionnaire, upload supporting documentation, and submit the case for investigation.
-   **[Investigating a dispute](investigate-a-dispute.md)**  
Complete tasks such as initiate provisional credit, determine a recovery option, write off a disputed transaction amount, provide immediate final credit, notify the merchant, determine reversal of provisional credit, and investigate the transaction.
-   **[Initiating a chargeback](initiate-a-chargeback.md)**  
You can access the **Chargeback** stage by opening a disputed transaction in the **Processing** stage of the playbook. During the **Chargeback** stage, the dispute is forwarded to the card network. The card network then forwards the dispute to the acquirer. There is a wait period to see if there is a representment.

**Parent Topic:**[Managing dispute service requests](../concept/managing-card-disputes.md)

