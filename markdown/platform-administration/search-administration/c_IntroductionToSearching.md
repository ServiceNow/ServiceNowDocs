---
title: Available search options
description: Zing offers users several search interfaces and search operators to conduct text searches.
locale: en-US
release: zurich
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer]
---

# Available search options

Zing offers users several search interfaces and search operators to conduct text searches.

|Search interface|Description|
|----------------|-----------|
|[Global search](c_GlobalTextSearch.md)|Find records in multiple tables using the global search field in the [Next Experience Unified Navigation](https://www.servicenow.com/docs/access?context=using-the-next-experience-global-header&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).|
|[Search a list](https://www.servicenow.com/docs/access?context=t_SearchAList&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)|Find records in a list; search in a specific field \(Go to\), all fields \(Search\), or in a specific column.|
|[Knowledge Base](https://www.servicenow.com/docs/access?context=r_KnowledgeSearch&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)|Find knowledge articles.|
|[Live feed](https://www.servicenow.com/docs/access?context=c_UseLiveFeed&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)|Filter, search, or sort messages in live feed.|
|[UI pages](https://www.servicenow.com/docs/access?context=r_UIPages&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)|Create a custom UI page to search for records in a table.|

|Search operator|Description|
|---------------|-----------|
|[Boolean operators](c_BooleanOperators.md)|Construct complex searches using Boolean AND, OR, and NOT operators in global text searches.|
|[Quotation marks](c_PhraseSearches.md)|Wrap search terms in quotation marks to search for an exact phrase consisting of one or more words.|
|[Wildcard characters](c_Wildcards.md)|Expand search results to match any non-space character. Zing supports both single-character and multiple-character wildcards.|

-   **[List search finds records from the current table](c_TextSearchesInRecordLists.md)**  
Search records from a table list view.
-   **[Boolean operators allow conditional search results](c_BooleanOperators.md)**  
Construct complex searches using Boolean AND, OR, and NOT operators in global text searches.
-   **[Quotation marks allow exact phrase searches](c_PhraseSearches.md)**  
Wrap search terms in quotation marks to search for an exact phrase consisting of one or more words.
-   **[Wildcard characters allow searching for patterns and variations](c_Wildcards.md)**  
Expand search results to match any non-space character. Zing supports both single-character and multiple-character wildcards.
-   **[Enable or disable the Zing junk filter](../task/t_DisableTheJunkFilter.md)**  
When its junk filter is enabled, Zing doesn't index or search for 2-digit numbers or single-character words \(unless they are Chinese or Japanese characters\). You can enable or disable the junk filter for individual tables.
-   **[Debug Zing](../task/t_DebugZing.md)**  
Debugging messages create a log of search processes as they occur. These messages may help administrators configure optimal performance settings.

**Parent Topic:**[Zing text indexing and search engine](c_ZingTextSearch.md)

**Related topics**  


[Features of Zing text indexing and search engine](../reference/features-zing.md)

[Global search finds records from multiple tables](c_GlobalTextSearch.md)

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

