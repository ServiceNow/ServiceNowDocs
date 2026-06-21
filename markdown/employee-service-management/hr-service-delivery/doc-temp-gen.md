---
title: Using Document Templates: Generic use case
description: Understand how to use Document Templates outside of HR Service Delivery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/hr-service-delivery/doc-temp-gen.html
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Document Templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Using Document Templates: Generic use case

Understand how to use Document Templates outside of HR Service Delivery.

## Before you begin

Role required: admin

## Procedure

1.  Define a document template for a given table, for example, Incident table.

2.  If participants are configured for the document template, use the following API to initiate document tasks for participants:

    ```javascript
    /**
    * Description: Method to prefill document with mapped values and attach it to record table.
    * @param {GlideRecord} taskGr (GlideRecord of task table)
    * @param {String} htmlBody html body of document (Optional, if not passed then it will be generated from template for html template)
    * @param {SysId} docTemplateId (sysId of document template)
    * @param {String} generatedPdfName name of generated pdf (Optional, if not passed then it will be taken from template name)
    * @param {String} documentId (word template attachment sysId) (Only for word templates)
    * @return {boolean} true/false
    */
    new sn_doc.GenerateDocumentAPI().initiateDocumentTasks(taskGr, htmlBody, docTemplateId, generatedPdfName, documentId)
    
    ```

3.  To generate a PDF document from a document template, use the following API:

    ```javascript
    /**
    * Description: Method to generate a PDF from a document template.
    * @param {GlideRecord} recordId (GlideRecord of task table)
    * @param {documentTemplateId} docTemplateId (sysId of document template)
    * @param {String} pdfName name of generated pdf (Optional, if not passed then it will be taken from template name)
    * @return {sysId} (sysId of the attachment)
    */
    new sn_doc.GenerateDocumentAPI().generateDocumentForTask(recordId, documentTemplateId, pdfName)
    ```

4.  To view the document tasks that are associated to a record:

    1.  Open the record, for example, an incident record.
    2.  Configure the related lists.\[Omitted image "config-rl.png"\] Alt text: Configure Related Lists on a record

        A slushbucket opens. Add **Document Task -&gt; Parent** and **Save**.\[Omitted image "config-rl2.png"\] Alt text: Add document Tasks related list to an incident record

        Document tasks associated to the record are displayed in **Document tasks** related list.

        \[Omitted image "doc-tasks-rl.png"\] Alt text: Document tasks related list appears on the record form


