---
title: AI Search release notes
description: The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-02-06"
reading_time_minutes: 6
---

# AI Search release notes

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Yokohama release.

## AI Search highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Improve search precision and contextual relevance with hybrid search, available for customers with Now Assist in AI Search installed.
-   Gain insights into search behavior with a refreshed and updated Search Preview UI.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Search more intuitively with an updated, consumer-grade user experience in search portals, global search, and workspace search.

[Yokohama Early Availability](../quality/yokohama-security-notables.md)

-   Restrict index size and increase search performance with guardrails that limit the number of Task and Alert table records indexed for search
-   Customize the semantic vector search experience by configuring semantic indexing settings for your indexed sources
-   Improve the focus of search results by excluding search sources in a search profile from being used to generate search results or Genius Result answers
-   Expand search recall by indexing content from knowledge blocks
-   Highlight important search results by boosting relevancy for results that match synonyms in a synonym dictionary

See [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

## Important information for upgrading AI Search to Yokohama

When you upgrade to Yokohama from an earlier release, make knowledge block content searchable by reindexing all your indexed sources that include knowledge articles. For details on reindexing, see [Perform a full table index or reindex for a single AI Search indexed source](https://www.servicenow.com/docs/access?context=index-single-source-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) or [Perform a full table index or reindex for multiple AI Search indexed sources](https://www.servicenow.com/docs/access?context=index-multiple-sources-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## New in the Yokohama release

-   **[Improve search precision and contextual relevance with hybrid search](https://www.servicenow.com/docs/access?context=hybrid-search-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Beginning with Now Assist in AI Search 15.0, customers with Now Assist in AI Search installed can enable the new hybrid search mode. Hybrid search combines keyword-based search with semantic understanding to deliver more accurate and relevant search results, with fewer zero-result searches.


-   **[Improve semantic search with third-party embedding models](https://www.servicenow.com/docs/access?context=ais-rag&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Use custom and third-party embedding models supported by the AI Search RAG application to generate more accurate and relevant semantic search results.


-   **[Limit the number of Task and Alert records indexed with indexed source guardrails](https://www.servicenow.com/docs/access?context=indexed-source-guardrails-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Index guardrail settings restrict index size and increase search performance by limiting the number of Task and Alert table records indexed for search.

-   **[Exclude search sources in a search profile from search result or Genius Result generation](https://www.servicenow.com/docs/access?context=genius-results-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Tune your search results by configuring search source exclusion settings in your search profiles. You can exclude a search source from being used to generate regular search results, Genius Result answers, or both. When excluding a search source's records from Genius Result answer generation, you can also choose to exclude its attachments.

-   **[Knowledge block content indexing](https://www.servicenow.com/docs/access?context=exclude-know-blocks-ais-index&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    When you index knowledge articles for search, AI Search now includes content from knowledge blocks to improve search recall. Administrators can disable indexing of knowledge block content if desired.

-   **[Boost relevancy for search results that match synonyms from a synonym dictionary](https://www.servicenow.com/docs/access?context=boost-results-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Define synonyms in a synonym dictionary and configure a result improvement rule to apply relevancy boosts \(positive or negative\) to search results that match any of those synonyms.

-   **[Customize semantic indexing settings for indexed sources](https://www.servicenow.com/docs/access?context=semantic-index-cfg-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Customize semantic indexing settings for your indexed sources.

-   **[Fuzzy numeric search](https://www.servicenow.com/docs/access?context=fuzzy-numeric-search&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Find records by their Number using numeric search terms like `23583`, with no need to match alphabetical prefixes or leading zeroes.


## Changed in this release

-   **[Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    If you have Now Assist in AI Search installed, Now Assist Multi-Content Response Genius Results are supported in global and workspace search. Activating Now Assist Multi-Content Response Genius Results in global or workspace search profiles overrides all other Genius Result configurations, so that global and workspace searches only display Genius Result answers from Now Assist Multi-Content Response Genius Results. Virtual Agent topic citations from Now Assist Multi-Content Response Genius Result answers in global or workspace search open the selected topic in the Now Assist panel so the user can continue their conversation on that topic.

-   **[Search Suggestions](https://www.servicenow.com/docs/access?context=search-suggestions-overview&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Search administrators with the ais\_admin granular admin role can access all Search Suggestions tables. Assign search administrators this role to eliminate needless propagation of full admin access.

-   **[Gain insights into search behavior with a refreshed and updated Search Preview UI.](https://www.servicenow.com/docs/access?context=search-preview-ui-new&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Preview search query results using settings from a search application configuration or a search profile. Choose between keyword and hybrid search modes. Display search results as individual EVAM cards or as a JSON-format search query response object, with search and syntax highlighting. Review search query behavior and results and specify search query settings with the new Summary, Genius Results, Details, and Profile admin tools.


-   **[Consumer-grade search experience for search portals](https://www.servicenow.com/docs/access?context=viewing-search-results-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The search results page for search portals has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. Search terms are no longer highlighted in search results.

-   **[Consumer-grade search experience for global search and workspace search](https://www.servicenow.com/docs/access?context=using-ais-next-experience-app&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The search results page for global search and workspace search has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. A new **glide.ui.ais.show\_all\_facets** system property enables you to display facets from all sources when no source is selected. \(The default behavior is to hide facets until a source is selected.\) Search terms are no longer highlighted in search results.

-   **[Sort facet buckets alphabetically](https://www.servicenow.com/docs/access?context=create-facet-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Override the default sorting of facet buckets by their search result counts and display them sorted alphabetically by their labels.

-   **[Improved display for grouped attachment search results](https://www.servicenow.com/docs/access?context=grouping-attachment-srch-results-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    When grouped with their parent search results, attachment search results now appear in collapsed form to save space. If a parent search result includes more than three grouped attachments, you can use the new **Show more** and **Show less** links to control how many attachments are visible.


## Deprecations

Starting with the Now Assist in AI Search 8.0 release, the External Content Q&amp;A Genius Results feature is being prepared for future deprecation. It will continue to be supported until it is deprecated. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

AI Search is a ServiceNow AI Platform feature that is active by default.

## Browser requirements

AI Search doesn’t support Internet Explorer.

## Localization information

AI Search supports international languages. For details of language support by feature, see [Internationalization support for AI Search](https://www.servicenow.com/docs/access?context=international-language-support-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Advanced AI Search Management Tools](https://www.servicenow.com/docs/access?context=adv-ais-mgmt-tools-content-pack&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The Advanced AI Search Management Tools application adds new functionality to AI Search. Administrators can review dashboards with metrics, trends, and reports relating to AI Search usage and configuration.

-   **[Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The Now Assist in AI Search application combines the power of search with the Now LLM Service agentic AI model to answer questions in user searches with actionable AI-generated answers from relevant Knowledge articles.

-   **[Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Administrators can activate the ServiceNow® Knowledge Management Advanced plugin to install the FAQ \[kb\_template\_faq\] table. AI Search can return records in this table as Q&amp;A Genius Result answers for common user search questions.

-   **[AI Search Admin console](https://www.servicenow.com/docs/access?context=ais-admin-console&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The AI Search Admin console is a powerful tool designed to help AI Search administrators manage, monitor, and optimize the search experience of their configured search applications.


**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

