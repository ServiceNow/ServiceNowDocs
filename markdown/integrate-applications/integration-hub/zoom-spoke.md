---
title: Zoom Spoke
description: Create and manage Zoom meetings with the Zoom spoke from your ServiceNow instance. With this spoke, you can add participants, retrieve details, end or delete a meeting, or fetch the participant details of a conference.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Zoom Spoke

Create and manage Zoom meetings with the Zoom spoke from your ServiceNow instance. With this spoke, you can add participants, retrieve details, end or delete a meeting, or fetch the participant details of a conference.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Zoom spoke v4.6.2 is the latest version.

## Supported versions

Zoom API version v2.0.

## Spoke dependencies

If you’re having trouble installing the app, make sure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Key Management Framework \(com.glide.kmf.global\)
-   NOW Platform Encryption \(com.glide.now.platform.encryption\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)

## Spoke flows

This spoke has no sample flows.

## Spoke subflows

The Zoom spoke provides sample subflows for processing inbound events that are related to meetings, recordings, webinars, and users. Available sample subflows are described in the following table.

<table id="table_hrg_1hg_h4b"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Zoom Process Meeting Events

</td><td>

Handles Zoom meeting webhook events.

</td></tr><tr><td>

Zoom Process Recording Events

</td><td>

Handles Zoom recording webhook events.

</td></tr><tr><td>

Zoom Process User Events

</td><td>

Handles Zoom user webhook events.

</td></tr><tr><td>

Zoom Process Webinar Event

</td><td>

Handles Zoom webinar webhook events.

</td></tr><tr><td>

Create Zoom Meeting

</td><td>

Creates a Zoom meeting and provides the Zoom meeting URL.This subflow is used by the Meeting scheduler AI agent in the [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md) application.

</td></tr></tbody>
</table>## Spoke modules

The Zoom spoke adds the Zoom application to your instance and includes the modules in the following table.

|Module|Description|
|------|-----------|
|Phone Numbers|Displays a list of Zoom Phone numbers.|
|Zoom Webhook Registries|Displays a list of webhook registries that are associated to Zoom.|

## Spoke actions

The Zoom spoke provides you with actions so that you can automate Zoom tasks when events occur in the ServiceNow AI Platform. Th available actions are described in the following table.

<table id="table_u1p_kh2_hfb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th><th>

Granular scope needed

</th></tr></thead><tbody><tr><td rowspan="3">

Cloud Recording Management

</td><td>

Look up meeting recording settings

</td><td>

Retrieves the settings of the meeting’s cloud recordings.**Note:** The meeting password is retrieved and displayed as plain text.

</td><td>

cloud\_recording:read:recording\_settings:admin

</td></tr><tr><td>

Look up meeting recordings

</td><td>

Retrieves all the recorded meetings for the specified meeting ID.

</td><td>

cloud\_recording:read:list\_recording\_files:admin

</td></tr><tr><td>

Look up recordings stream

</td><td>

Lists all the recorded meetings of the specified user.

</td><td>

cloud\_recording:read:list\_user\_recordings:admin

</td></tr><tr><td rowspan="18">

Phone Management

</td><td>

Assign calling plan To User

</td><td>

Assigns a calling plan to a user.

</td><td>

phone:write:calling\_plan:admin

</td></tr><tr><td>

Assign phone number to user

</td><td>

Assigns a phone number to a user who has already enabled Zoom Phone.

</td><td>

phone:write:user\_number:admin

</td></tr><tr><td>

Get country codes \(metadata\)

</td><td>

Retrieves the metadata of countries and their ISO codes.

</td><td>

 

</td></tr><tr><td>

Look up account call logs stream

</td><td>

Retrieves the call logs for an account.

</td><td>

phone:read:list\_call\_logs:admin

</td></tr><tr><td>

Look up calling plans

</td><td>

Retrieves a list of calling plans.

</td><td>

phone:read:list\_calling\_plans:admin

</td></tr><tr><td>

Look up phone number details

</td><td>

Retrieves the details of a specified phone number in a Zoom account.

</td><td>

phone:read:numbers:admin

</td></tr><tr><td>

Look up phone numbers stream

</td><td>

Retrieves the list of phone numbers.

</td><td>

phone:read:list\_numbers:admin

</td></tr><tr><td>

Look up phone users stream

</td><td>

Retrieves all the users that are associated to an account with assigned Zoom Phone licenses.

</td><td>

phone:read:list\_users:admin

</td></tr><tr><td>

Look up user call logs stream

</td><td>

Retrieves the call logs of a user’s Zoom Phone.

</td><td>

phone:read:list\_call\_logs:admin

</td></tr><tr><td>

Look up user phone profile

</td><td>

Retrieves a Zoom Phone user’s profile.

</td><td>

phone:read:user:admin

</td></tr><tr><td>

Look up user recordings stream

</td><td>

Retrieves a Zoom Phone user’s recordings.

</td><td>

phone:read:list\_recordings:admin

</td></tr><tr><td>

Look up user phone settings

</td><td>

Retrieve a user's Zoom Phone profile.

</td><td>

phone:read:user\_setting:admin

</td></tr><tr><td>

Look up user voicemails Stream

</td><td>

Retrieves a Zoom Phone user’s voicemails.

</td><td>

phone:read:list\_voicemails:admin

</td></tr><tr><td>

Unassign user calling plan

</td><td>

Unassigns a calling plan to a user who has enabled Zoom Phone.

</td><td>

phone:delete:users\_calling\_plan:admin

</td></tr><tr><td>

Unassign user phone number

</td><td>

Unassigns a phone number to a user who has enabled Zoom Phone.

</td><td>

phone:delete:user\_number:admin

</td></tr><tr><td>

Update main company number

</td><td>

Updates the main company number of an account.

</td><td>

 

</td></tr><tr><td>

Update user phone profile

</td><td>

Updates a user’s Zoom Phone profile.

</td><td>

phone:update:user:admin

</td></tr><tr><td>

Update user phone settings

</td><td>

Updates the settings of a specific Zoom Phone user.

</td><td>

phone:update:user\_setting:admin

</td></tr><tr><td rowspan="11">

Meeting Management

</td><td>

Add meeting registrant

</td><td>

Registers a participant for a specific meeting.

</td><td>

meeting:write:meeting:admin

</td></tr><tr><td>

Create meeting

</td><td>

Creates a meeting for a user using their Zoom user ID or the email address and other details such as start time, type of meeting, and agenda. The action can also include in the meeting details one or more alternative hosts' email ID.

</td><td>

meeting:write:meeting:admin

</td></tr><tr><td>

Download Meeting Transcript

</td><td>

Downloads the meeting transcript for the specified transcript ID.

</td><td>

cloud\_recording:read:recording:admin

</td></tr><tr><td>

Delete meeting

</td><td>

Deletes a specific meeting by using its meeting ID.

</td><td>

meeting:delete:meeting:admin

</td></tr><tr><td>

End meeting

</td><td>

Ends an ongoing meeting.

</td><td>

meeting:delete:meeting:admin

</td></tr><tr><td>

Look up meeting Details

</td><td>

Gets details of a specific meeting by its meeting ID.

</td><td>

meeting:read:meeting:admin

</td></tr><tr><td>

Update Meeting

</td><td>

Identifies a meeting by its ID and then updates its details such as start time, duration, and topic.

</td><td>

meeting:update:meeting:admin

</td></tr><tr><td>

Look up ended meeting instances

</td><td>

Lists all the meeting instances that were ended.

</td><td>

meeting:read:list\_meetings:admin

</td></tr><tr><td>

Look up live meetings by user stream

</td><td>

Lists all the live or ongoing meetings for a specific user.

</td><td>

meeting:read:list\_meetings:admin

</td></tr><tr><td>

Look up Meetings Stream

</td><td>

Lists the given user's meetings.

</td><td>

meeting:read:list\_meetings:admin

</td></tr><tr><td>

Look up Past Meeting Participants Stream

</td><td>

Lists information on participants from a past meeting.

</td><td>

meeting:read:list\_past\_participants:admin

</td></tr><tr><td rowspan="6">

User Management

</td><td>

Create user

</td><td>

Creates a user in your account. **Note:** A Zoom [pro plan](https://zoom.us/pricing) or later is required for this action. You must enable pre-provisioning for SSO users in your Zoom account.

</td><td>

user:write:user:admin

</td></tr><tr><td>

Delete user

</td><td>

Deletes a specific user from your account.

</td><td>

user:delete:user:admin

</td></tr><tr><td>

Disassociate user

</td><td>

Unlinks a specific user from your account.

</td><td>

user:delete:user:admin

</td></tr><tr><td>

Look up user details

</td><td>

Gets the details of a specific user on your account by using their user ID.

</td><td>

user:read:user:admin

</td></tr><tr><td>

Look up users stream

</td><td>

Retrieves all the users that are associated to your account.

</td><td>

user:read:list\_users:admin

</td></tr><tr><td>

Update user settings

</td><td>

Updates the settings of a specific user.

</td><td>

user:update:user:admin

</td></tr><tr><td rowspan="9">

Chat Management

</td><td>

Add members to channel

</td><td>

Adds members to a Zoom channel.

</td><td>

team\_chat:write:members:admin

</td></tr><tr><td>

Create channel

</td><td>

Creates a Zoom channel.

</td><td>

team\_chat:write:user\_channel:admin

</td></tr><tr><td>

Look up channel

</td><td>

Retrieves the details of a Zoom channel.

</td><td>

team\_chat:read:user\_channel:admin

</td></tr><tr><td>

Look up channel members stream

</td><td>

Retrieves the details of the members in a Zoom channel.

</td><td>

team\_chat:read:list\_members:admin

</td></tr><tr><td>

Look up user chat message stream

</td><td>

Retrieves the details of a member's chats in a Zoom channel.

</td><td>

team\_chat:read:list\_user\_messages:admin

</td></tr><tr><td>

Look up user channels stream

</td><td>

Retrieves the names of theZoom channels.

</td><td>

team\_chat:read:list\_user\_channels:admin

</td></tr><tr><td>

Remove member from channel

</td><td>

Removes a member from a Zoom channel.

</td><td>

team\_chat:delete:member:admin

</td></tr><tr><td>

Send chat message

</td><td>

Sends a chat message to a Zoom channel.

</td><td>

team\_chat:write:user\_message:admin

</td></tr><tr><td>

Update channel

</td><td>

Updates a Zoom channel's details.

</td><td>

team\_chat:update:user\_channel:admin

</td></tr><tr><td>

Utility Actions

</td><td>

Copy chat message attachment to record

</td><td>

Copies the attachment that contains the chat message to the incident record.

</td><td>

team\_chat:read:user\_message:admin

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-use-case-ai-agents.md) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-ai-agent.md) for more information about creating a clone.
-   See [Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-ai-agents.md) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|Zoom user management AI agent|Looks up the details of a user, and creates, deletes, and disassociates a user.|
|Zoom meeting management AI agent|Creates, ends, and deletes meetings, looks up meeting details, and adds a meeting registrant.|
|Zoom cloud recording management AI agent|Looks up meeting recordings and meeting recording settings.|
|Zoom chat management AI agent|Enables users to create and manage chat channels, send and update messages, and handle member-related operations.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Zoom spoke requirements

These actions use REST calls, which can run on an instance or Zoom spoke See [Building flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flows.md) for more information. Use the connection record that is associated with the Zoom alias to configure where actions run and set Zoom spoke selection attributes. For more information about the alias, see [Connection and credential alias](zoom-spoke.md#section_ibn_pj2_hfb).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r-credentials.md).

This spoke uses the Zoom Connection &amp; Credential Alias record to authorize actions. For information about setting up the spoke, see [Set up the Zoom spoke](../task/setup-zoom.md#).

