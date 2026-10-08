---
title: Activate the third-party embedding model
description: Activate your preferred embedding model so that your AI Search RAG application knows which model to use for generating embeddings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/activate-3p-embedding-model.html
release: brazil
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring your embedding model, AI Search RAG \(Retrieval-Augmented Generation\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate the third-party embedding model

Activate your preferred embedding model so that your AI Search RAG application knows which model to use for generating embeddings.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** and then enter `ais_semantic_embedding_model.list` in the filter.

2.  Select an embedding model from the list of AI Search Semantic Embedding Models.

    The selected AI Search Semantic Embedding Model page opens.

3.  Select the **Active** option to turn on the embedding model.

4.  Select **Update**.

5.  Select the **Validate** button to run a quick check if everything is setup correctly.

    **Note:** You must validate the embedding model if you make any changes to its configuration.


## Result

The preferred embedding model ready to use in the AI Search RAG application.

## What to do next

Add your embedding model to the semantic index configuration to enable content ingestion using that model. For more information, see [Configure semantic indexing settings for an indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/configure-semantic-indexing-ais.md).

