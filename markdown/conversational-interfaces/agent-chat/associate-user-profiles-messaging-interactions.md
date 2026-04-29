---
title: Associating user profiles on messaging interactions
description: Use extension points to call custom scripts.
locale: en-US
release: australia
product: Agent Chat
classification: agent-chat
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Agent Chat, Conversational Interfaces]
---

# Associating user profiles on messaging interactions

Use extension points to call custom scripts.

## Before you begin

Role required: admin

## About this task

When a requester sends a message, the system checks if there is an existing user profile that has a matching identifier \(such as a phone number\) and channel details. If there is a matching user, then the system will populate the interaction record with the identifier, channel details, and the user profile in the Opened for field. If there is no user profile that matches the identifier and channel, then the system creates a channel user profile.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Click the desired extension point to view the record details.

    You can create multiple implementations for each extension point and assign an order number for each implementation. The implementation that has the lowest ordered applicable implementation is executed first.

    |Extension point|Description|
    |---------------|-----------|
    |global.ChannelUserProfileExtPoint|Use channel\_user\_id to find record to channel\_user\_profile user\_table/user\_document|
    |global.InteractionChannelUserProfileExtPoint|Defines how users are synchronized between the interaction and channel\_user\_profile tables|
    |global.AgentInitiatedConversationUtil|Get From and To options to show in UI for agent initiated conversations|


**Parent Topic:**[Configuring Agent Chat](../concept/ci-agent-chat-configuring.md)

