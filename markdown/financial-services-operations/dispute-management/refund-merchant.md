---
title: Return funds to merchant
description: A merchant can be refunded if their representment evidence is approved.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Initiating a chargeback, Resolving disputes without network integration, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Return funds to merchant

A merchant can be refunded if their representment evidence is approved.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

If a decision to refund the merchant was selected during the Review representment task, the Return funds to merchant task is triggered in the workflow. After the issuing bank evaluates the merchant's representment evidence after a chargeback has occurred, and makes the determination to rescind a chargeback, the issuing bank returns the funds associated with the transaction to the merchant.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Return funds to merchant** activity under the Chargeback playbook stage.

7.  On the form, fill in the required fields and any other related information that you've gathered.

8.  After you have entered the details in the task, select **Update**.

9.  Close the task from the playbook.

    |Dispute activity|Action|
    |----------------|------|
    |**To close the task**|Select **Close task**.|


## Result

The task updates to the Close complete state. If the transaction was the only or final transaction to be resolved for the case, the case moves to the Closure stage. See [Close a card dispute](closure-dispute-case.md) for more information.

**Parent Topic:**[Initiating a chargeback](initiate-a-chargeback.md)

