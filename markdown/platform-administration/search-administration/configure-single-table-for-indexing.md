---
title: Configure a table for indexing and searching
description: Enable Zing text indexing for a table to allow users to search its records for string values. Configure the table's text indexing attributes, stop words, and synonym dictionaries to control search behavior.Text indexing excludes fields that meet certain name, type, attribute, or encryption conditions. User searches don't match or return values from excluded fields.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure a table for indexing and searching

Enable Zing text indexing for a table to allow users to search its records for string values. Configure the table's text indexing attributes, stop words, and synonym dictionaries to control search behavior.

## Before you begin

Role required: ts\_admin or admin

## About this task

Enabling text indexing for a table allows users to search for string values in records on that table. You can configure attributes, stop words, and synonym dictionaries to control indexing and search behavior for an indexed table.

By default, the system creates text indexes for the tables with a Text index record \(**All** &gt; **System Definition** &gt; **Text Indexes**\). For example:

-   Knowledge-related tables
-   Core-data-related tables
-   Connect-related tables
-   Task table
-   User table

Enabling text indexing for a table also enables it for all child tables. If you want to disable text indexing for a child table, see [Remove the text index for a child table](remove-index-child-table.md).

**Note:** Whenever you create an index table, the system also creates Access Control Roles \(ACLs\) for new tables.

Text indexing can be a resource-intensive task that may take a while to complete. You may notice performance degradation or incomplete search results during index generation. To estimate text indexing duration, you can [view historical text indexing statistics](../reference/r_ViewTextIndexingStatsAndStatus.md).

**Note:**

New tables created by update set transfers have text indexing disabled, even if it's enabled for the tables included in the update set.

To enable users to search tables created by update set transfers, you must manually enable text indexing for those tables.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Text Index Configurations** and select **New**.

2.  In **Applies to**, select **Table**.

3.  In **Table**, select the table that you want to configure text indexing for.

4.  If you intend to use the table in multi-table searches or if you want to use the BM25 scoring algorithm on the table, upgrade its indexing format to V4.

    1.  If the value in **Format** isn't grayed out, select **v4**, then select **Submit** and skip to step [5](configure-single-table-for-indexing.md#configure-indexing).

    2.  If the value in **Format** is grayed out, select **Submit**.

        The grayed-out value means that the table has already been indexed and needs its indexing upgraded to V4.

    3.  Navigate to **All** &gt; **System Definition** &gt; **Text Index Configurations** and select the table you submitted.

    4.  Under **Related Links**, select **Show index name record**.

    5.  Under **Related Links**, select **Upgrade to V4** and select **Submit**.

        The specified table's indexing is upgraded from V3 to V4. Now, this table can be part of multiple-table indexing and BM25 is used to score the table's relevance score. Optionally, select **Show Configuration** under **Related Links**to show the table indexing format on the **Text Index Configuration** page.

5.  Configure indexing and search attributes on the selected table.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Text Index Configurations** and select the table you configured.

    2.  In the Text Index Table Attribute Maps related list, select **New**.

        Attributes pertain to the way Zing indexes documents and ranks documents returned in search results.

    3.  On the Text Index Table Attribute Maps form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Table|Table to define attributes for.|
        |Attribute name|Search engine attribute. For a list of the attributes and valid values, see [Zing index and search attributes](../reference/index-attributes.md).|
        |Value|Value for attribute.|

    4.  Repeat this procedure to define additional attributes for the table.

    5.  In the Related Links section, select **Generate Text Index**.

6.  Configure column-level attributes.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Text Index Configurations** and select a table.

    2.  In the Text Index Column Attribute Maps related list, select **New**.

    3.  On the Text Index Column Attribute Map form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Table|Table that contains the column you want to define attributes for. Only tables in the index group and their child tables display.|
        |Attribute name|Attribute. For a list of the attributes and valid values, see [Zing index and search attributes](../reference/index-attributes.md).|
        |Column|The name of the column in the selected table you want to apply the search attribute to.|
        |Value|Value for attribute.|

    4.  Select **Submit**.

    5.  Repeat this procedure to define additional search engine parameters for table columns in the index group.

    6.  In the Related Links section, select **Generate Text Index**.

7.  Add stop words.

    Stop words are words that you don't want to index, such as `the`, `a`, or `an`. There is a global list of common stop words, so you only have to add stop words specific to your situation. To see the global list of stop words, navigate in your browser to `https://<instance name>.service-now.com/ts_stop_list.do`.

    1.  On the **Index Stop Words** tab, select **New**.

    2.  In **Index**, select the index to add the stop word to.

    3.  In **Word**, enter a single word you don't want to index and select **Submit**.

8.  Add a synonym dictionary.

    Specifying a synonym dictionary searches on the search term as well as synonyms of the search term, such as car, and its synonym, auto. Zing provides a default synonym dictionary.

    1.  On the **Index synonym Dictionaries** tab, select **New**.

    2.  In **Index**, select the index to add the stop words to.

    3.  In **Synonym dictionary**, select the synonym dictionary to use on the specified table.

        To add a dictionary, select **New** and follow the procedure in [Create synonym dictionaries](create-synonym-dictionaries.md).


## Result

The list search for text option appears on the list views for the table and its child tables.

## What to do next

You can search records on the indexed table using list search in form view. To learn more about using list search, see [List search finds records from the current table](../concept/c_TextSearchesInRecordLists.md).

You can also query the indexed table for string matches using the `GlideRecord.addQuery(name, value)` or `GlideRecord.addEncodedQuery(name, value)` methods with the `123TEXTQUERY321` reserved name. For more information about querying for string matches, see Querying tables in script.

**Parent Topic:**[Zing indexes words](../concept/zing-indexes-words.md)

**Related topics**  


[Zing indexes punctuation as part of some words](../concept/c_PunctuationForSearchResults.md)

[Zing indexes some HTML elements](../concept/c_SearchingHTMLContent.md)

[Configure a text index group to search across multiple tables](index-multiple-tables.md)

[Zing index and search dictionary attributes](../reference/index-attributes.md)

[Regenerate a text index for a table](t_RegenerateATextIndexForATable.md)

[Remove an index](t_RemoveAnIndex.md)

[Remove an index for a specific field](t_RemoveAnIndexForASpecificField.md)

[Remove the text index for a child table](remove-index-child-table.md)

[Change the query mode of an indexed table](configure-table-query-mode.md)

[Enable indexing of text in multi-row variable sets](index-text-multi-row-variable-sets.md)

[Text indexing statistics and status](../reference/r_ViewTextIndexingStatsAndStatus.md)

[Configure tables to use the Japanese tokenizer](configure-tables-japanese-tokenizer.md)

## Fields excluded from text indexing

Text indexing excludes fields that meet certain name, type, attribute, or encryption conditions. User searches don't match or return values from excluded fields.

Text indexing excludes a field if it meets any of the conditions in the following table.

<table id="table_lqx_lgc_bpb"><thead><tr><th>

Category

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field name

</td><td>

Text indexing includes the **sys\_class\_name** and **sys\_tags** fields but excludes all other fields whose names begin with **sys\_**.

</td></tr><tr><td>

Field type

</td><td>

Text indexing excludes fields of these types:-   Date
-   Date/Time
-   Duration
-   True/False
-   Workflow

 For more information on these types, see [Field types reference](../../reference-pages/reference/r_FieldTypes.md).

</td></tr><tr><td>

Field attributes

</td><td>

Text indexing excludes fields that have the **no\_text\_index** attribute set to **true**.For more information on this attribute, see [Remove an index for a specific field](t_RemoveAnIndexForASpecificField.md).

</td></tr><tr><td>

Field encryption

</td><td>

Text indexing excludes fields configured for Edge Encryption. For more information on configuring fields with Edge Encryption, see Encrypt fields using encryption configurations.

</td></tr></tbody>
</table>