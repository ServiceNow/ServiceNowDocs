---
title: Work on a document task to verify documents for a policy service case
description: Work on a document task to manage and track documents \(inbound and outbound\) that are needed for a policy service case.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Work on a policy service case, Use, Personal Lines Servicing, Property and Casualty Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Work on a document task to verify documents for a policy service case

Work on a document task to manage and track documents \(inbound and outbound\) that are needed for a policy service case.

## Before you begin

Role required: sn\_bom\_document.b2c\_agent

## About this task

The Document Processor service determines which documents \(inbound and outbound\) are required in a workflow. If any documents must be collected or distributed to the customer, a task is automatically generated for a document agent. The task is assigned to the document service team or a document agent based on the assignment rules.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Document Service**, open the task list.

    -   For your assigned tasks, click **Assigned to me**.
    -   For all document tasks, click **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Find out which documents are required for the case:

    -   For a list of inbound documents, click the **Inbound Documents** tab.
    -   For a list of outbound documents, click the **Outbound Documents** tab.
6.  Verify the completeness of all documents that the customer has submitted \(inbound\) or the bank should share with the customer \(outbound\).

<table id="choicetable_t3f_5r1_wnb"><thead><tr><th align="left" id="d113498e169">

Task

</th><th align="left" id="d113498e172">

Action

</th></tr></thead><tbody><tr><td id="d113498e178">

**Verify an inbound or outbound document**

</td><td>

1.  In the list, click the document that you want to verify.
2.  Check the document details and click **Verify**.


</td></tr><tr><td id="d113498e199">

**Defer an inbound document**

</td><td>

If the customer can't submit a document and has requested to submit it at a future date, you can defer this document. 1.  In the list, click the document to defer.
2.  Click **Request Deferment**.
 **Note:** This option is available only if a deferment is enabled for the document category.

</td></tr><tr><td id="d113498e223">

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

-   The document task moves to the Closed Complete state and the associated case moves to the next stage.
-   A new task that is based on the configured workflow is automatically generated in a respective task tab of the associated case. The new task is assigned to an assignment group or agent based on the assignment rules.

**Parent Topic:**[Work on a policy service case](work-ins-policy-case.md)

