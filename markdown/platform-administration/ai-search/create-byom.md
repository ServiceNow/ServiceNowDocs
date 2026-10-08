---
title: Create a custom embedding model
description: Create your custom embedding model in the Generative AI Model Configuration table so that your AI Search RAG application can use it to generate embeddings for semantic indexing. This setup ensures the model is recognized and properly connected to send and receive requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/create-byom.html
release: brazil
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring bring your own model \(BYOM\), Configuring your embedding model, AI Search RAG \(Retrieval-Augmented Generation\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a custom embedding model

Create your custom embedding model in the Generative AI Model Configuration table so that your AI Search RAG application can use it to generate embeddings for semantic indexing. This setup ensures the model is recognized and properly connected to send and receive requests.

## Before you begin

You must create a connection and credential alias for your embedding model. For more information, see [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/connection-alias.md)

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_generative_ai_model_config.list` in the filter to go to the Generative AI Model Configuration \[sys\_generative\_ai\_model\_config\] table.

2.  Select **New**.

3.  On the form, fill in the fields.

4.  <table id="table_ynd_bjk_bgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option to activate the embedding model.

</td></tr><tr><td>

Model

</td><td>

A unique name for your embedding model.

</td></tr><tr><td>

Domain

</td><td>

Domain you want to associate the model with. For example, AI Search RAG.

</td></tr><tr><td>

External

</td><td>

Option to make this model available for external use.

</td></tr><tr><td>

Connection and Credential Alias

</td><td>

Connection and credential alias that you created on your own for the custom embedding model.

</td></tr><tr><td>

Supported Language

</td><td>

Languages supported for this model. By default, the supported language is English.

</td></tr><tr><td>

Model Type

</td><td>

The type of model used for a specific purpose. For example Embedding Model.

</td></tr><tr><td>

Vector Dimension

</td><td>

The value shouldn't exceed 4096.This field appears only if you have selected `Embedding Model` in the **Model Type** field.

</td></tr><tr><td>

Application

</td><td>

Name of the application this model is configured for.

</td></tr><tr><td>

Provider

</td><td>

Name of the Generative AI provider mapping.

</td></tr><tr><td>

Max Tokens

</td><td>

Maximum limit to generate embeddings.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

The new embedding model is created.

## What to do next

Set a provider for an embedding model.

