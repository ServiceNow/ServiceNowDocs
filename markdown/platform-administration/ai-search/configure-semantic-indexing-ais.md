---
title: Configure semantic indexing settings for an indexed source
description: Specify the semantic indexing configuration settings you want to apply when AI Search indexes records from your indexed sources.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-03"
reading_time_minutes: 2
breadcrumb: [Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Configure semantic indexing settings for an indexed source

Specify the semantic indexing configuration settings you want to apply when AI Search indexes records from your indexed sources.

## Before you begin

The AI Search Semantic Controller plugin \(com.glide.ais.semantic\_search\) must be active on your instance. This plugin is automatically activated when any [Now Assist application](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) is installed on your instance.

Role required: ais\_admin

## About this task

As an AI Search admin, you can perform this task to choose the fields from and indexed source's table that you want the system to index for semantic vector search. You can also choose the embedding models and content chunking strategy to use for semantically-indexed content from the source table.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Select the indexed source that you want to configure semantic indexing settings for.

    The selected indexed source opens in Indexed Source form view.

3.  In the Semantic Index Configuration related list, select **New**.

    **Note:** If you don't see the Semantic Index Configuration related list on the Indexed Source form, check with your administrator to make sure that your instance has at least one [Now Assist application](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) installed. Installing any Now Assist application activates the AI Search Semantic Controller plugin \(com.glide.ais.semantic\_search\), which is required for semantic index configuration.

4.  On the Semantic Index Configuration form, fill in the fields.

    For a description of the field values, see [Semantic Index Configuration form](../reference/semantic-index-configuration-form.md).

5.  Select **Submit**.

    If you're updating an existing semantic index configuration, select **Update** instead.

    The Semantic Index Configuration form reloads and displays your selected field values and the Semantic Index Fields related list.

6.  In the Semantic Index Fields related list, create a new record for each field with content that you want to include in the semantic index for the specified indexed source.

    1.  Select **New**.

    2.  On the Semantic Index Field form, fill in the fields.

        For a description of the field values, see [Semantic Index Field form](../reference/semantic-index-field-form.md).

    3.  Select **Submit**.

        The new semantic index field record appears in the Semantic Index Fields related list.


## What to do next

After changing the semantic index configuration settings for an indexed source, you need to reindex content from that indexed source. For reindexing steps, see [Perform a full table index or reindex for a single AI Search indexed source](index-single-source-ais.md).

**Note:** Indexing content for semantic vector search is typically slower than indexing for keyword search. Your indexed source may take more time to reindex once you've defined a semantic index configuration for it.

**Parent Topic:**[Semantic index configuration for indexed sources](../concept/semantic-index-cfg-ais.md)

