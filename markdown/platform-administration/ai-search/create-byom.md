---
title: Create a custom embedding model
description: Create a custom embedding model in the Generative AI Model Configuration \[sys\_generative\_ai\_model\_config\] table so that your AI Search Retrieval Augmented Generation \(RAG\) application can use it to generate embeddings for semantic indexing. This setup ensures that the model is recognized and properly connected to send and receive requests.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring bring your own model \(BYOM\), Configuring an external or custom embedding model, AI Search Retrieval Augmented Generation \(RAG\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a custom embedding model

Create a custom embedding model in the Generative AI Model Configuration \[sys\_generative\_ai\_model\_config\] table so that your AI Search Retrieval Augmented Generation \(RAG\) application can use it to generate embeddings for semantic indexing. This setup ensures that the model is recognized and properly connected to send and receive requests.

## Before you begin

You must create a connection and credential alias for your embedding model. For more information, see [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_generative_ai_model_config.list` in the filter to go to the Generative AI Model Configuration \[sys\_generative\_ai\_model\_config\] table.

2.  Select **New**.

3.  On the form, fill in the fields.

    For a description of the field values, see .

4.  Select **Submit**.


## Result

The new embedding model is created.

## What to do next

Set a provider for the embedding model.

**Parent Topic:**[Configuring bring your own model \(BYOM\)](../concept/creating-byom.md)

