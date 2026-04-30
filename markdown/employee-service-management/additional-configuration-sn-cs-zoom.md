---
title: Chat-specific configuration for Collaboration services for Zoom
description: Configure chat-specific options for Collaboration services for Zoom.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Enhance employee experience by integrating ServiceNow with Zoom, Integrate, ServiceNow for Zoom, Employee Service Management]
---

# Chat-specific configuration for Collaboration services for Zoom

Configure chat-specific options for Collaboration services for Zoom.

ServiceNow Collaboration services for Zoom enables agents to customize the following aspects of Zoom chats:

-   Configure Chat group to include On-call Scheduling users for Start Zoom Team Chat
-   Configure chat form for different record types
-   Create chat configuration to auto-import chats
-   Create requester mapping
-   Configure chat close condition

If you have the ServiceNow Collaboration services for Zoom in your environment, the customized chat-specific additional configuration is applicable by default for the following tables:

-   Request Item \(sc\_req\_item\)
-   Task \(sc\_task\)
-   Incident \(incident\)
-   Request \(sc\_request\)
-   Change request \(change\_request\)

The admin can extend the custom configuration to the other tables as required. You can create one chat configuration for only one table at a time. You can extend the chat configuration to other tables by creating another chat configuration record.

## Functionality of auto importing messages

All the chat messages from Zoom Team Chat will be auto imported to the ServiceNow instance at an interval of 30 minutes. The system looks for all new messages across all the chats and import the messages to the ServiceNow instance.

To prevent polling from running indefinitely on inactive conversations, if there are no new messages, the polling interval gradually extends until the polling stops.

The system verifies the record for new messages for every 30 minutes. If there are no new messages, the system checks for the new messages for an interval of 1 hour, 2 hours, 4 hours, and 8 hours. If there are no new messages in an interval of eight hours for seven days, the Auto Import polling activity is disabled.

If there is any message during any of the intervals, the auto import timer looks for new messages in the next interval and imports the messages. The timer is then reset to 30-minutes interval.

## System Limits

The system imports a maximum of 500 active chats in a 30-minute interval. If there are more than 500 active chats, the system will not auto-import the new chat records for the 30-minute interval.

The system executes a maximum of 10000 sub-flows to import the chats for an interval of 30 minutes, 1 hour, 2 hours, 4 hours, and 8 hours intervals. This is a count of all the active sub-flows that auto-import the messages into ServiceNow.

If the system reaches the limit, a message is displayed to the agent on the **Start Zoom Chat** modal that, "Zoom Team Chat auto import system limits is reached. New chats will not be auto imported.".

When a ticket is closed, the system triggers auto import for one last time and posts the new messages in the **Work notes** \(Chat history\) section.

If there is an interaction record associated with the parent record then interaction record is also closed. The chat record is also closed as a part of this flow.

-   **[Configure Chat group to include On-call Scheduling users for Start Zoom Team Chat](oncall-users-start-zoom-chat.md)**  
On-call Scheduling users will be shown for Start Zoom Team Chat for an incident record.
-   **[Customize the Zoom chat form](../task/create-chat-config-customize-zoom-chat-form.md)**  
Customize the chat form for additional ServiceNow® Collaboration services tables by creating a chat configuration.
-   **[Create requester mapping](../task/create-requester-mapping-zoom.md)**  
Create a requester mapping to extend the Zoom chat functionality to other tables.
-   **[Define how a Zoom chat is closed](../task/configure-close-condition-zoom.md)**  
Define the way a Zoom chat is closed.

**Parent Topic:**[Enhance employee experience by integrating ServiceNow with Zoom](enhance-emp-exp-integrating-sn-zoom.md)

