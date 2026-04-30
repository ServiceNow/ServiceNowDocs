---
title: Issue credit
description: Issue immediate final credit to the card holder during the Investigation stage based on the amount being disputed and the policy for the credit.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Investigating a dispute, Working on a dispute case, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Issue credit

Issue immediate final credit to the card holder during the Investigation stage based on the amount being disputed and the policy for the credit.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

Based on the business rules, the bank decides to issue immediate final credit to the card holder.

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

7.  Select the **Immediate final credit** activity.

8.  Review the dispute amount and enter the refund details.

9.  In the **Remarks** field, enter any comments.

10. Select **Close task**.

11. Close the task from the playbook.


## Result

The task state updates to Closed Complete. The dispute transaction moves to the **Chargeback** stage.

**Parent Topic:**[Investigating a dispute](investigate-a-dispute.md)

