---
title: Import messages from a ticket manually
description: You can import the conversation with a user from Microsoft Teams and append them in the Comments to store all the important messages in the ServiceNow instance.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Request-based chat: Chat from classic view, Agent actions, Use ITSM and HRSD integrations with Microsoft Teams, Use Microsoft Teams integration for Employee Experience, Use, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Import messages from a ticket manually

You can import the conversation with a user from Microsoft Teams and append them in the **Comments** to store all the important messages in the ServiceNow instance.

## Before you begin

Role required: user

## About this task

Importing messages helps agents to view the history of the ticket, allow the requester to see all discussions about their ticket in one place. This helps to capture the information required for post-ticket review and continuous improvement processes.

## Procedure

1.  Navigate to an open ticket \(Incident, change request, request item, HR case or a catalog task\) in your ServiceNow instance.

2.  Click **Import messages from Microsoft Teams**.

3.  On the **Import messages from Microsoft Teams** form, fill in the fields:

<table id="table_tjg_yp5_knb"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Show conversations

</td><td>

Choose from:-   Started from this record: Lists all the communication tasks created for the record.
-   List all conversations: Lists all conversations by the logged in agent.


</td></tr><tr><td>

Select a conversation

</td><td>

Choose a conversation to import the messages for the record.

</td></tr><tr><td>

Import messages as

</td><td>

-   **Additional comments**: The messages will be appended under Additional comments.
-   **Work notes**: The messages will be appended under Work notes.


</td></tr></tbody>
</table>    ![Import messages from a record](../images/import-messages-record-01.png)

4.  Select the messages, files, and the images you would like to import and click **Import messages**.

    If you try to import the messages manually for a ticket that will automatically import the messages, the system displays a message that the chat is being imported using auto-import.

    ![Import messages modal error message for automaticlaly imported chats](../images/manual-import-error.png)


**Parent Topic:**[Request based chat - Start and import chat from classic view](../concept/initiate-conversation-requester.md)

