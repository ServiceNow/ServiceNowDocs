---
title: Reset the credit limit for a customer
description: Revert a card's credit limit to its original limit for a customer who requested a temporary increase in the credit limit.
locale: en-US
release: zurich
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Increasing the credit limit, Use, Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Reset the credit limit for a customer

Revert a card's credit limit to its original limit for a customer who requested a temporary increase in the credit limit.

## Before you begin

Role required: sn\_bom\_credit\_card.agent or sn\_bom\_credit\_card.agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

This credit card service case is automatically created for a credit card service case for a temporary increase in the credit limit when the **Duration** field is set to **Limited Time**.

If the request is for a temporary increase in the credit limit, the case remains in the Work in Progress state even after increasing the credit limit. The system automatically creates a new credit card service case on the specified end date to reset the credit limit.

The **sn\_bom\_credit\_card.reserverd\_hours\_to\_update\_credit\_limit** [card property](../reference/properties-installed-card-ops.md) defines the number of hours before the end date when the system creates a credit card service case to revert the credit limit.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Credit Card Service Cases**, open the case list.

    -   For your assigned cases, click **Assigned to me**.
    -   For all cases, click **All**.
4.  In the list, select the case that you want to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.

5.  In the **Requested limit amount** field, decrease the credit limit to the card's original limit.

6.  Update the **Decrease credit limit** task.

    1.  In the **Tasks** tab, click the credit card task that you want to work on.

    2.  In the **State** field, change the state of the task to **Work in Progress**.

    3.  In the **Work notes** field, enter any comments.

    4.  To close the task, In the **State** field, change the state of the task to **Closed Complete**.

    5.  Click **Save**.


## Result

-   The stage of both the Reset credit limit case and the original credit card service case for increasing the credit limit changes to Closed – Complete.
-   The customer receives a pre-configured email notification about the credit limit reset and case closure.

