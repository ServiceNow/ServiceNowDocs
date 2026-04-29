---
title: Work on a document task to verify documents
description: Work on a document task to manage and track documents \(inbound and outbound\) that are needed for a loan service case.
locale: en-US
release: australia
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on a document task to verify documents

Work on a document task to manage and track documents \(inbound and outbound\) that are needed for a loan service case.

## Before you begin

Role required:

-   For a personal loan service case: sn\_bom\_document.b2c\_agent
-   For a business loan service case: sn\_bom\_document.b2b\_agent

## About this task

The Document Processor service determines which documents \(inbound and outbound\) are required in a workflow. If any documents must be collected or distributed to the customer, a task is automatically generated for a document agent. The task is assigned to the document service team or a document agent based on the assignment rules.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Document Service**, open the task list.

    -   For your assigned tasks, click **Assigned to me**.
    -   For all document tasks, click **All**.
4.  In the list, select the task that you want to work on.

    To work on a task that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.

5.  Find out which documents are required for the case:

    -   For a list of inbound documents, click the **Inbound Documents** tab.
    -   For a list of outbound documents, click the **Outbound Documents** tab.
6.  Verify the completeness of all documents that the customer has submitted \(inbound\) or the bank should share with the customer \(outbound\).

<table id="choicetable_t3f_5r1_wnb"><thead><tr><th align="left" id="d54866e171">

Task

</th><th align="left" id="d54866e174">

Action

</th></tr></thead><tbody><tr><td id="d54866e180">

**Verify an inbound or outbound document**

</td><td>

1.  In the list, click the document that you want to verify.
2.  Check the document details and click **Verify**.


</td></tr><tr><td id="d54866e201">

**Defer an inbound document**

</td><td>

If the customer can't submit a document and has requested to submit it at a future date, you can defer this document. 1.  In the list, click the document to defer.
2.  Click **Request Deferment**.
 **Note:** This option is available only if a deferment is enabled for the document category.

</td></tr><tr><td id="d54866e225">

**Request exception for an inbound document**

</td><td>

If the customer is not able to submit a document and seeks an exemption from submitting it, you can request an exception for this document.1.  In the list, click the document to request an exception for.
2.  Click **Request Exception**.
 **Note:** This option is available only if an exception is enabled for the document category.

</td></tr></tbody>
</table>    **Note:** Depending on the document rules, a deferment or an exception for a document might require an approval by a document agent to close the task. To approve, click the **Approvals** tab in the document and click **Approve**.

7.  In the **Work notes** field, enter any comments.

8.  Click **Close**.


## Result

-   The document task moves to the Closed Complete state and the associated loan case moves to the next stage.
-   A new task that is based on the workflow is automatically generated in the **Tasks** tab of the associated case. The new task is assigned to an assignment group or agent based on the assignment rule.

