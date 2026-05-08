---
title: Create Document Templates for License and Permit Playbook
description: With the ServiceNow Document Templates application, you can create HTML and PDF document templates to generate standard letters or documents. You can automate and simplify the process of filling, signing, and reviewing a document online.​ Use the Document Templates application to generate templates for various types of Licenses and Permits that will be issued to applicants through the License and Permit Playbook.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [License and Permit Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Create Document Templates for License and Permit Playbook

With the ServiceNow Document Templates application, you can create HTML and PDF document templates to generate standard letters or documents. You can automate and simplify the process of filling, signing, and reviewing a document online.​ Use the Document Templates application to generate templates for various types of Licenses and Permits that will be issued to applicants through the License and Permit Playbook.

## About this task

By default, the License and Permit Playbook comes with a standard License and Permit document template, used for generating standard license or permit documents to be issued to the applicant via the Government Service Portal. Use the following steps to generate additional document templates for custom license and permit class types that fall outside of the standard, default template.

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

Audience criteria for this document. For example, you can create a permit intended for only Canadian residents.**Note:** When defining conditions like case sensitivity or null values, see API GlideFilter - Scoped, Global.

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
</table>5.  Select **Update**.

    You must map the newly created Document Template to the corresponding Install Base Item/Items Received extension table you wish to generate the license/permit in. This is accomplished by using Document Template Mapping in Decision Tables. By default, the default License and Permit Document Template, mapped to the License and Permit Install Base table, is used to generate a standard license/permit PDF document.

6.  Select the **Parse PDF** related link to automatically parse information and fields from the PDF, and store that information in the PDF Mapping table for reuse.

    **Note:** **Parse PDF** appears only for an editable PDF.

    Using **Parse PDF** will allow each PDF field to be mapped to its corresponding Mapping Field in the License and Permit install base table.

7.  In the **PDF Template Mappings** related list, define additional PDF field mappings.

    **Note:** The **PDF Template Mappings** related list is only available for an editable PDF. See Define a PDF field mapping for more information.

8.  Navigate to **Decision Management** &gt; **Decision Builder**.

9.  Open the **Document Template Mapping** table.

10. On the form, fill in the fields to add additional decision rows to configure additional Document Templates.

    |Field|Description|
    |-----|-----------|
    |Document Template Category|Use this field to have multiple templates for a single Install Base Item Table. For example, you may enter **License and Permit** as the Document Template Category to map Document Templates that are different from the default template to the License and Permit category.|
    |Table Name|Select the table that should map to the document template. For a license/permit that is to be issued to an applicant at the end of the application process, select the License and Permit install base item table \(sn\_gsm\_license\_permit\_install\_base\_item\).|
    |Document Template|Indicate what Document Template will be used for the document template category and table name. Select the Document Template that was created in steps 3-5.|
    |isPdfTemplate|Select **\(value = true\)** if the Document Template selected is a PDF template. Select **\(value = false\)** if the Document Template selected is an HTML template.|

11. Select **Submit** or **Save**.

12. Open the **Install Base Item Table Mapping** table.

13. On the form, fill in the fields to configure the table in which an install base item \(the license/permit that is to be issued to an applicant at the end of the application process\) should be created.

    By default, this is the License and Permit case table \(sn\_gsm\_license\_permit\_case\).

    |Field|Description|
    |-----|-----------|
    |Table Name|Select the case table where the License and Permit request will be created. By default, this is the License and Permit case table \(sn\_gsm\_license\_permit\_case\).|
    |Document Template|Indicate what Document Template will be used for the document template category and table name. Select the Document Template that was created in steps 3-5.|

14. Select **Submit** or **Save**.


## Result

After the agent makes a decision in the **Propose decision** activity of the License and Permit Playbook, the PDF generated by the Document Template is created. An agent will be able to view the generated PDFin the **Create License/Permit** activity in the **Decision** stage, and the applicant will be able to view the PDF in the portal.

