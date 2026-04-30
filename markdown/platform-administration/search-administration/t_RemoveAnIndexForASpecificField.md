---
title: Remove an index for a specific field
description: You can remove the index for a specific field in a table if you no longer want the search engine to return results for that field.
locale: en-US
release: zurich
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer]
---

# Remove an index for a specific field

You can remove the index for a specific field in a table if you no longer want the search engine to return results for that field.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Open the dictionary record for the table field.

    The dictionary record for a table field is the record with **Table** matching the table's name and **Column name** matching the field's name, as shown in the following example image.

    ![Dictionary Entry table showing a table field's dictionary record with matching Table and Column name.](../image/table-field-dictionary-record.png)

3.  In the Attributes related list, select **New**.

4.  On the Dictionary Attribute form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Attribute|No text index|
    |Value|true|

5.  Select **Submit**.

6.  Select **Update**.


## Result

The system no longer indexes text from the specified table field or queries it for text search results. This change also disables text indexing and search for the specified field in all tables that extend the specified table.

**Parent Topic:**[Zing indexes words](../concept/zing-indexes-words.md)

**Related topics**  


[Zing indexes punctuation as part of some words](../concept/c_PunctuationForSearchResults.md)

[Zing indexes some HTML elements](../concept/c_SearchingHTMLContent.md)

[Configure a table for indexing and searching](configure-single-table-for-indexing.md#)

[Configure a text index group to search across multiple tables](index-multiple-tables.md)

[Zing index and search dictionary attributes](../reference/index-attributes.md)

[Regenerate a text index for a table](t_RegenerateATextIndexForATable.md)

[Remove an index](t_RemoveAnIndex.md)

[Remove the text index for a child table](remove-index-child-table.md)

[Change the query mode of an indexed table](configure-table-query-mode.md)

[Enable indexing of text in multi-row variable sets](index-text-multi-row-variable-sets.md)

[Text indexing statistics and status](../reference/r_ViewTextIndexingStatsAndStatus.md)

[Configure tables to use the Japanese tokenizer](configure-tables-japanese-tokenizer.md)

