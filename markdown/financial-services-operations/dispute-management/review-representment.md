---
title: Review representment
description: Review the representment evidence provided by a merchant during a chargeback request. A representment is the process where a business can prove that a charge that is being questioned is valid and the consumer's charge should not be reversed.
locale: en-US
release: xanadu
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Initiating a chargeback, Work on a dispute case, Managing dispute service requests, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review representment

Review the representment evidence provided by a merchant during a chargeback request. A representment is the process where a business can prove that a charge that is being questioned is valid and the consumer's charge should not be reversed.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

If a merchant disagrees with a chargeback, they can submit representment evidence in an attempt to contest the chargeback and support their claim that a transaction is valid to their acquiring bank by way representment. The issuing bank reviews the evidence and determines further action on the disputed transaction.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Review representment** activity under the Chargeback playbook stage.

7.  Select the review representment task that you want to complete.

8.  On the form, fill in the required fields and any other related information that you've gathered.

9.  In the **Work notes** field, enter any comments.

10. Select **Update** to save your changes.

11. Select **Submit for approval**.

    The case is submitted for a review and approval to the dispute manager.

12. Close the task from the playbook.

    |Dispute activity|Action|
    |----------------|------|
    |**To close the Review representment task**|Select **Close**.|


## Result

The task state moves to the Closed complete state.

The merchant's representment evidence is submitted to their acquiring bank, which then transmits the information to the issuing bank to evaluate.

-   If the issuing bank makes determination to uphold the chargeback, the case moves to either the Provide final credit or Convert provisional credit to final credit task.
-   If the issuing bank makes determination to rescind the chargeback, the case moves to the Return funds to merchant task. If provisional credit was previously given to the customer, the case moves to the Reverse provisional credit task before moving to the Return funds to merchant task.

**Parent Topic:**[Initiating a chargeback](initiate-a-chargeback.md)

