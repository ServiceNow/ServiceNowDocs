---
title: Configure the chat to enable auto-import
description: Create a chat configuration to automatically import the chats between the agents and the requesters for additional tables to extend the auto import functionality.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Import messages from Microsoft Teams to ServiceNow, HR Service Delivery integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Configure the chat to enable auto-import

Create a chat configuration to automatically import the chats between the agents and the requesters for additional tables to extend the auto import functionality.

## Before you begin

Role required: admin

## Procedure

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


**Parent Topic:**[Configure Request-based chats to import messages from Microsoft Teams to ServiceNow](../concept/auto-import-messages.md)

