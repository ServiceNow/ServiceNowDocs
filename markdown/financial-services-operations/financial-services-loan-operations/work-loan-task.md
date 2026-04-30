---
title: Work on a loan task for a loan service case
description: Work on a loan task to review and authorize a loan service request, update a loan account, or to disburse a loan when a loan service request is fulfilled.
locale: en-US
release: zurich
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on a loan task for a loan service case

Work on a loan task to review and authorize a loan service request, update a loan account, or to disburse a loan when a loan service request is fulfilled.

## Before you begin

Role required:

-   For a business loan service task: sn\_bom\_loan\_b2b.agent or sn\_bom\_loan\_b2b.agent\_connector
-   For a personal loan service task: sn\_bom\_loan.b2c\_agent or sn\_bom\_loan.agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

For the following loan workflows, agents can also use the case playbook that guides them through the steps that are needed to resolve the case.

-   Loan Forgiveness workflow for business loan operations
-   Loan Deferment workflow for personal loan operations

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Loan Tasks**, open the task list.

    -   For your assigned tasks, click **Assigned to me**.
    -   For all credit assessment tasks, click **All**.
4.  In the list, select the task that you want to work on.

    To work on a task that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.

5.  Finish the work that is required to complete the loan task in your core banking system.

    **Note:** When using a loan task to authorize a loan request, click **Request Info** if you need any required information to complete the review.

6.  In the **Work notes** field, enter any comments.

7.  Close the loan task.

    |Loan task|Action|
    |---------|------|
    |**For authorizing a loan service request**|Click **Approve** to approve or **Reject** to reject the request.|
    |**For updating a loan account**|Click **Close**.|
    |**For disbursing a loan**|Click **Close**.|


## Result

-   The loan task moves to the Closed Complete state and the associated loan case moves to the next stage.
-   If the loan task is for authorizing a loan service request, a new task that is based on the workflow is automatically generated in the **Tasks** tab of the associated case. The new task is assigned to an assignment group or agent based on the assignment rules.
-   If the loan task is for updating a loan account or disbursing a loan, the associated loan case moves to the Closed Complete stage.

