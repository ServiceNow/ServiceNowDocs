---
title: AI Search release notes
description: The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-02-06"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
---

# AI Search release notes

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Zurich release.

## AI Search highlights for the Zurich release

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Improve search precision and contextual relevance with hybrid search, available for customers with Now Assist in AI Search installed.
-   Gain insights into search behavior with a refreshed and updated Search Preview UI.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Search more intuitively with an updated, consumer-grade user experience in search portals, global search, and workspace search.

[Zurich Early Availability](../quality/zurich-security-notables.md)

-   Improve search precision by displaying external content search results in languages configured for the user's search session.
-   Increase search recall by indexing searchable content and metadata from Multiple Choice and Select Box variables in records on the Catalog Item table and its child tables.

See [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

## Important information for upgrading AI Search to Zurich

After you upgrade to Zurich from an earlier family release, run full document crawls in all your external content connectors to update their semantic vector indexing field mappings.

## New in the Zurich release

-   **[Improve search precision and contextual relevance with hybrid search](https://www.servicenow.com/docs/access?context=hybrid-search-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Beginning with Now Assist in AI Search 15.0, customers with Now Assist in AI Search installed can enable the new hybrid search mode. Hybrid search combines keyword-based search with semantic understanding to deliver more accurate and relevant search results, with fewer zero-result searches.


-   **[Improve semantic search with third-party embedding models](https://www.servicenow.com/docs/access?context=ais-rag&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Use custom and third-party embedding models supported by the AI Search RAG application to generate more accurate and relevant semantic search results.


-   **[Filter external content search results by language](https://www.servicenow.com/docs/access?context=language-filtering-external-content&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    AI Search filters external content search results, displaying only results that contain content in languages relevant for the user's search. These languages include:

    -   The search user's session language
    -   The fallback language for the user's session language \(if configured\)
    -   The language of the global fallback locale \(if configured\)
-   **[Indexing support for variables in records on Catalog Item and child tables](https://www.servicenow.com/docs/access?context=variable-types-ais-index&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Index searchable content from Multiple Choice and Select Box variables in records on the Catalog Item table and tables that extend it.

-   **[New display properties for Search Result EVAM cards](https://www.servicenow.com/docs/access?context=search-result-evam-card-opts&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Search Result EVAM cards include new **customIcon**, **customIconSize**, **forceNewTab**, and **useAttachmentViewer** properties that you can use to modify display settings and behavior for search results.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    If you have Now Assist in AI Search installed, Now Assist Multi-Content Response Genius Results are supported in global and workspace search. Activating Now Assist Multi-Content Response Genius Results in global or workspace search profiles overrides all other Genius Result configurations, so that global and workspace searches only display Genius Result answers from Now Assist Multi-Content Response Genius Results. Virtual Agent topic citations from Now Assist Multi-Content Response Genius Result answers in global or workspace search open the selected topic in the Now Assist panel so the user can continue their conversation on that topic.

-   **[Search Suggestions](https://www.servicenow.com/docs/access?context=search-suggestions-overview&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Search administrators with the ais\_admin granular admin role can access all Search Suggestions tables. Assign search administrators this role to eliminate needless propagation of full admin access.

-   **[Gain insights into search behavior with a refreshed and updated Search Preview UI.](https://www.servicenow.com/docs/access?context=search-preview-ui-new&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Preview search query results using settings from a search application configuration or a search profile. Choose between keyword and hybrid search modes. Display search results as individual EVAM cards or as a JSON-format search query response object, with search and syntax highlighting. Review search query behavior and results and specify search query settings with the new Summary, Genius Results, Details, and Profile admin tools.


-   **[Consumer-grade search experience for search portals](https://www.servicenow.com/docs/access?context=viewing-search-results-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    The search results page for search portals has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. Search terms are no longer highlighted in search results.

-   **[Consumer-grade search experience for global search and workspace search](https://www.servicenow.com/docs/access?context=using-ais-next-experience-app&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    The search results page for global search and workspace search has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. A new **glide.ui.ais.show\_all\_facets** system property enables you to display facets from all sources when no source is selected. \(The default behavior is to hide facets until a source is selected.\) Search terms are no longer highlighted in search results.

-   **[Sort facet buckets alphabetically](https://www.servicenow.com/docs/access?context=create-facet-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Override the default sorting of facet buckets by their search result counts and display them sorted alphabetically by their labels.

-   **[Improved display for grouped attachment search results](https://www.servicenow.com/docs/access?context=grouping-attachment-srch-results-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    When grouped with their parent search results, attachment search results now appear in collapsed form to save space. If a parent search result includes more than three grouped attachments, you can use the new **Show more** and **Show less** links to control how many attachments are visible.


## Activation information

AI Search is a ServiceNow AI Platform feature that is active by default.

## Browser requirements

AI Search doesn’t support Internet Explorer.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Localization information

AI Search supports international languages. For details of language support by feature, see [Internationalization support for AI Search](https://www.servicenow.com/docs/access?context=international-language-support-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Advanced AI Search Management Tools](https://www.servicenow.com/docs/access?context=adv-ais-mgmt-tools-content-pack&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    The Advanced AI Search Management Tools application adds new functionality to AI Search. Administrators can review dashboards with metrics, trends, and reports relating to AI Search usage and configuration.

-   **[Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    The Now Assist in AI Search application combines the power of search with the Now LLM Service agentic AI model to answer questions in user searches with actionable AI-generated answers from relevant Knowledge articles.

-   **[External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    The External Content Connectors ServiceNow Store application enables AI Search applications to search content and metadata from supported external source systems, including Atlassian Confluence Cloud, Atlassian Jira, Google Drive, Microsoft SharePoint Online, Microsoft Teams, Salesforce Slack, ServiceNow product documentation, and public websites supported by the predefined web sources external content connector.


**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

