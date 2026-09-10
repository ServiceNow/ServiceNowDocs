---
title: Hybrid search in AI Search
description: In hybrid search mode, AI Search blends keyword search and semantic vector search to find results that best match the terms and meaning of your search. Hybrid search is usable for any indexed source that has semantic vector search enabled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/hybrid-search-ais.html
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-08-25"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring ServiceNow Otto for AI Search, ServiceNow Otto for AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Hybrid search in AI Search

In hybrid search mode, AI Search blends keyword search and semantic vector search to find results that best match the terms and meaning of your search. Hybrid search is usable for any indexed source that has semantic vector search enabled.

## Overview of hybrid search

In older releases, AI Search performs all searches in keyword search mode. This mode looks for the best matches for your search terms, but doesn't take the context or meaning of those terms into account. The keyword search relevance score for a search result indicates how well the indexed terms in that search result match your search terms.

Starting with the Yokohama Patch 11 release, AI Search includes an alternate semantic vector search mode in features which work with the Now LLM Service. Semantic vector search analyzes the meanings and context of your search terms and uses that information to find results with similar meanings. It improves search recall by interpreting natural language to more accurately reflect your search's intent. The semantic vector search relevance score for a search result indicates how closely the search result matches the meaning of your search.

**Note:** To learn more about semantic vector search mode and how it differs from keyword search mode, see [Semantic vector search in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/semantic-search-ais.md).

Installation of ServiceNow Otto for AI Search offers a new hybrid search mode. This mode combines keyword relevance scores and semantic similarity scores into a single result ranking using Reciprocal Rank Fusion \(RRF\). By blending keyword and semantic vector search modes, AI Search offers the best of both worlds, providing users with both search precision and contextual relevance.

Upgrading an existing installation doesn't change current hybrid search settings. Users with the admin role can activate or deactivate hybrid search for individual SACs after installation.

**Note:** Hybrid search applies to any indexed source that's included in the semantic index. By default, the following indexed sources ship with preconfigured semantic indexing and work with hybrid search:

-   Knowledge Table indexed source \[kb\_knowledge table\]
-   Catalog Item Table indexed source \[sc\_cat\_item table\]
-   Skills indexed source \[sys\_gen\_ai\_skill table\]
-   All External Content Connectors indexed sources \[connector-specific tables\]

You can manually configure additional indexed sources to be included in the semantic index, extending hybrid search to those sources as well. For details on this procedure, see [Configure semantic indexing settings for an indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configure-semantic-indexing-ais.md).

In portal search, hybrid search queries the default semantic field names, **title** and **body**. These default field names are specified by the value of the **glide.ais.query.default\_hybrid\_semantic\_fields** system property. If your indexed source's semantic configuration uses non-default semantic field names, you can set the value of the **glide.ais.query.use\_default\_hybrid\_semantic\_fields** system property to **false**. With this value set, hybrid search resolves each indexed source's own semantic field mappings instead of using the default field names.

## Benefits of hybrid search

Hybrid search offers these benefits when compared with keyword search.

-   **Improved search quality and recall**

    Hybrid search combines keyword and semantic matching, increasing the chances of retrieving relevant results, even when users phrase their queries differently.

-   **More relevant top-ranked search results**

    Understanding the intent of your search, along with matching the words you use, helps find results that match what you mean.

-   **Fewer zero-result searches**

    Hybrid search can return useful results even for vague or misspelled queries because it uses semantic matching to understand meaning beyond exact keywords. This reduces the number of searches that return no results.


## Availability of hybrid search

Hybrid search requires installation of the ServiceNow Otto for AI Search application. This feature is available beginning in ServiceNow Otto for AI Search 15.

**Note:** Search application configurations that use the legacy Zing text indexing and search engine don't support hybrid search.

Hybrid search isn't automatically activated for your search application configurations that use AI Search as their search engine. To learn how to manually activate hybrid search for these search application configurations in the AI Search Admin console, see [Manage hybrid search in search applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/enable-hybrid-search-aisac.md).

## Interactions with other features

Activating hybrid search in a search application configuration disables search result counts for facets in that search application configuration. For more information on search result counts for facets, see [Show search result counts for facets on the results page for a search application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/display-result-counts-ais.md).

When you activate hybrid search in a search application configuration, the behavior of the **Most recent** search result sort option changes for the specified search application. Instead of sorting the entire list of search results by last modification date, AI Search first retrieves keyword search results and the most relevant semantic vector search results, then merges those results and sorts them by last modification date. To learn about sorting search results based on recency, see [Change the sort order for your search results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/sort-search-results-ais.md).

**Parent Topic:**[Configuring ServiceNow Otto for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configuring-now-assist-ais.md)

