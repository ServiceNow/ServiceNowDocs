---
title: Configure a Microsoft Word document template
description: Upload a word document and add participants with whom you require signatures.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure templates for standard letters, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure a Microsoft Word document template

Upload a word document and add participants with whom you require signatures.

## Before you begin

-   Role required: sn\_cm\_core.contract\_config
-   Set content controls in a Microsoft Word document.

## Procedure

1.  Navigate to **All** &gt; **Document Templates**.

2.  Select **New**.

3.  Select **Word Document Template**.

4.  On the form, fill in the fields:

<table id="table_xm3_tm3_zhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the word document template.

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

Option for enabling the word document template for use.

</td></tr><tr><td>

User criteria

</td><td>

Audience criteria for this document. For example, you can create a letter intended for only Canadian employees.**Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Signing type

</td><td>

Option to specify the application that is used for signing the document.-   The default value is none. If none, then document will not be triggered for signature. If DocuSign or AdobeSign is selected, then document shall be triggered for electronic signature via cases.
-   You can change the signing type from None to DocuSign or Adobe Sign or vice versa, when the template is in Draft or editing state.

**Note:** Signing types are available only when respective integration plugins are installed.

</td></tr><tr><td>

Document

</td><td>

Option to upload the attachment of a word \(.docx\) files only.

</td></tr><tr><td>

Template date format

</td><td>

Format in which you want the date to appear when an agent previews the document, generates the attachment, or initiates document tasks for participants.**Note:**

-   When signing using a ServiceNow application or the AdobeSign application: If no value is selected in **Template date format**, the value specified in the **template\_date\_format** system property is considered. If both **Template date format** and **template\_date\_format** system property are empty, the value in the Date format field from the agent's user profile is considered.
-   When signing using a DocuSign application: The date format selected in Signing settings in the DocuSign application is considered over **Template date format** in the configured word template in a ServiceNow instance.


</td></tr><tr><td>

Template language

</td><td>

Language in which you want dynamic tokens to be translated when an agent previews the document, generates the attachment, or initiates document tasks for participants.**Note:**

-   Template language is a mandatory field. The default language is none.
-   Translation feature is available only when language plugins are installed on the ServiceNow instance.


</td></tr><tr><td>

Source template

</td><td>

Source template from which you created a copy of the current template.

</td></tr><tr><td>

Start date

</td><td>

Date on which the Word document template becomes valid. Providing a start date helps when maintaining multiple versions of same template.

</td></tr><tr><td>

End date

</td><td>

Date until which the Word document template is valid. Providing an end date helps when maintaining multiple versions of same template.

 If the values in the **Start date** and **End date** fields are empty the template will always be valid.

 **Note:**

If you specify an end date, you must also specify a start date.

</td></tr></tbody>
</table>5.  Select **Submit**.


## What to do next

1.  To add participants with whom you must obtain signatures, see [Create participants for document templates](cncore-wdt-create-participant.md).
2.  To create template mappings, click **Parse Word Document**.
3.  To insert signatures, open a **Signature\_** record in the **Template mappings** related list.

    1.  In **Document field type**, specify Signature.
    2.  In the **Participant** field, specify the participant with whom you require the signature.
    3.  Click **Update**.
    Similarly, update the following records.

    -   Sign
    -   Sign date
    -   field
    -   Signatory name
    -   Signatory email
    -   Signatory title
    For a full list, see [Content controls in Word Document Templates](../concept/cncore-wdt-doc-contentctrl.md)

4.  Select **Publish**.

**Parent Topic:**[Configure document templates for standard letters or documents](cncore-wdt-other-bu.md)

