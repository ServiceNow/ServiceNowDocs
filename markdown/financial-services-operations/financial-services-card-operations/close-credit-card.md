---
title: Close a credit card account
description: Close a customer's credit card account as per the credit card service request.
locale: en-US
release: yokohama
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing credit card service requests, Card Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Close a credit card account

Close a customer's credit card account as per the credit card service request.

## Before you begin

Role required: sn\_bom\_credit\_card.agent or sn\_bom\_credit\_card.agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

When a credit card service case for closing a card is created, the Close Credit Limit flow is triggered. This flow automatically creates a credit card task to close the customer's credit card account in the **Tasks** tab of the case.

For more information on the flows that are installed with the Financial Services Card Operations application, see [Designer flows for Financial Services Operations applications](../../fso-common/reference/flow-designer-flows-fso-apps.md).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Credit Card Service Cases**, open the case list.

    -   For your assigned cases, click **Assigned to me**.
    -   For all cases, click **All**.
4.  In the list, select the case that you want to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.

5.  Close the customer's credit card account as per the request.

6.  Update the Close credit card task.

    1.  In the **Tasks** tab, click the credit card task.

    2.  In the **State** field, change the state of the task to **Work in Progress**.

    3.  In the **Work notes** field, enter any comments.

    4.  To close the task, in the **State** field, change the state of the task to **Closed Complete**.

    5.  Click **Save**.


## Result

-   The stage of the credit card service case changes from Update Account to Closed – Complete.
-   The customer receives a pre-configured email notification about the case closure.

