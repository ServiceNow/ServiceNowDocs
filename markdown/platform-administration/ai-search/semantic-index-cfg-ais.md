---
title: Semantic index configuration for indexed sources
description: The AI Search generalized RAG \(Retrieval-Augmented Generation\) framework offers a streamlined way to configure semantic indexing settings for records indexed from ServiceNow AI Platform tables.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-10-03"
reading_time_minutes: 3
breadcrumb: [Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Semantic index configuration for indexed sources

The AI Search generalized RAG \(Retrieval-Augmented Generation\) framework offers a streamlined way to configure semantic indexing settings for records indexed from ServiceNow AI Platform® tables.

## Semantic index configuration overview

AI Search admins can configure semantic indexing settings for an indexed source. These settings specify how AI Search indexes content from the indexed source for use with semantic vector search. The group of semantic indexing settings for a particular indexed source is called a semantic index configuration.

Each semantic index configuration includes the following elements:

-   **Indexed source**

    A reference to an existing indexed source with field values or attachments that you want indexed for semantic vector search.

    For more information on indexed sources, see [Indexed sources in AI Search](indexed-sources-ais.md). To learn more about semantic vector search, see [Semantic vector search in AI Search](semantic-search-ais.md).

-   **Embedding models**

    A list of one or more embedding models for the system to use when indexing content from the indexed source for semantic vector search.

    An embedding model specifies how information found in your indexed content is encoded in a vector map. Semantic vector search uses the encoded information from the vector map to find search results that have meanings similar to those of your search terms.

-   **Chunking strategy and related parameters**

    A chunking strategy and related parameter values that together determine how content from the indexed source's selected fields and attachments is handled during indexing for semantic vector search.

    Chunking is the process of breaking text down into smaller portions \(called chunks\) during indexing. By chunking your content, AI Search reduces search load and improves context and relevancy for semantic vector matches.

    The following image shows how a two-paragraph block of sample field value text might be broken into chunks for semantic indexing. As shown, chunks can contain multiple sentences and may span paragraph breaks found in the original text.![Two paragraphs of sample text and four multi-sentence text chunks identified when the text is semantically indexed.](../image/chunking-text-example.png)

-   **Semantic index fields**

    References to one or more semantic index fields that provide semantic indexing settings for content from the indexed source.

    Each semantic index field defines semantic indexing settings for a single field from the indexed source table, or for attachments from that table. You can specify the order in which semantic index fields are evaluated when indexing content from the indexed source for semantic vector search.


**Note:** You can define multiple semantic index configurations for an indexed source, but each configuration after the first imposes an additional performance cost at indexing time.

## Activating semantic index configuration

Semantic index configuration functionality is provided by the AI Search Semantic Controller plugin \(com.glide.ais.semantic\_search\). This plugin is automatically activated for your instance when you install any [Now Assist application](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

You can verify whether semantic index configuration is activated by navigating to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources** and selecting an indexed source record. If you see the Semantic Index Configuration related list on the Indexed Source form, the plugin is activated.

-   **[Configure semantic indexing settings for an indexed source](../task/configure-semantic-indexing-ais.md)**  
Specify the semantic indexing configuration settings you want to apply when AI Search indexes records from your indexed sources.
-   **[AI Search Retrieval Augmented Generation \(RAG\)](ais-rag.md)**  
You can enhance the search accuracy of your AI Search results by using the AI Search Retrieval Augmented Generation \(RAG\) application. With RAG, you can limit a large language model's \(LLM's\) focus to a specific, contextual dataset, instead of the broad, general data that it was trained on.

**Parent Topic:**[Indexed sources in AI Search](indexed-sources-ais.md)

