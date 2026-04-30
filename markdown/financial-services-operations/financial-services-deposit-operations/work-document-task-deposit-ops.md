---
title: Work on a document task to verify documents for a deposit case
description: Work on a document task to verify inbound documents that are needed for a deposit service case.
locale: en-US
release: xanadu
product: Financial Services Deposit Operations
classification: financial-services-deposit-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Financial Services Deposit Operations, Financial Services Deposit Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on a document task to verify documents for a deposit case

Work on a document task to verify inbound documents that are needed for a deposit service case.

## Before you begin

Role required:

-   For a business deposit service case: sn\_bom\_document.b2b\_agent
-   For a personal deposit service case: sn\_bom\_document.b2c\_agent

## About this task

The Document Management Service determines which documents are required in a workflow. If any documents must be collected from the customer, a task is automatically generated for a document agent. The task is assigned to the document service team or a document agent based on the assignment rules.

For more information, see .

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![lists icon.](../../fso-card-operations/image/list-icon.png)\).

3.  In the **Lists** tab, under **Document Service**, open the task list.

    -   For your assigned tasks, click **Assigned to me**.
    -   For all document tasks, click **All**.
4.  In the list, select the task that you want to work on.

    To work on a task that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.

5.  In the **Inbound Documents** tab, choose a document.

6.  Once the document has been reviewed, click **Verify**.

7.  In the **Work notes** field, enter any comments.

8.  Click **Close**.


## Result

-   The document task moves to the Closed Complete state.
-   In the parent deposit case, the Verify documents stage in the case playbook shows as complete and the case moves to the next stage.

**Parent Topic:**[Using Financial Services Deposit Operations](../concept/using-deposit-ops.md)

