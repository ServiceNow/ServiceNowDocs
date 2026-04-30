---
title: Refund a merchant
description: A merchant can be refunded if their representment evidence is approved.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Initiating a chargeback, Working on a dispute case, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Refund a merchant

A merchant can be refunded if their representment evidence is approved.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

If a decision to refund the merchant was selected during the Review representment task, the Return funds to merchant task is triggered in the workflow. After the issuing bank evaluates the merchant's representment evidence after a chargeback has occurred, and makes the determination to rescind a chargeback, the issuing bank returns the funds associated with the transaction to the merchant.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Return funds to merchant** activity under the Chargeback playbook stage.

7.  Select the Return funds to merchant task that you want to complete.

8.  On the form, fill in the required fields and any other related information that you've gathered.

9.  In the **Work notes** field, enter any comments.

10. After you have entered the details in the task, select **Update**.

11. Close the task from the playbook.

    |Dispute activity|Action|
    |----------------|------|
    |**To close the Return funds to merchant task**|Select **Close**.|


## Result

The task updates to the Close complete state. If the transaction was the only or final transaction to be resolved for the case, the case moves to the **Closed complete** state and stage.

**Parent Topic:**[Initiating a chargeback](initiate-a-chargeback.md)

