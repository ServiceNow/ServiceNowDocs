---
title: Combined AI Search release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for AI Search from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-aisearch-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined AI Search release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for AI Search from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family AI Search release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading AI Search to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

[Xanadu Patch 3](https://www.servicenow.com/docs/access?context=xanadu-patch-3&family=xanadu&ft:locale=en-US):

-   After you upgrade to Xanadu Patch 3 from an earlier release, make knowledge block content searchable by reindexing all your indexed sources that include knowledge articles. For details on reindexing, see [Index or reindex an indexed source](https://www.servicenow.com/docs/access?context=index-single-source-ais&family=xanadu&ft:locale=en-US) or [Index or reindex multiple indexed sources](https://www.servicenow.com/docs/access?context=index-multiple-sources-ais&family=xanadu&ft:locale=en-US).

 Xanadu:

 After you upgrade to Xanadu from an earlier release, perform the following steps to add the Dashboards, data visualizations, and KPIs navigation tabs to global search results in AI Search for Next Experience:

1.  Update the AI Search for Next Experience ServiceNow Store application to version 4 or later. For update instructions, see [Update an application](https://www.servicenow.com/docs/access?context=t_InstallUpdates&family=xanadu&ft:locale=en-US).
2.  Commit the update set provided in the [AI Search for Next Experience 4.0 PAR tables update sets \(KB1644544\)](https://support.servicenow.com/kb_view.do?sysparm_article=KB1644544) article in the Now Support Knowledge Base. To learn more about update sets, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for AI Search.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **\([Xanadu Patch 9](https://www.servicenow.com/docs/access?context=xanadu-patch-9&family=xanadu&ft:locale=en-US)\) [Improve semantic search with third-party embedding models](https://www.servicenow.com/docs/access?context=ais-rag&family=xanadu&ft:locale=en-US)**

Use custom and third-party embedding models supported by the AI Search RAG application to generate more accurate and relevant semantic search results.


-   **\([Xanadu Patch 3](https://www.servicenow.com/docs/access?context=xanadu-patch-3&family=xanadu&ft:locale=en-US)\) [Knowledge block content indexing](https://www.servicenow.com/docs/access?context=index-single-source-ais&family=xanadu&ft:locale=en-US)**

When you index knowledge articles for search, AI Search now includes content from knowledge blocks to improve search recall.

-   **[NLQ Genius Results support searching for multiple CMDB tables](https://www.servicenow.com/docs/access?context=genius-result-nlq-ais&family=xanadu&ft:locale=en-US)**

When your search includes terms that could match multiple CMDB tables, NLQ Genius Result answers display a drop-down list of potential CMDB table matches for each affected term. Use these drop-down lists to select the CMDB tables that you want to surface information for.

-   **[Middle dot support for Japanese](https://www.servicenow.com/docs/access?context=international-language-support-ais&family=xanadu&ft:locale=en-US)**

Increase search precision for Japanese phrases that include nakaguro \(中黒, middle dot\) characters. When indexing Japanese text or searching in Japanese, AI Search preserves individual terms separated by a nakaguro instead of merging them into a single term.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Improve semantic search with third-party embedding models](https://www.servicenow.com/docs/access?context=ais-rag&family=yokohama&ft:locale=en-US)**

Use custom and third-party embedding models supported by the AI Search RAG application to generate more accurate and relevant semantic search results.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Improve search precision and contextual relevance with hybrid search](https://www.servicenow.com/docs/access?context=hybrid-search-ais&family=zurich&ft:locale=en-US)**

Beginning with Now Assist in AI Search 15.0, customers with Now Assist in AI Search installed can enable the new hybrid search mode. Hybrid search combines keyword-based search with semantic understanding to deliver more accurate and relevant search results, with fewer zero-result searches.


</td></tr><tr><td>

Australia

</td><td>

-   **[Improve search precision and contextual relevance with hybrid search](https://www.servicenow.com/docs/access?context=hybrid-search-ais&family=australia&ft:locale=en-US)**

Beginning with Now Assist in AI Search 15.0, administrators on instances with Now Assist in AI Search installed can enable the new hybrid search mode. Hybrid search combines keyword-based search with semantic understanding to deliver more accurate and relevant search results, with fewer zero-result searches.

-   **[Configure AI Search as the source for Ask ServiceNow Otto suggestions](https://www.servicenow.com/docs/access?context=configure-ai-search-source-ask-now-assist-suggestions&family=australia&ft:locale=en-US)**

Admins can configure the system to use AI Search as the source for Ask Now Assist suggestions in enhanced chat. Making this change activates suggestion term highlighting in Ask Now Assist and provides improvements such as wildcard searching and lemmatization for suggestions.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing AI Search features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Facets display refinement filters in the search user's language](https://www.servicenow.com/docs/access?context=create-facet-ais&family=xanadu&ft:locale=en-US)**

When displaying reference field values as facet refinement filters, AI Search uses field value translations for the search user's language if available. If no translations are available for the user's language, AI Search uses translations for the system language.

-   **[Late binding security implementation preserves correct click rank search signals](https://www.servicenow.com/docs/access?context=content-security-ais&family=xanadu&ft:locale=en-US)**

When late binding security removes inaccessible results, click rank search signals correctly reflect the final result ordering.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Consumer-grade search experience for search portals](https://www.servicenow.com/docs/access?context=viewing-search-results-ais&family=yokohama&ft:locale=en-US)**

The search results page for search portals has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. Search terms are no longer highlighted in search results.

-   **[Consumer-grade search experience for global search and workspace search](https://www.servicenow.com/docs/access?context=using-ais-next-experience-app&family=yokohama&ft:locale=en-US)**

The search results page for global search and workspace search has been revised to offer a more intuitive and consistent experience. Navigation tabs have been replaced with source facet buckets. All search results now open in a new browser tab, preserving your search in the existing browser tab. Facet buckets now show minimum search result counts, reflecting results removed by late binding content security. A new **glide.ui.ais.show\_all\_facets** system property enables you to display facets from all sources when no source is selected. \(The default behavior is to hide facets until a source is selected.\) Search terms are no longer highlighted in search results.

-   **[Sort facet buckets alphabetically](https://www.servicenow.com/docs/access?context=create-facet-ais&family=yokohama&ft:locale=en-US)**

Override the default sorting of facet buckets by their search result counts and display them sorted alphabetically by their labels.

-   **[Improved display for grouped attachment search results](https://www.servicenow.com/docs/access?context=grouping-attachment-srch-results-ais&family=yokohama&ft:locale=en-US)**

When grouped with their parent search results, attachment search results now appear in collapsed form to save space. If a parent search result includes more than three grouped attachments, you can use the new **Show more** and **Show less** links to control how many attachments are visible.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Summary Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&family=zurich&ft:locale=en-US)**

If you have Now Assist in AI Search installed, Now Assist Multi-Content Response Genius Results are supported in global and workspace search. Activating Now Assist Multi-Content Response Genius Results in global or workspace search profiles overrides all other Genius Result configurations, so that global and workspace searches only display Genius Result answers from Now Assist Multi-Content Response Genius Results. Virtual Agent topic citations from Now Assist Multi-Content Response Genius Result answers in global or workspace search open the selected topic in the Now Assist panel so the user can continue their conversation on that topic.

-   **[Search Suggestions](https://www.servicenow.com/docs/access?context=search-suggestions-overview&family=zurich&ft:locale=en-US)**

Search administrators with the ais\_admin granular admin role can access all Search Suggestions tables. Assign search administrators this role to eliminate needless propagation of full admin access.

-   **[Gain insights into search behavior with a refreshed and updated Search Preview UI.](https://www.servicenow.com/docs/access?context=search-preview-ui-new&family=zurich&ft:locale=en-US)**

Preview search query results using settings from a search application configuration or a search profile. Choose between keyword and hybrid search modes. Display search results as individual EVAM cards or as a JSON-format search query response object, with search and syntax highlighting. Review search query behavior and results and specify search query settings with the new Summary, Genius Results, Details, and Profile admin tools.


</td></tr><tr><td>

Australia

</td><td>

-   **[Summary Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&family=australia&ft:locale=en-US)**

If you have Now Assist in AI Search installed, Now Assist Multi-Content Response Genius Results are supported in global and workspace search. Activating Now Assist Multi-Content Response Genius Results in global or workspace search profiles overrides all other Genius Result configurations, so that global and workspace searches only display Genius Result answers from Now Assist Multi-Content Response Genius Results. Virtual Agent topic citations from Now Assist Multi-Content Response Genius Result answers in global or workspace search open the selected topic in the Now Assist panel so the user can continue their conversation on that topic.

-   **[Search Suggestions](https://www.servicenow.com/docs/access?context=search-suggestions-overview&family=australia&ft:locale=en-US)**

Search administrators with the ais\_admin granular admin role can access all Search Suggestions tables. Assign search administrators this role to eliminate needless propagation of full admin access.

-   **[Gain insights into search behavior with a refreshed and updated Search Preview UI.](https://www.servicenow.com/docs/access?context=search-preview-ui-new&family=australia&ft:locale=en-US)**

Preview search query results using settings from a search application configuration or a search profile. Choose between keyword and hybrid search modes. Display search results as individual EVAM cards or as a JSON-format search query response object, with search and syntax highlighting. Review search query behavior and results and specify search query settings with the new Summary, Genius Results, Details, and Profile admin tools.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some AI Search features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some AI Search features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Starting with the Now Assist in AI Search 8.0 release, the External Content Q&amp;A Genius Results feature is being prepared for future deprecation. It will continue to be supported until it is deprecated. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Yokohama

</td><td>

Starting with the Now Assist in AI Search 8.0 release, the External Content Q&amp;A Genius Results feature is being prepared for future deprecation. It will continue to be supported until it is deprecated. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate AI Search.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

AI Search is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Activation information**

AI Search is a ServiceNow AI Platform feature that is active by default.


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

AI Search is a ServiceNow AI Platform feature that is active by default.


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

AI Search is a ServiceNow AI Platform feature that is active by default.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for AI Search we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for AI Search we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

AI Search doesn’t support Internet Explorer.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Browser requirements**

For optimal performance, use AI Search in the latest release of Google Chrome or Mozilla Firefox. AI Search doesn’t support Internet Explorer.


</td></tr><tr><td>

Zurich

</td><td>

-   **Browser requirements**

For optimal performance, use AI Search in the latest release of Google Chrome or Mozilla Firefox. AI Search doesn’t support Internet Explorer.


</td></tr><tr><td>

Australia

</td><td>

-   **Browser requirements**

For optimal performance, use AI Search in the latest release of Google Chrome or Mozilla Firefox. AI Search doesn’t support Internet Explorer.


</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for AI Search, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for AI Search we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

AI Search supports international languages. For details of language support by feature, see [Internationalization support](https://www.servicenow.com/docs/access?context=international-language-support-ais&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   **Localization information**

AI Search supports indexing and search in all languages offered by the ServiceNow AI Platform. Search features, such as stop words and synonyms, are available in many supported languages. For details of language support by feature, see [Internationalization support](https://www.servicenow.com/docs/access?context=international-language-support-ais&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Localization information**

AI Search supports indexing and search in all languages offered by the ServiceNow AI Platform. Search features, such as stop words and synonyms, are available in many supported languages. For details of language support by feature, see [Internationalization support](https://www.servicenow.com/docs/access?context=international-language-support-ais&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Localization information**

AI Search supports indexing and search in all languages offered by the ServiceNow AI Platform. Search features, such as stop words and synonyms, are available in many supported languages. For details of language support by feature, see [Internationalization support](https://www.servicenow.com/docs/access?context=international-language-support-ais&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for AI Search we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

[Xanadu Patch 3](https://www.servicenow.com/docs/access?context=xanadu-patch-3&family=xanadu&ft:locale=en-US):

-   Expand search recall by indexing content from knowledge blocks.

 Xanadu:

-   Surface information across multiple CMDB tables with NLQ Genius Results.
-   Increase search precision for Japanese phrases that include nakaguro \(中黒, middle dot\) characters.
-   Scroll through multiple Genius Result answer cards in a carousel to select the most actionable answer for your question.

 See [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Index and search text and attachments from ServiceNow AI Platform tables and external document repositories.
-   Machine learning relevancy intelligently tunes search result relevancy scores based on previous search users' selections.
-   Semantic vector search and hybrid search modes find results that match the intent and context of your search.
-   Genius Results highlight the best answers for a search query and provide immediate access to relevant actions.
-   Content security preserves user access permissions for your searchable content.

 See [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Index and search text and attachments from ServiceNow AI Platform tables and external document repositories.
-   Machine learning relevancy intelligently tunes search result relevancy scores based on previous search users' selections.
-   Semantic vector search and hybrid search modes find results that match the intent and context of your search.
-   Genius Results highlight the best answers for a search query and provide immediate access to relevant actions.
-   Content security preserves user access permissions for your searchable content.

 See [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Index and search text and attachments from ServiceNow AI Platform tables and external document repositories.
-   Machine learning relevancy intelligently tunes search result relevancy scores based on previous search users' selections.
-   Semantic vector search and hybrid search modes find results that match the intent and context of your search.
-   Genius Results highlight the best answers for a search query and provide immediate access to relevant actions.
-   Content security preserves user access permissions for your searchable content.

 See [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

