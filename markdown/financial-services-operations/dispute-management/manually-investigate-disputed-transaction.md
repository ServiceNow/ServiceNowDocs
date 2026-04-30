---
title: Investigate transactions
description: If a merchant refuses or declines a transaction dispute, the case may move to the manual investigation activity.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Investigating a dispute, Working on a dispute case, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Investigate transactions

If a merchant refuses or declines a transaction dispute, the case may move to the manual investigation activity.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

During the **Investigation** stage of a transaction dispute, if a merchant declines the dispute, the transaction moves to Investigate transactions activity. Here the dispute agent can pursue a chargeback on behalf of the card holder from the merchant.

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

7.  Select the **Investigate transactions** activity under the Investigation stage.

8.  Select whether to create a chargeback request in the **Pursue chargeback** drop-down list.

    -   `Yes` - Pursue a chargeback from the merchant.
    -   `No` - Do not pursue chargeback from the merchant.
9.  In the **Remarks** field, enter any comments.

    The chargeback eligibility is displayed based on the rules.

10. Select **Update** to save your changes.

11. Select **Continue**.

    The case is submitted to the dispute manager for review and approval when the chargeback eligibility is `No` and the **Pursue Chargeback** value is `Yes`. After the manager approves the task, the agent can continue with the dispute.

12. Select **Initiate dispute**.


## Result

A dispute is initiated.

**Parent Topic:**[Investigating a dispute](investigate-a-dispute.md)

