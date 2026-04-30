---
title: Microsoft Teams Communications Spoke
description: Manage groups calls and meetings in the Microsoft Teams Communications account from your ServiceNow instance. Also reuse this short description in the release notes.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Microsoft Teams Communications Spoke

Manage groups calls and meetings in the Microsoft Teams Communications account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Teams Communications spoke v1.5.0 is the latest version.

## Supported versions

This spoke was built for Microsoft Teams Communications API version v1 and beta version, but may be compatible with later versions.

**Note:** The Create Online Meeting and Mute Participants spoke actions use the beta API version. All the remaining actions use the API version v1.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Microsoft Teams Communications spoke provides actions to automate tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Call Management|Delete Group Call|Deletes the specified active group call.|
|Get Group Call Details|Retrieves details of the specified active group call.|
|Get Group Call Participant Details|Retrieves the properties and relationships of a participant object or list of participant objects from Microsoft Graph API.|
|Invite Participants to Group Call|Invites participants to the specified active group call.|
|Keep Group Call Alive|Keeps a group call alive if the keep alive request is made within 45 minutes of the previous request. If the request is not made within 45 minutes, the group call is considered as an inactive call.|
|Mute Participants in Group Call|Mutes one or more participants in an active group call.|
|Start Group Call|Initiates a group call.|
|Meeting Management|Create Meeting Event|Creates a Microsoft Teams-enabled calendar event with comprehensive meeting configuration options. This action allows you to schedule online meetings, manage attendee lists, configure meeting settings, and support both one-time and recurring meeting patterns.|
|Create Notification Subscription|Creates a subscription to receive real-time notifications for Microsoft Teams resources. This action allows you to monitor changes to resources such as chats and online meeting artifacts such as transcripts and recordings, by subscribing to specified event types.|
|Create User Online Meeting|Creates a user online meeting using the /users/\{userId\}/onlineMeetings Microsoft Graph API endpoint.|
|Create Online Meeting|Creates a user online meeting using the /communications/onlineMeeting Microsoft Graph API endpoint.|
|Look up meeting data|Retrieves meeting details associated with the specified event ID.|
|Look up Meeting Recording Content|Retrieves the recording content of a specified online meeting.|
|Look up transcript data|Retrieves the meeting transcript using the specified user ID and meeting ID.|
|Look up transcripts|Retrieves Microsoft Teams transcripts using the specified user ID, meeting ID, and transcript ID.|
|User Management|Look up User IDs Stream|Retrieves the user ID and display name for the specified users.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Microsoft Teams Communications spoke](../task/setup-msteams-comm.md#).

