---
title: Configuring bring your own model \(BYOM\)
description: As an administrator, you can create your own custom embedding model to use in the AI Search Retrieval Augmented Generation \(RAG\) application to generate embeddings for semantic indexing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/creating-byom.html
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring an external or custom embedding model, AI Search Retrieval Augmented Generation \(RAG\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Configuring bring your own model \(BYOM\)

As an administrator, you can create your own custom embedding model to use in the AI Search Retrieval Augmented Generation \(RAG\) application to generate embeddings for semantic indexing.

Use the BYOM capability to create a custom embedding model from third-party providers that helps to create embeddings for your specific RAG needs. The process for onboarding BYOM includes:

1.  Create a connection and credential alias for the embedding model and complete its setup. For more information, see Create a connection and credential alias for a custom embedding model.
2.  Create a custom embedding model in the Generative AI Model Configuration \[sys\_generative\_ai\_model\_config\] table for the AI Search RAG application to use in semantic indexing. For more information, see [Configure a custom embedding model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-byom.md).
3.  Select an AI provider for your embedding model so that it can integrate with the AI Search RAG application. For more information, see [Set a provider for an embedding model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/set-provider-for-byom.md).
4.  Enable the AI Search Retrieval Augmented Generation \(RAG\) application to recognize your custom embedding model and use it for generating embeddings. For more information, see [Connect your custom embedding model with the Generative AI application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/connect-em-with-genai.md).
5.  Manage errors from custom embedding models when generating semantic vectors. For more information, see [Create an error handler extension point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-error-handler-extention-point.md).
6.  Add your new embedding model to the semantic indexing table to enable it for semantic indexing. For more information, see [Enable the custom embedding model for semantic indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/enable-byom-for-semnatic-indexing.md).
7.  Activate your preferred embedding model so the AI Search RAG application can use it for generating embeddings. For more information, see [Activate a third-party embedding model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/activate-3p-embedding-model.md).
8.  Select your preferred embedding model to use for semantic indexing. For more information, see [Configure semantic indexing settings for an indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/configure-semantic-indexing-ais.md).

