---
title: Initiate chargeback and recover funds from merchant
description: Initiate a request for the card network issuer to credit the customer.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Chargeback, Resolving disputes without network integration, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Initiate chargeback and recover funds from merchant

Initiate a request for the card network issuer to credit the customer.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

A manual investigation can result in an outcome of initiating a chargeback, creating a task to recover transaction funds from the merchant.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Initiate chargeback and fill merchant response** activity under the Chargeback playbook stage.

7.  On the form, review the populated fields and add any other related information that you've gathered.

8.  In the **Work notes** field, enter any comments.

9.  After you have entered the details in the task, select **Update**.

10. To submit the request, select **Initiate chargeback**.

11. Record the merchant response.

    |Network|Action|
    |-------|------|
    |**Visa**|In the **Dispute response received** field, indicate whether a response was received from the merchant.|
    |**Other networks**|In the **Represented by merchant** field, select whether the merchant is providing representment to contest the chargeback request.|

12. Select **Close task** to close the task from the playbook.


## Result

The task state moves to the Closed complete state. Additionally:

-   The merchant’s bank makes a determination whether to provide the credit to the issuing bank.

    **Note:** Tracking funds credited from the merchant's bank occurs outside of the Financial Services Card Operations application. The application requires integration with the applicable card network.

-   The merchant can provide evidence for the transaction and refuse the chargeback, or the merchant can accept the chargeback, which will result in the customer being credited back with the funds.

## What to do next

If the merchant has provided representment, proceed to [Review merchant representment](review-representment.md). Otherwise, proceed to [Provide final credit to customer](provide-final-credit-to-customer.md) or [Convert provisional credit to final credit](convert-provisional-credit-to-final-credit.md).

**Parent Topic:**[Initiating a chargeback](initiate-a-chargeback.md)

