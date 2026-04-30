---
title: ServiceNow for Microsoft Teams integration API permissions for Request-based chat and SSO
description: Following are API permissions requested by the ServiceNow integration with Microsoft Teams for Request-based chat and SSO.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# ServiceNow for Microsoft Teams integration API permissions for Request-based chat and SSO

Following are API permissions requested by the ServiceNow® integration with Microsoft Teams for Request-based chat and SSO.

|App|API Permission|Description|
|:---|:-------------|:----------|
|Request-Based Chat|Offline\_access \(delegated\) \(Application\)|ServiceNow® stores an access token for each user, which allows them to re-authenticate with ServiceNow, within Microsoft Teams, without having to go through a login prompt. Offline access allows us to automatically refresh the access token.|
|Chat.ReadWrite \(delegated\)|The Read part of the Chat.ReadWrite permission allows us to import request-based chats from Microsoft Teams. The Write part of the Chat.ReadWrite permission is used in the “Start Chat” screen, where an opening message is provided on behalf of the agent.|
|User.Read \(delegated\)|This permission is automatically added whenever an app is created to read the basic information of the user like name, email-id.|
|User.ReadBasic.All \(delegated\)|This permission is required to obtain the names and Microsoft Azure IDs of users. ServiceNow stores the Azure ID in order to create chats on behalf of users and import chats on their behalf.|
|Files.Read.All \(delegated\)|This permission is used when importing request-based chats from Microsoft Teams. It allows attachments to be imported, as part of the Microsoft Teams chat.|
|ChatMember.ReadWrite \(delegated\)|When a request with a Teams chat is set to inactive, participants are automatically removed from the corresponding chat. This permission is required to remove the chat participants.|
|Chat.Create \(delegated\)|Permission used in the creation of reauthenticatequest-based chats.|
|Chat.ReadBasic \(delegated\)|This permission is used when importing request-based chats. It allows us to display which participant sent each message in the chat.|
|Presence.Read.All \(Delegated\)|This permission is used when starting a Microsoft Teams chat to get informed of the presence of each user who will be added to the chat. This allows users to know real time status of chat participants before adding them to the group chat.|
|User.Read.All \(Application\)|This permission is used in Guest access feature, where a guest member can also start a chat. Microsoft does not allow a Guest Token \(with delegated permission\) to access the '/users' API end point. So, the Application permission is needed to fetch details of Microsoft Azure users and map the UPN with ServiceNow users.|
|Tab SSO|User.Read \(delegated\)|This permission enables the user to authenticate into a ServiceNow Portal embedded in Microsoft Teams.|
|Offline\_access \(delegated\)|This permission is required for the use of Tab SSO, to enable user authentication with a Microsoft Teams tab.|
|openid \(delegated\)|This permission is required for accessing the ID tokens.|
|email \(delegated\)|This permission is required to add the user's primary email address to the ID token.|
|TeamsActivity.Send \(delegated\)|This permission is required to send a team work activity to user.|
|profile \(delegated\)|This permission is required for giving the basic user details.|

**Parent Topic:**[ServiceNow for Microsoft Teams reference](reference-sn-teams.md)

