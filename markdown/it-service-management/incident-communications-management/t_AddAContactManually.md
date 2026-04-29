---
title: Add a user as a contact
description: Add a user to a communication plan if you have not added the user earlier in the contact. You can assign a communication task to the user to resolve an issue.
locale: en-US
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Incident Communications Management and Contacts, Managing Incident Communications, Incident Communications Management, IT Service Management]
---

# Add a user as a contact

Add a user to a communication plan if you have not added the user earlier in the contact. You can assign a communication task to the user to resolve an issue.

## Before you begin

Role required: ia\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Incident Communications Management** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Open an incident communications plan record.

3.  Select the **Users** related list and then select **New**.

    ![Add a user as a contact for the plan](../image/NewContactAdHoc.png)

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

The incident communication plan for which you are creating the contact.

</td></tr><tr><td>

Responsibility

</td><td>

Responsibility that the user is expected to handle throughout the communication process.

</td></tr><tr><td>

Type

</td><td>

Type of contact such as user, group, or recipient list that you want to involve in the plan. **Note:** To add a user, select **User** for the **Type** field.

</td></tr><tr><td>

User

</td><td>

Name of the user who is considered as the contact.

</td></tr></tbody>
</table>5.  Click **Submit**.

    The contact information appears in the Users related list.


**Parent Topic:**[Incident Communications Management and Contacts](../concept/c_IncidentAlertContact.md)

**Related topics**  


[Responsibilities for Incident Communication Plan](../reference/r_ResponsibilitiesForIncidentAlerts.md)

[Define contact responsibilities](t_CreateAContactResponsibility.md)

[Create a contact definition](t_CreateAContactDefinition.md)

[Create a default override](t_CreateADefaultOverride.md)

