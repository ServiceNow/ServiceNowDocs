---
title: Configure an HR PDF document template for an Adobe Sign template
description: If you are using the Adobe Sign integration, configure an HR PDF document template for each Adobe Sign template that you want to make available for signing. You must map each signature field from the Adobe Sign template to an appropriate user field in a table.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrating with the Adobe Sign service, HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure an HR PDF document template for an Adobe Sign template

If you are using the Adobe Sign integration, configure an HR PDF document template for each Adobe Sign template that you want to make available for signing. You must map each signature field from the Adobe Sign template to an appropriate user field in a table.

## Before you begin

Create the Adobe Sign template that you want to make available for signing through theAdobe Sign system. See the Adobe Sign user guide for more information. You must also synchronize your accounts to bring the Adobe Sign template \(and any other new or updated templates\) into the ServiceNow system. See [Sync Adobe Sign with ServiceNow](https://www.servicenow.com/docs/access?context=setup-adobe-sign&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) for more information.

**Note:** Each Adobe Sign in template must have one associated document. Multiple documents per template are not supported.

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Document Templates**.

2.  Click **New** or open a record.

    **Note:** If you are creating a record, make sure to select **PDF Document Template**.

3.  On the PDF Document Template form, set the **Template type** field to `Adobe Sign Templates`.

    ![Set the template type to Adobe Sign Templates](../image/set-template-adobe.png)

    **Note:** Pre filled Adobe sign templates are not supported.

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

Set the value to `Adobe Sign Templates`.

</td></tr><tr><td>

Adobe Sign Document

</td><td>

Select the Adobe Sign template to use.**Note:** You must synchronize each time you need to get new or updated Adobe Sign templates.

</td></tr><tr><td>

HR criteria

</td><td>

Defines the conditions that the subject person of an HR case must meet for an HR agent to be able to access the HR document template on their behalf.**Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) API API.

</td></tr></tbody>
</table>5.  Right-click on the form header and click **Save**.

    The PDF Template Mappings section is displayed.

6.  In the **PDF Template Mappings** section, you must manually map fields from the Adobe Sign template to corresponding table fields to populate the document when it is generated for signing.

    ![How to assign the signing order for serial signing in Adobesign.](../image/pdf-mapping-adobe.png)

<table id="table_gs5_stf_sjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field name

</td><td>

Name of the field that is being mapped from the Adobe Sign system to the ServiceNow system. **Note:** Ensure that the **Field name** of **Document field type** `Signature` is specified as Participant1, Participant2, Participant3, and so on.

</td></tr><tr><td>

HR PDF Template

</td><td>

Name of the HR PDF template.

</td></tr><tr><td>

Document field

</td><td>

Suitable name of the field that is being mapped.

</td></tr><tr><td>

Document field type

</td><td>

Type of the document field that is being mapped, such as **Signature**, **Text**, or **check box**.

</td></tr><tr><td>

Mapping table

</td><td>

HR table that stores all the field mappings.

</td></tr><tr><td>

Mapping field

</td><td>

Reference field from which the value is rendered in the **Document** field.

</td></tr><tr><td>

Signing order

</td><td>

Order in which the participants are to sign the document. **Note:**

-   If the **Signing order** column is not visible, click the gear icon to personalize the list columns. Add the **Signing order** field to the Selected column.
-   Ensure that the signing order of the first participant is lesser than the signing order of the second participant.
-   The **Signing order** field remains empty in case of parallel signing.


</td></tr><tr><td>

Active

</td><td>

Option for enabling or disabling a field mapping.

</td></tr></tbody>
</table>    **Note:** Field mappings are case sensitive.

7.  Click **Submit**.


**Parent Topic:**[Integrating with the Adobe Sign service](../concept/integrating-with-adobe-sign-service.md)

