---
title: Global search finds records from multiple tables
description: Search multiple record types from a single search field.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2025-02-04"
reading_time_minutes: 4
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Global search finds records from multiple tables

Search multiple record types from a single search field.

To perform a global search, perform one of the following actions based on your UI version.

|UI version|Action|
|----------|------|
|Next Experience UI|Enter your search terms in the Unified Navigation search field, then select **View results** or press Enter.|
|Core UI|Select the search icon in the banner on the upper right of the [System settings for the user interface \(UI\)](https://www.servicenow.com/docs/access?context=r_UI16BannerFrame&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) , then enter your search terms and press Enter.|

All UI versions also have a global search keyboard shortcut. The `ui_global_text_search` UI Macro provides the global search field.

For a list of search source tables that the system searches by default, along with steps for adding new search source tables, see [Default global search sources for Next Experience UI](search-settings-filter-group-table.md#) and [Default global text search groups for Core UI](search-settings-filter-group-table.md#).

Global search supports Boolean operators, quoted phrases, and wildcard characters. For details on these search features, see [Boolean operators allow conditional search results](c_BooleanOperators.md), [Quotation marks allow exact phrase searches](c_PhraseSearches.md), and [Wildcard characters allow searching for patterns and variations](c_Wildcards.md).

-   **[Global search displays a page of matching results](global-search-polaris-ui.md#)**  
Global search displays a page of results that match your search, grouped by table.
-   **[Text search views control format of global search results for tables](text-search-view-formats-results.md)**  
The text\_search view for a table determines how global search displays results from that table.
-   **[Search settings filter and group global search results by table](search-settings-filter-group-table.md#)**  
Global search filters and groups matching results by table. You can configure search sources \(in Next Experience UI\) or search groups to define tables and groups for global search.
-   **[Global search displays exact matching records](exact-matches-global-search.md#)**  
When your search exactly matches the **Number** field value for a record, global search takes you directly to that record, bypassing the search results page.
-   **[Global search displays your most recent search queries and results in Next Experience UI](global-search-recent-queries-results.md)**  
When you select the empty Unified Navigation search field, the system displays lists showing your most recent search queries and your most recently viewed search results. Select a **Recently Searched** query to repeat it, or select a **Recently Viewed** search result record to navigate to it.
-   **[Set global text search properties](../task/set-global-text-search-properties.md)**  
Administrators can control how global text search behaves with system properties.
-   **[Set the preview limit for global or workspace search in Next Experience UI](../task/set-app-preview-limit-polaris-ui.md)**  
Override the default limit of 5 preview results per search source on the Next Experience UI search results page for global or workspace search.
-   **[Hide per-table search result counts in Next Experience UI](../task/hide-result-counts-polaris-ui.md)**  
Suppress display of per-table search result counts in the Next Experience UI search results page.
-   **[Add a workspace application to the Unified Navigation search context menu](../task/add-app-search-context-polaris-ui.md)**  
Enable users to view results for their Unified Navigation searches in workspace applications as well as in global search.
-   **[Global text search suggestions](../reference/r_GlobalTextSearchSuggestions.md)**  
Global text search offers two types of search suggestions.

**Parent Topic:**[Zing text indexing and search engine](c_ZingTextSearch.md)

**Related topics**  


[Features of Zing text indexing and search engine](../reference/features-zing.md)

[Available search options](c_IntroductionToSearching.md)

[Zing generates search results in four phases](c_SearchProcess.md)

[Zing filters search results with access controls](zing-filters-search-results.md)

[Zing computes document scores using three components](c_DocumentScoring.md)

[Zing indexes words](zing-indexes-words.md)

[Zing can include attachments in search results](c_SearchingForAttachments.md)

[Zing removes stop words from queries](stop-words-removed-from-queries.md)

[Zing matches derived words with stemming](stemming-matches-derived-words.md)

[Zing can expand search results with synonyms](search-synonyms-expand-results.md)

[Zing displays search suggestions as users enter search terms](search-suggestions-zing.md)

[Installed with Zing](../reference/installed-with-zing.md)

[Keyboard shortcuts](https://www.servicenow.com/docs/access?context=r_KeyboardShortcuts&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

