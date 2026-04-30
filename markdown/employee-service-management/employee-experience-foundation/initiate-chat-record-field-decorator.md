---
title: Request-based chat - Start and import chat from field decorator
description: Interact with a requester in Microsoft Teams from the chat icon from the workspace to quickly resolve the ticket.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Request-based chat: Chat from classic view, Agent actions, Use ITSM and HRSD integrations with Microsoft Teams, Use Microsoft Teams integration for Employee Experience, Use, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Request-based chat - Start and import chat from field decorator

Interact with a requester in Microsoft Teams from the chat icon from the workspace to quickly resolve the ticket.

## Before you begin

Role required: user with access to the respective records

## Procedure

1.  Navigate to an open ticket \(an incident, a change request, a request item, an HR case or a catalog task\) in your ServiceNow instance.

2.  Point to ![Microsoft Teams](../images/teams-decorator.png) next to the **Caller** field.

3.  Within the dialog box that appears, select the participants for the chat.

    ![Start chat modal with user presence status](../images/start-chat-modal-fd-user-presence.png)

    The dialog box displays the **Recommended** and **Selected** participants along with their current presence status in Microsoft Teams.

    All users from the assigned group for the ticket are in the recommended section by default. The user who initiates the chat is added to the selected list of participants.

4.  On the form, fill the fields.

<table id="table_lrq_gx1_sqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add Participants

</td><td>

Option to add the users and the stakeholders to work towards the resolution of the ticket.

 -   **Users**: Enter the name of the user to include in the chat.
-   **Group**: Enter the group of users to be included in the chat.

If the On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is activated, the On-Call Scheduling users will be added when you select a group. On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin isn't activated, it adds all users from the selected group.

-   **Email**: Enter a valid email of the participant to be included in the chat.
 After adding the required stakeholders, click **Add to selected**.

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
</table>5.  Click **Start Chat**.

    The Microsoft Teams app displays the chat title and the opening message provided by the agent.

    ![Chat conversation](../images/chat-conversation-ms-teams.png)

    The system captures the work notes about the chat details.

    ![Chat work notes](../images/chat-work-notes.png)

    If the agent initiates the chat from the record with the same user, the **Start Microsoft Teams Chat** appears as shown.

    ![Continue chat modal](../images/continue-chat.png)

    The system displays **Continue Chat** button to resume the conversation. However, if any other user is added, the chat modal displays the **Chat title** and the **Create an opening message** fields.

    The interaction is only created when the conversation is with the requester. If the conversation doesn't include the requester, such as a conversation between the agent and a collaborator, an interaction is not created, but the Microsoft Teams chat record is still created.

    A Microsoft Teams chat interaction is automatically created and you can access the chat details from the Activities log.

    1.  In the Activities log of the record, look for the comment that has the link to access the chat interaction.
    2.  Click the link.

        The chat transcript is stored in the **Activities** section.

        ![Chat details in Activities section](../images/chat-details-activities-section.png)

    |Field|Description|
    |:----|:----------|
    |Users|Users associated with the chat|
    |Document|Source record number|
    |Initiated by|Agent who has initiated the chat interaction.|
    |Auto Import|Status of the auto-import messages. If the option is not selected, the messages pertaining to the record will not be auto-imported.|
    |Topic|Chat title|
    |Activities|Chat transcript|


**Parent Topic:**[Request based chat - Start and import chat from classic view](../concept/initiate-conversation-requester.md)

