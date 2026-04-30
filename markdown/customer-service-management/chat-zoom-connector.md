---
title: Chat Zoom Connector
description: Resolve issues quickly and engage better with customers with video and screen sharing options in Zoom using the ServiceNow Chat Zoom Connector application.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enable communication channels, Configure, Customer Service Management]
---

# Chat Zoom Connector

Resolve issues quickly and engage better with customers with video and screen sharing options in Zoom using the ServiceNow® Chat Zoom Connector application.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Overview

The Chat Zoom Connector application integrates the chat communication channel with the Notify communication channel by managing and initiating a Zoom meeting directly from a chat. An interaction record is created for each Zoom meeting initiated from a chat.

As an agent, you can use the Chat Zoom Connector application to initiate Zoom meetings from a customer chat and optionally record the meeting.

As an agent manager, you can access an interaction record of type Zoom to view the meeting details such as the meeting URL, participants, and recording.

As a customer, you can join a Zoom meeting with an agent regardless of whether you have a Zoom account.

To get started with the Chat Zoom Connector application, see [Configure Chat Zoom Connector](../task/config-chat-zoom-connector.md).

## Key features

-   Initiate Zoom meetings using the Quick Actions list in chats.
-   Track Zoom meetings as interactions on the ServiceNow platform.
-   Track participants in Zoom meetings.
-   Post the meeting recording to the interaction activity stream.

## Example scenario

The following example scenario shows the use of the Chat Zoom Connector application in resolving a configuration issue with an agent initiating a Zoom meeting directly from a customer chat.

![Infographic displaying the process of an agent resolving a customer issue over chat. For the text description, refer to the following steps.](../image/chat-zoom-connector.png "Agent resolving a customer issue over Zoom")

1.  A customer engages with Support over chat to report an issue for a product.
2.  An agent receives the chat request and realizes that the issue can be resolved through a minor configuration change.
3.  The agent initiates a Zoom meeting using the Quick Actions list in the chat and invites the customer to join the meeting.

    **Note:** The customer does not need a Zoom account to join the meeting.

4.  The customer shares the screen over Zoom and the agent guides the customer on updating the configuration and resolves the issue.

