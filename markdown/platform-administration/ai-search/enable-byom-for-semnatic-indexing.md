---
title: Enable the custom embedding model for semantic indexing
description: Add a new embedding model in the semantic indexing table so that the AI Search Retrieval Augmented Generation \(RAG\) application can use this model for semantic indexing.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring bring your own model \(BYOM\), Configuring an external or custom embedding model, AI Search Retrieval Augmented Generation \(RAG\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Enable the custom embedding model for semantic indexing

Add a new embedding model in the semantic indexing table so that the AI Search Retrieval Augmented Generation \(RAG\) application can use this model for semantic indexing.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `ais_semantic_embedding_model.list` in the filter to go to the AI Search Semantic Embedding Models \[sys\_generative\_ai\_config\] table.

2.  Select **New**.

3.  In the **Name** field, enter a unique name.

    For example, Azure OpenAI Large Text Embedding.

4.  In the **Model Id** field, enter a unique ID.

    An ID starts with a letter or number and may include letters, digits, periods \(.\), or hyphens \(-\) after the first character.

5.  In the **One Extend Capability Definition** field, select a BYOM capability definition that you created to set a provider for the embedding model.

6.  In the **Model Config** field, select an embedding model that is already configured.

7.  Select **Active**.

8.  If you want to configure batching for your embedding model, do these steps:

    Batching helps the embedding model to process multiple inputs at once. The minimum and maximum batch size values control how inputs are grouped and processed to call the embedding generation API.

    1.  Select **Batching Supported**.

    2.  In the **Minimum Batch Size** and **Maximum Batch Size** fields, enter the required values.

        For example, the minimum number of inputs allowed in a single batch is 4 and the maximum number of inputs that can be processed together in one batch is 16.

9.  In the **Error Handler Extension Instance** field, select an error handler instance.

    You create a scripted extension point to handle embedding generation errors that occur when custom embedding models generate semantic vectors. For more information, see [Create an error handler extension point](create-error-handler-extention-point.md).

10. Select **Submit**.


## What to do next

Add your embedding model to the semantic index configuration to enable content ingestion with that model. For more information, see [Configure semantic indexing settings for an indexed source](configure-semantic-indexing-ais.md).

