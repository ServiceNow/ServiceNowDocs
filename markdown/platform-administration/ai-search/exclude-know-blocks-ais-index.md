---
title: Exclude knowledge block content from the AI Search index
description: Prevent AI Search from indexing content found in your knowledge blocks.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-16"
reading_time_minutes: 1
breadcrumb: [Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Exclude knowledge block content from the AI Search index

Prevent AI Search from indexing content found in your knowledge blocks.

## Before you begin

Role required: admin

## About this task

AI Search includes content specified in your published knowledge blocks when it indexes content and metadata from your knowledge articles.

Administrators can override this default behavior and exclude your knowledge block content from the search index by setting the value of the **glide.ais.disable\_kbb** system property. If this system property's value is set to **true**, AI Search ignores knowledge block content when indexing content and metadata from your knowledge articles.

To learn more about creating and publishing knowledge blocks for reference in your knowledge articles, see [Using knowledge blocks](https://www.servicenow.com/docs/access?context=using-knowlege-blocks&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Search for a system property record with name **glide.ais.disable\_kbb**.

    -   If a system property record with this name exists, open the record by selecting it.
    -   If no system property record with this name exists, select **New**, then enter `glide.ais.disable_kbb` in the System Property form's **Name** field.
3.  In the System Property form's **Value** field, enter **true**.

4.  Save the modified System Property record by selecting **Submit** or **Update**.


## What to do next

To make the new setting take effect, reindex the Knowledge Table indexed source. For details on reindexing, see [Perform a full table index or reindex for a single AI Search indexed source](index-single-source-ais.md).

**Parent Topic:**[Indexed sources in AI Search](../concept/indexed-sources-ais.md)

