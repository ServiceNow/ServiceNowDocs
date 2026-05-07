---
title: Enable indexing of tags for an AI Search indexed source
description: Configure an indexed source attribute to enable indexing of content from tags found on records from an indexed source.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Indexed source attributes, Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable indexing of tags for an AI Search indexed source

Configure an indexed source attribute to enable indexing of content from tags found on records from an indexed source.

## Before you begin

Role required: ais\_admin

## About this task

By default, AI Search indexing ignores tags from source records. You can enable indexing of tags for all records from an indexed source. Choose whether you want to index all shared and globally visible tags or only globally visible tags. Private tags are never indexed.

For more general instructions on defining indexed source attributes, see [Create an indexed source attribute in AI Search](create-indexed-source-attr-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Open the indexed source that you want to enable tag indexing for.

3.  In the Advanced Configuration related list, select **New**.

4.  On the Indexed Source Attribute form, fill in the fields.

    1.  In the **Attribute** field, enter `index_tags`.

    2.  In the **Value** field, enter one of the following options:

    |Option|Description|
    |------|-----------|
    |everyone\_only|Only tags shared with everyone are indexed.|
    |all\_shared|All shared tags \(**Everyone**, **Groups and Users**\) are indexed.|

    For a description of the field values, see [Indexed Source Attribute form](../reference/indexed-source-attribute-form-ais.md).

5.  Select **Submit**.


## Result

The new **index\_tags** indexed source attribute appears in the Advanced Configuration related list.

## What to do next

To make the new **index\_tags** attribute take effect, perform a full table reindex for the indexed source. For details on this procedure, see [Perform a full table index or reindex for a single AI Search indexed source](index-single-source-ais.md).

**Parent Topic:**[Indexed source attributes for AI Search](../concept/indexed-source-attributes-ais.md)

