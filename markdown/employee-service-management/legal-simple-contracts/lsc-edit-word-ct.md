---
title: Edit a contract template of type Microsoft word
description: Edit a contract template to reflect any modifications that must be included in the template to generate a standard contract when an employee submits a contract request.
locale: en-US
release: zurich
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Edit a contract template of type Microsoft word

Edit a contract template to reflect any modifications that must be included in the template to generate a standard contract when an employee submits a contract request.

## Before you begin

Role required: sn\_lg\_contracts.contracts\_config

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Simple Contracts Admin** &gt; **Contract Templates**.

2.  Open a contract template from the list.

3.  On the form, modify the fields.

<table id="table_qfw_c4s_ypb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the contract template.

</td></tr><tr><td>

Table

</td><td>

Table to which you want to associate the contract template.

</td></tr><tr><td>

Category

</td><td>

Document category to which you want to associate the contract template.

</td></tr><tr><td>

Document

</td><td>

The document from which you want to import template field mapping. The selected document should be a Microsoft Word \(.docx\) document and should have valid content controllers. For more information, see [Add content controls in a Microsoft Word document](lsc-cont-contr-word-tmplt.md).

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

State

</td><td>

The state is automatically set to Draft.

</td></tr><tr><td>

Application

</td><td>

Application to which the contract template belongs. This field is automatically set to the application scope in which you’re creating the contract template.

</td></tr><tr><td>

Active

</td><td>

Option to make the template active and available for use.

</td></tr></tbody>
</table>4.  In the **Contract Type** field, select only one category of the contract type.

    If you’re creating a template for non-disclosure agreement, select **Non Disclosure Agreement** as the contract type.

5.  Select **Parse Document** to extract any modified content marked by content control from the imported document.

    Any new added content controls will be listed under Template Mappings.

6.  Map any new meta data found during parsing.

    For more information, see [Update contract template mappings for legal contract template](lsc-template-map-msword.md).

7.  Select **Update** to save the modifications.


