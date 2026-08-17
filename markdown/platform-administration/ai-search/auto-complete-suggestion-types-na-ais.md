---
title: Auto-complete suggestion types included with ServiceNow Otto for AI Search
description: ServiceNow Otto for AI Search includes an auto-complete suggestion type that displays suggestedconfirm name ServiceNow Otto for Virtual Agent conversational prompts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/auto-complete-suggestion-types-na-ais.html
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-07-25"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [ServiceNow Otto for AI Search reference, ServiceNow Otto for AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Auto-complete suggestion types included with ServiceNow Otto for AI Search

ServiceNow® Otto for AI Search includes an auto-complete suggestion type that displays suggested ServiceNow® Otto for Virtual Agent conversational prompts.

To learn more about how this auto-complete suggestion type appears to search and chat users, see [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-enhanced-chat.md). For details on configuring and using auto-complete suggestion types in your search application configurations, see [Auto-complete suggestions in AI Search applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/auto-complete-ais.md).

<table id="table_rc4_z2y_v2c"><thead><tr><th>

Auto-complete suggestion type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Now Assist Suggested Query Reader Group for &lt;application name&gt;

</td><td>

Displays Virtual Agent conversational prompts based on previous user searches \(utterances\) that produced synthesized Genius Result responses. Selecting a suggested prompt opens a Virtual Agent conversation within the enhanced chat window or full-page experience. ServiceNow Otto for AI Search scores conversational prompt suggestions based on how search users have interacted with and rated their synthesized Genius Result responses. Suggestions with higher scores are preferentially displayed when searching.

 User queries from Virtual Agent conversations are stored as suggestions in the Utterance Suggestions \[sys\_suggested\_utterance\] table. The system prunes this table and automatically removes conversational prompt suggestions that meet any of these conditions:

-   The conversational prompt suggestion's query and result combination have not been used in a search within the last 180 days.
-   The conversational prompt suggestion refers to a record \(such as a Catalog Item or a knowledge article\) that has been deleted or deactivated.

 New conversational prompt suggestions are disabled if they match any exclusion rule entry from the Search Suggestion Exclusion List \[sys\_search\_suggestion\_blacklist\] table. When a new exclusion rule is added to the Search Suggestion Exclusion List table, existing conversational prompt suggestions that match it are disabled. For details on the Search Suggestion Exclusion List table, see [Prevent the creation of suggestions in special cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-suggestions/preventing-suggestions.md).

 Conversational prompt suggestions are only returned from the search user's domain. Only search users with the global domain can see utterance suggestions from the global domain.

 When you create a new search application configuration, this suggestion reader group isn't linked to it by default. If you enable enhanced chat in a search portal, this suggestion reader group is linked to the search application configuration record shared between the portal and Virtual Agent.

 Conversational prompt suggestions are displayed in search portals by default. To make conversational prompt suggestions available in global and workspace search, you must enable ServiceNow Otto panel enhanced chat. For details on this procedure, see [Activate ServiceNow Otto panel enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-enhanced-activate.md).

 Default section header: `Ask ServiceNow Otto`

 Readers: ServiceNow Otto Suggested Utterance Reader

 **Note:** This suggestion reader group is only supported in search application configurations for applications that support the enhanced chat experience, such as the **ServiceNow Otto in VA** search application configuration.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow Otto for AI Search reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/reference-now-assist-ais.md)

