---
title: Configure Request-based chats to import messages from Microsoft Teams to ServiceNow
description: Configure request-based chats for IT Service Management integration with Microsoft Teams and HR Service Delivery integration with Microsoft Teams applications enable the system to auto import the chat conversations between the agents and the employees.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [HR Service Delivery integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Configure Request-based chats to import messages from Microsoft Teams to ServiceNow

Configure request-based chats for IT Service Management integration with Microsoft Teams and HR Service Delivery integration with Microsoft Teams applications enable the system to auto import the chat conversations between the agents and the employees.

If you are installing the ServiceNow for Microsoft Teams in your environment, the auto-import functionality is applicable by default for the following tables.

-   HR Core task \(sn\_hr\_core\_task\)
-   HR Life events Case \(sn\_hr\_le\_case\)
-   HR Core case \(sn\_hr\_core\_case\)
-   Request Item \(sc\_req\_item\)
-   Task \(sc\_task\)
-   Incident \(incident\)
-   Request \(sc\_request\)
-   Change request \(change\_request\)

The admin can extend the auto import feature to the other tables as required. For more information see, [Create requester mapping](../task/create-requester-mapping.md).

If you are upgrading your ServiceNow instance to IT Service Management integration with Microsoft Teams 2.2.0 or HR Service Delivery integration with Microsoft Teams 2.2.0, you must manually enable the auto import feature.

## Functionality of auto importing messages

All the chat messages from Microsoft Teams will be auto imported to the ServiceNow instance at an interval of 30 minutes. The system looks for all the new messages across all the chats and import the messages to ServiceNow instance.

To prevent polling from running indefinitely on inactive conversations, if there are no new messages, the polling interval will gradually lengthen until, eventually, polling stops.

The system verifies the record for new messages for every 30 minutes. If there are no new messages, the system checks for the new messages for an interval of one hour, two hour, four hour and eight hours. If there are no new messages in an interval of eight hours for seven days, the Auto Import polling activity is disabled.

If there is any message during any of the intervals, the auto import timer will look for the new messages in the next interval, and import the messages. The timer is then reset to 30-minutes interval.

## System Limits

The system imports a maximum of 500 active chats in a 30-minute interval. If there are more than active 500 chats the system will not auto-import the new chat records for the 30-minute interval.

The system executes a maximum of 10,000 sub-flows to import the chats for an interval of 30 minutes, 1 hour, 2 hour, 4-hour, 8-hour intervals. This is a count of all the active subflows that auto-import the messages into ServiceNow.

If the system reaches the limit, a message is displayed to the agent that the system level is reached and the chat can’t be auto imported on the **Start Microsoft Teams Chat** modal.

![System limit reached.](../images/system-limit-reached.png)

When the ticket is closed, the system will trigger auto import for one last time posts the new messages in the Work notes \(Chat history\).

If there is an interaction record associated with the parent record then interaction record is also closed. The chat record will also be closed as part of this flow.

If you want to continue using the default configuration, you can skip the following procedures to extend the auto-import functionality. However, if you want to extend the auto-import functionality to other tables, perform the steps mentioned in the topics below.

-   **[Configure the chat to enable auto-import](../task/configure-auto-import-chats.md)**  
Create a chat configuration to automatically import the chats between the agents and the requesters for additional tables to extend the auto import functionality.
-   **[Create requester mapping](../task/create-requester-mapping.md)**  
Create a requester mapping to extend the auto-import functionality to other tables.
-   **[Configure close condition](../task/configure-close-condition.md)**  
Configure the condition to exclude the chat conversation from auto importing.

**Parent Topic:**[Configure HR Service Delivery integration with Microsoft Teams](sn-ms-teams-config-hr.md)

