---
title: Request-based chat - Start and import chat from field decorator
description: Interact with a requester in Microsoft Teams for an issue related to an incident, request item, change request, and a catalog task ticket to quickly resolve the ticket.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Request-based chat - Chat from Workspace, Agent actions, Use ITSM and HRSD integrations with Microsoft Teams, Use Microsoft Teams integration for Employee Experience, Use, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Request-based chat - Start and import chat from field decorator

Interact with a requester in Microsoft Teams for an issue related to an incident, request item, change request, and a catalog task ticket to quickly resolve the ticket.

## Before you begin

Role required: user with access to the respective records

## Procedure

1.  Navigate to an open ticket \(an incident, a change request, a request item, an HR case, or a catalog task\) in your ServiceNow instance.

2.  Point to ![Field decorator](../images/field-decorator-a-ws.png) next to the **Opened for** field.

    The chat is initiated with the user in **Microsoft Teams**.

    ![Agnet Workspace User presence](../images/agent-workspace-start-chat-modal-user-presence.png)

    When you start typing the names of the participants, the system displays their current status in Microsoft Teams. The status is also displayed against their name in the **Participants** field.

3.  On the form, fill in the fields.

<table id="table_v3t_f1b_sqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Participants

</td><td>

Option to add the users and the stakeholders to work towards the resolution of the ticket.

</td></tr><tr><td>

Groups

</td><td>

Option to add the groups required to work towards the resolution of the ticket.

</td></tr><tr><td>

Recommended

</td><td>

System displays the list of users associated with the ticket.

 Select the user to include in the chat conversation.

</td></tr><tr><td>

Chat title

</td><td>

The chat title specified shows up as the title of the chat in Microsoft Teams. The default title is the ticket number appended with the short description. You can modify the chat title.

</td></tr><tr><td>

Create an opening message

</td><td>

Option to provide an opening message to the user before beginning the interaction.

</td></tr><tr><td>

Choose your preferred chat client

</td><td>

Option to choose the default chat client.

 -   Desktop Application – Open the chat interaction in Microsoft Teams desktop application.
-   Web Client – Opens the chat interaction in Microsoft Teams web client.
 The system remembers the selected option and will open the chats in the preferred chat client for all the further chat interactions.

</td></tr></tbody>
</table>4.  Click **Start Chat**.

    The Microsoft Teams app displays the chat title and the opening message provided by the agent.

    ![Chat conversation](../images/chat-conversation-ms-teams.png)

    The system captures the work notes about the chat details.

    ![Chat work notes](../images/record-work-space.png)


**Parent Topic:**[Request-based chat - Start and import chat from Workspace](../concept/initiate-chat-agent-workspace.md)

