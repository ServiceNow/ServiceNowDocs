---
title: Installed with Zing
description: Several types of components are installed with Zing.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Installed with Zing

Several types of components are installed with Zing.

<table id="table_fsw_xnt_bz"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Text Index \[ts\_index\_name\]

</td><td>

Stores the tables the system indexes.

</td></tr><tr><td>

Index Stop Word \[ts\_index\_stop\]

</td><td>

Stores the stop words for a specific table.

</td></tr><tr><td>

Stop Word \[ts\_stop\]

</td><td>

Stores the global stop words.

</td></tr><tr><td>

Text Search Groups \[ts\_group\]

</td><td>

Stores search groups for global text search.

</td></tr><tr><td>

-   ts\_attachment
-   ts\_chain\_summary
-   ts\_chain
-   ts\_deleted\_doc
-   ts\_document
-   ts\_index\_stats
-   ts\_phrase
-   ts\_search\_stats
-   ts\_search\_summary
-   ts\_word\_roots
-   ts\_word

</td><td>

System tables that support Zing. Extending or modifying these tables isn't recommended.

</td></tr></tbody>
</table>|Business Rule|Description|
|-------------|-----------|
|Text Search Property Change Rationally|Ensures that valid values are entered for Zing text search properties.|
|Text Index Stop Reminder|Warns the user of stop word changes that require the index to be rebuilt \(table-specific\). The warning is issued if record is deleted that had a stop mode "neither index nor query", if record's stop mode is updated to something else and was "neither index nor query", and if record's word is updated to something else and stop mode is "neither index nor query".|
|Stop Word Reminder|Warns the user of stop word changes that require the index to be rebuilt \(global\). The warning is issued if record is deleted and it was active, if record is inactivated, and if record's word is changed and was active.|

|Scheduled job|Description|
|-------------|-----------|
|TS Search Stats|Compiles type-ahead suggestions each night. See [Update A Type-Ahead Suggestion](../task/t_UpdateATypeAheadSuggestion.md).|
|TS Index Stats|Collects statistics and performs maintenance for text search and indexing. Runs nightly.|
|text index events process|Collects statistics and performs maintenance for text search and indexing. Runs every 30 seconds.|
|TS Chain Summary|Compiles search chain statistics each hour.|

|UI action|Description|
|---------|-----------|
|Regenerate Text Index|Displays the **Regenerate Text Index** link on Text Index forms.|

-   **[Zing roles](roles-zing.md#)**  
Zing is installed with these roles.

**Parent Topic:**[Zing text indexing and search engine](../concept/c_ZingTextSearch.md)

**Related topics**  


[Features of Zing text indexing and search engine](features-zing.md)

[Available search options](../concept/c_IntroductionToSearching.md)

[Global search finds records from multiple tables](../concept/c_GlobalTextSearch.md)

[Zing generates search results in four phases](../concept/c_SearchProcess.md)

[Zing filters search results with access controls](../concept/zing-filters-search-results.md)

[Zing computes document scores using three components](../concept/c_DocumentScoring.md)

[Zing indexes words](../concept/zing-indexes-words.md)

[Zing can include attachments in search results](../concept/c_SearchingForAttachments.md)

[Zing removes stop words from queries](../concept/stop-words-removed-from-queries.md)

[Zing matches derived words with stemming](../concept/stemming-matches-derived-words.md)

[Zing can expand search results with synonyms](../concept/search-synonyms-expand-results.md)

[Zing displays search suggestions as users enter search terms](../concept/search-suggestions-zing.md)

