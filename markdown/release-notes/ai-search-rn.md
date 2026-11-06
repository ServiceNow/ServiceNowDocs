---
title: AI Search release notes
description: The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. See the following sections for release notes by version.The Brazil Patch 2 release adds the ability to exclude high-churn fields from indexing.The Brazil Early Availability 2 release adds the option to display search suggestions and search result titles as links that you can open in new browser tabs, expands hybrid search to support all indexed sources configured for semantic vector indexing, and updates the list of LLMs supported by the Now LLM Service.the option to open Summary Genius Results citations in new browser tabsthe ability to use separate search application configurations for portal search and ServiceNow Otto for Virtual Agent enhanced chat
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/ai-search-rn.html
release: australia
topic_type: topic
last_updated: "2026-10-19"
reading_time_minutes: 2
keywords: [AI Search, AI Search]
breadcrumb: [ServiceNow AI Platform administration release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# AI Search release notes

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. See the following sections for release notes by version.

## About AI Search

-   Index and search text and attachments from ServiceNow AI Platform tables and external document repositories.
-   Machine learning relevancy intelligently tunes search result relevancy scores based on previous search users' selections.
-   Semantic vector search and hybrid search modes find results that match the intent and context of your search.
-   Genius Results highlight the best answers for a search query and provide immediate access to relevant actions.
-   Content security preserves user access permissions for your searchable content.

See  for more information.

## Activation and other requirements

-   **Activation information**

    AI Search is a ServiceNow AI Platform feature that is active by default.

-   **Browser requirements**

    For optimal performance, use AI Search in the latest release of Google Chrome or Mozilla Firefox. AI Search doesn’t support Internet Explorer.


## Accessibility and localization

-   **Localization information**

    AI Search supports indexing and search in all languages offered by the ServiceNow AI Platform. Search features, such as stop words and synonyms, are available in many supported languages. For details of language support by feature, see .


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/now-platform-admin-rn-landing.md)

## Brazil Patch 2

The Brazil Patch 2 release adds the ability to exclude high-churn fields from indexing.

### What's new

-   **Exclude high-churn fields from indexing**

    Reduce the frequency and duration of indexing operations and improve search performance by excluding frequently updated fields from the index. Excluding these high-churn fields avoids needless reindexing and reduces the size of your index, making search more efficient.


## Brazil Early Availability 2

The Brazil Early Availability 2 release adds the option to display search suggestions and search result titles as links that you can open in new browser tabs, expands hybrid search to support all indexed sources configured for semantic vector indexing, and updates the list of LLMs supported by the Now LLM Service.

### What's new

-   **Display search suggestion links as standard HTML anchors**

    Preserve your search state in portal search and global/workspace search by configuring display of search suggestion links as standard HTML anchors. With this setting configured, you can open search suggestions in new browser tabs using your browser's native right-click or long-press functionality.

-   **Display search result title links as standard HTML anchors**

    Preserve your search state in portal search and global/workspace search by configuring display of search result title links as standard HTML anchors. With this setting configured, you can open search results in new browser tabs using your browser's native right-click or long-press functionality.


### What's changed

-   **Expanded support for hybrid search**

    Hybrid search now supports all indexed sources that have semantic vector indexing configured.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


