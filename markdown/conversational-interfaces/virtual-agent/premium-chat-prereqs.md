---
title: Prerequisites for premium chat
description: Your instance must meet eligibility requirements to use premium chat, and your network must allow traffic to the premium chat service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/virtual-agent/premium-chat-prereqs.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-10-16"
reading_time_minutes: 1
keywords: [Virtual Agent, LLM]
breadcrumb: [Premium chat, Using ServiceNow Otto for Virtual Agent, Use, Virtual Agent, Conversational Interfaces]
---

# Prerequisites for premium chat

Your instance must meet eligibility requirements to use premium chat, and your network must allow traffic to the premium chat service.

ServiceNow automatically performs eligibility checks and displays the premium chat option when your instance qualifies. Premium chat isn't available for instances that use regional data routing.

If your instance doesn't meet the requirements for premium chat, you can continue using the standard or enhanced chat experience. If you're a new customer, premium chat might be the only available chat experience, depending on the assistant type and supported display experience. If you're an existing customer, you can choose whether to opt in to premium chat when your instance is eligible.

**Note:**

If your organization's network firewall uses an allow list policy, you must add the premium chat domains to your list of allowed outbound domains before enabling premium chat. The premium chat domains include:

-   `https://nextwave-prod-main-ycgytz.sncapps.service-now.com/sncapps/nextwave/health/all`
-   `https://nextwave-preview-main-ycgytz.sncapps.service-now.com/sncapps/nextwave/health/all`
-   `https://nextwave-demo-main-ycgytz.sncapps.service-now.com/sncapps/nextwave/health/all`
-   `https://nextwave-dev-main-phxbwi.sncapps.service-now.com/sncapps/nextwave/health/all`
-   `https://nextwave-evals-main-phxbwi.sncapps.service-now.com/sncapps/nextwave/health/all`

If you don't add these domains, the premium chat client can't reach the premium chat service, and chat functionality fails or appears unresponsive. The allow list requirement applies to premium chat for ServiceNow Otto for Virtual Agent and ServiceNow Otto panel assistants.

