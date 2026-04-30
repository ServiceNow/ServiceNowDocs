---
title: Configure a PDF document template
description: Upload an editable, fillable PDF template and customize the template according to your business needs.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Document Templates of type PDF \(Advanced forms\), Configure, Document Templates, HR Documents, HR Service Delivery, Employee Service Management]
---

# Configure a PDF document template

Upload an editable, fillable PDF template and customize the template according to your business needs.

## Before you begin

Role required: sn\_hr\_core.admin and Delegated developer

**Note:**

-   For legally binding e-signatures and digital signatures use the following signing types: [DocuSign](../concept/docusign-doc.md), [AdobeSign](../concept/adobe-sign-doc.md), [Digital Signature - Smart Cards](https://www.servicenow.com/docs/access?context=digital-signature&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   Update sets do not support large attachments. If your template includes large documents, manually export the PDF template record XML from the source instance and import it into the target instance.

## About this task

How to configure a PDF document template 

## Procedure

1.  Navigate to **All** &gt; **Document Templates** &gt; **All Document Templates**.

2.  Select **New**.

3.  Select **PDF Document Template**.

4.  On the form, fill in the fields:

<table id="table_xm3_tm3_zhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the PDF document template.

</td></tr><tr><td>

Table

</td><td>

Tables appear based on the application scope selected.

</td></tr><tr><td>

Category

</td><td>

Document category in which the template is added.

</td></tr><tr><td>

Application

</td><td>

Scope of the application in which the document template is created.

</td></tr><tr><td>

State

</td><td>

Current state of the document template.-   **Draft**: Indicates that the document template is not yet published.
-   **Editing**: Indicates that the document template is being edited after it has been published.
-   **Published**: Indicates that the document template can be consumed by services and cases.


</td></tr><tr><td>

Active

</td><td>

Option for enabling the PDF document template for use.

</td></tr><tr><td>

User criteria

</td><td>

Audience criteria for this document. For example, you can create a letter intended for only Canadian employees.**Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Signing type

</td><td>

Option to specify the application that is used for signing the document. For example, ServiceNow Sign, [DocuSign](../concept/docusign-doc.md), [AdobeSign](../concept/adobe-sign-doc.md), [Digital Signature - Smart Cards](https://www.servicenow.com/docs/access?context=digital-signature&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

**Note:** Signing Types are available only when respective integration plugins are installed.

</td></tr><tr><td>

Document storage destination

</td><td>

Option to specify the location where the signed document is stored.**Note:** This option appears only when **Digital Signature - Smart Cards** is selected as Signing Type.

</td></tr><tr><td>

Owner

</td><td>

Option to specify the owner of the document storage destination.**Note:** This option appears only when **Digital Signature - Smart Cards** is selected as Signing Type.

</td></tr><tr><td>

Attachment type

</td><td>

Option to upload a new document or select a document from ServiceNow Managed Documents.

</td></tr><tr><td>

Document revision

</td><td>

Option to select a document from ServiceNow Managed Documents.**Note:** This field appears when **Select from document revision** is selected in **Attachment type**.

</td></tr><tr><td>

Document

</td><td>

Option to upload the attachment of a fillable PDF for further customization.**Note:** This field appears when **Upload new document** is selected in **Attachment type**.

</td></tr><tr><td>

Start date

</td><td>

Date starting which the PDF document template is valid. **Start date** helps in maintaining multiple versions of same template.**Note:** Start date must be before the end date.

</td></tr><tr><td>

End date

</td><td>

Date until which the PDF document template is valid. **End date** helps in maintaining multiple versions of same template.By default, if values in **Start date** and **End date** are empty it will imply that the template will always be valid.

If you specify an end date, you must also specify a start date.

</td></tr><tr><td>

Template date format

</td><td>

Format in which you want the date to appear when an agent previews the document, or generates the attachment, or initiates document tasks for participants.**Note:**

-   When signing using a ServiceNow application or the AdobeSign application: If no value is selected in **Template date format**, the value specified in the **template\_date\_format** system property is considered. If both **Template date format** and **template\_date\_format** system property are empty, the value in the Date format field from agent's user profile is considered.
-   When signing using the DocuSign application: The date format selected in Signing settings in the DocuSign application is considered over **Template date format** in the configured PDF template in a ServiceNow instance.


</td></tr><tr><td>

Template language

</td><td>

Language in which dynamic tokens are translated when an agent previews the document, or generates the attachment, or initiates document tasks for participants.**Note:**

-   Template language is a mandatory field. The default language is none.
-   Translation feature is available only when the language plugins are installed on the instance.


</td></tr><tr><td>

Acknowledgment text

</td><td>

Text that prompts the user to select a check box when submitting a filled document.

</td></tr><tr><td>

Source template

</td><td>

Source template from which you created a copy of current template.

</td></tr></tbody>
</table>5.  Select **Submit** or **Save**.


## What to do next

-   Select the **Parse PDF** related link to automatically parse information on the PDF and store that information in the PDF Mapping table for reuse.
-   In the **Participants** related list, [create participants](create-participant.md#).
-   In the **PDF Template Mappings** related list, [define field mappings](edit-pdf-mappings.md).
-   Select [Mark a signature block](create-participant.md#).
-   Publish the template. Flows using the template might get effected in case you want to edit a published template.

