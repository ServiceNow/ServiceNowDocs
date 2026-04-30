---
title: Configuring an external or custom embedding model
description: You can connect and configure an external or custom embedding model in the AI Search Retrieval Augmented Generation \(RAG\) application to generate embeddings.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [AI Search Retrieval Augmented Generation \(RAG\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring an external or custom embedding model

You can connect and configure an external or custom embedding model in the AI Search Retrieval Augmented Generation \(RAG\) application to generate embeddings.

## Embedding model overview

The AI Search Retrieval Augmented Generation \(RAG\) application uses embedding models to retrieve relevant information from the indexed sources and generate embeddings. These embeddings are a way to transform complex objects—like words or images—into numerical forms that capture their meanings and relationships. This transformation helps machine learning \(ML\) models analyze and understand data more effectively, improving tasks like natural language processing \(NLP\), recommendation systems, and image recognition.

With the AI Search RAG application, you can create your own custom embedding model by using the Bring Your Own Model \(BYOM\) capability. The application also supports third-party embedding models, such as the Azure OpenAI Embedding model and Google Gemini Embedding model. You can configure the default connection and credential aliases that are provided for these third-party embedding models to authenticate and enable the integration between your instance and the selected embedding model.

## Configuring embedding models

Configure your custom and third-party embedding models in the AI Search RAG application:

-   **Configuring third-party embedding models**

    You can integrate a third-party embedding model with your system:

    1.  Set up a connection and credentials for a third-party embedding model. For more information, see [Setting up connection and credentials for third-party embedding model](../task/setup-alias-for-3p-embedding-model.md).
    2.  Activate a third-party embedding model. For more information, see [Activating the third-party embedding model](../task/activate-3p-embedding-model.md).
-   **Configuring custom embedding models**

    You can configure a custom embedding model end-to-end by leveraging the Bring Your Own Embedding Model \(BYOM\) capability. For more information, see [Configuring bring your own model \(BYOM\)](creating-byom.md).


-   **[Set up a connection and credential alias for a third-party embedding model](../task/setup-alias-for-3p-embedding-model.md)**  
Set up a connection and credential alias to authenticate an integration between your ServiceNow instance and a third-party embedding model.
-   **[Activate a third-party embedding model](../task/activate-3p-embedding-model.md)**  
Activate your preferred embedding model, whether third-party or custom, so that the AI Search Retrieval Augmented Generation \(RAG\) application knows which model to use for generating embeddings.
-   **[Configuring bring your own model \(BYOM\)](creating-byom.md)**  
As an administrator, you can create your own custom embedding model to use in the AI Search Retrieval Augmented Generation \(RAG\) application to generate embeddings for semantic indexing.

**Parent Topic:**[AI Search Retrieval Augmented Generation \(RAG\)](ais-rag.md)

