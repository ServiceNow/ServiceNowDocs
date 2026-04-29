---
title: Configure Request-based chats to import messages from Microsoft Teams to ServiceNow
description: Configure request-based chats for IT Service Management integration with Microsoft Teams and HR Service Delivery integration with Microsoft Teams applications enable the system to auto import the chat conversations between the agents and the employees.Create a chat configuration to automatically import the chats between the agents and the requesters for additional tables to extend the auto import functionality.Create a requester mapping to extend the auto-import functionality to other tables.Configure the condition to exclude the chat conversation from auto importing.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [IT Service Management integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
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

When the ticket is closed, the system will trigger auto import for one last time posts the new messages in the Work notes \(Chat history\).

If there is an interaction record associated with the parent record then interaction record is also closed. The chat record will also be closed as part of this flow.

If you want to continue using the default configuration, you can skip the following procedures to extend the auto-import functionality. However, if you want to extend the auto-import functionality to other tables, perform the steps mentioned in the topics below.

**Parent Topic:**[Configure IT Service Management integration with Microsoft Teams](sn-ms-teams-config-it.md)

## Configure the chat to enable auto-import

Create a chat configuration to automatically import the chats between the agents and the requesters for additional tables to extend the auto import functionality.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Chat Administration** &gt; **Chat Configuration**.

    ![Chat configuration](../images/chat-configuration.png)

2.  Click **Default** option to view the default OOB configuration.

    ![Default chat configuration](../images/default-chat-configuration.png)

    **Note:** If you want to auto-import chats for certain conditions, create a condition.

3.  Navigate to **ServiceNow for Microsoft Teams** &gt; **Chat Administration** &gt; **Chat Configuration**.

4.  Click **New**.

    ![New chat configuration](../images/new-chat-configuration.png)

5.  On the form, fill the fields.

<table id="table_kjb_nl1_sqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Value for the configuration.

</td></tr><tr><td>

Order

</td><td>

Order for the configuration.

 You can define multiple chat configurations for a single table. The system executes the query based on the descending order.

</td></tr><tr><td>

Active

</td><td>

Option to activate the configuration.

 Select the check box to activate the configuration.

</td></tr><tr><td>

Auto Import

</td><td>

Option to automatically import the chat.

 Select the check box to automatically import the chat.

</td></tr><tr><td>

Default

</td><td>

Option to keep the configuration as default.

 **Note:** You cannot define multiple default values for chat configuration.

</td></tr><tr><td>

Table

</td><td>

Option to select the auto-import for a table.

</td></tr><tr><td>

Inherit

</td><td>

Extend and apply to the child tables.

</td></tr><tr><td>

Conditions

</td><td>

Option to define a condition for a chat to be auto-imported.

</td></tr><tr><td>

Opening message

</td><td>

Option to provide a text message that displays to the agent when the agent initiates a chat.

 This field is enabled only if the **Auto Import** option is selected.

</td></tr></tbody>
</table>    ![New chat configuration](../images/new-chat-configuration-2.png)

6.  Click **Submit**.

    The chat configuration defined will be applicable only for the table selected. You can extend the chat configuration to other tables by creating another chat configuration record.


## Create requester mapping

Create a requester mapping to extend the auto-import functionality to other tables.

### Before you begin

Role required: admin

**Note:**

If there is no requestor mapping defined for a table, the interaction records will not be created. An error log is created for the admin to notify that the requestor mapping is not defined for a table.

A requestor-mapping record defines which field, in any given table, is the field representing the requestor of a ticket.

### Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Chat Administration** &gt; **Requestor Mapping**.

2.  Click **New**.

    ![Requestor mapping](../images/requester-mapping.png)

3.  On the form, fill in the fields.

    |Field|Description|
    |:----|:----------|
    |Table|Table to which the requestor mapping \(auto-import feature\) should be applicable.|
    |Requestor field|Field to select the requestor for a record.|
    |Inherit|Extend and apply the auto-import feature to the child tables.|
    |Active|Option to activate the requestor-mapping record.|

4.  Click **Submit**.


## Configure close condition

Configure the condition to exclude the chat conversation from auto importing.

### Before you begin

Role required: admin

### About this task

When a ticket is set to inactive, the system does one final poll for any messages in the chat, removes the participants such that no further messages about the ticket can be exchanged in the chat, and then stops polling that chat. This is determined by the "active" field on a table being set to "false".

For any table with an active field, this behavior works automatically. If your custom application does not use an "active" field for determining whether the ticket remains active, define an alternate condition that can be used to denote the ticket as being closed or inactive.

Alternately, to adhere to platform standards, consider adding an active field to your custom application and maintaining the state of that field in accordance with the business logic of your application.

**Important:**

If you are creating a close condition for a new table, ensure to create business rule for close condition. For more information, see [Configure business rule for close condition](../task/business-rule-close-condition.md).

### Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Chat Administration** &gt; **Close Conditions**.

2.  Click **New**.

    ![Configure close condition](../images/configure-close-condition.png)

3.  On the form, fill in the fields.

    |Field|Description|
    |:----|:----------|
    |Table|Option to select a table to which the requester mapping \(auto-import feature\) should be applicable.|
    |Inherit|Extend and apply the auto-import feature to the child tables.|
    |Active|Option to activate the requester-mapping record.|
    |Close conditions|Condition builder to define a condition that the record is closed.|

4.  Click **Submit**.


