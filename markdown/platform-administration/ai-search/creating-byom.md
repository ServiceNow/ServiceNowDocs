---
title: Configuring bring your own model \(BYOM\)
description: As an administrator, you can create your own custom embedding model to use in the AI Search Retrieval Augmented Generation \(RAG\) application to generate embeddings for semantic indexing.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring an external or custom embedding model, AI Search Retrieval Augmented Generation \(RAG\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring bring your own model \(BYOM\)

As an administrator, you can create your own custom embedding model to use in the AI Search Retrieval Augmented Generation \(RAG\) application to generate embeddings for semantic indexing.

Use the BYOM capability to create a custom embedding model from third-party providers that helps to create embeddings for your specific RAG needs. The process for onboarding BYOM includes:

1.  Create a connection and credential alias for the embedding model and complete its setup. For more information, see [Create a connection and credential alias for a custom embedding model](https://www.servicenow.com/docs/access?context=connection-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).
2.  Create a custom embedding model in the Generative AI Model Configuration \[sys\_generative\_ai\_model\_config\] table for the AI Search RAG application to use in semantic indexing. For more information, see [Configure a custom embedding model](../task/create-byom.md).
3.  Select an AI provider for your embedding model so that it can integrate with the AI Search RAG application. For more information, see [Set a provider for an embedding model](../task/set-provider-for-byom.md).
4.  Enable the AI Search Retrieval Augmented Generation \(RAG\) application to recognize your custom embedding model and use it for generating embeddings. For more information, see [Connect your custom embedding model with the Generative AI application](../task/connect-em-with-genai.md).
5.  Manage errors from custom embedding models when generating semantic vectors. For more information, see [Create an error handler extension point](../task/create-error-handler-extention-point.md).
6.  Add your new embedding model to the semantic indexing table to enable it for semantic indexing. For more information, see [Enable the custom embedding model for semantic indexing](../task/enable-byom-for-semnatic-indexing.md).
7.  Activate your preferred embedding model so the AI Search RAG application can use it for generating embeddings. For more information, see [Activate a third-party embedding model](../task/activate-3p-embedding-model.md).
8.  Select your preferred embedding model to use for semantic indexing. For more information, see [Configure semantic indexing settings for an indexed source](../task/configure-semantic-indexing-ais.md).

-   **[Create a custom embedding model](../task/create-byom.md)**  
Create a custom embedding model in the Generative AI Model Configuration \[sys\_generative\_ai\_model\_config\] table so that your AI Search Retrieval Augmented Generation \(RAG\) application can use it to generate embeddings for semantic indexing. This setup ensures that the model is recognized and properly connected to send and receive requests.
-   **[Set a provider for an embedding model](../task/set-provider-for-byom.md)**  
Determine which AI provider to use so that your embedding model can work in the AI Search Retrieval Augmented Generation \(RAG\) application.
-   **[Connect your custom embedding model with the Generative AI application](../task/connect-em-with-genai.md)**  
Integrate your custom embedding model with a capability definition to help the Generative AI application understand your data better and deliver more relevant, tailored responses.
-   **[Create an error handler extension point](../task/create-error-handler-extention-point.md)**  
Create a scripted extension point to handle the embedding generation errors that occur when custom embedding models in the AI Search Retrieval Augmented Generation \(RAG\) application generate semantic vectors.
-   **[Enable the custom embedding model for semantic indexing](../task/enable-byom-for-semnatic-indexing.md)**  
Add a new embedding model in the semantic indexing table so that the AI Search Retrieval Augmented Generation \(RAG\) application can use this model for semantic indexing.

**Parent Topic:**[Configuring an external or custom embedding model](setting-up-3p-embedding-models.md)

