---
title: Microsoft Teams Graph Spoke
description: The Microsoft Teams Graph spoke manages applications, calendar, teams, channels, chats, notifications, and webhooks in Microsoft Teams. To create, manage, or delete users and groups, use the Microsoft Entra ID spoke \(formerly Microsoft Azure Active Directory spoke\).
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-01-30"
reading_time_minutes: 12
keywords: [AI Agent, Agentic AI]
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Teams Graph Spoke

The Microsoft Teams Graph spoke manages applications, calendar, teams, channels, chats, notifications, and webhooks in Microsoft Teams. To create, manage, or delete users and groups, use the Microsoft Entra ID spoke \(formerly Microsoft Azure Active Directory spoke\).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:**

-   Teams in the Microsoft Teams Graph spoke are created from the groups in Microsoft Entra ID \(formerly Microsoft Azure Active Directory\). To create a team using the Microsoft Teams Graph spoke, the associated group must be present in Microsoft Entra ID.
-   User and group management can be done using Microsoft Entra ID only and not Microsoft Teams Graph spoke.
-   Teams can be created from the Microsoft Office 365 group only.
-   The team ID in Microsoft Teams is the same as the group ID of the associated group in Microsoft Entra ID.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Teams Graph spoke v4.4.1 is the latest version.

## Supported version

Microsoft Graph REST API v1.0.

## Spoke dependencies

If you’re having trouble installing the app, confirm that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   Flow Designer Model \(com.glide.hub.designer\_backend.model\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Remote Tables \(com.glide.script.vtable\)
-   ServiceNow IntegrationHub Action Step - Get Connection Info \(com.glide.hub.action\_step.get\_connection\_info\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Microsoft Teams Graph spoke provides a sample flow, Post ServiceNow Incident Worknotes Updates to Microsoft Teams Chat, to demonstrate automating the task of posting a Microsoft Teams chat message to the assigned user with details about the latest work notes added to the incident.

## Spoke subflows

The Microsoft Teams Graph spoke provides samples subflows to demonstrate automating the tasks. To customize a sample flow, copy it to the required application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Post Incident Details|Posts details of the required incident to a Microsoft Teams channel.|
|Process Inbound Notifications|Retrieves the details of the specified message based on the input data received from webhook subscription.|
|Renew Webhook Subscription Helper Subflow|Renews a subscription if renewal is required, which is decided based upon inputs.|
|Renew Webhook Subscriptions|Retrieves all the webhook subscriptions and renews them if renewal is required.|
|Subscribe Webhook|Creates a webhook subscription for the specified team's channel.|

## Spoke actions

The Microsoft Teams Graph spoke provides actions to automate team and channel tasks when an incident is created in the ServiceNow instance.

You can perform some actions by using the Microsoft Teams Spoke connection and the remaining actions by using the Microsoft Teams Graph Client Credentials connection.

The actions in the following table use the Microsoft Teams Spoke connection and credential alias record. These actions require the delegated permissions.

<table id="table_lh1_44v_m1c"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th><th colspan="2">

Permissions required \(from least to most privileged\)

</th></tr></thead><tbody><tr><td rowspan="2">

Application Management

</td><td>

Install Application to User

</td><td>

Installs the specified application in the personal scope of the user.

</td><td>

Delegated \(work or school account\)

</td><td>

TeamsAppInstallation.ReadWriteSelfForUser, TeamsAppInstallation.ReadWriteForUser

</td></tr><tr><td>

Look up User App Installation

</td><td>

Retrieves the details of the specified application's installation for the user.

</td><td>

Delegated \(work or school account\)

</td><td>

TeamsAppInstallation.ReadForUser, TeamsAppInstallation.ReadWriteSelfForUser, TeamsAppInstallation.ReadWriteForUser

</td></tr><tr><td>

Calendar Management

</td><td>

Look up Schedules

</td><td>

Retrieves the availability information \(free or busy\) for a collection of users, distributions lists, or resources \(rooms or equipment\) for the specified time period.

</td><td>

Delegated \(work or school account\)

</td><td>

Calendars.Read, Calendars.ReadWrite

</td></tr><tr><td rowspan="9">

Channel Management

</td><td>

Add Member to Channel

</td><td>

Adds the specified member to the specified channel.

</td><td>

Delegated \(work or school account\)

</td><td>

ChannelMember.ReadWrite.All

</td></tr><tr><td>

Create Channel

</td><td>

Create a new channel in a team.

</td><td>

Delegated \(work or school account\)

</td><td>

Channel.Create, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delete Channel

</td><td>

Removes the specified channel from the required team and deletes all conversations.

</td><td>

Delegated \(work or school account\)

</td><td>

Channel.Delete.All, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Look up Channel

</td><td>

Retrieves the properties and relationships of a channel.

</td><td>

Delegated \(work or school account\)

</td><td>

Channel.ReadBasic.All, ChannelSettings.Read.All, ChannelSettings.ReadWrite.All, Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Look up Channel by Name

</td><td>

Retrieves the Channel ID and properties given a channel name and team ID.

</td><td>

Delegated \(work or school account\)

</td><td>

Channel.ReadBasic.All, ChannelSettings.Read.All, ChannelSettings.ReadWrite.All, Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Look up Channel Members

</td><td>

Retrieves a list of channel members.

</td><td>

Delegated \(work or school account\)

</td><td>

ChannelMember.Read.All, ChannelMember.ReadWrite.All

</td></tr><tr><td>

Look up Channel Messages

</td><td>

Retrieves the list of messages in a channel of a team.

</td><td>

Delegated \(work or school account\)

</td><td>

ChannelMessage.Read.All

</td></tr><tr><td>

Look up Channels

</td><td>

Retrieves the list of channels in this team.

</td><td>

Delegated \(work or school account\)

</td><td>

Channel.ReadBasic.All, ChannelSettings.Read.All, ChannelSettings.ReadWrite.All, Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Remove Member from Channel

</td><td>

Removes the specified user from the specified channel.

</td><td>

Delegated \(work or school account\)

</td><td>

ChannelMember.ReadWrite.All

</td></tr><tr><td rowspan="8">

Chat Management

</td><td>

Create Chat

</td><td>

Creates a chat between the users.

</td><td>

Delegated \(work or school account\)

</td><td>

Chat.Create, Chat.ReadWrite

</td></tr><tr><td rowspan="2">

Look up Chat Message Deltas Stream

</td><td rowspan="2">

Retrieves the list of messages \(without the replies\) from a team's channel.

</td><td>

Delegated \(work or school account\)

</td><td>

Mail.ReadBasic, Mail.Read, Mail.ReadWrite

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Mail.ReadBasic, Mail.Read, Mail.ReadWrite

</td></tr><tr><td>

Look up Chat Messages

</td><td>

Retrieves the list of messages in a chat.

</td><td>

Delegated \(work or school account\)

</td><td>

Chat.Read, Chat.ReadWrite

</td></tr><tr><td>

Look up Chats

</td><td>

Retrieves the list of chats that the user is a part of.

</td><td>

Delegated \(work or school account\)

</td><td>

Chat.ReadBasic, Chat.Read, Chat.ReadWrite

</td></tr><tr><td>

Look up Message

</td><td>

Retrieves the details of the specified message.

</td><td>

Delegated \(work or school account\)

</td><td>

Chat.Read, Chat.ReadWrite

</td></tr><tr><td>

Look up Message Replies Stream

</td><td>

Retrieves the list of replies for the specified message from a team's channel.

</td><td>

Delegated \(work or school account\)

</td><td>

ChannelMessage.Read.All

</td></tr><tr><td>

Post Message to Chat

</td><td>

Posts message to a Microsoft Teams chat.

</td><td>

Delegated \(work or school account\)

</td><td>

ChatMessage.Send, Chat.ReadWrite, Group.ReadWrite.All

</td></tr><tr><td rowspan="6">

Notification Management

</td><td>

Post Change Details

</td><td>

Posts details of the required change to a Microsoft Teams channel.

</td><td>

Delegated \(work or school account\)

</td><td>

ChannelMessage.Send, Group.ReadWrite.All

</td></tr><tr><td>

Post Incident Details

</td><td>

Posts details of the required incident to a Microsoft Teams channel.

</td><td>

Delegated \(work or school account\)

</td><td>

ChannelMessage.Send, Group.ReadWrite.All

</td></tr><tr><td>

Post Message

</td><td>

Posts message to a Microsoft Teams channel.

</td><td>

Delegated \(work or school account\)

</td><td>

ChannelMessage.Send, Group.ReadWrite.All

</td></tr><tr><td>

Post Problem Details

</td><td>

Posts details of the required problem to a Microsoft Teams channel.

</td><td>

Delegated \(work or school account\)

</td><td>

ChannelMessage.Send, Group.ReadWrite.All

</td></tr><tr><td>

Post Reply to Message

</td><td>

Posts a reply to the specified message.

</td><td>

Delegated \(work or school account\)

</td><td>

ChannelMessage.Send, Group.ReadWrite.All

</td></tr><tr><td>

Post Record Details

</td><td>

Posts details of the specified record to the specified Microsoft Teams channel.

</td><td>

Delegated \(work or school account\)

</td><td>

ChannelMessage.Send, Group.ReadWrite.All

</td></tr><tr><td rowspan="10">

Team Management

</td><td>

Add Member to Team

</td><td>

Adds the specified user to the specified team.

</td><td>

Delegated \(work or school account\)

</td><td>

TeamMember.ReadWrite.All

</td></tr><tr><td>

Archive Team

</td><td>

When a team is archived, users can no longer send or like messages on any channel in team or make Team setting updates.

</td><td>

Delegated \(work or school account\)

</td><td>

TeamSettings.ReadWrite.All, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Create Team

</td><td>

Create a team from an existing Office 365 group.**Note:** The team ID is the same as the group ID.

</td><td>

Delegated \(work or school account\)

</td><td>

Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delete Team

</td><td>

Deletes the specified team.

</td><td>

Delegated \(work or school account\)

</td><td>

Group.ReadWrite.All

</td></tr><tr><td>

Look up Team

</td><td>

Retrieves the properties and relationships of a team.

</td><td>

Delegated \(work or school account\)

</td><td>

Team.ReadBasic.All, TeamSettings.Read.All, TeamSettings.ReadWrite.All, Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Look up Team Members Stream

</td><td>

Retrieves list of team members.

</td><td>

Delegated \(work or school account\)

</td><td>

TeamMember.Read.All, TeamMember.ReadWrite.All

</td></tr><tr><td>

Look up Teams by User

</td><td>

Lists teams of the user containing IDs and their display names.

</td><td>

Delegated \(work or school account\)

</td><td>

Team.ReadBasic.All, TeamSettings.Read.All, TeamSettings.ReadWrite.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Remove Member from Team

</td><td>

Removes the specified member from the specified team.

</td><td>

Delegated \(work or school account\)

</td><td>

TeamMember.ReadWrite.All

</td></tr><tr><td>

Unarchive Team

</td><td>

Restores an archived team. Enables members to post to channels in the team, make comments, and like posts again.

</td><td>

Delegated \(work or school account\)

</td><td>

TeamSettings.ReadWrite.All, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Update Team

</td><td>

Updates the properties of a specific team.

</td><td>

Delegated \(work or school account\)

</td><td>

TeamSettings.ReadWrite.All, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr></tbody>
</table>The actions in the following table use the Microsoft Teams Graph Client connection and credential alias record. These actions require the application permissions.

|Category|Action|Description|Permissions required \(from least to most privileged\)|
|--------|------|-----------|------------------------------------------------------|
|Calendar Management|Create Meeting|Creates an online meeting event in the MS Teams calendar.|Application|Calendars.ReadWrite|
|Delete Meeting|Deletes meeting event from the MS Teams calendar.|Application|Calendars.ReadWrite|
|Look up Meeting|Retrieves meeting event details from the MS Teams calendar.|Application|Calendars.Read|
|Look up Meeting Occurrences|Retrieves recurrence child meeting ID from the MS Teams calendar.|Application|Calendars.Read|
|Look up Meetings Stream|Retrieves meeting events details from the MS Teams calendar.|Application|Calendars.Read, Calendars.ReadWrite|
|Update Meeting|Creates an online meeting event in the MS Teams calendar.|Application|Calendars.ReadWrite|
|Webhook Management|Look up Webhook Subscription|Retrieves details of the required webhook subscription.|Application|ChannelMessage.Read.All, Chat.Read.All|
|Look up Webhook Subscriptions Stream|Retrieves details of all webhook subscriptions.|Application|ChannelMessage.Read.All, Chat.Read.All|
|Renew Webhook Subscription|Renews the specified webhook subscription.|Application|ChannelMessage.Read.All, Chat.Read.All|
|Subscribe Webhook|Creates a webhook subscription for the specified resource.|Application|ChannelMessage.Read.All, Chat.Read.All|
|Unsubscribe Webhook|Deletes the specified webhook subscription.|Application|ChannelMessage.Read.All, Chat.Read.All|

**Important:** Ensure that you’re aware about these default spoke configurations.

-   By default, the grant type is set to **Authorization Code**.
-   All actions in the Application Management, Channel Management, Chat Management, Notification Management, and Team Management categories, and Look up Schedules action in the Calendar Management category use the **Microsoft Teams Spoke** connection and credential alias and these actions require delegated permissions.
-   The Calendar and Webhook Management spoke actions \(except Lookup schedules action in Calendar Management\) use the **Microsoft Teams Graph Client Credentials** connection and credential alias and these actions require application permissions.

If you want to use the Microsoft Teams Graph Spoke without user interaction, you should change the grant type to **Client Credentials** so that the ServiceNow application can access the Microsoft Teams Graph API without user involvement. For instructions on how to change grant type and the required configurations, see the [Knowledge Base article - KB1635160](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1635160) on [ServiceNow - NOW Support](https://support.servicenow.com/now).

For more information about the required permissions, see [Microsoft Teams documentation](https://docs.microsoft.com/en-gb/).

**Note:** Some of the spoke actions require the channel ID, group ID, or team ID as one of the inputs. To learn these details, log in to Microsoft Teams, navigate to **Teams**, and click **Get link to channel** for the required channel. The channel link contains the required details. For example, if the channel link is `https://teams.microsoft.com/l/channel/ 19%3a1aa3730712e245a0af31e4095d66d613%40thread.skype /New%2520channel%2520in%2520team? groupId= 7fb91938-5e8c-4968-bf7d-3987df7716f3 &tenantId= a46df9b7-2c9b-49d5-8c9f-d1b3de4ba59f`, the group ID and team ID are `7fb91938-5e8c-4968-bf7d-3987df7716f3`, and the channel ID is`19:1aa3730712e245a0af31e4095d66d613@thread.skype` or `1aa3730712e245a0af31e4095d66d613`.

For more information about accessing the channel ID and group ID through Microsoft Teams, see [Microsoft Teams documentation](https://docs.microsoft.com/en-gb/).

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|Microsoft Teams application management AI agent|Automates tasks related to Microsoft Teams and Integration Hub. Performs actions such as looking up app installations and installing applications for the users.|
|Microsoft Teams channel management AI agent|Manages Microsoft Teams channels through IntegrationHub. It provides capabilities such as creating channels, managing members, and retrieving channel information.|
|Microsoft Teams chat management AI agent|Automates workflows between ServiceNow and Microsoft Teams by providing capabilities such as looking up chats and messages.|
|Microsoft Teams notification management AI agent|Automates communication between ServiceNow and Microsoft Teams by sending messages, updates, and replies to Microsoft Teams channels. The agent supports actions like 'Post Change Details', 'Post Message', and 'Post Reply to Message' to ensure effective notification management for change requests.|
|Microsoft Teams team management AI agent|Automates tasks such as creating and managing Teams, adding or removing members, and retrieving team-related information. Enhances team management and communication workflows within an organization.|
|Microsoft Teams calendar management AI agent|Automates workflows between ServiceNow and Microsoft Teams. Provides calendar management capabilities. Performs actions such as deleting, and retrieving meeting details.|

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Spoke modules

The Microsoft Teams Graph spoke adds the Microsoft Teams Graph Spoke to your ServiceNow instance and includes these modules.

|Module|Description|
|------|-----------|
|Delta Token|Displays the list of available Delta Tokens.|
|Webhook Registry|Displays the list of available webhook registries.|
|Webhook Decision Policy|Displays the list of decision policies.|
|Webhook Subscriptions|Displays the details of webhook subscriptions.|

## Microsoft account requirements

The Microsoft Teams Graph spoke requires registering an application using the Microsoft Azure portal to generate OAuth 2.0 tokens.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Microsoft Teams Graph spoke](../task/set-up-msteams.md#).

## MID Server requirements

The Microsoft Teams Graph spoke actions use REST calls, which can run on an instance or a MID Server. Use the connection record associated with the Microsoft alias to configure where actions run as well as set MID Server selection attributes. For more information, see [MID server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

