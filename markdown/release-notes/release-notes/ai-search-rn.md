---
title: AI Search release notes
description: The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
---

# AI Search release notes

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Australia release.

## AI Search highlights for the Australia release

[Australia Patch 1](../quality/australia-patch-1.md)

-   Provide actionable search and chat responses in global and workspace search with support for Now Assist Multi-Content Response Genius Results.
-   Improve search precision and contextual relevance with hybrid search.
-   Augment the enhanced chat experience by configuring AI Search as the source for Ask Now Assist suggestions.
-   Gain insights into search behavior with a refreshed and updated Search Preview UI.

See [AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/overview-ais.md) for more information.

## New in the Australia release

-   **[Improve search precision and contextual relevance with hybrid search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/hybrid-search-ais.md)**

    Hybrid search combines keyword-based search with semantic understanding to deliver more accurate and relevant search results, with fewer zero-result searches.

-   **[Configure AI Search as the source for Ask Now Assist suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configure-ai-search-source-ask-now-assist-suggestions.md)**

    Admins can configure the system to use AI Search as the source for Ask Now Assist suggestions in enhanced chat. Making this change activates suggestion term highlighting in Ask Now Assist and provides improvements such as wildcard searching and lemmatization for suggestions.


## UI changes

-   **[Show borders between search result cards in portal search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/show-borders-search-result-cards-portal-search.md)**

    By default, AI Search displays no borders between search result cards on the portal search results page. Administrators can enable display of borders between search result cards on the portal search results page by configuring the Faceted Search Service Portal widget.

-   **[Show borders between search result cards in global search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/show-borders-search-result-cards-global-search.md)**

    By default, AI Search displays no borders between search result cards on the global search results page. Administrators can enable display of borders between search result cards on the global search results page by configuring the search result wrapper component for the Unified Navigation app in UI Builder.


## Changed in this release

-   **[Now Assist Multi-Content Response Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/now-assist-multi-content-qna-genius-results.md)**

    If you have Now Assist in AI Search installed, Now Assist Multi-Content Response Genius Results are supported in global and workspace search. Activating Now Assist Multi-Content Response Genius Results in global or workspace search profiles overrides all other Genius Result configurations, so that global and workspace searches only display Genius Result answers from Now Assist Multi-Content Response Genius Results. Virtual Agent topic citations from Now Assist Multi-Content Response Genius Result answers in global or workspace search open the selected topic in the Now Assist panel so the user can continue their conversation on that topic.

-   **[Search Suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-suggestions/search-suggestions-overview.md)**

    Search administrators with the ais\_admin granular admin role can access all Search Suggestions tables. Assign search administrators this role to eliminate needless propagation of full admin access.

-   **[Gain insights into search behavior with a refreshed and updated Search Preview UI.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/search-preview-ui-new.md)**

    Preview search query results using settings from a search application configuration or a search profile. Choose between keyword and hybrid search modes. Display search results as individual EVAM cards or as a JSON-format search query response object, with search and syntax highlighting. Review search query behavior and results and specify search query settings with the new Summary, Genius Results, Details, and Profile admin tools.


## Activation information

AI Search is a ServiceNow AI Platform feature that is active by default.

## Browser requirements

AI Search doesn’t support Internet Explorer.

## Localization information

AI Search supports international languages. For details of language support by feature, see [Internationalization support for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/international-language-support-ais.md).

## Related ServiceNow applications and features

-   **[Advanced AI Search Management Tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/adv-ais-mgmt-tools-content-pack.md)**

    The Advanced AI Search Management Tools application adds new functionality to AI Search. Administrators can review dashboards with metrics, trends, and reports relating to AI Search usage and configuration.

-   **[Now Assist in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/now-assist-ais.md)**

    The Now Assist in AI Search application combines the power of search with the Now LLM Service agentic AI model to answer questions in user searches with actionable AI-generated answers from relevant Knowledge articles.

-   **[External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/ext-cont-connectors-landing-page.md)**

    The External Content Connectors ServiceNow Store application enables AI Search applications to search content and metadata from supported external source systems, including Atlassian Confluence Cloud, Atlassian Jira, Google Drive, Microsoft SharePoint Online, Microsoft Teams, Salesforce Slack, ServiceNow product documentation, and public websites supported by the predefined web sources external content connector.


**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

