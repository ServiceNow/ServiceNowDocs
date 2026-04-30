---
title: Define the semantic indexing configuration for an indexed source
description: Define the semantic indexing configuration for your indexed sources so that AI Search can analyze and understand your content accurately. By doing this process, you can help to ensure that you get more relevant search results.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing the indexed sources from the AI Search Admin console, Using the AI Search Admin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Define the semantic indexing configuration for an indexed source

Define the semantic indexing configuration for your indexed sources so that AI Search can analyze and understand your content accurately. By doing this process, you can help to ensure that you get more relevant search results.

## Before you begin

Role required: admin or ais\_admin

## About this task

AI Search indexes content from the indexed source for use with a semantic vector search. The group of semantic indexing settings for a particular indexed source is called a semantic index configuration. For more information, see [Semantic index configuration for indexed sources](../concept/semantic-index-cfg-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  On the **Shared Configurations** tab, select the **Indexed Sources** table.

3.  Select the indexed source that you want to configure the semantic indexing settings for.

    The selected indexed source opens in the Configuration form view.

4.  In the Semantic indexing configurations section, select **Edit**.

5.  On the Semantic Indexing form, select **Create**.

6.  On the form, fill in the fields.

    For a description of the field values, see [Semantic Index Configuration form](../reference/semantic-index-configuration-form.md).

7.  Select **Save**.

    The Semantic indexing configuration form reloads and displays your selected field values and the Semantic fields section.

8.  In the Semantic fields section, follow these steps for each field that contains the content you want to include in the semantic index for the specified indexed source.

    1.  Select **Add**.

    2.  On the form, fill in the fields.

        For a description of the field values, see [Semantic Index Field form](../reference/semantic-index-field-form.md).

    3.  Select **Add**.

    The new semantic field configuration appears in the Semantic fields section.


## What to do next

After updating the semantic index configuration settings for an indexed source, you must index or reindex the content from that indexed source. For more information, see [Index the content from an indexed source for searchability](ais-admin-console-start-content-indexing.md).

**Parent Topic:**[Managing the indexed sources from the AI Search Admin console](../concept/ais-managing-indexed-source.md)

