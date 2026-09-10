---
title: Consumer messaging apps
description: Omnichannel for Customer Service Management \(CSM\) provides a unified way to handle customer interactions across multiple channels from a single workspace, with centralized routing through Advanced Work Assignment \(AWA\). Consumer messaging apps are a supported channel type, allowing customers to contact support through familiar messaging platforms while agents work in the same environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/consumer-messaging-apps.html
release: australia
topic_type: concept
last_updated: "2026-04-27"
reading_time_minutes: 4
keywords: [consumer messaging, WhatsApp, Facebook Messenger, LINE, Apple Messages for Business, omnichannel, messaging integration]
breadcrumb: [Configure omnichannel, Configure, Customer Service Management]
---

# Consumer messaging apps

Omnichannel for Customer Service Management \(CSM\) provides a unified way to handle customer interactions across multiple channels from a single workspace, with centralized routing through Advanced Work Assignment \(AWA\). Consumer messaging apps are a supported channel type, allowing customers to contact support through familiar messaging platforms while agents work in the same environment.

For integration details, see [Integrating with consumer messaging apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/messg-integrate-channels.md).

## Supported messaging platforms

Omnichannel for ServiceNow supports the following consumer messaging platforms:

-   **WhatsApp**

    Your organization's WhatsApp Business number receives messages from customers. Conversations persist across sessions, allowing customers to return to the same thread without repeating information. Agents can send outbound messages from contact records and share rich media including images, documents, and location.

    ServiceNow Otto in Virtual Agent can automatically resolve common customer questions before an interaction reaches an agent. For more information see, [Configure ServiceNow Otto for Customer Service Management \(CSM\) in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/configure-now-assist-for-customer-service-management-csm-in-virtual-agent.md).

    For integration details, see [Integrating WhatsApp with Customer Service Management using the WhatsApp Cloud API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/messg-integrating-whatsapp-with-csm-whatsapp-cloud.md) and [Integrating WhatsApp with Customer Service Management through Twilio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/messg-integrate-whatsapp-csm.md).

-   **Facebook Messenger**

    Customers start conversations from the Messenger app or from your organization's Facebook page. Each conversation creates an interaction record that links to contact information and case history.

    For integration details, see [Integrating Facebook Messenger with Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/messg-integrate-fbm-csm.md) and [Conversational Integration with Facebook Messenger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/messg-fbm.md).

-   **LINE**

    Your organization's LINE Official Account receives messages after customers add it. Conversations support text, images, and stickers.

    For integration details, see [Integrating LINE with Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/messg-integrate-line-csm.md) and [Conversational Integration with LINE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/messg-line.md).

-   **Apple Messages for Business**

    Customers tap the Messages icon on your website, in Maps, in Safari, or in Search to start a conversation in the native Messages app. Organizations must register with Apple Business Register and use an approved Messaging Service Provider \(MSP\).

    Agents can send rich messages including list pickers, time pickers, and quick reply buttons to guide customers through common workflows. Conversations support images, documents, and Apple Pay transactions.

    For integration details, see [Integrating Apple Messages for Business with Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/integrate-amb-with-csm.md) and [Conversational Integration with Apple Messages for Business](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/integration-apple-mssg.md).


## Benefits of consumer messaging apps

|Role|Benefit|
|----|-------|
|Customers|Customers reach support through the messaging apps they already use, without downloading additional software or creating new accounts. Messaging conversations are asynchronous, allowing customers to send messages and return later without staying connected. Conversation history persists across sessions, so customers don't repeat information when they return.|
|Agents|Agents handle messaging interactions in the same workspace used for chat, email, and voice. Each messaging conversation displays customer context including account details, case history, and previous interactions. Agents can transfer conversations to other agents, escalate to cases, and send outbound messages to customers from contact records.|
|Administrators|Messaging platforms are configured independently and can be activated incrementally. AWA applies the same routing logic across all messaging platforms, so you can manage agent workloads and service level agreements from one system. All messaging interactions are tracked as interaction records, providing consistent visibility into volume, resolution, and agent activity.|

## Integration approaches

Consumer messaging apps can be integrated with CSM using two approaches:

-   **Conversational integration**

    Conversational integration routes messaging conversations through Virtual Agent before escalating to live agents. Customers interact with virtual agent topics that try to resolve the issue on their own. When the virtual agent can't resolve the issue, the conversation escalates to a live agent with full context. This approach is available for WhatsApp, Facebook Messenger, LINE, and Apple Messages for Business.

-   **Direct integration**

    Direct integration routes messaging conversations directly to live agents without virtual agent deflection. Customers send messages that create interaction records and are routed to agents based on AWA rules. This approach is available for WhatsApp and provides the fastest path to live agent support.


