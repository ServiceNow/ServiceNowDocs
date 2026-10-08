---
title: Configuring your embedding model
description: Connect and configure your external or custom embedding model to enable it generate embeddings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/setting-up-3p-embedding-models.html
release: brazil
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [AI Search RAG \(Retrieval-Augmented Generation\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring your embedding model

Connect and configure your external or custom embedding model to enable it generate embeddings.

ServiceNow AI Search RAG application offers a Bring Your Own Model \(BYOM\) feature that you can use to create your own custom embedding model. It also supports third-party embedding models such as Azure OpenAI Embedding model and Gemini Text Embedding model for generating embeddings. You can use the default connection and credential aliases provided for the Azure OpenAI and Gemini embedding models. These aliases can be configured based on your requirements to authenticate and enable integration between your instance and the selected embedding model.

The end-to-end configuration for your preferred third-party embedding model includes:

-   [Setting up connection and credentials for third-party embedding model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/setup-alias-for-3p-embedding-model.md)
-   [Activating the third-party embedding model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/activate-3p-embedding-model.md)

The end-to-end configuration for your custom embedding model includes using the BYOM capability. For more information see, [Configuring bring your own model \(BYOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/creating-byom.md).

