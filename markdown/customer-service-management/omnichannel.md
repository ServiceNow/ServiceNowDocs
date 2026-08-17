---
title: Omnichannel
description: Omnichannel routes customer conversations from every channel into one workspace. Agents can see the full interaction history and resolve issues without switching context.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/omnichannel.html
release: australia
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

The following omnichannel workflow example shows how Alex, a customer service manager at a growing retail company, improves support across chat, email, messaging apps, and voice. Customers can start in one channel and continue in another without repeating themselves. A virtual agent collects order and issue details and attempts self-service resolution. When escalation is needed, the conversation moves to a live agent with full context, who creates and resolves the case while keeping the complete interaction history linked. From the unified workspace, Alex’s team can view every channel in one place, reduce resolution times, and provide consistent, informed service at each touchpoint.

\[Omitted image "omnichannel-use-case-workflow-revised1.png"\] Alt text: Omnichannel workflow diagram showing how customer interactions across channels connect to a unified agent workspace

## Channel descriptions

|Channel|Role|Description|
|-------|----|-----------|
|[Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_ChatFeature.md)|Agent|Review incoming chat with full customer history and open cases, resolve the issue, and record a wrap-up code to close the interaction.|
|Admin|Set up chat queues, define routing rules to distribute incoming chats by priority or skill, configure Virtual Agent escalation paths, and adjust agent capacity settings to balance workload.|
|[Email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceEmailCommunication.md)|Agent|Review Al-generated email thread summaries and the full activity stream to understand customer issues without reading every message, compose responses, and log outcomes with wrap-up codes.|
|Admin|Configure email routing rules to send messages to the correct team, set up shared inboxes for team access, and enable AI summarization to reduce agent review time.|
|[Messaging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/messg-integrate-channels.md)|Agent|Engage with customers over messaging at a flexible pace and transfer conversations to other agents while preserving the full conversation thread.|
|Admin|Connect and manage multiple messaging channels \(SMS, WhatsApp, social messaging\) from a single ServiceNow interface instead of toggling between separate tools.|
|[Voice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_PhoneCommunication.md)|Agent|Handle inbound and outbound calls with customer details and case history displayed before answering, then record a wrap-up code when complete.|
|Admin|Integrate a CCaaS platform with ServiceNow, define voice routing rules, and manage agent availability, all within ServiceNow rather than switching to a separate platform.|

**Related topics**  


[Configure Omnichannel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/enable-comm-channels.md)

