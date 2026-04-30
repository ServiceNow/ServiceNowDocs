---
title: AI Search Retrieval Augmented Generation \(RAG\)
description: You can enhance the search accuracy of your AI Search results by using the AI Search Retrieval Augmented Generation \(RAG\) application. With RAG, you can limit a large language model's \(LLM's\) focus to a specific, contextual dataset, instead of the broad, general data that it was trained on.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search Retrieval Augmented Generation \(RAG\)

You can enhance the search accuracy of your AI Search results by using the AI Search Retrieval Augmented Generation \(RAG\) application. With RAG, you can limit a large language model's \(LLM's\) focus to a specific, contextual dataset, instead of the broad, general data that it was trained on.

## AI Search RAG overview

RAG combines information retrieval with AI text generation. It works in two steps. It indexes the data to make it searchable and then searches that indexed data by using queries.

The effectiveness of AI Search RAG relies on its embedding model, which is used by the advanced search methods, such as a semantic or vector search, to retrieve the context-oriented information from indexed sources. The embedding model generates embeddings that are based on the user's search query. The embeddings are then used by an LLM to produce relevant responses. The embedding model is the engine behind RAG that enables it to search, retrieve, and embed information into a vector map before passing it to an LLM. By default, RAG uses the Embedding \(E5\) model, but it also supports additional third-party models such as Azure OpenAI Embedding and Google Gemini Embedding. Users can also bring their own custom embedding models from third-party providers to create embeddings for their specific RAG needs.

## Activating AI Search RAG

AI Search RAG functionality is provided by the AI Search RAG plugin \(sn\_ais\_rag\). This plugin is automatically activated for your instance when you install [Generative AI Controller](https://www.servicenow.com/docs/access?context=installing-generative-ai-controller&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) or any [Now Assist application](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

-   **[Configuring an external or custom embedding model](setting-up-3p-embedding-models.md)**  
You can connect and configure an external or custom embedding model in the AI Search Retrieval Augmented Generation \(RAG\) application to generate embeddings.

**Parent Topic:**[Semantic index configuration for indexed sources](semantic-index-cfg-ais.md)

