---
title: Prerequisites for premium chat
description: Premium chat is available for instances that meet ServiceNow readiness requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/now-assist-in-virtual-agent/premium-chat-prereqs.html
release: australia
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

**Note:**

If your organization's network firewall uses an allow list policy, you must add the premium chat domains to your list of allowed outbound domains before enabling premium chat. The premium chat domains include:

-   `https://nextwave-prod-main-ycgytz.sncapps.service-now.com/sncapps/nextwave/health/all`
-   `https://nextwave-preview-main-ycgytz.sncapps.service-now.com/sncapps/nextwave/health/all`
-   `https://nextwave-demo-main-ycgytz.sncapps.service-now.com/sncapps/nextwave/health/all`
-   `https://nextwave-dev-main-phxbwi.sncapps.service-now.com/sncapps/nextwave/health/all`
-   `https://nextwave-evals-main-phxbwi.sncapps.service-now.com/sncapps/nextwave/health/all`

If you don't add these domains, the premium chat client can't reach the premium chat service, and chat functionality fails or appears unresponsive. The allow list requirement applies to premium chat for ServiceNow Otto for Virtual Agent and ServiceNow Otto panel assistants.

Administrators must have the following for premium chat:

-   Zurich patch 9 or later
-   Australia patch 3 or later
-   Latest version of a ServiceNow Otto store app, such as ServiceNow Otto for ITSM

Premium chat requires the ServiceNow default chat widget button to be turned on. Complete the following actions for premium chat to display a synthesized response after entering a search query through the portal:

-   [Configure the portal's AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configuring-ais.md).
-   Turn on the ServiceNow default Search page widget.
-   Turn on the ServiceNow default chat widget button.

Complete the following actions for premium chat to display a synthesized response in the full-page experience after entering a search query through the portal's search bar:

-   Configure the portal's AI Search.
-   Turn on the ServiceNow default Search page widget.
-   Turn on the ServiceNow default chat widget button.
-   Turn on the ServiceNow default Search Typeahead widget.

