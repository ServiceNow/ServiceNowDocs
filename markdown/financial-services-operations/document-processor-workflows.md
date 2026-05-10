---
title: Document Processor workflows
description: The Financial Services Document Processor application installs automated workflows for enabling document collection and verification.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Document Processor, Integrate, Financial Services Operations \(FSO\)]
---

# Document Processor workflows

The Financial Services Document Processor application installs automated workflows for enabling document collection and verification.

## Workflows available with the application

The following predefined workflows for Document Processor are available with the application.

|Document Processor workflows|
|----------------------------|
|Deferred Document Followup|
|Exception Document Approval|
|Generate DocIntel Field|
|Generate DocIntel Document task|
|Generate DocIntel Use case|

These workflows are built using [Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/flow-designer.md). The application admin can review and customize these predefined flows that are based on the business needs of an organization.

## General workflow for Document Processor

Document Processor determines the documents that are required in a workflow in a Financial Services Operations \(FSO\) application. If any documents must be verified, a document verification task is automatically generated for a document agent.

The following is a typical loan workflow in the Financial Services Loan Operations application.

**Note:** Depending on the request type, individual workflows might have additional or fewer tasks.

1.  The document processor determines the documents that are required. If any documents must be verified, a document verification task is generated for the document collector or agent.
2.  The document processor looks up existing documents that have already been verified.
3.  A document collector collects the required customer documents and submits the documents for verification, or requests an exception or deferral for specified documents.
4.  A document verification task is generated.
5.  A document agent manually verifies or rejects the document, or approves or rejects an exception or deferral request.

    **Note:** For documents specified to required OCR processing, Document Intelligence can automatically extract data and verify a document if the extracted data attributes are sufficiently provided. For more information, see [Integrating with Document Intelligence](integration-with-document-intelligence.md).


