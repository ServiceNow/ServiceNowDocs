---
title: Zing text indexing and search engine
description: Index and search record data by table.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2025-10-06"
reading_time_minutes: 3
breadcrumb: [Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zing text indexing and search engine

Index and search record data by table.

The ServiceNow® Zing text indexing and search engine is a legacy search engine that you can use to search ServiceNow AI Platform® record data. Its engine is created entirely with ServiceNow code and implemented within the relational model.

**Note:** To learn about the AI Search engine, which is the default search engine for ServiceNow AI Platform record data, see [AI Search](../../ai-search/concept/overview-ais.md).

The Zing text search index is split into multiple database shards for parallel querying. Its search engine logic yields fast results and emphasizes relevancy scoring. Relevancy scores include frequency and proximity weighting. Scores also include weighting for specific indexed fields such as title, short description, and metadata.

Zing provides type-ahead search suggestions and **Did you mean:** global search suggestions.

Administrators and users with the ts\_admin role can configure the following Zing text search settings:

-   match relevance
-   relevancy field weights for each indexed table
-   global stop words
-   stop words for each index
-   synonym dictionaries for each table
-   tables with attachment indexing

<table id="table_khb_w2v_lbc"><tbody><tr><td>

Explore

 -   Yokohama
-   [Features of Search administration](../reference/features-search-administration.md)
-   [Features of Zing text indexing and search engine](../reference/features-zing.md)

</td><td>

Set up

 -   [Set global text search properties](../task/set-global-text-search-properties.md)
-   [Zing can include attachments in search results](c_SearchingForAttachments.md)
-   [Zing can expand search results with synonyms](search-synonyms-expand-results.md)

</td><td>

Administer

 -   [Zing indexes words](zing-indexes-words.md)
-   [Global search finds records from multiple tables](c_GlobalTextSearch.md)
-   [List search finds records from the current table](c_TextSearchesInRecordLists.md)

</td></tr><tr><td>

Use

 -   [Boolean operators allow conditional search results](c_BooleanOperators.md)
-   [Quotation marks allow exact phrase searches](c_PhraseSearches.md)
-   [Wildcard characters allow searching for patterns and variations](c_Wildcards.md)

</td><td>

Develop

 -   [Developer training](https://developer.servicenow.com/app.do#!/training/landing)
-   [Developer documentation](https://developer.servicenow.com/app.do#!/documentation)
-   [Create synonym dictionaries](../task/create-synonym-dictionaries.md)

</td><td>

Troubleshoot and get help

 -   [Ask or answer questions in the Platform forum](https://community.servicenow.com/community/service-automation-platform)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

</td></tr></tbody>
</table>-   **[Features of Zing text indexing and search engine](../reference/features-zing.md)**  
Enable and configure Zing text indexing and search engine features.
-   **[Available search options](c_IntroductionToSearching.md)**  
Zing offers users several search interfaces and search operators to conduct text searches.
-   **[Global search finds records from multiple tables](c_GlobalTextSearch.md)**  
Search multiple record types from a single search field.
-   **[Zing generates search results in four phases](c_SearchProcess.md)**  
Generate search results by dividing documents among shards, searching shard documents, scoring shard documents, and merging scores into an index.
-   **[Zing filters search results with access controls](zing-filters-search-results.md)**  
Zing filters search results to only display records the user can access.
-   **[Zing computes document scores using three components](c_DocumentScoring.md)**  
The Zing search engine computes document scores based on the frequency, sequence, and weight of search terms in the document.
-   **[Zing indexes words](zing-indexes-words.md)**  
Index documents by dividing them into words. Depending on the languages your instance supports, a word may be a single character such as a Chinese or Japanese pictogram or a sequence of characters separated by spaces such as with Latin, Arabic, and Pinyin languages.
-   **[Zing can include attachments in search results](c_SearchingForAttachments.md)**  
Search content from attachments on indexed tables. Display attachments for search results from the Knowledge \[kb\_knowledge\] table.
-   **[Zing removes stop words from queries](stop-words-removed-from-queries.md)**  
Remove common words from search queries that don't produce meaningful results.
-   **[Zing matches derived words with stemming](stemming-matches-derived-words.md)**  
Convert any multiple-character search keyword to its stem form to find derived versions of the word.
-   **[Zing can expand search results with synonyms](search-synonyms-expand-results.md)**  
Expand search results to include additional search terms.
-   **[Zing displays search suggestions as users enter search terms](search-suggestions-zing.md)**  
Display possible search query completions as users enter search terms.
-   **[Installed with Zing](../reference/installed-with-zing.md)**  
Several types of components are installed with Zing.

**Parent Topic:**[Search administration](../reference/search-administration.md)

