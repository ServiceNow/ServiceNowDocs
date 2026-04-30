---
title: Create document list item definitions for a document list definition
description: Create document list item definitions for a document list definition. For example, for the Proof of Name Change document category, the document list item could be Name change of customer.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Document Processor, Integrate, Financial Services Operations \(FSO\)]
---

# Create document list item definitions for a document list definition

Create document list item definitions for a document list definition. For example, for the Proof of Name Change document category, the document list item could be Name change of customer.

## Before you begin

Role required: sn\_doc\_processor.admin

You can associate one or more document list item definitions with a document list definition.

## Procedure

1.  Navigate to **Document Processor** &gt; **Administration** &gt; **Document list definitions**.

2.  In the list, click the document list that you want to add a document list item to.

3.  In the Document List Item Definitions related list, click **New**.

4.  On the form, fill in the fields.

<table id="doc-list-item-definition-fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Document list

</td><td>

Name of the document type that is displayed in document service tasks. An example is Passport.

</td></tr><tr><td>

Document category

</td><td>

Option to activate this document type to be used in document service tasks.

</td></tr><tr><td>

Use existing document

</td><td>

Option to enable to request for use of a previously submitted document that currently exists in the system.

</td></tr><tr><td>

Can request exception

</td><td>

Option to enable request for exemption from submission of this document list item.

</td></tr><tr><td>

Can request deferment

</td><td>

Option to enable to request for deferral of this document list item for submission at a future date.

</td></tr><tr><td>

Has fillable document

</td><td>

Option to include a Document template with the task.

</td></tr><tr><td>

No of documents

</td><td>

The number of documents required for each category.

</td></tr><tr><td>

Mandatory

</td><td>

Set the document list item as mandatory, if required. **Note:** If a document list item is set as mandatory, the document verification task in a workflow can't be closed without verifying the documents of this category.

</td></tr><tr><td>

OCR processing needed

</td><td>

Option to require text or data to be automatically extracted from the document list item definition using optical character recognition. For more information, see [Integrating with Document Intelligence](../concept/integration-with-document-intelligence.md).

</td></tr></tbody>
</table>5.  Select **Submit**.


**Parent Topic:**[Configuring Financial Services Operations Document Processor](../concept/configuring-fso-document-processor.md)

