---
title: Features of Zing text indexing and search engine
description: Enable and configure Zing text indexing and search engine features.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Features of Zing text indexing and search engine

Enable and configure Zing text indexing and search engine features.

<table id="table_l31_lxp_fz"><thead><tr><th>

Feature

</th><th>

Description

</th><th>

Top tasks

</th><th>

State

</th></tr></thead><tbody><tr><td>

[Zing indexes words](../concept/zing-indexes-words.md)

</td><td>

Index documents by dividing them into words. Depending on the languages your instance supports, a word may be a single character such as a Chinese or Japanese pictogram or a sequence of characters separated by spaces such as with Latin, Arabic, and Pinyin languages.

</td><td>

-   [Configure a table for indexing and searching](../task/configure-single-table-for-indexing.md#)
-   [Regenerate a text index for a table](../task/t_RegenerateATextIndexForATable.md)
-   [Configure tables to use the Japanese tokenizer](../task/configure-tables-japanese-tokenizer.md)

</td><td>

Active

</td></tr><tr><td>

[Zing computes document scores using three components](../concept/c_DocumentScoring.md)

</td><td>

Compute document scores based on the frequency, sequence, and weight of search terms in the document.

</td><td>

-   [Score search terms by inverse document frequency \(IDF\)](../task/enable-IDF-scoring.md)
-   [Set the relative weight of a field](../task/t_ControlMatchRelevanceByField.md)

</td><td>

Active

</td></tr><tr><td>

[Global search finds records from multiple tables](../concept/c_GlobalTextSearch.md)

</td><td>

Search multiple record types from a single search field.

</td><td>

-   [Add a search group for Core UI](../concept/search-settings-filter-group-table.md#)
-   [Configure a table for indexing and searching](../task/configure-single-table-for-indexing.md#)

</td><td>

Active

</td></tr><tr><td>

[Search results page in Core UI and UI15](../concept/global-search-polaris-ui.md#)

</td><td>

Display global text search results for each table as Zing generates them.

</td><td>

-   [Add a search group for Core UI](../concept/search-settings-filter-group-table.md#)
-   [Revert to the legacy global search UI](../task/revert-to-legacy-global-search.md#)

</td><td>

Active

</td></tr><tr><td>

[List search finds records from the current table](../concept/c_TextSearchesInRecordLists.md)

</td><td>

Search records from a table list view.

</td><td>

-   [Configure a table for indexing and searching](../task/configure-single-table-for-indexing.md#)
-   [Regenerate a text index for a table](../task/t_RegenerateATextIndexForATable.md)

</td><td>

Active

</td></tr><tr><td>

[Zing can include attachments in search results](../concept/c_SearchingForAttachments.md)

</td><td>

Search content from attachments on indexed tables. Display attachments for search results from the Knowledge \[kb\_knowledge\] table.

</td><td>

-   [Index attachments on a table](../../form-administration/task/t_DisablingAttachmentsOnATable.md)
-   [Configure a table for indexing and searching](../task/configure-single-table-for-indexing.md#)

</td><td>

Active

</td></tr><tr><td>

[Zing removes stop words from queries](../concept/stop-words-removed-from-queries.md)

</td><td>

Remove common words from search queries that don't produce meaningful results.

</td><td>

-   [Configure a global stop word](../task/t_ConfigureAGlobalStopWord.md)
-   [Configure a table-specific stop word](../task/t_ConfigureATableSpecificStopWord.md)

</td><td>

Active

</td></tr><tr><td>

[Zing matches derived words with stemming](../concept/stemming-matches-derived-words.md)

</td><td>

Convert any multiple-character search keyword to its stem form to find derived versions of the word.

</td><td>

-   [System Localization properties](../../localization/reference/set-localization-props.md)
-   [Activate a language](../../localization/task/t_ActivateALanguage.md)

</td><td>

Active

</td></tr><tr><td>

[Zing can expand search results with synonyms](../concept/search-synonyms-expand-results.md)

</td><td>

Expand search results to include additional search terms. ![icon](../../platform-common/image/icon-configuration-required.png) Requires configuration before use

</td><td>

-   [Enable search synonyms](../task/enable-text-index-synonyms.md)
-   [Create synonym dictionaries](../task/create-synonym-dictionaries.md)

</td><td>

Inactive

</td></tr></tbody>
</table>