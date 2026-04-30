---
title: Convert provisional credit to final credit
description: Convert provisional credit previously issued to a customer to a final credit issuance.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Initiating a chargeback, Working on a dispute case, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Convert provisional credit to final credit

Convert provisional credit previously issued to a customer to a final credit issuance.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

If a merchant's supporting representment evidence was not provided or approved as sufficient by the issuing bank, the issuing bank upholds the chargeback, and provisional credit previously issued to a customer is converted to final credit issued to the customer.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![List icon.](../../../common/image/icon-list.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Convert provisional credit to final credit** activity under the Chargeback playbook stage.

7.  Select the convert provisional credit to final credit task that you want to complete.

8.  On the form, fill in the required fields and any other related information that you've gathered.

9.  In the **Work notes** field, enter any comments.

10. After you have entered the details in the task, select **Update**.

11. Close the task from the playbook.

    |Dispute activity|Action|
    |----------------|------|
    |**To close the Convert provisional credit to final credit task**|Select **Close**.|


## Result

Once final credit issuance to the customer is submitted, the transaction task state updates to **Closed complete**.

**Parent Topic:**[Initiating a chargeback](initiate-a-chargeback.md)

