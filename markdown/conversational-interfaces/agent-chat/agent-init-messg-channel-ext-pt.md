---
title: Determine whether messaging channels are available for agent-initiated messages
description: Use scripted extension points to call custom scripts for determining whether a messaging channel is applicable to a user profile in an agent-initiated message.
locale: en-US
release: australia
product: Agent Chat
classification: agent-chat
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Agent-Initiated Messaging Interface, Configure, Agent Chat, Conversational Interfaces]
---

# Determine whether messaging channels are available for agent-initiated messages

Use scripted extension points to call custom scripts for determining whether a messaging channel is applicable to a user profile in an agent-initiated message.

## Before you begin

Install the Agent-Initiated Messaging Interface application. For more information, see [Install agent-initiated messaging interface](install-agent-init-messg.md).

Role required: admin

## About this task

By using extension points, you can easily integrate customizations without having to alter the base code. You can extend standard base functionality using customized scripts. For more information, see [Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md).

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** column, search for and select **sn\_agent\_initiated.ChannelsQualifyingFoAgentMessaging**.

3.  On the Extension Point form, create and register a custom script include.

4.  Determine whether a messaging channel is applicable to a user profile in an agent-initiated message by adding the sn\_agent\_initiated.ChannelsQualifyingForAgentMessaging extension point to the script include.

    You can create multiple implementations for an extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed first.

    |Customization|Implementation|
    |-------------|--------------|
    |Associate a messaging channel ID for agent-initiated messages with the custom script|Include the isValidForChannel method in the sn\_agent\_initiated.ChannelsQualifyingForAgentMessaging extension point.|
    |Check whether a user qualifies for the messaging channel for agent-initiated messages|Include the isChannelValidForAgentInitiatedMessaging method in the sn\_agent\_initiated.ChannelsQualifyingForAgentMessaging extension point.|

    **Note:** Based on the messaging channel ID set in the isValidForChannel method, the users are evaluated for sending agent-initiated messages in the isChannelValidForAgentInitiatedMessaging method.

5.  On the Extension Point form, click **Update**.


**Parent Topic:**[Configuring Agent-Initiated Messaging Interface](../concept/config-agent-init-messg-interface.md)

