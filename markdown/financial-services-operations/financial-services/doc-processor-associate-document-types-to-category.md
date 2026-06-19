---
title: Associate document types to a document category
description: Associate the relevant document types to a document category. For example, for the Proof of Identity document category, the types of documents could be Driver's License and Passport.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/financial-services/doc-processor-associate-document-types-to-category.html
release: australia
product: Financial Services
classification: financial-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Document Processor, Integrate, Financial Services Operations \(FSO\)]
---

# Associate document types to a document category

Associate the relevant document types to a document category. For example, for the Proof of Identity document category, the types of documents could be Driver's License and Passport.

## Before you begin

Role required: sn\_doc\_processor.admin

You can associate one or more document types with a document category.

## Procedure

1.  Navigate to **Document Processor** &gt; **Administration** &gt; **Document Categories**.

2.  In the list, select the document category that you want to add a document type to.

3.  In the Document type related list, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the document type that is displayed in document service tasks. An example is Passport.|
    |Active|Option to activate this document type to be used in document service tasks.|

5.  Select **Submit**.

6.  Select the newly created Document Type record.

7.  In the Document Type record, select **New** in the Attributes related list to define an attribute for the document type.

    Attributes are defined values in a document type, such as first name, last name, or date of birth. These attributes define the values Document Intelligence extracts from documents.

8.  Fill out the **Name** field for the attribute, and select **Submit**.


## What to do next

[Create a document list definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services/doc-processor-define-document-list.md)

**Parent Topic:**[Configuring Financial Services Operations Document Processor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services/configuring-fso-document-processor.md)

