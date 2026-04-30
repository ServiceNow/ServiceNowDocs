---
title: Create participants for an HTML document template
description: Define actions and the order of actions for participants. The type of action and order are considered while initiating document tasks.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Document Templates of type HTML, Configuring Document Templates, Document Templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Create participants for an HTML document template

Define actions and the order of actions for participants. The type of action and order are considered while initiating document tasks.

## Before you begin

-   Role required: sn\_hr\_core.admin
-   This content applies only to the document templates that are created in the Document Templates application \(sn\_doc\). Document Templates is different from HR Document Templates. For HR Document Templates, refer to [HR document templates](../concept/c_HRDocumentTemplates.md).

## Procedure

1.  Navigate to **All** &gt; **Document Template** &gt; **All Document Templates**.

2.  Select the HTML template you want to use.

3.  Configure the required template and click **Submit**.

4.  In the **Participants** related list, click **New**.

5.  On the form, fill in the fields:

<table id="table_ryw_fv4_byb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Display name of the mapped participant.

</td></tr><tr><td>

Action

</td><td>

Type of action performed by the participant: Sign**Note:** In addition, the participant can choose to decline signing the document. The option to decline signing appears only when the **Signing Type** is **ServiceNow**.

For more information, see [Sign an HTML document](sign-html-document.md).

</td></tr><tr><td>

User

</td><td>

Mapping user field to a participant.**Note:**

-   When you select a value, the participant is considered to be an internal user. If Participant Name and Participant Email fields \(optional for internal user\) are filled along with User field, the electronic signature task will be sent to Participant Name and Participant Email, not the Name and Email from the User field.

When you do not select a value in the User field, the participant will be considered an external user \(Participant who does not have access to ServiceNow system\). For such participants, Participant Name, Participant Email are to be specified.

-   The value in the User field is cleared when you save or update the template with the Advanced script field selected.


</td></tr><tr><td>

Participant name

</td><td>

Option to specify the name when the defined participant is an external user.**Note:**

-   When you select a value in User field, the Participant name field will be an optional field. When you do not select a value in User field, the Participant name field will be a mandatory field.
-   The value in the Participant name field is cleared when you save or update the template with the Advanced script field selected.
-   This field is available only when signing type is AdobeSign or DocuSign.


</td></tr><tr><td>

Participant email

</td><td>

Option to specify an email address when the defined participant is an external user. **Note:**

-   When you select a value in the User field, the Participant email field will be an optional field. When you do not select a value in User field, Participant email field will be a mandatory field.
-   The value in the Participant email field is cleared when you save or update the template with the Advanced script field selected.
-   This field is available only when signing type is AdobeSign or DocuSign.


</td></tr><tr><td>

Table

</td><td>

Table \(sys\_user table or any table extending sys\_user table\) from which you are choosing to populate the variables.

</td></tr><tr><td>

Document template

</td><td>

Name of the document template.

</td></tr><tr><td>

Document task template

</td><td>

Template selected on the Document Template task table to populate additional details for the document task, such as description and short description for sign tasks. **Note:** If additional details are not defined, the default values of the template are used in the document template task.

</td></tr><tr><td>

Advanced script

</td><td>

Option to display the Script field.

</td></tr><tr><td>

Script

</td><td>

Script indicating the participant conditions with User ID, Participant name and Participant email. This field is enabled only when the Advanced script field is selected.

</td></tr><tr><td>

Optional

</td><td>

When enabled, a participant will be skipped if the participant name and email is not available. This check is done during runtime only and not while configuring the template.

</td></tr><tr><td>

Signature height

</td><td>

Option to indicate the height of signature.

</td></tr><tr><td>

Signature width

</td><td>

Option to indicate the width of signature.

</td></tr></tbody>
</table>6.  Click **Submit**.


