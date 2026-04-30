---
title: Zing removes stop words from queries
description: Remove common words from search queries that don't produce meaningful results.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zing removes stop words from queries

Remove common words from search queries that don't produce meaningful results.

Stop words are common words that aren't indexed because they aren't meaningful in search results. Articles, conjunctions, personal pronouns, and prepositions are examples of stop words that aren't used in keyword searches. Administrators can configure stop words for all indexed tables and for specific tables.

By default, the system maintains two types of stop words.

|Stop word type|Description|
|--------------|-----------|
|System-wide text index stop words|The system always ignores system-wide text index stop words when generating text indexes. Any search for a system-wide stop word returns no search results.|
|Table-specific stop words|The system uses the table-specific Text Index record to determine whether to index the stop word or to just remove it from keyword search queries against the table.|

By default, the system has stops words for common English words. Search administrators typically create stop words from search terms that produce too many search results such as articles, conjunctions, personal pronouns, and prepositions.

-   **[Configure a global stop word](../task/t_ConfigureAGlobalStopWord.md)**  
Configure stop words that shouldn't be indexed by the search.
-   **[Configure a table-specific stop word](../task/t_ConfigureATableSpecificStopWord.md)**  
You can configure stop words for a specific table.
-   **[Enable automatic stop words for a table](../task/t_ConfigureAnAutomaticStopWord.md)**  
The system can identify and generate stop words when a search term exceeds an occurrence threshold.
-   **[Disable a stop word in Zing](../task/disable-stop-word-zing.md)**  
Configure Zing to return results for text search terms that match a stop word's stemmed form.

**Parent Topic:**[Zing text indexing and search engine](c_ZingTextSearch.md)

**Related topics**  


[Features of Zing text indexing and search engine](../reference/features-zing.md)

[Available search options](c_IntroductionToSearching.md)

[Global search finds records from multiple tables](c_GlobalTextSearch.md)

[Zing generates search results in four phases](c_SearchProcess.md)

[Zing filters search results with access controls](zing-filters-search-results.md)

[Zing computes document scores using three components](c_DocumentScoring.md)

[Zing indexes words](zing-indexes-words.md)

[Zing can include attachments in search results](c_SearchingForAttachments.md)

[Zing matches derived words with stemming](stemming-matches-derived-words.md)

[Zing can expand search results with synonyms](search-synonyms-expand-results.md)

[Zing displays search suggestions as users enter search terms](search-suggestions-zing.md)

[Installed with Zing](../reference/installed-with-zing.md)

