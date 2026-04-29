---
title: Zing can expand search results with synonyms
description: Expand search results to include additional search terms.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zing can expand search results with synonyms

Expand search results to include additional search terms.

By default, Zing includes a sample synonym dictionary consisting of a list of synonym sets \(synsets\). Zing supports two types of synonym sets.

|Synonym set type|Description|Example|
|----------------|-----------|-------|
|Synonym list|A synonym list is a list of words separated by commas. When a search uses any word from the list, Zing expands the search to include all words in the list.|Cyber,Internet,Cybercafe|
|Synonym map|A synonym map is two word lists separated by the equal and greater than characters =&gt; . When a search uses any word from the list on the left, Zing expands the search to include all words from the list on the right. When a search uses a word from the list on the right, Zing doesn't expand the search to include terms from the list on the left.|IOT,Internet of Things=&gt;Chip,Nest thermostat,RFID,IOT|

## Search results, synonym expansion and weighting

In search results, documents containing the original search keywords have a higher score than documents containing the search synonyms. For example, documents with the search keyword `IOT` have a higher score than documents with the synonym `Internet of Things`.

-   One-way synonym expansion to/from multiple terms `(blork, cork => malork, elastic)` works as expected. `Blork` and `cork` both expand to `malork` and `elastic`.
-   Multi-level one-way expansion `(blork => cork => malork)` doesn't work transitively. Neither `blork` nor `cork` expands to `malork`.
-   Multi-level one-way expansion split between multiple synonym set records `(blork => cork)(cork => malork)` doesn't work transitively. Only `cork` expands to `malork`, `blork` only expands to `cork` but not `malork`.

By default, synonyms don't use the same weight as regular search terms. Synonyms are only weighted at 10% of the default search weight. Additionally, multiple instances of a synonym in a single doc/field don't increase the search weight. The weight of synonyms is controlled by the property **glide.ts.synonym.expanded.boost**. When this property value = 1, synonyms are weighted equally to normal search terms. 0.5 = 50% weight etc.

## Wildcard characters and synonym matching

Zing doesn't expand the `%` and `*` wildcard characters when looking for synonyms that match your search term. These characters are treated as literal characters when finding matching synonyms. As an example, if you search for `issu*`, Zing doesn't find synonyms for `issue`, but it does find synonyms for `issu*`.

-   **[Enable search synonyms](../task/enable-text-index-synonyms.md)**  
Enabling text index synonyms allows Zing to expand text searches with additional search keywords.
-   **[Create synonym dictionaries](../task/create-synonym-dictionaries.md)**  
You can create synonym dictionaries to expand Zing text searches with additional search keywords.
-   **[Select synonym dictionaries for a table](../task/select-synonym-dictionaries.md)**  
Search administrators can specify one or more synonym dictionaries available to a particular table.
-   **[Disable synonyms for a table](../task/disable-synonyms-for-a-table.md)**  
By default, Zing uses all active synonym dictionaries when a user performs a text search. Search administrators can disable synonym dictionary usage on a per-table basis.
-   **[Debug synonym searches](../task/debug-synonym-searches.md)**  
You can view debug messages to determine if synonym searches are working as expected.

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

[Zing removes stop words from queries](stop-words-removed-from-queries.md)

[Zing matches derived words with stemming](stemming-matches-derived-words.md)

[Zing displays search suggestions as users enter search terms](search-suggestions-zing.md)

[Installed with Zing](../reference/installed-with-zing.md)

