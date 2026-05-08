---
title: Work on a document verification task
description: A document agent can review and approve or reject a document submitted for verification.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Document Processor, Integrate, Financial Services Operations \(FSO\)]
---

# Work on a document verification task

A document agent can review and approve or reject a document submitted for verification.

## Before you begin

**Note:** An OCR-processed document can be automatically reviewed and approved. For information on OCR-processed documents, see [Integrating with Document Intelligence](integration-with-document-intelligence.md).

Role required: sn\_doc\_processor.agent​

## Procedure

1.  Navigate to **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![List icon.](../../../use/reporting/image/inline-data-vis-list.png)\).

3.  In the **Lists** tab, under **Document verification**, open the task list.

    -   For your assigned tasks, select **Assigned to me**.
    -   For all document verification tasks, select **All**.
4.  In the list, select the document verification task that you want to work on.

    To work on a verification task that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Verify the completeness of all documents that are submitted.

    If a document has been processed through OCR, you can select **Open in DocIntel** to review the document and update document field values.

    The **External ID** field in the document verification task is populated with the ID of the Document Intelligence use case that processes and extracts the data.

    Review and update any extracted values in the **Extracted Values** related list.

    For more information, see [Integrating with Document Intelligence](integration-with-document-intelligence.md).

6.  From the **Notes and Activity** tab in the **Work notes** field, enter any comments.

7.  Select one of the following options.

<table id="choicetable_t3f_5r1_wnb"><thead><tr><th align="left" id="d132816e209">

Task

</th><th align="left" id="d132816e212">

Action

</th></tr></thead><tbody><tr><td id="d132816e218">

**Verify**

</td><td>

Select **Verify** if the document details are sufficient.

</td></tr><tr><td id="d132816e230">

**Reject**

</td><td>

You can reject a document verification task if the details are insufficient.1.  From the **Rejection reason** field, select the reason from the following options.
    -   Information mismatch
    -   Incorrect document
    -   Expired document
    -   Scanning issues
    -   Fraudulent document
2.  Select **Reject**.


</td></tr></tbody>
</table>
## Result

If the task is verified, the document verification task state shows as **Verified**. If the task is rejected for verification, the document verification task state shows as **Not Submitted**.

