---
title: Document generation methods
description: A PDF document can be generated automatically, manually, or by using an API.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Document Templates: HR Service Delivery use case, Document Templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Document generation methods

A PDF document can be generated automatically, manually, or by using an API.

## Automatically

A PDF document is automatically added as an attachment to the case when:

1.  The [configured template](../task/configure-editable-pdf.md) is selected on the HR template of a service.
2.  The **Automatically Initiate Document tasks** case option is selected on the HR service of a case.
3.  The state of the HR case is changed to work in progress.
4.  The document tasks of all the participants are complete.

## Manually

A PDF document can be generated manually using the **Generate** option on the **Preview Document** option on the case.

## API

The following API generates and attaches the document to the target record that is passed to the API.

```
//recordId - Sys ID of the target record. This record must be from the table defined in the document template.
//documentTemplateId - Sys ID of the document template to use for pdf generation.
//pdfName - Name of the pdf generated
new sn_doc.GenerateDocumentAPI().generateDocumentForTask(recordId, documentTemplateId, pdfName);
```

**Note:** If your table is caller restricted, calling this API may generate RCA records from components in the Document Templates scope to your table. You must allow them.

**Parent Topic:**[Using Document Templates: HR Service Delivery use case](using-doc-templates.md)

**Related topics**  


[Document template categories](document-types-document-templates.md)

[Document Templates of type HTML](document-templates-flow-html.md)

[Document Templates of type PDF \(Advanced forms\)](document-templates-PDF-flow.md)

[Document Templates configurations](doc-template-configs.md#)

[Work on a document task](../task/work-doctemp-tasks.md)

[Document tasks generation](../task/task-mapped-participants.md)

