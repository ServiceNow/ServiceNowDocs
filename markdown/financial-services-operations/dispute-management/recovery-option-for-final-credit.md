---
title: Determine recovery option for providing final credit
description: Complete the Recovery option task to choose whether to pursue chargeback for a transaction where final credit to the card customer will be provided.
locale: en-US
release: xanadu
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Investigating a dispute, Work on a dispute case, Managing dispute service requests, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Determine recovery option for providing final credit

Complete the Recovery option task to choose whether to pursue chargeback for a transaction where final credit to the card customer will be provided.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

A chargeback is bank initiated, pursued when a card provider requests from the merchant the return to the customer of lost funds on a fraudulent or disputed transaction. If chargeback will not be pursued, the agent selects whether to deny or write off the transaction.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Recovery option** activity under the Investigation playbook stage.

7.  Select the recovery task that you want to complete.

8.  On the form, fill in the required fields and any other related information that you've gathered.

9.  -   In the **Pursue chargeback** field, select whether the determination is to pursue chargeback from the merchant.
-   In the **Deny dispute** field, select whether the determination is to deny the dispute.
10. In the **Work notes** field, enter any comments.

11. After you have entered the details in the task, select **Update**.

12. Close the task from the playbook.

    |Dispute activity|Action|
    |----------------|------|
    |**To close the Recovery option task**|Select **Close**.|


## Result

-   If determination was made to deny the dispute, the transaction task state updates to Closed complete.
-   If determination was made to pursue chargeback, the relevant tasks for the transaction will trigger for the Chargeback stage.

**Parent Topic:**[Investigating a dispute](investigate-a-dispute.md)

