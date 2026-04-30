---
title: Set up Agent-Initiated Messaging Interface for a messaging channel
description: Set up the Agent-Initiated Messaging Interface application to send messages from a messaging channel.
locale: en-US
release: zurich
product: Agent Chat
classification: agent-chat
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Agent-Initiated Messaging Interface, Configuring Agent Chat, Agent Chat, Conversational Interfaces]
---

# Set up Agent-Initiated Messaging Interface for a messaging channel

Set up the Agent-Initiated Messaging Interface application to send messages from a messaging channel.

## Before you begin

-   [Install agent-initiated messaging interface](install-agent-init-messg.md).
-   [Review the list of messaging channels available for the Agent-Initiated Messaging Interface application](../reference/agent-init-messg-sc-setting.md).
-   Set the application scope to the application associated with the messaging channel using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

    For example, for using the SMS messaging channel, set the application scope to the Conversational SMS service channel application.


Role required: admin

## About this task

A messaging channel is available when you install the application associated with a service channel.

For example, use the SMS messaging channel to send an SMS message to a customer. The SMS messaging channel is available when you have installed the [Conversational SMS service channel](../../advanced-work-assignment/task/install-conversational-sms.md) application.

## Procedure

1.  In the navigation filter, enter `sn_agent_initiated_msg_config.list`.

2.  In the Agent initiated messaging configurations list, modify an existing configuration or create another configuration for a messaging channel.

    -   To modify an existing configuration, in the **Active** column, click the value link corresponding to the messaging channel displayed in the **Channel** column.

        For example, to send messages by using the SMS messaging channel, click the link in the **Active** column corresponding to the **SMS** channel.

    -   To create another configuration for a messaging channel, click **New** in the Agent initiated messaging configurations list.
3.  On the form, fill in the fields.

<table id="table_zxn_lvp_znb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Channel

</td><td>

Messaging channel using which agents can initiate messages to connect with requesters.

</td></tr><tr><td>

Check if active recipient profile exists

</td><td>

Option to ensure that an active channel user profile exists when sending messages to the user from the channel.If there are no active channel user profiles, the associated channel is not available for agent-initiated messages. In this case, the channel does not appear in the **Channel** field of the Compose Message form. For information on the Compose Message form available in CSM Configurable Workspace, see [Initiate messaging conversations from CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=agent-init-messg-csm-cws&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

</td></tr><tr><td>

Show option to enter recipient ID manually

</td><td>

Option to display the field to manually enter recipient ID.For example, select this check box to enable agents to enter a phone number manually for sending an SMS message to a consumer.

</td></tr><tr><td>

Application

</td><td>

Scope of the application that contains the channel. This field is automatically set based on the application scope selected in the application picker.

</td></tr><tr><td>

Active

</td><td>

Option to activate the use of the channel for agent-initiated messages.

</td></tr><tr><td>

Order

</td><td>

Order number for each channel in which they appear for agent on the Compose Message form when composing messages. The channel that has the lowest order number is displayed first.For information on the Compose Message form available in CSM Configurable Workspace, see [Initiate messaging conversations from CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=agent-init-messg-csm-cws&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Save the configuration setting.

    -   If you created a new configuration setting, click **Submit**.
    -   If you modified an existing configuration setting, click **Update**.

**Parent Topic:**[Configuring Agent-Initiated Messaging Interface](../concept/config-agent-init-messg-interface.md)

