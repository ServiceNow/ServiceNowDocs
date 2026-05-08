---
title: Configure Zing tag indexing for text search
description: Zing text indexing is available for tags on records.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tags, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Configure Zing tag indexing for text search

Zing text indexing is available for tags on records.

## Before you begin

Text indexing must be enabled for the table that you want to index tags for. For instructions for this procedure, see Configure a table for indexing and searching.

Role required: admin

## About this task

By default, the Zing text indexing and search engine does not index tag text for search. You can enable text indexing of tags on a table-by-table basis. Private tags are never indexed.

When you enable text indexing for a table's tags, Zing stores search data for the tags in its text index for that table. This increases the text index's size. The exact increase depends on the number of indexable tags present in records on the table.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary** and edit the dictionary entry for the table you want to enable tag indexing for.

    The dictionary entry for a table is the record with the table's name as its **Table** field value, an empty **Column name** field, and a **Type** value of `Collection`.

2.  In the Attributes related list, select **New**.

3.  Select the Lookup using list icon \(![Lookup using list icon](../../../administer/ai-search/image/icon-lookup-using-list.png)\) to see all available attributes.

4.  Select the **Text Index Tags** attribute \(**text\_index\_tags**\).

5.  For the attribute value, enter one of the following options.

    |Option|Description|
    |------|-----------|
    |everyone\_only|Only tags shared with everyone are indexed.|
    |all\_shared|All shared tags \(**Everyone**, **Groups and Users**\) are indexed.|

6.  Select **Submit**.

7.  In the Dictionary Entry form's Related Links section, select **Generate Text Index** to reindex the table.


## What to do next

After you turn on text indexing for tags on a table, records on the table are reindexed when any of the following actions occurs.

-   When you add or remove tags.
-   When you modify a tag, as long as fewer than 100 records are affected. If there are more records, you must manually reindex.
-   When you manually reindex an entire table \(required after initial tag indexing setup\).

**Parent Topic:**[Tags](../concept/c_Tags.md)

