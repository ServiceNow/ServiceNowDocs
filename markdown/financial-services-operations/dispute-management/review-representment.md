---
title: Review merchant representment
description: Review the representment evidence provided by a merchant during a chargeback request. A representment is the process where a business can prove that a charge that is being questioned is valid and the consumer's charge should not be reversed.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Initiating a chargeback, Resolving disputes without network integration, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review merchant representment

Review the representment evidence provided by a merchant during a chargeback request. A representment is the process where a business can prove that a charge that is being questioned is valid and the consumer's charge should not be reversed.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

If a merchant disagrees with a chargeback, they can submit representment evidence in an attempt to contest the chargeback and support their claim that a transaction is valid to their acquiring bank by representment. The issuing bank reviews the evidence and determines further action on the disputed transaction.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Review merchant representment** activity under the Chargeback playbook stage.

7.  On the form, fill in the required fields and any other related information that you've gathered.

8.  Select **Update** to save your changes.

9.  Select **Continue**.

    If merchant representment is not accepted, the case is submitted to the dispute manager for review and approval.

10. Close the task from the playbook.

    |Dispute activity|Action|
    |----------------|------|
    |**To close the task**|Select **Close task**.|


## Result

The task state moves to the Closed complete state.

If the representment is accepted and the transaction has provisional credit, proceed to [Reverse provisional credit](reverse-provisional-credit.md). If the representment is accepted with no provisional credit, proceed to [Return funds to merchant](refund-merchant.md).

If the representment is not accepted, proceed to [Provide final credit to customer](provide-final-credit-to-customer.md) or [Convert provisional credit to final credit](convert-provisional-credit-to-final-credit.md).

**Parent Topic:**[Initiating a chargeback](initiate-a-chargeback.md)

