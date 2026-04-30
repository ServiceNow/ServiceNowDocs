---
title: Submit a document for verification
description: A document collector can collect and submit a document for verification.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Document Processor, Integrating with Document Processor, Integrating with other ServiceNow applications, Integrating applications, Financial Services Operations \(FSO\)]
---

# Submit a document for verification

A document collector can collect and submit a document for verification.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![Lists icon.](../../../common/image/icon-list.png)\).

3.  In the **Lists** tab, under **Document verification**, open the task list.

    -   For your assigned tasks, select **Assigned to me**.
    -   For all document verification tasks, select **All**.
4.  In the list, select the document verification task that you want to work on.

    To work on a verification task that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Complete these steps as applicable:

    -   Under Document Information, enter information into the applicable fields.
    -   Attach any documents to be submitted for verification.
6.  In the **Work notes** field, enter any comments.

7.  Select **Submit document**.


## Result

A document verification task is created.

If Document Intelligence is integrated, once a document verification task is created, a record is also created on a Document Intelligence task if the following criteria are met:

-   The OCR processing needed checkbox is selected.
-   The document verification task has a document attached.
-   The document verification task shows a current stated of Submitted.

## What to do next

A document agent can [Work on a document verification task](../concept/doc-processor-work-on-doc-verification-task.md).

