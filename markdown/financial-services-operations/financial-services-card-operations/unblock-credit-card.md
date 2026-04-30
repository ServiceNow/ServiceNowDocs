---
title: Unblock a credit card
description: Unblock a customer's credit card as per the credit card service request.
locale: en-US
release: zurich
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Unblock a credit card

Unblock a customer's credit card as per the credit card service request.

## Before you begin

Role required: sn\_bom\_credit\_card.agent or sn\_bom\_credit\_card.agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

When a credit card service case for unblocking a card is created, the Unblock Credit Card flow is triggered. This flow automatically creates a credit card task in the **Tasks** tab of the case to decrease the credit limit for the customer.

For more information on the flows that are installed with the Financial Services Card Operations application, see [Designer flows for Financial Services Operations applications](../../fso-common/reference/flow-designer-flows-fso-apps.md).

**Note:** An unblock credit card case is also automatically created for a case for temporarily blocking a card when the **Duration** field is set to **Limited Time**.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Credit Card Service Cases**, open the case list.

    -   For your assigned cases, click **Assigned to me**.
    -   For all cases, click **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Unblock the customer's credit card as per the request.

6.  Update the Unblock credit card task.

    1.  In the **Tasks** tab, click the credit card task.

    2.  In the **State** field, change the state of the task to **Work in Progress**.

    3.  In the **Work notes** field, enter any comments.

    4.  To close the task, in the **State** field, change the state of the task to **Closed Complete**.

    5.  Click **Save**.


## Result

-   The stage of the credit card service case changes from Update Account to Closed – Complete.

    **Note:** If this unblock credit card case was created as part of the [Blocking a credit card](../concept/work-block-credit-card-case.md) flow, the case for blocking the card also moves to the Closed – Complete stage.

-   The customer receives a pre-configured email notification about the case closure.

