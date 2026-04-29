---
title: Create a new channel for your custom chat integration
description: Create a new channel or update an existing channel for your custom chat integration. Channels are defined in the Messaging Channels \[sys\_cs\_channel\] table.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [sys\_channel, conversational custom chat integration, Messaging Channels, Virtual Agent, Agent chat, com.glide.cs.custom.adapter, CCCIF, Integration Hub]
breadcrumb: [Create conversational custom chat integration, Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Create a new channel for your custom chat integration

Create a new channel or update an existing channel for your custom chat integration. Channels are defined in the Messaging Channels \[sys\_cs\_channel\] table.

## Before you begin

Activate the [Glide Virtual Agent plugin](activate-virtual-agent.md) \(com.glide.cs.chatbot\) if it's not already activated. This plugin automatically activates the Conversational Custom Chat Integration plugin \(com.glide.cs.custom.adapter\) for custom chat integrations.

**Note:** The Conversational Custom Chat Integration Framework \(CCCIF\) uses Integration Hub. Transactions count against your Integration Hub quota.

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_channel.list` in the navigation filter.

2.  On the Messaging Channels page, select **New**.

    Alternatively, select an existing channel to open it.

3.  On the form, fill in the fields.

<table id="table_ixm_ldk_1mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your channel, such as Mobile App or SMS.

</td></tr><tr><td>

Opted in all topics by default

</td><td>

Option to make all topics available in this channel.

</td></tr><tr><td>

Enable Notifications

</td><td>

Option to turn notifications on or off on this channel.

</td></tr><tr><td>

Live Agent Only

</td><td>

Option to initiate conversations with live agents, bypassing the Virtual Agent bot.

</td></tr><tr><td>

Store app page link

</td><td>

This field should be left empty.

</td></tr><tr><td>

Type

</td><td>

Channel type.-   **Chat**: Standard chat experience
-   **Messaging**: Long-running conversation
-   **Phone**: Phone \(audio\) conversation
-   **Walk-up**: In-person conversation


</td></tr><tr><td>

Conversation Idle Timeout

</td><td>

Number of seconds that abandoned Virtual Agent and Agent Chat conversations remain open in the channel, after the requester's last response.

 This channel-specific value overrides the following settings:

-   Default idle conversation timeout value, which is 7200 seconds
-   Idle conversation time-out value set through the **com.glide.cs.conversation\_idle\_timeout** system property to override the default timeout value
For more information about conversation idle timeouts, see [Closing Virtual Agent and Agent Chat conversations](../concept/va-open-conversations.md).

</td></tr><tr><td>

Secure

</td><td>

Option for the channel to be secure to support handling of sensitive data such as passwords.

</td></tr><tr><td>

Support typing indicator

</td><td>

Option to display typing indicators for this channel. Flag applies to both agent and bot indicators.

</td></tr><tr><td>

Icon

</td><td>

This field should be left empty.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

[Configure a provider for your custom chat integration](create-provider-va-cccif.md)

**Parent Topic:**[Create a Virtual Agent conversational custom chat integration](create-adapter-for-virtual-agent.md)

