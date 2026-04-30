---
title: Work on a credit task for a loan service case
description: Work on a credit task to review or authorize the credit for a loan customer. You can approve or reject the request based on your findings. A credit task is also used to update the covenant when you are working on a covenant breach.
locale: en-US
release: zurich
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on a credit task for a loan service case

Work on a credit task to review or authorize the credit for a loan customer. You can approve or reject the request based on your findings. A credit task is also used to update the covenant when you are working on a covenant breach.

## Before you begin

Role required:

-   For a personal loan service task: sn\_bom\_credit\_asmt.b2c\_agent or sn\_bom\_credit\_asmt.b2b\_agent\_connector
-   For a business loan service task: sn\_bom\_credit\_asmt.b2b\_agent or sn\_bom\_credit\_asmt.b2c\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

If a credit assessment is required for a loan service request, the workflow automatically generates a credit task for a credit agent. The task is assigned to the credit operations team or a credit agent based on the assignment rules.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Credit Tasks**, open the task list.

    -   For your assigned tasks, click **Assigned to me**.
    -   For all credit assessment tasks, click **All**.
4.  In the list, select the task that you want to work on.

    To work on a task that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.

5.  Finish the work that is required to complete the task in your core banking system.

6.  In the **Work notes** field, enter any comments that are related to your findings.

7.  Click **Approve** to approve or **Reject** to reject the request.

    **Note:** To enable a credit task to update a covenant, click **Close**.


## Result

-   The credit task moves to the Closed Complete state.
-   A new task that is based on the workflow is automatically generated in the **Tasks** tab of the associated case. The new task is assigned to an assignment group or agent based on the assignment rule.

