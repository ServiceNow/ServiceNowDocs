---
title: Deploying Virtual Agent topics in other channels
description: When creating a topic or topic block, you can specify the chat channels in which the topic or topic block will run. During conversation design, Virtual Agent Designer provides built-in guardrails to help you tailor your conversations to those channels.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Virtual Agent, Designer, topic, block, channel, Slack, Workplace, Microsoft, Teams, MSTeams, channel, chat, custom]
breadcrumb: [Exploring other Virtual Agent features, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Deploying Virtual Agent topics in other channels

When creating a topic or topic block, you can specify the chat channels in which the topic or topic block will run. During conversation design, Virtual Agent Designer provides built-in guardrails to help you tailor your conversations to those channels.

In Virtual Agent, a channel is a chat interface or application in which Virtual Agent interacts with end users. Default channels are the chat applications natively supported by Virtual Agent, such as the Slack, Microsoft Teams, Workplace, and Facebook Messenger applications, and the web and mobile clients. Virtual Agent also supports custom channels created through the [conversational custom chat integrations](va-custom-adapter-framework.md) feature, which enables third-party applications \(other chat providers\) to work in Virtual Agent.

For example, admins can build a custom conversational chat integration for a specific messaging provider, such as Skype. Admins also define the controls that can be used in topics that run in these channels. For details about creating channels for chat providers and specifying the controls used in a channel, see [Creating conversational custom chat integrations in Virtual Agent](va-custom-adapter-framework.md).

## Specifying channels in your topics or topic blocks

When you create or edit a topic or topic block, you can specify the applicable channels in the **Channels** field under Advanced properties in the Topic Properties page. Applicable channels are the custom channels created for your instance through the conversational custom chat integrations. Use this field to specify chat clients in which the topic or topic block will run.

**Note:** An updated Assistant Designer Asset library user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not activated, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](../reference/vad-prev-topics-page.md).

![The Topic Properties page displaying the Channels support field under Advanced properties, along with the Channels pop-up.](../images/va-prop-channelsup-2.png "Additional channel support field in the Topic Properties page")

During conversation design, Virtual Agent checks the various controls used to build the conversation flow to confirm that the control is valid for the channels in which the topic or block will run.

## Design checks for specified channels during conversation design

When you're designing your conversation, built-in guardrails identify the Virtual Agent Designer controls that are not suited for the custom channels that you specified in the Topic Properties page. These messages are displayed in the following views:

-   **Properties** tab \(Topic Properties page\)

    In the following example, Skype and SMS are the additional channels in which the topic will run. The banner message identifies the controls that are not supported on the channels for the topic. As you develop the conversation flow, you can revise your conversation so that it does not use any of the specified controls for your selected channels.

    ![Virtual Agent Designer topic properties page with defined channels.](../images/channel-support-prop-example1.png "Topic Properties tab with defined channels")

-   **Flow** tab \(Virtual Agent Designer canvas\)

    In the following example flow, the banner message identifies the controls that are not supported for the specified channels. The property sheet for the affected nodes also displays a message indicating that the control is not supported. For example, when you highlight a particular node \(control\) in the flow, the associated property sheet for the node indicates that the control is not supported in the Skype and SMS channels.

    If you have controls that cannot be used, you can branch the flow so that you can continue building the flow with the controls that are supported.

    ![Virtual Agent Designer conversation builder interface, with unsupported controls for messaging channels flagged on the flow tab and detailed in a pop-up message.](../images/channel-support-canvas-example2a.png "Topic Flow tab with channel warnings")


## Finding the channels available in your instance

To see a list of the available channels in your instance, use the filter icon \(![](../images/filter-icon.png)\) in the Assistant Designer Asset library \(**Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**\). The Messaging Channels \[sys\_cs\_channel\] table also shows the available channels.

![Use the filter icon to find topics based on channel support on the Assistant Designer Asset library.](../images/va-custom-channels-2.png "Filtering supported channels in the home page")

The default channels in Virtual Agent are the web chat and mobile clients and also the Virtual Agent messaging integrations for the Slack, Microsoft Teams, Workplace, and Facebook Messenger messaging applications. In the previous example, SMS is an available chat channel that was created for your instance through a conversational chat integration. When you choose a channel, the home page lists your topics \(cards\) by channel type. For more information, see [Creating conversational custom chat integrations in Virtual Agent](va-custom-adapter-framework.md).

**Parent Topic:**[Exploring other Virtual Agent features](exploring-other-vad-features.md)

