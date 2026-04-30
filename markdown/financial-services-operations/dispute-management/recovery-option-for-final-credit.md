---
title: Set recovery option
description: Determine whether to initiate a chargeback for a transaction, where the cardholder has not yet received the final credit, ensuring that the recovery process aligns with established guidelines.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Investigating a dispute, Working on a dispute case, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Set recovery option

Determine whether to initiate a chargeback for a transaction, where the cardholder has not yet received the final credit, ensuring that the recovery process aligns with established guidelines.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

A chargeback is initiated by a bank. The chargeback is pursued when a card provider requests the merchant the return of lost funds on a fraudulent or disputed transaction. If chargeback is not pursued, the agent selects whether to deny or write off the transaction.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![List icon.](../../../common/image/icon-list.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the transaction ID in the transaction level playbook of the **Processing** tab.

    The **Investigate** stage is initiated for the transaction.

7.  Select the **Set recovery option** activity under the **Investigation** stage.

8.  Enter details about the decision on chargeback, write off, or transaction denial.

9.  In the **Pursue recovery** drop-down, select one of the following.

<table id="choicetable_gwh_bjs_3fc"><tbody><tr><td id="d41772e172">

**Yes**

</td><td>

The relevant tasks for the transaction trigger for the **Chargeback** stage.

</td></tr><tr><td id="d41772e184">

**No**

</td><td>

-   If you select **No**, the **Deny dispute** drop-down is displayed.
-   Select **Yes** to deny the dispute. The task is marked for approval. Once it is approved, the task moves to **Closed Rejected** state.
-   **No** to write off the final credit to the card holder.


</td></tr></tbody>
</table>10. In the **Remarks** field, enter any comments.

11. Select **Update**.

12. Close the task from the playbook.

    |Dispute activity|Action|
    |----------------|------|
    |**To close the recovery option task**|Select **Close task**.|


## Result

-   If the decision is to deny the dispute, the transaction task state updates to **Closed complete**.
-   If the decision is to pursue chargeback, the relevant tasks for the transaction trigger for the **Chargeback** stage.

**Parent Topic:**[Investigating a dispute](investigate-a-dispute.md)

