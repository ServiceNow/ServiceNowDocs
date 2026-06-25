---
title: Zing generates search results in four phases
description: Generate search results by dividing documents among shards, searching shard documents, scoring shard documents, and merging scores into an index.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/c\_SearchProcess.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zing generates search results in four phases

Generate search results by dividing documents among shards, searching shard documents, scoring shard documents, and merging scores into an index.

Zing generates search results in four phases:

1.  Divide searchable documents among index shards.
2.  Search and filter shard documents.
3.  Score shard documents.
4.  Merge shard document scores into an index.

## Phase 1: Divide searchable documents among index shards

When a search is executed, the system equally divides all searchable documents among 10 index shards. Each shard has a unique list of documents.

To maximize search efficiency, the system creates 10 query threads to simultaneously search each index shard.

\[Omitted image "IndexShardDivsions.png"\] Alt text: The system divides all searchable documents among 10 index shards from Shard 0 to Shard 9.

## Phase 2: Search and filter shard documents

Each query thread searches through its list of shard documents to identify documents that match the search criteria. For example, if you search for "`wifi network`," the system returns all documents containing both "`wifi`" and "`network`" in no particular order.

**Note:** A multiple word search is equivalent to multiple single word searches connected by an AND operator. For example, **\[contains\]\[wifi\]\[AND\]\[contains\]\[network\]**.

The query thread assigns each matching document a numeric value \(a document ID\) to uniquely identify it. All other documents are ignored.

## Phase 3: Score shard documents

The query thread [scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/c_DocumentScoring.md) each matching shard document.

\[Omitted image "IndexShardFilterAndIndex.png"\] Alt text: The system creates 10 Query threads to search, filter, and score shard documents.

## Phase 4: Merge and sort shard document scores

The system merges the document scores into a single index and sorts the documents from highest to lowest document score. The documents with the highest document score are most relevant to the search query.

\[Omitted image "IndexShardMerge.png"\] Alt text: Merge and sort shard document scores.

**Parent Topic:**[Zing text indexing and search engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/c_ZingTextSearch.md)

**Related topics**  


[Features of Zing text indexing and search engine]()

[Available search options]()

[Global search finds records from multiple tables]()

[Zing filters search results with access controls]()

[Zing computes document scores using three components]()

[Zing indexes words]()

[Zing can include attachments in search results]()

[Zing removes stop words from queries]()

[Zing matches derived words with stemming]()

[Zing can expand search results with synonyms]()

[Zing displays search suggestions as users enter search terms]()

[Installed with Zing]()

