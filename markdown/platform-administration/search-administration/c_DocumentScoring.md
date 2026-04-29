---
title: Zing computes document scores using three components
description: The Zing search engine computes document scores based on the frequency, sequence, and weight of search terms in the document.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zing computes document scores using three components

The Zing search engine computes document scores based on the frequency, sequence, and weight of search terms in the document.

## Document scores

The components of a document score for a search query are:

-   Frequency: how often the search terms appear in the document.
-   Sequence: how often the search terms appear in the same order as the search query.
-   Weight: how heavily weighted the source field is in which the search terms appear.

![Graphic showing frequency and sequence scoring for sample search query and document.](../image/DocumentScoring.png "Sample document score computation")

## Frequency points

Zing awards one point whenever a search term appears anywhere in the document. For example, when searching for `distributed database server`, a document that contains `distributed` three times, `database` five times, and `server` 17 times would have 25 frequency points.

To increase search result scores of search terms that appear more frequently in a document, but less frequently in a document set, you can [Score search terms by inverse document frequency \(IDF\)](../task/enable-IDF-scoring.md). When TF-IDF is enabled, search term scores are calculated by multiplying the term frequency score by the inverse document frequency score. Because enabling TF-IDF increases the weight of less common search terms, search results for that table are more likely to be relevant. For example, when searching for `distributed database server`, the term `distributed` might receive a higher score than `server` if it appears frequently in one document but less frequently in the document set as a whole.

Zing applies a multiplier to frequency points based on the value of the **ts\_weight** attribute for the field in which the search term appears. A field with a text search scoring weight of 30 \(**ts\_weight=30**\) would add 30 points for each inclusion of a search term.

## Sequence points

Zing awards a document more points when it contains the search terms in the same order in which they were typed. The more search terms in sequence there are, the exponentially higher the score becomes. Zing awards sequence points as 10^x, where x is the number of search terms that appear in sequence.

In the `distributed database server` search example, Zing awards a document 100 \(10^2\) sequence points for each time it includes the two-term string `database server`. Likewise, Zing awards a document 1000 \(10^3\) sequence points each time it includes the three-term string `distributed database server`.

Zing applies a multiplier to sequence points based on the value of the **ts\_weight** attribute for the field in which the sequence appears. The sequence points use the calculation \(10^x \* field **ts\_weight** attribute\).

## Field scoring weights

The system elevates the default scoring weight of Knowledge record numbers, Knowledge short descriptions and metadata, task record numbers, and task short descriptions. Default **ts\_weight** attributes for these fields are as follows:

-   **kb\_knowledge.number = 50**
-   **kb\_knowledge.short\_description = 10**
-   **kb\_knowledge.meta = 10**
-   **task.number = 50**
-   **task.short\_description = 10**

All other fields have a default **ts\_weight** attribute of 1. The maximum possible weight value is 255.

-   **[Score search terms by inverse document frequency \(IDF\)](../task/enable-IDF-scoring.md)**  
Enable term frequency–inverse document frequency \(TF-IDF\) to increase the search result scores of search terms that appear more frequently in a document, but less frequently in the whole collection of searchable documents.
-   **[Set the relative weight of a field](../task/t_ControlMatchRelevanceByField.md)**  
To improve search results, the Zing search engine assigns to each potential match a numeric score that represents its relevancy to the query.

**Parent Topic:**[Zing text indexing and search engine](c_ZingTextSearch.md)

**Related topics**  


[Features of Zing text indexing and search engine](../reference/features-zing.md)

[Available search options](c_IntroductionToSearching.md)

[Global search finds records from multiple tables](c_GlobalTextSearch.md)

[Zing generates search results in four phases](c_SearchProcess.md)

[Zing filters search results with access controls](zing-filters-search-results.md)

[Zing indexes words](zing-indexes-words.md)

[Zing can include attachments in search results](c_SearchingForAttachments.md)

[Zing removes stop words from queries](stop-words-removed-from-queries.md)

[Zing matches derived words with stemming](stemming-matches-derived-words.md)

[Zing can expand search results with synonyms](search-synonyms-expand-results.md)

[Zing displays search suggestions as users enter search terms](search-suggestions-zing.md)

[Installed with Zing](../reference/installed-with-zing.md)

