---
title: Create Document Templates for License and Permit Playbook
description: With the ServiceNow Document Templates application, you can create HTML and PDF document templates to generate standard letters or documents. You can automate and simplify the process of filling, signing, and reviewing a document online.​ Use the Document Templates application to generate templates for various types of Licenses and Permits issued through the License and Permit Playbook.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [License and Permit Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Create Document Templates for License and Permit Playbook

With the ServiceNow Document Templates application, you can create HTML and PDF document templates to generate standard letters or documents. You can automate and simplify the process of filling, signing, and reviewing a document online.​ Use the Document Templates application to generate templates for various types of Licenses and Permits issued through the License and Permit Playbook.

## Before you begin

Role required: admin

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

Determines where the documents are attached. Select License and Permit Case \[sn\_gsm\_license\_permit\_case\] to map the generated PDF to the case. Select License and Permit Install Base Item \[sn\_gsm\_license\_permit\_install\_base\_item\] to map the generated PDF fields to the Item Received.

</td></tr><tr><td>

Category

</td><td>

Document category in which the template is added. For License and Permit Playbook, select License and Permit.

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

User criteria

</td><td>

Audience criteria for this document. For example, you can create a permit intended for only Canadian residents.**Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Start date

</td><td>

Date starting which the PDF document template is valid. **Start date** helps in maintaining multiple versions of same template.**Note:** Start date must be before the end date.

</td></tr><tr><td>

End date

</td><td>

Date until which the PDF document template is valid. **End date** helps in maintaining multiple versions of same template.By default, if values in **Start date** and **End date** are blank, it is implied that the template will always be valid.

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
-   Translation feature is available only when the language plug-ins are installed on the instance.


</td></tr><tr><td>

Signing type

</td><td>

Option to specify the application that is used for signing or filling the document. For example, ServiceNow Sign, DocuSign or AdobeSign.**Note:** Signing types are available only when respective integration plug-ins are installed.

</td></tr><tr><td>

Attachment type

</td><td>

Option to upload a new document or select a document from ServiceNow Managed Documents.

</td></tr><tr><td>

Document

</td><td>

Option to upload the attachment of a fillable PDF for further customization.**Note:** This field appears when **Upload new document** is selected in **Attachment type**.

</td></tr><tr><td>

Document revision

</td><td>

Option to select a document from ServiceNow Managed Documents.**Note:** This field appears when **Select from document revision** is selected in **Attachment type**.

</td></tr><tr><td>

Active

</td><td>

Option for enabling the PDF document template for use.

</td></tr><tr><td>

Acknowledgment text

</td><td>

Text that prompts the user to select a check box when submitting a filled document.

</td></tr><tr><td>

Source template

</td><td>

Source template from which you created a copy of current template.

</td></tr></tbody>
</table>5.  Select the **Parse PDF** related link to automatically parse information and fields from the PDF and store that information in the PDF Mapping table for reuse.

    Each PDF field can now be mapped to its corresponding Mapping Field in the License and Permit install base table.

6.  In the **PDF Template Mappings** related list, define additional PDF field mappings.

    See [Define a PDF field mapping](https://www.servicenow.com/docs/access?context=edit-pdf-mappings&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US) for more information.

7.  Select **Update**.

    To determine what Document Template to use for generation, you must map the created Document Template to the corresponding Install Base Item/Items Received extension table. This is accomplished by using Document Template Mapping in Decision Tables.

8.  Navigate to **Decision Management** &gt; **Decision Builder**.

9.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Document Template Category|Use this field for having multiple templates for a single Install Base Item Table.|
    |Table Name|Use this field for what table should map to the document template.|
    |Document Template|Use this field to indicate what Document Template to use for a given document template category and table name.|
    |isPdfTemplate|Use this field to indicate whether the Document Template selected is a PDF template \(value = true\) OR an HTML template \(value = false\)|

10. Add additional decision rows to configure additional Document Templates.


## Result

The PDF generated by the Document Template is created after the **Propose decision** activity is granted/approved. You will be able to view the generated PDF that is attached to the corresponding install base item/item received in the **Create License/Permit** activity in the Decision stage.

## What to do next

In the **Participants** related list, add additional participants. See [Create participants for a PDF document template](https://www.servicenow.com/docs/access?context=create-participant&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US) for more information.

