---
title: Semantic vector search in AI Search
description: Semantic vector search allows the Now LLM Service to find results based on how similar they are in meaning to your search terms. Now Assist Q&amp;A Genius Results and Now Assist in Virtual Agent use semantic vector search to improve recall with natural language interpretation of search queries.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Semantic vector search in AI Search

Semantic vector search allows the Now LLM Service to find results based on how similar they are in meaning to your search terms. Now Assist Q&amp;A Genius Results and Now Assist in Virtual Agent use semantic vector search to improve recall with natural language interpretation of search queries.

By default, AI Search uses keyword search, meaning that it finds results for records that contain the best matches for the keywords \(terms\) in your search query. Term matching doesn't take into account the context or meaning of your search terms.

Starting in the Vancouver Patch 4 release, AI Search includes an alternate search mode called semantic vector search that's used in features which work with the Now LLM Service. Examples of such features include Now Assist in Virtual Agent conversations, Now Assist Multi-Content Response Genius Results, and Now Assist Actions Genius Results.

Semantic vector search analyzes the meanings and context of your search terms and uses that information to find results with similar meanings. It improves search recall by interpreting natural language to more accurately reflect your search's intent.

As an example, suppose you index a source record including text `how to prevent phishing` and search for `avoiding scams`.

-   In keyword search mode, AI Search returns no result for this record because your search query terms aren't literal matches for the terms included in the indexed content.
-   In semantic vector search mode, however, AI Search might return a result for the record based on the following context-aware analysis:
    -   Your search term `avoiding` is contextually similar in meaning to `prevent`
    -   Your search term `scams` has meaning that overlaps with the meaning of `phishing`

AI Search orders results from semantic vector search based on how similar they are to your search. In the example, if you had a second indexed record including text `how to prevent scams`, it would be more similar to the `avoiding scams` search and its search result would appear before the `how to prevent phishing` result.

Unlike the default keyword-based search mode, semantic vector search does not rely on your synonym dictionaries to find term equivalences. AI Search identifies term similarities automatically when indexing source content and metadata for semantic vector search.

Semantic vector search is automatically enabled and doesn’t include any configurable settings.

## Benefits of semantic vector search

In comparison with the default keyword search mode, semantic vector search provides the following benefits:

-   Helps improve recall for knowledge article, Catalog Item, and topic retrieval searches by matching results based on the underlying meaning of your search rather than matching on keywords.
-   Provides a more natural and consistent search experience by returning similar results for varied search queries with the same underlying meaning.
-   Reduces the need to create and maintain synonym dictionaries to anticipate similarities in searches.

## Semantic vector search output

Semantic vector search overrides the normal AI Search term matching and relevancy ranking mechanisms. Results are ordered based on their computed similarity to your search query terms, with the most similar results appearing first.

## Availability of semantic vector search

Semantic vector search is available in the following contexts.

-   Now Assist in Virtual Agent uses semantic vector search for Catalog Item retrieval and live agent topic retrieval. For more details, see [Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/now-assist-in-va-landing.md).
-   Now Assist Q&amp;A Genius Results use semantic vector search along with legacy keyword search when looking for knowledge articles that match your search query. They also use semantic vector search when looking for cached answers that match your query in the second-level cache. For more details, see [Now Assist Q&amp;A Genius Results](now-assist-qna-genius-results.md) and [Caching for Now Assist Q&amp;A Genius Results](caching-now-assist-q-a-gr.md#).
-   Now Assist Actions Genius Results use semantic vector search along with legacy keyword search when looking for Catalog Items that match your search query. For more details, see [Now Assist Actions Genius Results](now-assist-catalog-ordering-gr.md).
-   All connectors from the External Content Connectors application support semantic vector indexing when retrieving document content from external source systems. Only features which use semantic vector search with the Now LLM Service can take advantage of this support. For more information on external content connector configuration and usage, see [External Content Connectors](../reference/ext-cont-connectors-landing-page.md).

**Parent Topic:**[Administering AI Search](administer-ais.md)

