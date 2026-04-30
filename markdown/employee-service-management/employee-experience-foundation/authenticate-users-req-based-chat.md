---
title: Add permissions to the Microsoft Azure application
description: Assign permissions to users to enable them to start chat and import chat conversations with employees from Microsoft Teams to ServiceNow instance.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure Request-based chat on the Microsoft Azure portal, Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Add permissions to the Microsoft Azure application

Assign permissions to users to enable them to start chat and import chat conversations with employees from Microsoft Teams to ServiceNow® instance.

## Before you begin

Role required: admin

## Procedure

1.  Log in to the Microsoft Azure portal.

2.  Navigate to **Azure Services** &gt; **Azure Active Directory** &gt; **Manage** &gt; **App registrations**.

3.  Select the app that is created to enable agents to import the conversations from Microsoft Teams to the ServiceNow instance.

    Example: `Request based chat app`.

4.  Navigate to **Manage** &gt; **API Permissions** &gt; **Add a permission** &gt; **Microsoft Graph**.

5.  Select **Delegated permissions**.

6.  In the **Select permissions** field, enter the following permissions.

    -   Offline\_access \(delegated\): ServiceNow stores an access token for each user, which enables them to reauthenticate with ServiceNow, within Microsoft Teams, without having to go through a login prompt. Offline access enables you to refresh the access token automatically.
    -   Chat.ReadWrite \(delegated\): The Read part of the Chat.ReadWrite permission enables you to import request-based chats from Microsoft Teams. The Write part of the Chat.ReadWrite permission is used in the “Start Chat” screen, where an opening message is provided on behalf of the agent.
    -   User.Read \(delegated\): This permission is added when an app is created to read the basic information of a user like the name and email-id.
    -   User.ReadBasic.All \(delegated\): This permission is required to obtain the names and Azure IDs of users. ServiceNow stores the Azure ID to create chats and import chats on behalf of users.
    -   Files.Read.All \(delegated\): This permission is used when request-based chats are imported from Microsoft Teams. It enables attachments to be imported as part of the Teams chat.
    -   ChatMember.ReadWrite \(delegated\): When a request with a Teams chat is set to inactive, participants are automatically removed from the corresponding chat. This permission is required to remove the chat participants.
    -   Chat.Create \(delegated\): This permission is used to create request-based chats.
    -   Chat.ReadBasic \(delegated\): This permission is used when request-based chats are imported. It enables you to display which participant sent each message in the chat.
    -   Presence.Read.All\(delegated\): This permission is used to fetch a user's presence status from Microsoft Teams.
7.  Select **Add permissions**.

8.  In the **API permissions** screen, select the **Grant admin consent for \{tenant\}** link.

9.  Select **Yes** on the pop-up dialog box.

10. After upgrading an Azure application, remove the user tokens and reauthorize the users to fetch a token with the added permissions.

    1.  Log in to your ServiceNow instance.

    2.  Navigate to **All** &gt; **System OAuth** &gt; **Manage Tokens**

    3.  Remove the user tokens for the single tenant chat app.

    **Note:** Users must log in to their Microsoft Azure active directory account to fetch a token with the added permissions.


**Parent Topic:**[Register and configure the Request-based chat application on the Microsoft Azure portal](register-app-req-based-chats.md)

