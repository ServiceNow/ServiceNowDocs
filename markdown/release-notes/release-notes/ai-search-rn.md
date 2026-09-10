---
title: AI Search release notes
description: The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. See the following sections for release notes by version.The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Yokohama release.The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Yokohama release.The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Yokohama release.The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Yokohama release.The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2026-09-03"
reading_time_minutes: 6
---

# AI Search release notes

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. See the following sections for release notes by version.

## About AI Search

-   Index and search text and attachments from ServiceNow AI Platform tables and external document repositories.
-   Machine learning relevancy intelligently tunes search result relevancy scores based on previous search users' selections.
-   Semantic vector search and hybrid search modes find results that match the intent and context of your search.
-   Genius Results highlight the best answers for a search query and provide immediate access to relevant actions.
-   Content security preserves user access permissions for your searchable content.

See [AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/overview-ais.md) for more information.

## Activation and other requirements

-   **Activation information**

    AI Search is a ServiceNow AI Platform feature that is active by default.

-   **Browser requirements**

    For optimal performance, use AI Search in the latest release of Google Chrome or Mozilla Firefox. AI Search doesn’t support Internet Explorer.


## Accessibility and localization

-   **Localization information**

    AI Search supports indexing and search in all languages offered by the ServiceNow AI Platform. Search features, such as stop words and synonyms, are available in many supported languages. For details of language support by feature, see [Internationalization support for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/international-language-support-ais.md).


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-admin-rn-landing.md)

## January 2026

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Yokohama release.

### What's new

-   **[Improve search precision and contextual relevance with hybrid search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/hybrid-search-ais.md)**

    Beginning with Now Assist in AI Search 15.0, customers with Now Assist in AI Search installed can enable the new hybrid search mode. Hybrid search combines keyword-based search with semantic understanding to deliver more accurate and relevant search results, with fewer zero-result searches.


### What's changed

-   **[Now Assist Multi-Content Response Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/now-assist-multi-content-qna-genius-results.md)**

    If you have Now Assist in AI Search installed, Now Assist Multi-Content Response Genius Results are supported in global and workspace search. Activating Now Assist Multi-Content Response Genius Results in global or workspace search profiles overrides all other Genius Result configurations, so that global and workspace searches only display Genius Result answers from Now Assist Multi-Content Response Genius Results. Virtual Agent topic citations from Now Assist Multi-Content Response Genius Result answers in global or workspace search open the selected topic in the Now Assist panel so the user can continue their conversation on that topic.

-   **[Search Suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/search-suggestions-overview.md)**

    Search administrators with the ais\_admin granular admin role can access all Search Suggestions tables. Assign search administrators this role to eliminate needless propagation of full admin access.

-   **[Gain insights into search behavior with a refreshed and updated Search Preview UI.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/search-preview-ui-new.md)**

    Preview search query results using settings from a search application configuration or a search profile. Choose between keyword and hybrid search modes. Display search results as individual EVAM cards or as a JSON-format search query response object, with search and syntax highlighting. Review search query behavior and results and specify search query settings with the new Summary, Genius Results, Details, and Profile admin tools.


## August 2025

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Yokohama release.

### What's changed

-   **[Consumer-grade search experience for search portals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/viewing-search-results-ais.md)**

    The search results page for search portals has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. Search terms are no longer highlighted in search results.

-   **[Consumer-grade search experience for global search and workspace search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/using-ais-next-experience-app.md)**

    The search results page for global search and workspace search has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. A new **glide.ui.ais.show\_all\_facets** system property enables you to display facets from all sources when no source is selected. \(The default behavior is to hide facets until a source is selected.\) Search terms are no longer highlighted in search results.

-   **[Sort facet buckets alphabetically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/create-facet-ais.md)**

    Override the default sorting of facet buckets by their search result counts and display them sorted alphabetically by their labels.

-   **[Improved display for grouped attachment search results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/grouping-attachment-srch-results-ais.md)**

    When grouped with their parent search results, attachment search results now appear in collapsed form to save space. If a parent search result includes more than three grouped attachments, you can use the new **Show more** and **Show less** links to control how many attachments are visible.


## May 2025

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Yokohama release.

### What's new

-   **[Improve semantic search with third-party embedding models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ais-rag.md)**

    Use custom and third-party embedding models supported by the AI Search RAG application to generate more accurate and relevant semantic search results.


## Yokohama General Availability

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Yokohama release.

### What's new

-   **[Limit the number of Task and Alert records indexed with indexed source guardrails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/indexed-source-guardrails-ais.md)**

    Index guardrail settings restrict index size and increase search performance by limiting the number of Task and Alert table records indexed for search.

-   **[Exclude search sources in a search profile from search result or Genius Result generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/genius-results-ais.md)**

    Tune your search results by configuring search source exclusion settings in your search profiles. You can exclude a search source from being used to generate regular search results, Genius Result answers, or both. When excluding a search source's records from Genius Result answer generation, you can also choose to exclude its attachments.

-   **[Knowledge block content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/exclude-know-blocks-ais-index.md)**

    When you index knowledge articles for search, AI Search now includes content from knowledge blocks to improve search recall. Administrators can disable indexing of knowledge block content if desired.

-   **[Boost relevancy for search results that match synonyms from a synonym dictionary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/boost-results-ais.md)**

    Define synonyms in a synonym dictionary and configure a result improvement rule to apply relevancy boosts \(positive or negative\) to search results that match any of those synonyms.

-   **[Customize semantic indexing settings for indexed sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/semantic-index-cfg-ais.md)**

    Customize semantic indexing settings for your indexed sources.

-   **[Fuzzy numeric search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/fuzzy-numeric-search.md)**

    Find records by their Number using numeric search terms like `23583`, with no need to match alphabetical prefixes or leading zeroes.


## Yokohama

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Yokohama release.

### What's deprecated or removed

Starting with the Now Assist in AI Search 8.0 release, the External Content Q&amp;A Genius Results feature is being prepared for future deprecation. It will continue to be supported until it is deprecated. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

