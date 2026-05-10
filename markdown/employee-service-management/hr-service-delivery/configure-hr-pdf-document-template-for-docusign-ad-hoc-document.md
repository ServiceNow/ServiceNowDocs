---
title: Configure an HR PDF document template for an ad hoc document
description: If you are using the DocuSign integration, configure an HR PDF document template for each ad hoc document that you want to make available for signing.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating with the DocuSign service, HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure an HR PDF document template for an ad hoc document

If you are using the DocuSign integration, configure an HR PDF document template for each ad hoc document that you want to make available for signing.

## Before you begin

Create the managed document that you want to make available for signing through the DocuSign system. See [Managed Documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/document-management-services/c_ManagedDocuments.md) for more information.

Role required: sn\_hr\_core.admin

You can use an existing or create a new HR PDF document template. You can add signers to the document with **Mark Signatures**, and then map each signature field to an appropriate user field in a table. You can also parse the PDF to map document fields to corresponding table fields to auto-populate the document when it is generated for signing. As part of the DocuSign integration only, you can also enable serial signing for documents that require multiple signers.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Document Templates**.

2.  Click **New** or open a record

    **Note:** If you are creating a new record, make sure to select **PDF Document Template**.

3.  On the PDF Document Template form, set the **Template type** field to `HR PDF Templates`.

    ![Set the Template type field to HR PDF Templates.](../image/hr-pdf-document-template-for-adhoc.png)

4.  Configure the HR PDF document template, as appropriate.

    You can add signers to the document with **Mark Signatures**, and then map each signature field to an appropriate user field in a table. You can also parse the PDF to map document fields to corresponding table fields to auto-populate the document when it is generated for signing. For further details on configuring an HR PDF document template, see .

    **Note:** The positioning of **Mark Signatures** is not used, and the integration allows the signer to sign anywhere in the document.

5.  If you want to enable serial signing for documents that require multiple signers, assign the signing order for each signature field in the PDF Template Mappings section.

    **Note:**

    -   By default, if a document has two or more signature fields, parallel signing is enabled.
    -   If the **Signing order** column is not visible, click the gear icon to personalize the list columns. Add the **Signing order** field to the Selected column.
    ![How to assign the signing order for serial signing in DocuSign.](../image/docusign-serial-signing.png)

6.  Click **Update**.


**Parent Topic:**[Integrating with the DocuSign service](../concept/docusign-integration-for-hr.md)

