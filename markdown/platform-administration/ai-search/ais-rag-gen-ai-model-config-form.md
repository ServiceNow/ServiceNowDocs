---
title: Generative AI model configuration form
description: The Generative AI model configuration form contains information about a custom embedding model that your AI Search Retrieval Augmented Generation \(RAG\) application uses to generate embeddings for semantic indexing. Use this form when creating or modifying a custom embedding model.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-08-25"
reading_time_minutes: 1
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer]
---

# Generative AI model configuration form

The Generative AI model configuration form contains information about a custom embedding model that your AI Search Retrieval Augmented Generation \(RAG\) application uses to generate embeddings for semantic indexing. Use this form when creating or modifying a custom embedding model.

For details on creating or modifying a custom embedding model, see [Create a custom embedding model](../task/create-byom.md).

<table id="id_zlx_lbc_lgc"><thead><tr><th>

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

Unique name for the embedding model.

</td></tr><tr><td>

Domain

</td><td>

Domain that you want to associate the model with. For example, AI Search RAG.

</td></tr><tr><td>

External

</td><td>

Option to make this model to be used externally.

</td></tr><tr><td>

Connection and Credential Alias

</td><td>

Connection and credential alias that you created on your own for the custom embedding model.

</td></tr><tr><td>

Supported Language

</td><td>

Languages that are supported for this model. By default, the supported language is English.The current available languages for your third party supported custom embedding model are as follows: Brazilian Portuguese, Chinese, Chinese \(traditional\), Dutch, English, Finnish, French, French Canadian, German, Estonian, Italian, Japanese, Korean, Norwegian, Arabic, Pseudo, Polish, Portuguese, Russian, Turkish, Hebrew, Hungarian, Czech, Thai, Spanish, and Swedish.

</td></tr><tr><td>

Model Type

</td><td>

Type of model that is used for a specific purpose. For example, Embedding Model.

</td></tr><tr><td>

Vector Dimension

</td><td>

Vector dimension value that shouldn't exceed 4096.This field appears only if you have selected `Embedding Model` in the **Model Type** field.

</td></tr><tr><td>

Application

</td><td>

Name of the application that this model is configured for.

</td></tr><tr><td>

Provider

</td><td>

Name of the generative AI provider mapping. For example, Generic Embedder.

</td></tr><tr><td>

Max Tokens

</td><td>

Maximum limit to generate embeddings.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

