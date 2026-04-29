---
title: Synchronize types and categories to Document Intelligence
description: If Document Intelligence is installed after document types and categories were set up in Document Processor, run this script to synchronize these values between the two applications.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Document Intelligence, Integrate, Financial Services Operations \(FSO\)]
---

# Synchronize types and categories to Document Intelligence

If Document Intelligence is installed after document types and categories were set up in Document Processor, run this script to synchronize these values between the two applications.

## Before you begin

Role required: admin

## About this task

Follow this procedure if Document Intelligence is installed after document types and categories were set up in Document Processor. Running the script is required to enable optical character recognition \(OCR\) processing on Document List Items.

## Procedure

1.  In the navigation filter, enter `sysauto_script.list`.

2.  On the Scheduled Script Executions screen, open the record **Sync document processor type and attributes to DocIntel**.

3.  Select **Execute Now**.


## Result

Document Categories and Document Types created in Document Processor before Document Intelligence was installed are also created in Document Intelligence. This enables OCR processing on Document List Items.

**Parent Topic:**[Integrating with Document Intelligence](../concept/integration-with-document-intelligence.md)

**Related topics**  


[Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

[Using Document Processor](../concept/using-document-processor.md)

[Create document list item definitions for a document list definition](doc-processor-associate-document-list-items-to-category.md)

