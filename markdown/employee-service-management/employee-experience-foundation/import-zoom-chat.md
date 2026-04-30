---
title: Import Zoom Team Chat messages
description: Import the chat conversation manually or automatically with a user from  Zoom application, which appends and stores the messages in the  Comments section of the ticket in the ServiceNow instance.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Starting and importing a Zoom Team Chat, Enhance employee experience by integrating ServiceNow with Zoom, Integrate, ServiceNow for Zoom, Unified Employee Experience, Employee Service Management]
---

# Import Zoom Team Chat messages

Import the chat conversation manually or automatically with a user from  Zoom application, which appends and stores the messages in the  Comments section of the ticket in the ServiceNow® instance.

## Before you begin

You must have the write role to use the  Import messages from Zoom  feature for incident, request, and change request tasks. This role is available when you activate the IT Service Management role plugins or for all instances by default.

|Record|Role|Plugin|
|------|----|------|
|Incident|sn\_incident\_write|ITSM Roles - Incident Management \(com.snc.itsm.roles.incident\_management\) plugin|
|Change Request|sn\_change\_write|ITSM Roles — Change Management \(com.snc.itsm.roles.change\_management\) plugin|
|Request|sn\_request\_write|ITSM Roles — Request Management \(com.snc.itsm.roles.request\_management\) plugin|

Role required: agent

## About this task

Importing messages helps agents to view the history of a ticket in one place. So, the information required for post-ticket review is captured and results in continuous improvement processes.

When an agent imports a chat, attachments within the configured file size limit are uploaded to the record. If the uploaded attachments are larger than the configured file size limit, then those attachments appear as a link to the file on the  Zoom  server.

When an existing chat is continued, auto import occurs again. Auto import is cancelled when chats are archived.

If a parent chat in a thread is deleted, the **Import messages from Zoom** form displays the text that this message was deleted. The child messages in that thread are not deleted.

A tag with the label  **External**  indicates that a user is listed in the Zoom application users and not present in the ServiceNow instance, or when the user isn’t present in the Zoom application.

**Note:**

An agent can import a chat only if there’s an existing chat record for the ticket and they’re a participant of the chat.

## Procedure

1.  Navigate to an open task record \(incident, change request, or request item\) in your ServiceNow instance.

2.  Select  **Import messages from Zoom** from the Related Links section.

    **Note:**

    If you don’t see **Import messages from Zoom**, then on the form menu, select **Reload form** to refresh the ticket form.

3.  On the  Import messages from Zoom form, fill in the fields.

<table id="table_mm4_vgc_gvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select a conversation

</td><td>

Conversation to import the messages for the record.

</td></tr><tr><td>

Participants

</td><td>

List of users who are participants of the chat.

</td></tr><tr><td>

Import messages as

</td><td>

Method used to import messages.

 -   **Additional comments**: The messages are appended in an **Additional comments** field and the users can view them.
-   **Work notes**: The messages are appended in the **Work notes** field but can be viewed only by internal users.


</td></tr></tbody>
</table>    You can also select the nested message threads in a chat.

4.  Select **Import**.

    If the auto import of the messages is enabled in the chat configuration and you try to import the messages manually for a record, then the system displays a message that the chat is being imported using auto-import. For configuration information about auto import, see [Customize the Zoom chat form](create-chat-config-customize-zoom-chat-form.md).

5.  On the form menu, select **Reload form** to refresh the ticket form.


## Result

The imported chats and files are displayed in the **Activities** section of the ticket.

**Parent Topic:**[Starting and importing a Zoom Team Chat](../concept/start-import-chat.md)

