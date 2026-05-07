---
title: Block a credit card for a customer
description: Block a credit card for a customer as per the credit card service request.
locale: en-US
release: australia
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Blocking a credit card, Use, Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Block a credit card for a customer

Block a credit card for a customer as per the credit card service request.

## Before you begin

Role required: sn\_bom\_credit\_card.agent or sn\_bom\_credit\_card.agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

This credit card task is automatically created with a credit card service case for blocking a card request.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  Open the task from a credit card service case or from the Credit Card Task list.

<table id="choicetable_lgv_1db_hmb"><thead><tr><th align="left" id="d42426e117">

Option

</th><th align="left" id="d42426e120">

Steps

</th></tr></thead><tbody><tr><td id="d42426e126">

**From a credit card service case**

</td><td>

1.  In the **Lists** tab, under **Credit Card Service Cases**, click **Assigned to me**.
2.  In the list, click the case that you want to open.
3.  In the case, click the **Tasks** tab and select the credit card task.


</td></tr><tr><td id="d42426e159">

**From the Credit Card Task list**

</td><td>

1.  In the **Lists** tab, under **Credit Card Task**, click **All**.
2.  In the list, click the task that you want to open.


</td></tr></tbody>
</table>4.  In the **State** field, change the state of the task to **Work in Progress**.

5.  Block the customer's credit card as per the request.

6.  In the **Work notes** field, enter any comments.

7.  To close the task, in the **State** field, change the state of the task to **Closed Complete**.

8.  Click **Save**.


## Result

-   The stage of the associated credit card service case changes from Update Account to Closed – Complete.

    **Important:** If the request is for only temporarily blocking the credit card, the associated case remains in the Work in Progress state and in the Update Account stage until the end date is specified in the case. The system automatically creates a new credit card service case on the specified end date to unblock the card.

-   The customer receives a pre-configured email notification about the case closure.

## What to do next

If the associated case is for temporarily blocking the credit card, work on the new credit service case to [unblock the card](unblock-credit-card.md) on the end date.

