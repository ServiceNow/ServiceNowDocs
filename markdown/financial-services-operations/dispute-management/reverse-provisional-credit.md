---
title: Reverse provisional credit
description: Reverse the temporary credit issued by the bank to the card holder.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Initiating a chargeback, Resolving disputes without network integration, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Reverse provisional credit

Reverse the temporary credit issued by the bank to the card holder.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

The option to reverse provisional credit exists when provisional credit was issued to a customer in scenarios such as:

-   During the Investigation stage- During the manual investigation task a determination that a transaction was not fraud.
-   During the Chargeback stage- An issuing bank evaluates the merchant's representment evidence after a chargeback has occurred, and makes the determination to rescind a chargeback.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Reverse provisional credit** activity under the Chargeback playbook stage.

7.  Select the Reverse provisional credit task that you want to complete.

8.  On the form, fill in the required fields and any other related information that you've gathered.

9.  In the **Work notes** field, enter any comments.

10. After you have entered the details in the task, select **Update**.

11. Close the task from the playbook.

    |Dispute activity|Action|
    |----------------|------|
    |**To close the Reverse provisional credit task**|Select **Close**.|


## What to do next

Proceed to [Return funds to merchant](refund-merchant.md).

**Parent Topic:**[Initiating a chargeback](initiate-a-chargeback.md)

