---
title: Create or modify an e-signature template
description: Create or modify an e-signature template to define an electronic document and signature configuration for use in task forms.
locale: en-US
release: zurich
product: e-Signature
classification: e-signature
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using e-signature, E-signature, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create or modify an e-signature template

Create or modify an e-signature template to define an electronic document and signature configuration for use in task forms.

## Before you begin

Role required: sn\_esign.admin or sn\_esign.config\_manager

Each template is associated with a document type such as a managed document or knowledge article, and you can configure the template so that the signatory is required to sign the document with their typed or drawn signature, credentials, or as an acknowledgment.

## Procedure

1.  Navigate to **All** &gt; **E-signature** &gt; **E-signature template**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

<table id="table_ywy_fhh_wgb"><thead><tr><th>

Field

</th><th colspan="2">

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td colspan="2">

Name of the e-signature template.

</td></tr><tr><td>

Task table

</td><td colspan="2">

Task table that the e-signature template is associated with.

</td></tr><tr><td>

Document type

</td><td colspan="2">

Document type of the e-signature template. Select one of the following:-   **HR document template**: Make sure that the **Task table** field is set to HR Task \[sn\_hr\_core\_task\].

The HR document template that the signatory will sign is selected on the HR case form. See [Select an HR document template for an e-signature task](https://www.servicenow.com/docs/access?context=select-hr-document-template-for-e-signature-task&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

-   **Knowledge article**: In the **Knowledge article** field, select the knowledge article that the signatory will sign.
-   **Managed document**: In the **Managed document** field, select the managed document that the signatory will sign.


</td></tr><tr><td>

Signature type

</td><td colspan="2">

Signature type of the e-signature template. Select one of the following:-   **Acknowledgment**: The signatory acknowledges the document by accepting and completing the task.

**Note:** This option is not available for HR document templates.

-   **Credential**: The signatory signs the document with their credentials.

**Note:** This option is not available for HR document templates.

-   **Signature**: The signatory signs the document with their typed or drawn signature.


</td></tr><tr><td>

Acknowledgment text

</td><td colspan="2">

Adds a check box with accompanying acknowledgment text that the user must select before the signing is completed. This option can be used with any signature type.**Note:** Acknowledgment text is limited to 1,000 characters.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


## What to do next

You can use the e-signature template in task forms to request electronic signatures from users.

**Parent Topic:**[Using e-signature](../concept/using-esignature.md)

