---
title: Activate a third-party embedding model
description: Activate your preferred embedding model, whether third-party or custom, so that the AI Search Retrieval Augmented Generation \(RAG\) application knows which model to use for generating embeddings.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring an external or custom embedding model, AI Search Retrieval Augmented Generation \(RAG\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate a third-party embedding model

Activate your preferred embedding model, whether third-party or custom, so that the AI Search Retrieval Augmented Generation \(RAG\) application knows which model to use for generating embeddings.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** and then enter `ais_semantic_embedding_model.list` in the filter.

2.  Select an embedding model from the list of AI Search Semantic Embedding Models.

3.  On the Semantic Embedding Model page, turn on the embedding model by selecting **Active**.

4.  Select **Update**.

5.  Run a quick check to verify that everything is set up correctly by selecting **Validate**.

    **Note:** If you make any changes to its configuration, you must validate the embedding model.


## Result

Your preferred embedding model, whether third-party or custom, is ready to use in the AI Search Retrieval Augmented Generation \(RAG\) application.

## What to do next

Add your embedding model to the semantic index configuration to enable content ingestion by using that model. For more information, see [Configure semantic indexing settings for an indexed source](configure-semantic-indexing-ais.md).

**Parent Topic:**[Configuring an external or custom embedding model](../concept/setting-up-3p-embedding-models.md)

