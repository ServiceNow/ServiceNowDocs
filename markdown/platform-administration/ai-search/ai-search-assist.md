---
title: AI Search Assist record producer integration for Service Portal
description: AI Search Assist is a Service Portal widget that uses AI Search to improve incident deflection by displaying the most relevant set of related Catalog Item and knowledge article search results within a record producer. You can use AI Search Assist instead of Contextual Search.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search Assist record producer integration for Service Portal

AI Search Assist is a Service Portal widget that uses AI Search to improve incident deflection by displaying the most relevant set of related Catalog Item and knowledge article search results within a record producer. You can use AI Search Assist instead of Contextual Search.

## AI Search Assist overview

AI Search Assist can help a user find the most relevant Catalog Items and knowledge articles in a search on your portal. For example, a user, creating an Incident via the Service Portal, can see related Catalog Items that the user can order. The user can also view related knowledge articles to assist them to resolve the issue on their own without involving the service desk.

AI Search Assist helps with incident deflection for incident record producers, deflecting incidents by helping end users resolve issues before they raise an incident.

AI Search Assist supports ServiceNow mobile.

**Note:** AI Search Assist doesn't support external users. If an external user tries to use an Assist UI action, the system returns an error.

## Activation information

The AI Search Assist plugin \(com.snc.ai\_search\_assist\) is a ServiceNow AI Platform® application that is activated by default when AI Search is active.

-   **[Configure AI Search Assist for a record producer](../task/configure-ai-search-assist.md)**  
Configure AI Search Assist settings for a record producer to help users view related Catalog Item and knowledge article search results.
-   **[AI Search Assist roles](../reference/ai-search-assist-role.md#)**  
AI Search Assist includes the following roles.
-   **[AI Search Assist properties](../reference/ai-search-assist-properties.md)**  
The AI Search Assist properties determine when searching begins based on characters entered and the time that has elapsed. These properties reduce the impact of searches for systems with many Catalog Items or Knowledge articles.
-   **[Domain separation and AI Search Assist](ai-search-assist-domain-separation.md)**  
Domain separation is supported for AI Search Assist. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[Integrating AI Search into other ServiceNow AI Platform applications](integrate-ais.md)

