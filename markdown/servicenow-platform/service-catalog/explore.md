---
title: Conversational catalog item requests
description: Conversational Catalog Requests provides a conversational, generative AI-powered experience for submitting catalog item requests through Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/explore.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-06-26"
reading_time_minutes: 1
keywords: [explore]
breadcrumb: [Conversational Catalog Requests, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Conversational catalog item requests

Conversational Catalog Requests provides a conversational, generative AI-powered experience for submitting catalog item requests through Virtual Agent.

Instead of navigating static forms, users interact with a conversational flow that guides them through the request.

In Premium chat, the Catalog Agent processes catalog item requests end-to-end through an AI-native conversation. The Catalog Agent/LLM topic block is available for catalog items that meet specific eligibility criteria. The Catalog Agent collects required information from the user through a dynamic, slot-filling exchange. When the Catalog Agent can't process a catalog item, the request falls back to the LLM topic block only for conversational interactions; non-conversational interactions continue to use the catalog item form.

This dual-path approach keeps catalog items accessible through conversational interfaces regardless of whether the Catalog Agent processes them, keeping the experience consistent for users.

-   **[Catalog Agent for Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_catalog_agent.md)**  
The Catalog Agent for Premium chat uses AI Agent conversation through ServiceNow Otto to guide requesters through a conversational catalog request.
-   **[LLM topic block for Conversational Catalog Requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_llm_topic_block_ccr.md)**  
The LLM topic block is a Virtual Agent topic component that connects a conversational catalog request to ServiceNow Otto. It enables generative AI to interpret requester input during the conversation.
-   **[Catalog item request approaches](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/catalog-agent.md)**  
Catalog items can be requested conversationally, depending on how your admin has configured Virtual Agent and which approach is in use. The available approaches help you select the appropriate method for your environment.

**Parent Topic:**[Conversational Catalog Requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/now-assist-in-conversational-catalog-request.md)

