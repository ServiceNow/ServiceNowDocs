---
title: Using Asynchronous Chat in messaging channels
description: Enable your organization or brand to maintain constant engagement with end users. With Asynchronous Chat, your agents and end users can participate in long-running conversations without being online concurrently. Agents can also proactively contact users whenever there is useful information to share, such as important alerts or updates.
locale: en-US
release: yokohama
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
keywords: [Asynchronous Chat, messaging, channels, agents, Twilio, SMS]
breadcrumb: [Channels in Conversational Interfaces, Exploring Conversational Interfaces Console, Conversational Interfaces Console, Conversational Interfaces]
---

# Using Asynchronous Chat in messaging channels

Enable your organization or brand to maintain constant engagement with end users. With Asynchronous Chat, your agents and end users can participate in long-running conversations without being online concurrently. Agents can also proactively contact users whenever there is useful information to share, such as important alerts or updates.

With Asynchronous Chat, end users and agents can engage in conversations that might span several hours or even days. These conversations run on messaging channels that allow your users and agents to communicate at different times and to resume conversations where they left off. Users can respond at their convenience and are no longer limited to working with agents only during customer support hours.

Long-running conversations are supported on channels that are designated as messaging channels in the Messaging Channel \[sys\_cs\_channel\] table. Messaging channels provided with your base system include the SMS channel, which is used by the ServiceNow Conversational SMS Integration with Twilio app and the ServiceNow Conversational SMS service channel app.

Starting with the Rome release, you can also configure the web \(mweb\) channel, which includes the iOS, Android, and desktop devices, as a messaging channel instead of a chat channel. For configuration details, see [Configure asynchronous chat for the web channel](../task/configure-async-web.md).

**Note:** The web chat and mweb channels are the only channels that support both chat and messaging mode, depending on your need. Web chat can only be set up in one mode on any given instance. The Asynchronous Chat feature specifically refers to the mweb channel in messaging mode.

## Requirements

Asynchronous chat requires certain plugins and ServiceNow applications from the ServiceNow Store.

<table id="table_fnp_kfw_2qb"><thead><tr><th>

Plugin or ServiceNow app

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Glide Conversation Server

 \[com.glide.cs\]

</td><td>

Enables Virtual Agent functionality handled by the Conversation Server, including conversation settings and the Virtual Agent chat widget plugin \(com.glide.cs.sn-va-web-client-app\).

 The Conversation Server is included with Virtual Agent Lite, which is provided with your base system. For full Virtual Agent functionality, see [Activate Glide Virtual Agent](../task/activate-virtual-agent.md), which is available by subscription.

</td></tr><tr><td>

Conversational Messaging\[com.glide.messaging.awa\]

</td><td>

Enables features for conversational messaging, such as messaging actions in Workspace.

 For details, see [Activate Conversational Messaging](https://www.servicenow.com/docs/access?context=activate-messaging-actions&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Now Mobile app\(Version 12.2\)

</td><td>

Enables users to submit incidents and requests, manage tasks, and request help from Agent Chat \(and Virtual Agent if using Virtual Agent\).

 End users install the Now Mobile app for iOS or Android systems from the Apple App Store or the Google Play store, respectively.

</td></tr><tr><td>

Agent-initiated Messaging Interface\(Version 3.0\)

</td><td>

Supports agent-initiated conversations in messaging channels. This ServiceNow app, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home), also installs the Conversational Messaging plugin \(com.glide.messaging.awa\).

</td></tr></tbody>
</table>## How Asynchronous Chat works

Asynchronous Chat provides various features to help you improve the conversational experience for your users and agents, such as:

-   Message indicators that inform users of new and unread messages received when they're away from the chat window or when they've been offline.
-   System messages, displayed to users and agents, that are tailored to either messaging or chat channels.
-   Idle conversation timeout period that admins can adjust for messaging channels, as needed.
-   Proactive messaging capability that enables agents to initiate communication with users

The following sections explain how these features work for Asynchronous Chat.

## New and unread message indicators

End users can receive messages on a messaging channel, even when they're offline. Users can be anonymous \(guests\) or known \(authenticated\). The unread message count is displayed on the chat widget. The unread message count reflects the number of any offline messages that were sent by a live agent and any simple notifications received.

![The chat icon shows the number of new messages. When the user opens the chat window, line indicators show there are new unread messages in the conversation.](../images/msg-indicators.png "Unread message count and new message indicators")

-   There is no limit on the number of unread messages. Up to 50 unread messages can be viewed at a given time. Messages can span multiple conversations, either open \(current\) or closed \(past\) conversations.
-   When users open the chat client, they land on the very last message received. They can scroll up or down to read the unread messages, as directed by a **New messages above** button or **New messages below** button.
-   A new messages separator line displays between the read and unread messages.
-   When users close and re-open the chat window, the messages displayed are considered as "read" even though users might not have reviewed them.

## System messages

Certain system messages that are displayed to users and agents in chat mode are not applicable in messaging mode, and are suppressed as needed. The following table identifies system messages that are displayed or suppressed, depending on the mode.

<table id="table_ikh_hfw_2qb"><thead><tr><th>

System message

</th><th>

Messaging mode \(web and mobile\)

</th><th>

Chat mode

</th></tr></thead><tbody><tr><td>

X has closed the support session.\[Displayed when either the agent or user closes the chat session\]

</td><td>

Displayed

</td><td>

Displayed

</td></tr><tr><td>

The support session was closed.\[Displayed when the chat session was not closed by the agent or user\]

</td><td>

Suppressed

</td><td>

Displayed

</td></tr><tr><td>

X has entered the chat.

</td><td>

Suppressed

</td><td>

Displayed

</td></tr><tr><td>

Thank you for contacting support. I am looking into your question and will be with you shortly.

</td><td>

Displayed

</td><td>

Displayed

</td></tr><tr><td>

The conversation is timing out, are you still there?\[ [Controlling idle live chat sessions](../../conversational-interfaces/concept/ci-idle-chats.md) controlled by the **com.glide.cs.idle\_chat\_reminder\_message** system property\]

</td><td>

Suppressed

</td><td>

Displayed

</td></tr></tbody>
</table>## Idle conversations and messaging actions in messaging channels

In chat channels, the default idle conversation timeout period for Virtual Agent and Live Agent conversations is two hours \(7200 seconds\). However, for Live Agent conversations in messaging channels, certain messaging actions are automatically applied, which affects how idle conversations are handled. In messaging channels, when a requester hasn't responded to an agent message within two days, the conversation state changes to Closed Abandoned and the message is closed. For more information on messaging actions, see [Configure messaging actions](https://www.servicenow.com/docs/access?context=configure-messaging-actions&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

As admins, you can override the conversation idle timeout period per channel by setting the value in the **Conversation Idle Timeout** field in the Messaging Channels \[sys\_cs\_channel\] table. For details, see [Override the conversation timeout period by channel](va-open-conversations.md#section_yd3_fgp_14b).

## Proactive messaging

Using the [Agent-initiated messaging interface](../../conversational-interfaces/concept/agent-init-messg-interface.md), agents can proactively communicate with end users to share relevant or helpful information. When agents initiate messaging from the mweb channel in Asynchronous Chat, your users have the option to respond immediately and engage in a two-way conversational experience. Proactive messaging with the mweb channel has the following capabilities:

-   **Compose Message** feature that agents use to create and send messages to selected users. Messages can contain links and file attachments.
-   When a user replies to a message, the ongoing interaction context is retained, providing the agent with the information needed to maintain the conversation.

![Compose Message window with highlighted mweb dropdown and message reading Hello from agent, next to message window with highlighted Agent-initiated message on mweb channel.](../images/agt-init-msg.png "Agent-initiated message on mweb channel")

For more information on agent-intiated messages, see [Install agent-initiated messaging interface](../../conversational-interfaces/concept/ci-agent-chat-using.md#).

## End user experience in live agent conversations

When a user starts the chat widget after having received offline messages from a specific agent, for example Agent A, the conversation is in Live Agent mode:

-   If Agent A is available, the user can resume the conversation with Agent A.
-   If Agent A is not available, but Agent B is, depending on the agent reassignment settings, the chat window displays Agent B's name and avatar and the conversation resumes.
-   If no agents are available, the conversation is routed to an agent based on the Queue Max Wait Time. If there isn't a wait time, the conversation waits until an agent becomes available.

-   **[Configure asynchronous chat for the web channel](../task/configure-async-web.md)**  
Set the chat widget as a messaging channel for asynchronous chat.

**Parent Topic:**[Channels in Conversational Interfaces](../../conversational-interfaces/concept/ci-channels-overview.md)

