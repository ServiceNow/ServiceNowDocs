---
title: Provide final credit to customer
description: If a merchant's representment was not approved as sufficient supporting evidence by the issuing bank, the issuing bank upholds the chargeback.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Chargeback, Resolving disputes without network integration, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Provide final credit to customer

If a merchant's representment was not approved as sufficient supporting evidence by the issuing bank, the issuing bank upholds the chargeback.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

If a merchant's representment was not approved as sufficient supporting evidence by the issuing bank, the issuing bank upholds the chargeback, and final credit is provided to the customer.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Issue final credit** activity under the Chargeback playbook stage.

7.  On the form, fill in the required fields and any other related information that you've gathered.

8.  In the **Remarks** field, enter any comments.

9.  After you have entered the details in the task, select **Update**.

10. Close the task from the playbook.

    |Dispute activity|Action|
    |----------------|------|
    |**To close the task**|Select **Close task**.|


## Result

Once final credit issuance to the customer is submitted, the transaction task state updates to Closed complete.

**Parent Topic:**[Initiating a chargeback](initiate-a-chargeback.md)

