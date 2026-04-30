---
title: Configure an HR PDF document template for an ad hoc document
description: If you are using the Adobe Sign integration, configure an HR PDF document template for each ad hoc document that you want to make available for signing.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Adobe Sign service, HR Integrations, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure an HR PDF document template for an ad hoc document

If you are using the Adobe Sign integration, configure an HR PDF document template for each ad hoc document that you want to make available for signing.

## Before you begin

Create the managed document that you want to make available for signing through the Adobe Sign system. See [Managed Documents](https://www.servicenow.com/docs/access?context=c_ManagedDocuments&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

Role required: sn\_hr\_core.admin

You can use an existing or create an HR PDF document template. You can add signers to the document with Mark Signatures, and then map each signature field to an appropriate user field in a table. As part of the Adobe Sign integration, you can also enable serial signing for documents that require multiple signers.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Document Templates**.

2.  Click **New** or open a record.

    **Note:** If you are creating a record, make sure to select **PDF Document Template**.

3.  On the PDF Document Template form, set the **Template type** field to `HR PDF Templates`.

    ![Set the Template type field to HR PDF Templates.](../image/hr-pdf-document-template-for-adhoc.png)

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

Set the value to `HR PDF Templates`.

</td></tr><tr><td>

Document revision

</td><td>

Select the adhoc template to use.

</td></tr><tr><td>

HR criteria

</td><td>

Defines the conditions that the subject person of an HR case must meet for an HR agent to be able to access the HR document template on their behalf.**Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

</td></tr></tbody>
</table>5.  Right-click on the form header and click **Save**.

    The PDF Template Mappings section is displayed.

6.  [Configure an HR PDF document template](PDFTemplate.md), as appropriate.

    You can add signers to the document with **Mark Signatures**, and then map each signature field to an appropriate user field in a table. You can also parse the PDF to map document fields to corresponding table fields to auto-populate the document when it is generated for signing.

    **Note:** The positioning of **Mark Signatures** is not used, and the integration allows the signer to sign anywhere in the document.

7.  If you want to enable serial signing for documents that require multiple signers, assign the signing order for each signature field in the PDF Template Mappings section.

    If the **Signing order** column is not visible, click the gear icon to personalize the list columns. Add the **Signing order** field to the Selected column.

    **Note:**

    -   The **Signing order** field remains empty in case of parallel signing.
    -   Ensure that the **Field name** of **Document field type** `Signature` is specified as Participant1, Participant2, Participant3, and so on.
    -   Ensure that the signing order of the first participant is lesser than the signing order of the second participant.
8.  Click **Update**.


**Parent Topic:**[Integrating with the Adobe Sign service](../concept/integrating-with-adobe-sign-service.md)

