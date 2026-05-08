---
title: Enable indexing of text in multi-row variable sets
description: Make text from multi-row Service Catalog variable sets searchable in global search.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable indexing of text in multi-row variable sets

Make text from multi-row Service Catalog variable sets searchable in global search.

## Before you begin

Role required: admin

## About this task

By default, Zing doesn't index text from multi-row Service Catalog variable sets. Global search doesn't return results for text in these variable sets.

Administrators can override this default behavior by adding the **glide.ts.index.variableset**system property and setting its value to **true**. With this value set, Zing indexes text in multi-row variable sets, and global search returns results for that text.

To learn more about variable sets, see Service catalog variable sets.

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Search the table for a system property with name **glide.ts.index.variableset**.

    -   If the property already exists, change its value to **true** and skip the following steps.
    -   If the property doesn't exist, go on to the following steps.
3.  Select **New**.

4.  On the System Property form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Name|glide.ts.index.variableset|
    |Type|true \| false|
    |Value|true|

5.  Select **Submit**.


## Result

Zing indexes text from multi-row Service Catalog variable sets so that you can find it using global search.

## What to do next

To see text from multi-row variable sets immediately in global searches, regenerate the text indexes for the affected tables. For details on this procedure, see [Regenerate a text index for a table](t_RegenerateATextIndexForATable.md).

If you don't regenerate the text indexes for the affected tables, records on those tables will be reindexed as they are updated or added. Global searches will only return text from multi-row variable sets on reindexed records.

**Parent Topic:**[Zing indexes words](../concept/zing-indexes-words.md)

**Related topics**  


[Zing indexes punctuation as part of some words](../concept/c_PunctuationForSearchResults.md)

[Zing indexes some HTML elements](../concept/c_SearchingHTMLContent.md)

[Configure a table for indexing and searching](configure-single-table-for-indexing.md#)

[Configure a text index group to search across multiple tables](index-multiple-tables.md)

[Zing index and search dictionary attributes](../reference/index-attributes.md)

[Regenerate a text index for a table](t_RegenerateATextIndexForATable.md)

[Remove an index](t_RemoveAnIndex.md)

[Remove an index for a specific field](t_RemoveAnIndexForASpecificField.md)

[Remove the text index for a child table](remove-index-child-table.md)

[Change the query mode of an indexed table](configure-table-query-mode.md)

[Text indexing statistics and status](../reference/r_ViewTextIndexingStatsAndStatus.md)

[Configure tables to use the Japanese tokenizer](configure-tables-japanese-tokenizer.md)

