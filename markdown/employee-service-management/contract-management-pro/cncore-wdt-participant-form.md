---
title: Participant form for Microsoft Word document templates
description: Use the Participant form to add participants in a Microsoft Word document template.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create participants for document templates, Configure templates for standard letters, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Participant form for Microsoft Word document templates

Use the Participant form to add participants in a Microsoft Word document template.

<table id="simpletable_uzg_jlj_tkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique display name of the mapped participant.

</td></tr><tr><td>

Action

</td><td>

Type of action to be performed by the participant such as **Fill**, **Sign**, or **Review**.**Important:** In case of ServiceNow signing, **Fill** and **Review** actions are available for a PDF template. In case of external signing, **Sign** action is available for PDF and word document templates.

</td></tr><tr><td>

Order

</td><td>

Order in which a task has to be initiated for the participant to complete the action.

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

Template selected on the Document Template task table to populate additional details for the document task, such as description and short description for fill, sign and review tasks. **Note:** If additional details are not defined, the default values of the template are used in the document template task.

</td></tr><tr><td>

Due date source

</td><td>

Due date for the document task that is created for that participant.

</td></tr><tr><td>

Date offset type

</td><td>

Due date for the document task is picked from the task record. Additionally, you can offset the due date by days, weeks or months.

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

When enabled, a participant will be skipped if the participant user and participant email is not available. This check is done during runtime only and not while configuring the template.

</td></tr></tbody>
</table>**Parent Topic:**[Create participants for document templates](../task/cncore-wdt-create-participant.md)

