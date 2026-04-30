---
title: Hybrid search in AI Search
description: In hybrid search mode, AI Search blends keyword search and semantic vector search to find knowledge articles, Catalog Items, external content items, and topics that best match the terms and meaning of your search.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-02"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Hybrid search in AI Search

In hybrid search mode, AI Search blends keyword search and semantic vector search to find knowledge articles, Catalog Items, external content items, and topics that best match the terms and meaning of your search.

## Overview of hybrid search

By default, AI Search performs most searches in keyword search mode. This mode looks for the best matches for your search terms, but doesn't take the context or meaning of those terms into account. The keyword search relevance score for a search result indicates how well the indexed terms in that search result match your search terms.

Starting in the Vancouver Patch 4 release, AI Search includes an alternate semantic vector search mode in features which work with the Now LLM Service. Semantic vector search analyzes the meanings and context of your search terms and uses that information to find results with similar meanings. It improves search recall by interpreting natural language to more accurately reflect your search's intent. The semantic vector search relevance score for a search result indicates how closely the search result matches the meaning of your search.

Starting in Now Assist in AI Search 15, AI Search offers a hybrid search mode in features which work with the Now LLM Service. This mode combines keyword relevance scores and semantic similarity scores into a single result ranking using Reciprocal Rank Fusion \(RRF\). This blended approach offers the best of both worlds, helping to ensure that users get both search precision \(from keyword search term matching\) and contextual relevance \(from semantic vector search\).

**Note:** Hybrid search only affects knowledge article, Catalog Item, external content, and topic retrieval searches. AI Search continues to use keyword search when searching indexed content from other sources.

To learn more about semantic vector search mode and how it differs from keyword search mode, see [Semantic vector search in AI Search](semantic-search-ais.md).

## Benefits of hybrid search

Hybrid search offers these benefits when compared with keyword search.

-   **Improved search quality and recall**

    Hybrid search combines keyword and semantic matching, increasing the chances of retrieving relevant results, even when users phrase their queries differently.

-   **More relevant top-ranked search results**

    Semantic understanding helps surface answers that better match the user’s intent instead of just their search keywords.

-   **Fewer zero-result searches**

    Hybrid search can return useful results even for vague or misspelled queries because it uses semantic matching to understand meaning beyond exact keywords. This reduces the number of searches that return no results.


## Availability of hybrid search

If you installed Now Assist in AI Search 15 without having any previous version installed, hybrid search is automatically activated for your search application configurations that use AI Search as their search engine.

**Note:** Search application configurations that use the legacy Zing text indexing and search engine don't support hybrid search.

If you upgraded to Now Assist in AI Search 15 from a previous version, hybrid search isn't automatically activated for your search application configurations that use AI Search as their search engine. To learn how to manually activate hybrid search for these search application configurations, see [Manage hybrid search in search applications](../task/enable-hybrid-search-aisac.md).

## Interactions with other features

Activating hybrid search in a search application configuration disables search result counts for facets in that search application configuration. For more information on search result counts for facets, see [Show search result counts for facets on the results page for a search application](../task/display-result-counts-ais.md).

When you activate hybrid search in a search application configuration, the behavior of the **Most recent** search result sort option changes for the specified search application. Instead of sorting the entire list of search results by last modification date, AI Search first retrieves keyword search results and the most relevant semantic vector search results, then merges those results and sorts them by last modification date. To learn about sorting search results based on recency, see [Change the sort order for your search results](../task/sort-search-results-ais.md).

**Parent Topic:**[Configuring Now Assist in AI Search](configuring-now-assist-ais.md)

