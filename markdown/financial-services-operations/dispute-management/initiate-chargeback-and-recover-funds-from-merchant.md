---
title: Initiate chargeback and recover funds from merchant
description: Initiate a request for the card network issuer to credit the customer.
locale: en-US
release: xanadu
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Initiating a chargeback, Work on a dispute case, Managing dispute service requests, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
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

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Initiate chargeback** activity under the Chargeback playbook stage.

7.  Select the initiate chargeback task that you want to complete.

8.  On the form, fill in the required fields and any other related information that you've gathered.

    -   In the **Chargeback details** field, select the chargeback code.

        **Note:** To configure chargeback reason codes, an admin can navigate to **Financial Services Operations** &gt; **Reference Data** &gt; **Chargeback reason codes**.

    -   In the **Represented by merchant** field, select whether the merchant is providing representment to contest the chargeback request.
9.  In the **Work notes** field, enter any comments.

10. After you have entered the details in the task, select **Update**.

11. To submit the request, select **Initiate chargeback**.

12. Close the task from the playbook.

    |Dispute activity|Action|
    |----------------|------|
    |**To close the Initiate chargeback task**|Select **Close**.|


## Result

The task state moves to the Closed complete state. Additionally:

-   The merchant’s bank makes a determination whether to provide the credit to the issuing bank.

    **Note:** Tracking funds credited from the merchant's bank occurs outside of the Financial Services Card Operations application. The application requires integration with the applicable card network.

-   The merchant can provide evidence for the transaction and refuse the chargeback, or the merchant can accept the chargeback, which will result in the customer being credited back with the funds.

## What to do next

[Review representment](review-representment.md)

**Parent Topic:**[Initiating a chargeback](initiate-a-chargeback.md)

