---
title: Create an indexed source attribute in AI Search
description: Define an indexed source attribute to configure the AI Search content indexing behavior for all records on a source table.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Indexed source attributes, Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an indexed source attribute in AI Search

Define an indexed source attribute to configure the AI Search content indexing behavior for all records on a source table.

## Before you begin

Role required: ais\_admin

## About this task

For details on available indexed source attributes and values, see [List of AI Search indexed source attributes](../reference/indexed-source-attrs-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Open the indexed source that you want to define an attribute for.

3.  In the Advanced Configuration related list, select **New**.

4.  On the Indexed Source Attribute form, fill in the fields.

    For a description of the field values, see [Indexed Source Attribute form](../reference/indexed-source-attribute-form-ais.md).

5.  Select **Submit**.


## Result

The new indexed source attribute appears in the Advanced Configuration related list.

## What to do next

To make the new indexed source attribute take effect, perform a full table reindex for the indexed source. For details on this procedure, see [Perform a full table index or reindex for a single AI Search indexed source](index-single-source-ais.md).

**Parent Topic:**[Indexed source attributes for AI Search](../concept/indexed-source-attributes-ais.md)

