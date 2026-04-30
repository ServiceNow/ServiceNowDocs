---
title: Work on a dispute case
description: Work on a card dispute case to review case information, ensure that any outstanding tasks are completed, and resolve the service request.
locale: en-US
release: xanadu
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Managing dispute service requests, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on a dispute case

Work on a card dispute case to review case information, ensure that any outstanding tasks are completed, and resolve the service request.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

When a customer requires resolution of a dispute, there are two ways a case is raised:

-   An agent initiates a case and provides dispute transaction details, triggering a workflow for the transaction.
-   A customer files a dispute through their financial institution's customer portal. \(See [Dispute Intake in Portal](../concept/dispute-playbook-for-portal.md) for more information.\) The dispute agent assigned to the case then reviews the submitted details, makes updates as necessary, then submits the case for investigation.

Throughout the workflow, dispute agents complete their assigned tasks, and the statuses of tasks associated with the case update. Depending on the task updates, a workflow might have additional or fewer tasks. If there are more than one disputed transactions associated with a case, the case remains open until the workflows for each transaction are completed and closed.

Use the case playbook that provides the activities and tasks required to research and complete the request. Tasks in the playbook activities are also available in the Tasks tab of the case.

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

    -   **Initiate** - If this case was created by a dispute agent, this stage will be active. If the case was submitted through a customer dispute portal, it will show the details provided by the customer and all activities will be complete.

        This stage enables you to enter dispute information, upload documents, fill out the dispute questionnaire, and submit the case.

    -   **Review** - If this case was submitted through a customer dispute portal, this stage will be active. If the case was created by a dispute agent, it will be skipped.

        This stage includes activities to review details on a submitted case, including the selected transactions and reasons for dispute. You can also answer additional questions to provide more information, and modify responses for accuracy.

    -   **Investigation** - This stage enables you to determine the recovery option, write off a transaction amount, provide immediate final credit, trigger a pre-dispute collaboration, initiate provisional credit, determine reverse provisional credit, and investigate the transaction.
    -   **Chargeback** - This stage enables you to report fraud, initiate chargeback, and review merchant representment evidence.
    -   **Closure** - Once the case is in a state to be closed, you can select the resolution code and any resolution notes before closing the case.
    Any tasks generated during playbook activities appear in the **Tasks** tab of the case.

7.  In the **Work notes** field, enter any comments.

8.  Close the task from the task form.

    |Case/Dispute activity|Action|
    |---------------------|------|
    |**To submit a dispute case**|In the case playbook, select **Submit**.|
    |**    -   To close investigation tasks
    -   To close chargeback tasks
**|In the task form, select **Close** to close the task.|


## Result

The tasks update to Closed Complete.

-   **[Initiate a dispute](initiating-dispute.md)**  
Begin a dispute case in Financial Services Card Operations for a transaction associated with a card account. You can enter dispute information, fill out the dispute questionnaire, upload supporting documentation, and submit the case for investigation.
-   **[Review a dispute from cardholder intake](review-a-dispute-from-cardholder-intake.md)**  
Review dispute cases in Financial Services Operations submitted by customers from a dispute intake portal. You can verify the disputed transactions, update the dispute reason, and submit for investigation after review.
-   **[Investigating a dispute](investigate-a-dispute.md)**  
Complete tasks such as determining a recovery option, writing off a disputed transaction amount, and provide immediate final credit, notify the merchant, initiate provisional credit, determine reversal of provisional credit, and investigate the transaction.
-   **[Initiating a chargeback](initiate-a-chargeback.md)**  
Complete tasks such as reporting fraud, initiating a chargeback, and refunding a merchant.
-   **[Close a card dispute](closure-dispute-case.md)**  
After you have completed all tasks in a card dispute case, you can add final details and close the case in the Closure playbook stage.

**Parent Topic:**[Managing dispute service requests](../concept/managing-card-disputes.md)

