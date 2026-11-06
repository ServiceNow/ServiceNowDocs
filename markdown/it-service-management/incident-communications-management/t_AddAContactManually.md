---
title: Add a user as a contact
description: Add a user as a contact on an incident communication plan when the user isn't already a contact. You can then assign a communication task to the user to help resolve an issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-communications-management/t\_AddAContactManually.html
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Incident Communications Management and contacts, Managing incident communications, Incident Communications Management, IT Service Management]
---

# Add a user as a contact

Add a user as a contact on an incident communication plan when the user isn't already a contact. You can then assign a communication task to the user to help resolve an issue.

## Before you begin

Role required: ia\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Incident Communications Management** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/service-operations-workspace/redirect-ui16-module-links-sow.md).

2.  Open an incident communication plan record.

3.  Select the **Users** related list and then select **New**.

    \[Omitted image "NewContactAdHoc.png"\] Alt text: Add a user as a contact for the plan

4.  On the form, fill in the fields.

<table id="table_qjn_1dc_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Task table for which you are creating the contact.

</td></tr><tr><td>

Document

</td><td>

Incident communication plan for which you're creating the contact.

</td></tr><tr><td>

Responsibility

</td><td>

Responsibility that the user is expected to handle throughout the communication process.

</td></tr><tr><td>

Type

</td><td>

Type of contact, such as user, group, or recipient list, to involve in the plan. **Note:** To add a user, select **User** for the **Type** field.

</td></tr><tr><td>

User

</td><td>

Name of the user to add as the contact.

</td></tr></tbody>
</table>5.  Select **Submit**.

    The contact information appears in the Users related list.


**Parent Topic:**[Incident Communications Management and contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/c_IncidentAlertContact.md)

**Related topics**  


[Contact responsibilities for incident communication plans]()

[Define contact responsibilities]()

[Create a contact definition]()

[Create a default override]()

