---
title: Create a document task
description: Create a document task and upload single or multi-page documents that are in JPEG, PNG, or PDF formats to start extracting text or classifying documents.
locale: en-US
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Document Intelligence, Enable AI experiences]
---

# Create a document task

Create a document task and upload single or multi-page documents that are in JPEG, PNG, or PDF formats to start extracting text or classifying documents.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

## Before you begin

Role required: sn\_docintel.creation\_agent

## About this task

These are the manual steps to create a document task. If you have integrations set up with other workflows, this task may be automated. See [Integrating Document Intelligence with other applications](../concept/integrating-docintel.md).

## Procedure

1.  Do one of the following:

    -   To create a document task for document data extraction, navigate to **All** &gt; **Document Intelligence** &gt; **Document Data Extraction** &gt; **Create Document Task**.
    -   To create a document task for document classification, navigate to **All** &gt; **Document Intelligence** &gt; **Document Classification** &gt; **Create Document Task**.
2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Display Name|The name associated with this use case. For example, PO-1.|
    |Use Case|The use case created for this document type.|

3.  Select the **Manage Attachments** icon and select the document you want to upload for processing.

    ![Manage attachments button that opens the Attachments dialog box](../image/upload-documentsQ31.png)

4.  Select **Process Task**.

    Document Intelligence analyzes the document and extracts data or classes for the fields defined in the use case.


## What to do next

Find the document task in the document tasks list. After the **Is Processed** field changes to True, Document Intelligence has completed the analysis of the document. You can proceed to [complete the document task](extract-data-from-documents.md), which helps train the AI through your input or review of the extracted fields.

