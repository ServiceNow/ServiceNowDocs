---
title: Zing indexes words
description: Index documents by dividing them into words. Depending on the languages your instance supports, a word may be a single character such as a Chinese or Japanese pictogram or a sequence of characters separated by spaces such as with Latin, Arabic, and Pinyin languages.
locale: en-US
release: xanadu
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zing indexes words

Index documents by dividing them into words. Depending on the languages your instance supports, a word may be a single character such as a Chinese or Japanese pictogram or a sequence of characters separated by spaces such as with Latin, Arabic, and Pinyin languages.

Zing uses spaces to define the basic unit of word separation. Zing uses the following rules to index words.

|Rule|Behavior|
|----|--------|
|Punctuation|Zing indexes some punctuation marks as part of some words to improve search results for common search terms. Zing converts any non-indexed punctuation characters to spaces. See [Zing indexes punctuation as part of some words](c_PunctuationForSearchResults.md).|
|Pictograms|Zing supports the full range of Unicode pictogram characters. Each Chinese or Japanese pictogram is indexed as a separate word as if it were a single Latin-1 character surrounded by spaces.|
|Letter|Zing treats Latin-1, Arabic, and Pinyin characters as individual letters of space-separated-words. Sequences of letters define indexable words.|

-   **[Zing indexes punctuation as part of some words](c_PunctuationForSearchResults.md)**  
Zing indexes some punctuation marks as part of some words to improve search results for common search terms.
-   **[Zing indexes some HTML elements](c_SearchingHTMLContent.md)**  
Zing indexes the contents of certain HTML elements to improve document search results. This indexing is addition to the normal indexing by word.
-   **[Configure a table for indexing and searching](../task/configure-single-table-for-indexing.md#)**  
Enable Zing text indexing for a table to allow users to search its records for string values. Configure the table's text indexing attributes, stop words, and synonym dictionaries to control search behavior.
-   **[Configure a text index group to search across multiple tables](../task/index-multiple-tables.md)**  
Update tables to the V4 indexing format and include them in a text index group to facilitate searching across multiple tables.
-   **[Zing index and search dictionary attributes](../reference/index-attributes.md)**  
The following dictionary attributes either affect the way Zing indexes tables or ranks search results.
-   **[Regenerate a text index for a table](../task/t_RegenerateATextIndexForATable.md)**  
You can regenerate a table text index when you change table stop words or display values.
-   **[Remove an index](../task/t_RemoveAnIndex.md)**  
You can remove the index for a table if you no longer want the search engine to return results for that table. This procedure also removes the index for all tables that extend the specified table.
-   **[Remove an index for a specific field](../task/t_RemoveAnIndexForASpecificField.md)**  
You can remove the index for a specific field in a table if you no longer want the search engine to return results for that field.
-   **[Remove the text index for a child table](../task/remove-index-child-table.md)**  
You can remove the text index for a child table if you no longer want the search engine to return results for that child table.
-   **[Change the query mode of an indexed table](../task/configure-table-query-mode.md)**  
Set the query mode to specify whether searches on an indexed table must match all or only some of the search terms.
-   **[Enable indexing of text in multi-row variable sets](../task/index-text-multi-row-variable-sets.md)**  
Make text from multi-row Service Catalog variable sets searchable in global search.
-   **[Text indexing statistics and status](../reference/r_ViewTextIndexingStatsAndStatus.md)**  
To view text indexing statistics and status, navigate to **All** &gt; **System Definition** &gt; **Text Indexes**.
-   **[Configure tables to use the Japanese tokenizer](../task/configure-tables-japanese-tokenizer.md)**  
Improve search results in Japanese language searches by configuring individual tables to use the Japanese tokenizer.

**Parent Topic:**[Zing text indexing and search engine](c_ZingTextSearch.md)

**Related topics**  


[Features of Zing text indexing and search engine](../reference/features-zing.md)

[Available search options](c_IntroductionToSearching.md)

[Global search finds records from multiple tables](c_GlobalTextSearch.md)

[Zing generates search results in four phases](c_SearchProcess.md)

[Zing filters search results with access controls](zing-filters-search-results.md)

[Zing computes document scores using three components](c_DocumentScoring.md)

[Zing can include attachments in search results](c_SearchingForAttachments.md)

[Zing removes stop words from queries](stop-words-removed-from-queries.md)

[Zing matches derived words with stemming](stemming-matches-derived-words.md)

[Zing can expand search results with synonyms](search-synonyms-expand-results.md)

[Zing displays search suggestions as users enter search terms](search-suggestions-zing.md)

[Installed with Zing](../reference/installed-with-zing.md)

