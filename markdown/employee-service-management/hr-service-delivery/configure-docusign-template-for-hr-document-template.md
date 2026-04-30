---
title: Configure an HR PDF document template for a DocuSign template
description: If you are using the DocuSign integration, configure an HR PDF document template for each DocuSign template that you want to make available for signing.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [DocuSign service, HR Integrations, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure an HR PDF document template for a DocuSign template

If you are using the DocuSign integration, configure an HR PDF document template for each DocuSign template that you want to make available for signing.

## Before you begin

Create the DocuSign template that you want to make available for signing through the DocuSign system. See the [DocuSign eSignature User Guide](https://support.docusign.com/en/guides/ndse-user-guide) for more information. You must also synchronize your accounts to bring the DocuSign template \(and any other new or updated templates\) into the ServiceNow system. See [Synchronize Docusign with ServiceNow](https://www.servicenow.com/docs/access?context=sync-docusign-servicenow&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) for more information.

**Note:** Each DocuSign template must have one associated document. Multiple documents per template are not supported.

Role required: sn\_hr\_core.admin

## About this task

You must map each signature field from the DocuSign template to an appropriate user field in a table. You can also map fields from the DocuSign template to corresponding table fields to auto-populate the document when it is generated for signing.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Document Templates**.

2.  Click **New** or open a record.

    **Note:** If you are creating a new record, make sure to select **PDF Document Template**.

3.  On the PDF Document Template form, set the **Template type** field to `DocuSign Template`.

    ![Set the Template type field to DocuSign template.](../image/hr-pdf-document-template-for-docusign.png)

4.  Fill in the fields on the form, as appropriate.

<table id="table_knm_31c_zhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the HR document template.

</td></tr><tr><td>

Table

</td><td>

HR table that the HR document template is associated with.

</td></tr><tr><td>

Document type

</td><td>

Document type that the HR document template is categorized under.

</td></tr><tr><td>

Active

</td><td>

Option to activate the HR document template for use.

</td></tr><tr><td>

Template type

</td><td>

Set the value to `DocuSign Template`.

</td></tr><tr><td>

DocuSign template

</td><td>

Select the DocuSign template to use.**Note:** You must synchronize each time you need to get new or updated DocuSign templates. To synchronize, navigate to **DocuSign** &gt; **Accounts** and click the **Get Accounts** related link. See [Synchronize Docusign with ServiceNow](https://www.servicenow.com/docs/access?context=sync-docusign-servicenow&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) for more information.

</td></tr><tr><td>

HR criteria

</td><td>

Defines the conditions that the subject person of an HR case must meet for an HR agent to be able to access the HR document template on their behalf.**Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

</td></tr></tbody>
</table>5.  Right-click on the form header and click **Save**.

    The **Get template fields status** field, **Get Template Fields** related link, and PDF Template Mappings section displays.

6.  Click the **Get Template Fields** related link.

    **Note:** If any changes are made to the signature or document fields on the DocuSign template, you must click the **Get Template Fields** related link to synchronize those changes. Existing mappings are not affected.

    ![Click the Get Template Fields related link.](../image/hr-pdf-doc-template-docusign-get-template-fields.png)

7.  When the **Get template fields status** field changes to **Completed**, reload the form.

    **Note:** If you are using a Safari browser, you must reload the form to see the changed state.

    In the **PDF Template Mappings** section, a list of the mappable fields displays.

8.  In the **PDF Template Mappings** section, you must map each signature field from the DocuSign template to an appropriate user field in a table.

    **Note:** Configuration of the signature fields, including for parallel and serial signing, must be completed within the DocuSign system. You cannot add or configure the signature fields from within the HR PDF document template.

    ![How to map table fields to signature fields on a DocuSign template.](../image/docusign-template-signature-mapping.png)

9.  In the **PDF Template Mappings** section, you can also map fields from the DocuSign template to corresponding table fields to auto-populate the document when it is generated for signing.

    **Note:**

    -   Make sure that the data type of the DocuSign field matches that of the table field.
    -   Mapping is not supported for the following DocuSign field types:
        -   Initial
        -   Date signed
        -   Payment item
        -   Formula
        -   Attachment
        -   Note
        -   Approve
        -   Decline
10. Click **Update**.


**Parent Topic:**[Integrating with the DocuSign service](../concept/docusign-integration-for-hr.md)

