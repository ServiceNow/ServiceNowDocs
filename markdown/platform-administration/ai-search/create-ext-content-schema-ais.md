---
title: Create an external content schema table
description: Define a schema table with columns corresponding to fields on records from an external data source. AI Search uses the schema when indexing content from the external data source.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Indexing and searching external content, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an external content schema table

Define a schema table with columns corresponding to fields on records from an external data source. AI Search uses the schema when indexing content from the external data source.

## Before you begin

Role required: ais\_admin

## About this task

An external content schema table doesn't store data in the database. Instead, its columns serve as a map of AI Search index fields to populate when you index content from external data sources.

When you index or delete records associated with this content schema using endpoints from the External Content Ingestion REST API, you must specify the schema table name as a path parameter.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **External Content** &gt; **Create Schema**.

2.  Enter a name for your new external source schema table.

3.  Select **Submit**.

    The new external content schema table opens in list view.

4.  If you need to define additional field mappings for records from the external data source, add a new column for each field.

    1.  In the Columns related list, select **New**.

    2.  On the Dictionary Entry form, fill in the fields.

        For descriptions of these form fields, see [Dictionary Entry form](../../data-dictionary-tables/reference/r_DictionaryEntryForm.md).

        **Note:** When filling in the **Type** field, select **String**, **Date**, **Date/Time**, or **Integer**. AI Search doesn't support other column types on external content schema tables.

    3.  Select **Submit**.

5.  If you modified the default column set, select **Update** to save your changes.


## What to do next

Create a new indexed source with your external content schema table defined as its source. For instructions on creating an indexed source, see [Create an indexed source](create-indexed-source-ais.md)

**Parent Topic:**[Indexing and searching external content in AI Search](../concept/external-content-ais.md)

