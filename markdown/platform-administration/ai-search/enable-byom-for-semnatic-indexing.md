---
title: Enable the custom embedding model for semantic indexing
description: Add your newly created embedding model in the semantic indexing table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/enable-byom-for-semnatic-indexing.html
release: brazil
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable the custom embedding model for semantic indexing

Add your newly created embedding model in the semantic indexing table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `ais_symantic_embedding_model.list` in the filter to go to the AI Search Semantic Embedding Models \[sys\_generative\_ai\_config\] table.

2.  Select **New**.

3.  In the **Name** field, enter a unique name.

4.  In the Model Id field, enter a unique id.

5.  In the **One Extend Capability Definition** field, select a BYOM capability definition you created to set a provider for embedding model.

6.  In the **Model Config** field, select a configured embedding model.

7.  Select the **Active** option.

8.  Select the **Batching Supported** option if you want to configure batching for your embedding model.

9.  In the **Minimum Batch Size** and **Maximum Batch Size** fields, enter the required values.

10. In the **Error Handler Extension Instance** field, select an error handler instance.

    For more information, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/create-error-handler-extention-point.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/create-error-handler-extention-point.md).

11. Select **Submit**.


## What to do next

Add your embedding model to the semantic index configuration to enable content ingestion using that model. For more information, see [Configure semantic indexing settings for an indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/configure-semantic-indexing-ais.md).

