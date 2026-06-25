---
title: Configuring an external or custom embedding model
description: You can connect and configure an external or custom embedding model in the AI Search Retrieval Augmented Generation \(RAG\) application to generate embeddings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/setting-up-3p-embedding-models.html
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-05-29"
reading_time_minutes: 1
breadcrumb: [Semantic index configuration for indexed sources, Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
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

    1.  Set up a connection and credentials for a third-party embedding model. For more information, see [Setting up connection and credentials for third-party embedding model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/setup-alias-for-3p-embedding-model.md).
    2.  Activate a third-party embedding model. For more information, see [Activating the third-party embedding model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/activate-3p-embedding-model.md).
-   **Configuring custom embedding models**

    You can configure a custom embedding model end-to-end by leveraging the Bring Your Own Embedding Model \(BYOM\) capability. For more information, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/creating-byom.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/creating-byom.md).


