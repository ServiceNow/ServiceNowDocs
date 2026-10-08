---
title: AI Search RAG \(Retrieval-Augmented Generation\)
description: The AI Search RAG \(Retrieval-Augmented Generation\) capability provides a framework that enhances the search accuracy of AI Search results by narrowing the focus of your large language model \(LLM\) to a specific, contextual data set, instead of the vast, general data it was trained on.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/ais-rag.html
release: brazil
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search RAG \(Retrieval-Augmented Generation\)

The AI Search RAG \(Retrieval-Augmented Generation\) capability provides a framework that enhances the search accuracy of AI Search results by narrowing the focus of your large language model \(LLM\) to a specific, contextual data set, instead of the vast, general data it was trained on.

## AI Search RAG overview

RAG \(Retrieval Augmented Generation\) technology helps enhance search capabilities of your AI Search application by combining information retrieval with text generation. It includes the following steps:

-   **Indexing**

    Prepare and organize data to make it searchable. It includes the ais\_datasource table and semantic indexing configurations. For more information, see [Indexed sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/indexed-sources-ais.md).

-   **Searching**

    Find the most relevant results from the indexed data using a query. It includes RAG retrieval API to run search on indexed data of the search profile, and RAG capability that manages the RAG process, including retriever and re-ranker to deliver relevant results.


Components of AI Search RAG

The AI Search RAG capability orchestrates the complete RAG process using components, such as query rewrite, retriever, and re-ranker to deliver the most relevant results.

-   Query Rewrite: Rewrites the complex or long queries into concise, short form to avoid truncation issues with the embedding model's token limit.
-   Retriever: Uses the rewritten query to retrieve the most relevant results from indexed sources.
-   Re-ranker: Uses LLM to further refine the ranking of retrieved results.
-   Final Response: The output of the re-ranker is returned as the final response.

The following diagram shows how AI Search RAG components work together.

The AI Search RAG system works by first organizing data into a searchable format using specific indexing configurations. When a user asks a question, the system processes it and may rephrase the query for better understanding. It then searches for relevant information with the help of retriever and the re-ranker uses AI to arrange them in the most useful order. All of these steps work together under the guidance of a search profile to produce an accurate and context-rich answer for the user.

## Embedding model in AI Search RAG

AI Search RAG uses the advanced search methods, such as semantic or vector search to find relevant and more context-oriented information from the configured indexed sources. The semantic search further uses embedding model to retrieve the most relevant data based on the user search query for embedding generation. This retrieved information along with the search query then prompts the LLM model to generate the relevant response.

An embedding model is the engine behind RAG that helps it to search and retrieve the correct information from the indexed sources and embed that information into vector map before sending it to the LLM model. ServiceNow AI Search RAG uses the default ServiceNow Embedding \(E5\) model and it also supports additional third-party embedding models, such as Azure OpenAI Embedding and Gemini Text Embedding. You can also bring your own third-party hosted custom embedding model to create embeddings for your RAG use case.

## Activating AI Search RAG \(Retrieval-Augmented Generation\)

AI Search RAG \(Retrieval-Augmented Generation\) functionality is provided by the AI Search RAG plugin \(sn\_ais\_rag\). This plugin is automatically activated for your instance when you install [Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/installing-generative-ai-controller.md) or any [ServiceNow Otto® application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platform-now-assist-landing.md).

**Parent Topic:**[Semantic index configuration for indexed sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/semantic-index-cfg-ais.md)

