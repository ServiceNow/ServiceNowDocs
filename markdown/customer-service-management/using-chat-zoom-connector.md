---
title: Using Chat Zoom Connector
description: Initiate a Zoom meeting directly from a chat by using the Chat Zoom Connector application.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2023-08-03"
reading_time_minutes: 2
breadcrumb: [Manage cases, Using Customer Service Management, Customer Service Management]
---

# Using Chat Zoom Connector

Initiate a Zoom meeting directly from a chat by using the Chat Zoom Connector application.

As an agent you can initiate a Zoom meeting from a chat to understand and resolve customer issues faster through live interactions. For more information, see [Initiate Zoom meetings from chats](../task/initiate-chat-zoom.md).

By default, for each interaction record for a Zoom meeting, a Notify conference call number is also generated. As an agent, you or the agent manager can access the recording URL of the Zoom meeting from the activity stream of the interaction record. For more information, see [Interaction records in Agent Workspace](https://www.servicenow.com/docs/access?context=interaction-message-agent-workspace&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

As an agent manager, you can access the details of Zoom meetings initiated from a customer chat using the Zoom interaction record. The meeting recordings are available in the interaction record created for Zoom. For more information, see [View details for Zoom meetings initiated from chats](../task/view-details-chat-zoom.md).

**Note:** The conference call details of a Zoom meeting are stored in the Notify Conference Calls \[notify\_conference\_call\] table.

As a user in the notify\_admin or notify\_view role, you can access the details of a Zoom meeting by navigating to **Notify** &gt; **Recordings**, and selecting the corresponding conference call number. For more information, see [Notify conference calls](https://www.servicenow.com/docs/access?context=c_NotifyConferenceCalls&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Chat Zoom Connector user roles

The users with the roles listed in the following table can use the Chat Zoom Connector application.

|Roles|Tasks|
|-----|-----|
|agent\_workspace\_user|Initiate a Zoom meeting from a chat to understand customer issues and resolve issues faster through live interactions.|
|sn\_customerservice\_manager|View details for Zoom meetings initiated from a customer chat using the Zoom interaction record. The meeting recordings are available in the interaction record created for Zoom meetings.|
|notify\_admin, notify\_view|View details for Zoom meetings initiated from a customer chat by using Notify.|

## Activation information

Configure the Chat Zoom Connector application for initiating Zoom meetings from customer chats. For more information, see [Configure Chat Zoom Connector](../task/config-chat-zoom-connector.md).

**Related topics**  


[Chat Zoom Connector](chat-zoom-connector.md)

