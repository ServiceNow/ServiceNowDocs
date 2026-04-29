---
title: Remove an index
description: You can remove the index for a table if you no longer want the search engine to return results for that table. This procedure also removes the index for all tables that extend the specified table.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Remove an index

You can remove the index for a table if you no longer want the search engine to return results for that table. This procedure also removes the index for all tables that extend the specified table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Open the dictionary record for the table.

    The dictionary record for a table is the record with **Table** matching the table's name, an empty column name, and a **Type** value of **Collection**, as shown in the following example image.

    ![Dictionary Entry table showing a table's dictionary record with matching Table name, empty Column name and Type value of Collection.](../image/table-dictionary-record.png)

3.  If the **Text index** option field is hidden, configure the form layout to show it.

    For details on showing and hiding fields on a form, see [Configuring the form layout](../../form-administration/concept/configure-form-layout.md#).

4.  Clear the record's **Text index** option, then select **Update**.


## Result

The system no longer indexes text from the specified table or queries it for text search results. This change also disables text indexing and search for all tables that extend the specified table.

**Parent Topic:**[Zing indexes words](../concept/zing-indexes-words.md)

**Related topics**  


[Zing indexes punctuation as part of some words](../concept/c_PunctuationForSearchResults.md)

[Zing indexes some HTML elements](../concept/c_SearchingHTMLContent.md)

[Configure a table for indexing and searching](configure-single-table-for-indexing.md#)

[Configure a text index group to search across multiple tables](index-multiple-tables.md)

[Zing index and search dictionary attributes](../reference/index-attributes.md)

[Regenerate a text index for a table](t_RegenerateATextIndexForATable.md)

[Remove an index for a specific field](t_RemoveAnIndexForASpecificField.md)

[Remove the text index for a child table](remove-index-child-table.md)

[Change the query mode of an indexed table](configure-table-query-mode.md)

[Enable indexing of text in multi-row variable sets](index-text-multi-row-variable-sets.md)

[Text indexing statistics and status](../reference/r_ViewTextIndexingStatsAndStatus.md)

[Configure tables to use the Japanese tokenizer](configure-tables-japanese-tokenizer.md)

