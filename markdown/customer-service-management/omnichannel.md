---
title: Omnichannel
description: Omnichannel routes customer conversations from every channel into one workspace. Agents can see the full interaction history and resolve issues without switching context.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/omnichannel.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2026-05-27"
reading_time_minutes: 3
breadcrumb: [Explore, Customer Service Management]
---

# Omnichannel

Omnichannel routes customer conversations from every channel into one workspace. Agents can see the full interaction history and resolve issues without switching context.

## Omnichannel overview

Omnichannel brings together customer communications from email, chat, voice, messaging apps, web and portal, virtual agents, and in-person interactions. It keeps all conversations and context unified in one system as customers switch channels. Agents manage every interaction from a unified workspace to provide consistent service across every channel.

-   **Chat**

    Chat is available in self-service portals, third-party portals, and mobile apps through Virtual Agent and Engagement Messenger, and conversations carry across every channel.

-   **Email**

    Track, route, and resolve all emails in ServiceNow. Two workflows are available: Email as Interaction creates an interaction record for agent review before optionally converting to a case. Email to Case automatically creates and populates a case record, with all replies threaded within it. Full conversation history is preserved in both workflows.

-   **Messaging**

    Omnichannel messaging supports SMS, WhatsApp, Facebook Messenger, LINE, and Apple Messages for Business, so customers can message at their own pace through Virtual Agent or live agents across all channels.

-   **Voice**

    The Voice framework integrates with certified CCaaS platforms to deliver call features. ServiceNow serves as the unified agent workspace for organizations that need voice-only or embedded Computer Telephony Integration \(CTI\).


## Omnichannel workflow

This scenario shows the omnichannel customer service journey, and how ServiceNow connects every channel to keep agents fully informed at each step.

1.  A customer initiates a return. The Virtual Agent responds automatically, collects order details, and tries to resolve the issue through self-service.
2.  The conversation escalates to a live agent with full context.
3.  The agent creates a case from the interaction and resolves it.
4.  The agent sends the resolution to the customer via email with all details. ServiceNow links the outbound email to the case and keeps the chat history for reference.
5.  The customer accepts the resolution, which closes the case.

Throughout the journey, customers don't repeat themselves, and every agent has all information at every touchpoint.

\[Omitted image "omnichannel-use-case-updated.png"\] Alt text: Omnichannel workflow diagram showing how customer interactions across channels connect to a unified agent workspace

|Channels|Role|Benefits|
|--------|----|--------|
|[Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_ChatFeature.md)|Agent|Access full customer details and case history during each conversation and use wrap-up codes to record outcomes when closing.|
|Admin|Configure chat queues, routing rules, Virtual Agent, and agent capacity settings to manage workload across teams.|
|[Email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceEmailCommunication.md)|Agent|Manage inbound and outbound email with AI-generated summaries, wrap-up codes, and a full activity stream to capture context quickly without manually reviewing long email threads.|
|Admin|Set up and manage email routing rules, inboxes, and AI summarization settings to streamline agent workflows.|
|[Messaging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/messg-integrate-channels.md)|Agent|Manage messaging interactions at a flexible pace and transfer them without losing conversation history.|
|Admin|Configure and manage multiple messaging channels from a single interface.|
|[Voice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_PhoneCommunication.md)|Agent|Handle inbound and outbound voice interactions with full customer context and case data available before the interaction begins and use wrap-up codes to record outcomes when closing.|
|Admin|Configure CCaaS integration and routing rules within ServiceNow without switching platforms.|

