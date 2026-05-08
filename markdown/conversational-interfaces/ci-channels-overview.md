---
title: Channels in Conversational Interfaces
description: The various ways in which your end users engage with virtual and live agents are called channels. In Conversational Interfaces, users and agents converse through channels that have specific communication modes: chat mode for real-time conversations and messaging mode for long-running conversations.
locale: en-US
release: australia
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Channels, Conversational Interfaces, Chat, Messaging, Live Agent]
breadcrumb: [Exploring Conversational Interfaces Console, Conversational Interfaces Console, Conversational Interfaces]
---

# Channels in Conversational Interfaces

The various ways in which your end users engage with virtual and live agents are called channels. In Conversational Interfaces, users and agents converse through channels that have specific communication modes: chat mode for real-time conversations and messaging mode for long-running conversations.

Conversation channels provide your end users and agents with different options for interacting. These options are based on when your users and agents are available to connect, and the chat applications used in your business environment. There are two types of channels: chat channels and messaging channels.

## Chat channels

Chat channels support two-way conversations in real time. These conversations may involve a user and a live agent or a user and a virtual agent. This mode of conversation is synchronous, and the user is guaranteed a response. Supported chat channels let your end users and agents interact based on the chat applications \(clients\) that they’re using and when they’re available to connect.

The following channels are supported for synchronous chat:

-   Service Portal \(mweb\) chat widget
-   Mobile web \(mweb\) client
-   [Conversational Integration with Microsoft Teams](../../virtual-agent/concept/teams-conv-integration.md)
-   [Conversational Integration with Slack](../../virtual-agent/task/mssg-slack.md)
-   [Conversational Integration with Workplace from Facebook](../../virtual-agent/task/mssg-workplace.md)
-   [Conversational Integration with Alexa](../../virtual-agent/concept/conv-integ-alexa.md)
-   [Conversational Integration with WhatsApp \(powered by Twilio\)](../../virtual-agent/concept/messg-whatsapp-twilio.md)
-   [Conversational Integration with LINE](../../virtual-agent/concept/messg-line.md)
-   [Conversational Integration with Facebook Messenger](../../virtual-agent/concept/messg-fbm.md)

## Messaging channels

Messaging channels let end users and agents communicate over longer periods of time, especially when one party isn’t online. This mode of chat is asynchronous and happens at the parties' convenience.

When your end users and agents must communicate over longer periods without being online concurrently, pre-built messaging channels let them chat asynchronously, at their convenience.

The following channels are available for asynchronous chat:

-   Mobile web \(mweb\) client: Configure this channel for iOS, Android, and desktop devices for [asynchronous chat](../../virtual-agent/concept/async-chat.md)
-   Now Assist panel: Used by Now Assist panel.
-   SMS channel: Used by [Conversational SMS Integration with Twilio](../../virtual-agent/concept/sms-twilio-store-app.md)

## Messaging Channels table

Messaging channels are defined in the Messaging Channels table \[sys\_cs\_channel\]. If you’re using the [custom chat integration framework](../../virtual-agent/concept/va-custom-adapter-framework.md) to create custom chat integrations, you can specify the channel mode for those integrations—either chat or messaging. For channels such as the mweb channel, you can choose either chat or messaging as well.

![The Messaging Channels table displays all of the channels that are configured for the instance.](../image/messaging-channels-table.png "Configured channels for an instance")

## Live Agent support by channel

Not all channels may be suitable for Live Agent support. For example, you may want to disable support for the Bot-to-Bot and voice channels. Live Agent support is enabled by default, but admins can change this setting in the Messaging Channels \[sys\_cs\_channel\] table. For details, see [Disable live agent support for a channel](../task/disable-live-agent-support-channel.md).

## Chat and messaging features

The Conversational Interfaces channels offer basic features that make it easy for your agents and end users to stay connected:

-   Message indicators that inform your users of new and unread messages received when they’re away from chat or when they’ve been offline.
-   Typing indicators that show a chat participant is responding.
-   System messages, displayed to users and agents that provide information about the conversation state.
-   Secure handling of sensitive data, such as passwords or account numbers. This data is masked when users enter the information, and it cannot be viewed by others.
-   Automatic closing of [idle chat or messaging conversations](ci-idle-chats.md).

## New and unread message indicators

End users receive new message indicators on chat and messaging channels when they're offline. Users can be anonymous \(guests\) or known \(authenticated\). The unread message count is displayed on the chat widget.

In asynchronous chat, the unread message count reflects the number of any offline messages sent by a live agent and any simple notifications received.

![Unread message count and new message indicators in the Service Portal chat widget.](../image/unread-new-message-indicators.png "Unread message count and new message indicators (Service Portal chat widget)")

Message indicators are displayed as follows:

-   There is no limit on the number of unread messages. Up to 50 unread messages can be viewed at a given time. Messages can span multiple conversations, either open \(current\) or closed \(past\) conversations.

-   When users open the chat client, they’re shown the last message received. They can scroll up or down to read the unread messages, as directed by the **New messages above** button or **New messages below** button.

-   A new messages separator line is displayed between the read and unread messages.

-   When a user closes and reopens the chat window, the messages displayed are considered as "read" even though the user might not have reviewed them.


## System messages

During active conversations with live or virtual agents, certain system messages inform users and agents about the conversation state. For example, if a user is engaged in live chat, but doesn’t respond within a certain amount of time, a conversation timeout message is displayed: `The conversation is timing out, are you still there?`

You can change base system messages by editing their related system properties in Chat Settings in the Conversational Interfaces console.

-   **[Disable live agent support for a channel](../task/disable-live-agent-support-channel.md)**  
Add the **disable\_live\_agent** property to the Channel Properties related list to exclude it from live agent support.
-   **[Using Asynchronous Chat in messaging channels](../../virtual-agent/concept/async-chat.md)**  
Enable your organization or brand to maintain constant engagement with end users. With Asynchronous Chat, your agents and end users can participate in long-running conversations without being online concurrently. Agents can also proactively contact users whenever there is useful information to share, such as important alerts or updates.

**Parent Topic:**[Exploring Conversational Interfaces Console](exploring-ci.md)

