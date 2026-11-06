---
title: Prerequisites for premium chat
description: Premium chat is available for instances that meet ServiceNow readiness requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/now-assist-in-virtual-agent/premium-chat-prereqs.html
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-10-16"
reading_time_minutes: 1
keywords: [Virtual Agent, LLM]
breadcrumb: [Premium chat, Using ServiceNow Otto for Virtual Agent, ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Prerequisites for premium chat

Premium chat is available for instances that meet ServiceNow readiness requirements.

ServiceNow automatically performs eligibility checks and displays the premium chat option when your instance qualifies. Premium chat isn't available for instances that use regional data routing.

If your instance doesn't meet the requirements for premium chat, you can continue using the standard or enhanced chat experience. For new customers, premium chat might be the only available chat experience depending on the assistant type and supported display experience. Existing customers can choose whether to opt in to premium chat when eligible.

**Note:** If your organization's network firewall uses an allow list policy, you must add the premium chat domain to your list of allowed outbound domains before enabling premium chat. Without this, the premium chat client is unable to reach the premium chat service and chat functionality fails or appears unresponsive. This applies to premium chat for ServiceNow Otto for Virtual Agent and ServiceNow Otto panel assistants.

