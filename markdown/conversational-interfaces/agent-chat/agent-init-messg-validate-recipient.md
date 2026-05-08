---
title: Validate recipient IDs for agent-initiated messages
description: Use scripted extension points to call custom scripts for validating the format of a recipient ID associated with a messaging channel.
locale: en-US
release: australia
product: Agent Chat
classification: agent-chat
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Agent-Initiated Messaging Interface, Configure, Agent Chat, Conversational Interfaces]
---

# Validate recipient IDs for agent-initiated messages

Use scripted extension points to call custom scripts for validating the format of a recipient ID associated with a messaging channel.

## Before you begin

Install the Agent-Initiated Messaging Interface application. For more information, see [Install agent-initiated messaging interface](install-agent-init-messg.md).

Role required: admin

## About this task

By using extension points, you can easily integrate customizations without having to alter the base code. You can extend standard base functionality using customized scripts. For more information, see Using extension points to extend application functionality.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** column, search for and select **global.ChannelSendToValidation**.

3.  On the Extension Point form, either modify a script include to use the global.ChannelSendToValidation extension point or create and register a custom script include.

    -   Create and register a custom script include.
    -   Modify the existing script include by going to the Implementations related list and selecting a script include in the **Class** column.

        **Note:** The PhoneNumberValidationExtPointImpl script include that use the global.ChannelSendToValidation extension point is available for validating recipient IDs profiles associated with the [Conversational SMS service channel](../../advanced-work-assignment/concept/conversation-sms-service-channel-store-app.md) application.

4.  Associate user profiles for an agent-initiated messages by adding the global.ChannelSendToValidation extension point to the script include.

    You can create multiple implementations for an extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed first.

    |Customization|Implementation|
    |-------------|--------------|
    |Associate a channel ID for which the message was initiated|Include the isValid method in the global.ChannelSendToValidation extension point.|
    |Retrieve the recipient ID associated with the channel for which the message was initiated|Include the channelSendToValidation method in the sn\_agent\_initiated.AgentInitiatedMessagingUserDocument extension point.|

    **Note:** Based on the channel ID set in the isValid method, the recipient details are retrieved for validating a recipient ID in the channelSendToValidation method.

5.  On the Extension Point form, click **Update**.


**Parent Topic:**[Configuring Agent-Initiated Messaging Interface](../concept/config-agent-init-messg-interface.md)

