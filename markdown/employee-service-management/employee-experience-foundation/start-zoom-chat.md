---
title: Start a Zoom Team Chat
description: Start a Zoom Team Chat with an employee through an open ticket to resolve an incident, request item, and change request.Reassign a ticket to another user with a valid Zoom account.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Starting and importing a Zoom Team Chat, Enhance employee experience by integrating ServiceNow with Zoom, Integrating and using ServiceNow with Zoom, ServiceNow for Zoom, Unified Employee Experience, Employee Service Management]
---

# Start a Zoom Team Chat

Start a Zoom Team Chat with an employee through an open ticket to resolve an incident, request item, and change request.

## Before you begin

You must have the write role to use the  Start Zoom chat  feature for incident, request, and change request tasks. This role is available when you activate the IT Service Management role plugins or for all instances by default.

|Record|Role|Plugin|
|------|----|------|
|Incident|sn\_incident\_write|ITSM Roles - Incident Management \(com.snc.itsm.roles.incident\_management\) plugin|
|Change Request|sn\_change\_write|ITSM Roles — Change Management \(com.snc.itsm.roles.change\_management\) plugin|
|Request|sn\_request\_write|ITSM Roles — Request Management \(com.snc.itsm.roles.request\_management\) plugin|

Ensure you’ve installed the fix script to enable the display of the Zoom chat icon associated with the Caller field. For more information, see [Install fix-script for Collaboration services for Zoom](install-fix-script-cs.md).

Role required: agent

## Procedure

1.  Navigate to an open task record \(incident, change request, or request item\) in your ServiceNow instance.

2.  Start the chat by selecting **Start Zoom Chat** or the Start Zoom chat icon ![Start Zoom chat icon](../images/icon-start-zoom-chat.png) associated with the Caller field.

3.  In the Start Zoom chat dialog box, select the participants.

    All users from the assigned group for the ticket are in the Recommended section of the dialog box by default. The user who initiates the chat is added to the Selected list of participants.

4.  On the form, fill in the fields.

<table id="table_uc4_rnb_gvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add Participants

</td><td>

Option to add the users and stakeholders to work toward the resolution of the ticket.

 -   **User**: Enter the name of the user to include in the chat.
-   **Group**: Enter the group of users to be included in the chat.

If the On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is activated, the On-Call Scheduling users are added when you select a group. When On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin isn’t activated, it adds all users from the selected group.

-   **Email**: Enter a valid email of the participant to be included in the chat.
 After adding the required stakeholders, select  **Add to selected**.

</td></tr><tr><td>

Chat title

</td><td>

The title of the chat that will be displayed in the Zoom application. The default title is the ticket number appended with the short description.

</td></tr><tr><td>

Create an opening message

</td><td>

Option to provide an opening message to the user before beginning an interaction.

</td></tr></tbody>
</table>5.  Select **Start Chat**.

    When the user validation is complete and a Zoom Channel is created for the current instance of the ticket, you are directed to the chat channel in the Zoom application.

    Zoom Team Chat displays the chat title and the opening message provided by the agent.

6.  Interact with the ticket requester in Zoom Team Chat.

    You can send files supported by the Zoom application.

    On the ServiceNow instance, the system captures work notes about the chat details.

    A Zoom chat Interaction record is automatically created if the requester is a participant in the chat conversation. The requester can then access chat details in the **Activities** section. For information about a ticket requester mapping, see [Create requester mapping](create-requester-mapping-zoom.md).

    1.  In the Activities section of the record, find the comment that contains a link to access the chat interaction.
    2.  Select the link.

        The chat transcript is stored in the  Activities  section.

<table id="table_clm_jvb_gvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Users

</td><td>

Users associated with the chat.

</td></tr><tr><td>

Document

</td><td>

Source record number.

</td></tr><tr><td>

Initiated by

</td><td>

Agent who has initiated the chat interaction.

</td></tr><tr><td>

Topic

</td><td>

Chat title.

</td></tr><tr><td>

Activities

</td><td>

Chat transcript.

</td></tr></tbody>
</table>7.  Resume the chat either with the same user or with the same user plus additional users in the Start Zoom chat form.

    -   To continue the chat from the record with the same user, select **Continue Chat**.
    -   To start a new chat that includes additional users, add the users and provide a title for the chat in the **Chat title ** field and an opening message in the **Create an opening message** field.

**Parent Topic:**[Starting and importing a Zoom Team Chat](../concept/start-import-chat.md)

## Reassign a ticket

Reassign a ticket to another user with a valid Zoom account.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to an open task record \(incident, change request, or request item\) in your ServiceNow instance.

2.  Search and select the new user name in the **Assigned to** field.

    The new user must have a valid Zoom account. Else the ticket is not assigned to the new user and an error message is added in the system logs.

    Any logged in Zoom user who is not a participant of ticket/chat can reassign the ticket to a valid user on behalf of the chat initiator.

3.  Right-click the form header and click **Save**.


