---
title: AI Search release notes
description: The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. See the following sections for release notes by version.The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Zurich release.The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Zurich release.The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Zurich release.The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Zurich release.The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2026-09-03"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI]
---

# AI Search release notes

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. See the following sections for release notes by version.

## About AI Search

-   Index and search text and attachments from ServiceNow AI Platform tables and external document repositories.
-   Machine learning relevancy intelligently tunes search result relevancy scores based on previous search users' selections.
-   Semantic vector search and hybrid search modes find results that match the intent and context of your search.
-   Genius Results highlight the best answers for a search query and provide immediate access to relevant actions.
-   Content security preserves user access permissions for your searchable content.

See [AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/overview-ais.md) for more information.

## Activation and other requirements

-   **Activation information**

    AI Search is a ServiceNow AI Platform feature that is active by default.

-   **Browser requirements**

    For optimal performance, use AI Search in the latest release of Google Chrome or Mozilla Firefox. AI Search doesn’t support Internet Explorer.


## Accessibility and localization

-   **Localization information**

    AI Search supports indexing and search in all languages offered by the ServiceNow AI Platform. Search features, such as stop words and synonyms, are available in many supported languages. For details of language support by feature, see [Internationalization support for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/international-language-support-ais.md).


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-platform-admin-rn-landing.md)

## August 2026

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Zurich release.

### What's new

-   **[ServiceNow Otto for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-ais.md)**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows. Name changes include but aren't limited to:

    -   Now Assist in AI Search is now ServiceNow Otto for AI Search.
    -   Now Assist Actions is now Actions.
    -   Now Assist Q &amp; A is now Knowledge base articles.
    -   Now Assist Multi Content Response is now Summary.

## July 2026

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Zurich release.

### What's new

-   **[Generate multi-content synthesized responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/generate-multi-content-synthesized-sources.md)**

    AI Search can now use multi-source synthesis to gather and combine information from any indexed source in your system.


## December 2025

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Zurich release.

### What's new

-   **[Improve search precision and contextual relevance with hybrid search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/hybrid-search-ais.md)**

    Beginning with Now Assist in AI Search 15.0, customers with Now Assist in AI Search installed can enable the new hybrid search mode. Hybrid search combines keyword-based search with semantic understanding to deliver more accurate and relevant search results, with fewer zero-result searches.


### What's changed

-   **[Summary Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-multi-content-qna-genius-results.md)**

    If you have Now Assist in AI Search installed, Now Assist Multi-Content Response Genius Results are supported in global and workspace search. Activating Now Assist Multi-Content Response Genius Results in global or workspace search profiles overrides all other Genius Result configurations, so that global and workspace searches only display Genius Result answers from Now Assist Multi-Content Response Genius Results. Virtual Agent topic citations from Now Assist Multi-Content Response Genius Result answers in global or workspace search open the selected topic in the Now Assist panel so the user can continue their conversation on that topic.

-   **[Search Suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/search-suggestions-overview.md)**

    Search administrators with the ais\_admin granular admin role can access all Search Suggestions tables. Assign search administrators this role to eliminate needless propagation of full admin access.

-   **[Gain insights into search behavior with a refreshed and updated Search Preview UI.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/search-preview-ui-new.md)**

    Preview search query results using settings from a search application configuration or a search profile. Choose between keyword and hybrid search modes. Display search results as individual EVAM cards or as a JSON-format search query response object, with search and syntax highlighting. Review search query behavior and results and specify search query settings with the new Summary, Genius Results, Details, and Profile admin tools.


## Zurich General Availability

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Zurich release.

### What's new

-   **[Improve semantic search with third-party embedding models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ais-rag.md)**

    Use custom and third-party embedding models supported by the AI Search RAG application to generate more accurate and relevant semantic search results.


### What's changed

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


-   **[Consumer-grade search experience for search portals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/viewing-search-results-ais.md)**

    The search results page for search portals has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. Search terms are no longer highlighted in search results.

-   **[Consumer-grade search experience for global search and workspace search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/using-ais-next-experience-app.md)**

    The search results page for global search and workspace search has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. A new **glide.ui.ais.show\_all\_facets** system property enables you to display facets from all sources when no source is selected. \(The default behavior is to hide facets until a source is selected.\) Search terms are no longer highlighted in search results.

-   **[Sort facet buckets alphabetically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-facet-ais.md)**

    Override the default sorting of facet buckets by their search result counts and display them sorted alphabetically by their labels.

-   **Improved display for grouped attachment search results**

    When grouped with their parent search results, attachment search results now appear in collapsed form to save space. If a parent search result includes more than three grouped attachments, you can use the new **Show more** and **Show less** links to control how many attachments are visible.


## Zurich Early Availability

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Zurich release.

### What's new

-   **[Filter external content search results by language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/language-filtering-external-content.md)**

    AI Search filters external content search results, displaying only results that contain content in languages relevant for the user's search. These languages include:

    -   The search user's session language
    -   The fallback language for the user's session language \(if configured\)
    -   The language of the global fallback locale \(if configured\)
-   **[Indexing support for variables in records on Catalog Item and child tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/variable-types-ais-index.md)**

    Index searchable content from Multiple Choice and Select Box variables in records on the Catalog Item table and tables that extend it.

-   **[New display properties for Search Result EVAM cards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/search-result-evam-card-opts.md)**

    Search Result EVAM cards include new **customIcon**, **customIconSize**, **forceNewTab**, and **useAttachmentViewer** properties that you can use to modify display settings and behavior for search results.


