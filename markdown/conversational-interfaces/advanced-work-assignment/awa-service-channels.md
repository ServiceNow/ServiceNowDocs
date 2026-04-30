---
title: Service channels
description: Provide customer support by automatically routing incoming work to agents through service channels.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Service channels

Provide customer support by automatically routing incoming work to agents through service channels.

A service channel is a means of assigning a specific type and scope of work to agents. You can configure base system service channels to set the context and attributes that define work handled in the channel, or create your own custom service channel.

Advanced Work Assignment provides several service channels from which work items originate. These channels are:

<table id="table_wy2_qq4_sfb"><thead><tr><th>

Service channel

</th><th>

Description

</th><th>

Plugin

</th></tr></thead><tbody><tr><td>

Case

</td><td>

Routes and assigns customer service cases.

</td><td>

Included with Customer Service

</td></tr><tr><td>

Chat

</td><td>

Routes and assigns chat interactions.

</td><td>

Included with the Agent Chat plugin \(com.glide.interaction.awa\).

</td></tr><tr><td>

Chat - Asynchronous

</td><td>

Routes long-running conversations that use multiple service channels.

</td><td>

Included with the Conversational Messaging plugin \(com.glide.messaging.awa\).

</td></tr><tr><td>

Facebook Messenger

</td><td>

Routes requests from the Facebook Messenger chat conversations.

</td><td>

Included with the [Conversational Integration with Facebook Messenger](../../virtual-agent/concept/messg-fbm.md) store application.

</td></tr><tr><td>

Incident

</td><td>

Routes and assigns incidents.

</td><td>

Included with the Advanced Work Assignment for incidents plugin \(com.snc.incident.awa\).

</td></tr><tr><td>

Line

</td><td>

Routes requests from LINE chat conversations.

</td><td>

Included with the [Conversational Integration with LINE](../../virtual-agent/concept/messg-line.md) store application.

</td></tr><tr><td>

SMS

</td><td>

Routes long-running SMS conversations and conversations that use multiple service channels.

</td><td>

Included with the [Install Conversational SMS service channel](../task/install-conversational-sms.md) application.

</td></tr><tr><td>

Walk-up

</td><td>

Routes requests from walk-up contact channels.

</td><td>

Included with the Walk-up Experience plugin \(com.snc.walkup\).

</td></tr><tr><td>

WhatsApp

</td><td>

Routes requests from the WhatsApp chat conversations.

</td><td>

Included with the [Conversational Integration with WhatsApp \(powered by Twilio\)](../../virtual-agent/concept/messg-whatsapp-twilio.md) store application.

</td></tr></tbody>
</table>You can also set up a custom service channel to address work that is not supported in the base system channels. For more information, see [Set up a custom service channel](../task/setup-custom-channel.md).

For each service channel, you set attributes such as:

-   Agent capacity: Amount of work that can be handled by the agents supporting the channel.
-   Filters: Conditions that filter the type of work handled in the channel.
-   Utilization: Conditions that determine when work items are generated.

For each service channel, you also:

-   Create the agent inbox card layout used in Agent Workspace.
-   Set capacity overrides for specific agents.
-   Review and modify associated work item queues. For the Chat service channel, you can create queues using the **Queues** related list.

**Parent Topic:**[Exploring Advanced Work Assignment](awa-overview.md)

