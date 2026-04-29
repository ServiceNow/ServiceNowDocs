---
title: Using Document Templates: HR Service Delivery
description: Learn how to use Document Templates along with the HR Service Delivery application.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Document Templates, Document Templates, HR Documents, HR Service Delivery, Employee Service Management]
---

# Using Document Templates: HR Service Delivery

Learn how to use Document Templates along with the HR Service Delivery application.

**Note:** Only HTML and PDF document templates are supported in HR Service Delivery. Word document templates is not supported in HR Service Delivery.

## Activate plugin

As an administrator, activate the Document Templates plugin \[com.snc.document\_templates\].

## Generate document tasks for participants

To use the Document Templates application for filling, signing, and approving a document online, perform the following steps:

1.  Configure a document template by defining participants, defining tasks for participants, and inserting signatures. For configuring PDF document templates, see [Document Templates of type PDF \(Advanced forms\)](document-templates-PDF-flow.md), and for configuring HTML document templates, see [Document Templates of type HTML](document-templates-flow-html.md).
2.  Associate the document template to an HR case template.
3.  Add the HR case template while you [Configure an HR service](../task/configure-hr-service.md).
4.  Create a case under the configured HR service.
5.  Generate document tasks manually or automatically, see [Document tasks generation](../task/task-mapped-participants.md). Participants receive document tasks for filling, signing, and reviewing a document. When the document tasks of all the participants are complete, the final document is added as an attachment to the case.

End to end flow for document tasks 

## Generate a PDF document

To use the Document Templates application for generating a PDF document, perform the following steps:

1.  Create a document template. For configuring PDF document templates, see [Document Templates of type PDF \(Advanced forms\)](document-templates-PDF-flow.md), and for configuring HTML document templates, see [Document Templates of type HTML](document-templates-flow-html.md).

    **Note:** Defining participants and inserting signatures is not required if you want to use Document Templates only for generating documents.

2.  Associate the document template to an HR case template.
3.  Add the HR case template while you [Configure an HR service](../task/configure-hr-service.md).
4.  Create a case under the configured HR service.
5.  Click **Preview document**.
6.  If you want to modify the content in the document template, click **Edit**.

    **Note:** If you make any changes to variables in the HTML document template, you will no longer be able to reset the variables to their original values. You will have to enter the variable values manually.

7.  To generate a PDF copy of the document template, click Re**generate**.

-   **[Document tasks generation](../task/task-mapped-participants.md)**  
Document tasks can be generated either automatically or manually. The tasks get generated in the order defined for the participants.

**Parent Topic:**[Using Document Templates](using-doc-templates.md)

**Related topics**  


[Using Document Templates: Custom use case](../task/doc-temp-gen.md)

[Working on a document task](../task/work-doctemp-tasks.md)

[Using Guided Tours in Document Templates](../task/guided-tours-doc-temp.md)

