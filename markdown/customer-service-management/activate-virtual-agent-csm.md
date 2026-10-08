---
title: Activate Virtual Agent for Customer Service Management
description: Activate the Customer Service Virtual Agent plugin to enable predefined chatbot conversations that help customers complete common self-service tasks. The plugin includes ready-to-use topics that you can publish after activation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/activate-virtual-agent-csm.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [activate virtual agent csm, customer service virtual agent, csm chatbot conversations, virtual agent plugin]
breadcrumb: [Configure chat, Configure omnichannel, Configure, Customer Service Management]
---

# Activate Virtual Agent for Customer Service Management

Activate the Customer Service Virtual Agent plugin to enable predefined chatbot conversations that help customers complete common self-service tasks. The plugin includes ready-to-use topics that you can publish after activation.

## Before you begin

The Virtual Agent plugin \(com.glide.cs.chatbot\) must be activated. If Virtual Agent is not currently activated, contact ServiceNow to activate it.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  In the Name column, find and select Customer Service Virtual Agent Conversations.

    You can also search for the plugin ID: com.sn\_csm.virtualagent.

3.  Select **Activate/Upgrade**.

4.  In the Activate Plugin dialog box, review the plugin dependencies.

    The system displays any dependent plugins that will be activated automatically. Verify that all dependencies are acceptable before proceeding.

5.  Select **Activate**.

    The plugin activates and the predefined Customer Service Virtual Agent topics is set to available in the system. The Customer Service NLU Model for Virtual Agent Conversations \(com.sn\_csm.nlu\) plugin is automatically activated.


## Result

The predefined Virtual Agent topics are now available in your instance. Publish each topic to make it available to your customers.

**Related topics**  


[Publish a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/publish-virtual-agent-topic.md)

[Customer Service Virtual Agent conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-virtual-agent-chatbot.md)

[Get help using virtual agent conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-virtual-agent-conversation.md)

[Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/conversation-designer-virtual-agent.md)

