---
title: Service channels
description: Provide customer support by automatically routing incoming work to agents through service channels.
locale: en-US
release: xanadu
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
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

Included with the [Conversational Integration with Facebook Messenger](https://www.servicenow.com/docs/access?context=messg-fbm&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) store application.

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

Included with the [Conversational Integration with LINE](https://www.servicenow.com/docs/access?context=messg-line&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) store application.

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

Included with the [Conversational Integration with WhatsApp \(powered by Twilio\)](https://www.servicenow.com/docs/access?context=messg-whatsapp-twilio&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) store application.

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

-   **[Service channel capacity and utilization](awa-service-channel-capacity.md)**  
In Advanced Work Assignment, capacity is the number of work items automatically assigned to agents supporting a service channel. Utilization is the condition that identifies the work item states supported in the channel.
-   **[Conversational SMS service channel](conversation-sms-service-channel-store-app.md)**  
Using the Conversational SMS service channel app on the ServiceNow Store, workspace agents can provide support for long-running SMS conversations and conversations that use multiple service channels.
-   **[Set up a custom service channel](../task/setup-custom-channel.md)**  
Set up a custom service channel to expand the type and scope of work that is routed automatically to your agents.
-   **[Inbox layout](awa-inbox-layout.md)**  
The inbox layout determines the information shown on work item cards displayed in an agent's inbox.
-   **[Override agent capacity for selected agents](../task/awa-change-agent-capacity.md)**  
Change the default number of work items that an agent can handle for a service channel.
-   **[Create or change a work item size override](../task/awa-modify-work-item-size.md)**  
Create a work item size override if you want Agent Affinity to calculate an agent's workload using a work item size other than the default.

**Parent Topic:**[Configuring Advanced Work Assignment](../task/installing-awa.md)

**Related topics**  


[Advanced Work Assignment home page](awa-admin-console-home.md)

[Get started with Advanced Work Assignment](../task/implement-awa.md)

[Install Conversational SMS service channel](../task/install-conversational-sms.md)

[Activate Agent Affinity](../task/awa-activate-agent-affinity.md)

[Activate Conversational Messaging](../../virtual-agent/task/activate-messaging-actions.md)

[Work items](awa-work-items.md)

[Work assignments](awa-assignment.md)

[Using Agent Affinity](awa-agent-affinity-concept.md)

[Agent Inbox controls](agent-experience.md)

[Advanced Work Assignment Inbox Sentiment display](awa-inbox-sentiment-display.md)

[Management](management.md)

[AWA group queue priorities](awa-group-queue-priorities.md)

[Configure messaging actions](../../virtual-agent/task/configure-messaging-actions.md)

[Enable logging for Advanced Work Assignment](../task/awa-activate-logging.md)

