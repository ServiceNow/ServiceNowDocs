---
title: Submit a document for verification
description: A document collector can collect and submit a document for verification.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Document Processor, Integrate, Financial Services Operations \(FSO\)]
---

# Submit a document for verification

A document collector can collect and submit a document for verification.

## Before you begin

Role required: sn\_doc\_processor.collector

## Procedure

1.  Navigate to **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![Lists icon.](../../../common/image/icon-list.png)\).

3.  In the **Lists** tab, under **Document verification**, open the task list.

    -   For your assigned tasks, select **Assigned to me**.
    -   For all document verification tasks, select **All**.
4.  In the list, select the document verification task that you want to work on.

    To work on a verification task that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  On the form under Document Information, fill in the fields as required.

    |Field|Description|
    |-----|-----------|
    |Document category|The document category assigned to this document, such as Proof of Identity.|
    |Document type|The document type assigned to this document, such as Passport.|
    |Valid through|The date up to which the document is valid.|
    |File name|Name of the file.|
    |File format|The file format of the document.|
    |File size|The size of the file.|

6.  On the form under Process Information, fill in the fields as required.

    For a description of the field values, see [Create document list item definitions for a document list definition](doc-processor-associate-document-list-items-to-category.md).

7.  Attach any documents to be submitted for verification.

8.  In the **Work notes** field, enter any comments.

9.  Select **Submit document**.


## Result

A document verification task is created.

If Document Intelligence is integrated, once a document verification task is created, a record is also created on a Document Intelligence task if the following criteria are met:

-   The OCR processing needed checkbox is selected.
-   The document verification task has a document attached.
-   The document verification task shows a current stated of Submitted.

## What to do next

A document agent can [Work on a document verification task](../concept/doc-processor-work-on-doc-verification-task.md).

