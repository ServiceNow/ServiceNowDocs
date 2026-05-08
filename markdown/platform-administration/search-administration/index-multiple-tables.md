---
title: Configure a text index group to search across multiple tables
description: Update tables to the V4 indexing format and include them in a text index group to facilitate searching across multiple tables.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure a text index group to search across multiple tables

Update tables to the V4 indexing format and include them in a text index group to facilitate searching across multiple tables.

## Before you begin

Role required: ts\_admin or admin

## About this task

Text index groups enable you to index and search across multiple tables.

Performing searches across multiple tables requires normalizing the tables first so the relevance scores mean the same thing for all tables. V4 indexing provides that normalization. Zing uses the [Okapi BM25](https://en.wikipedia.org/wiki/Okapi_BM25) ranking function to calculate the relevancy score of search results.

The V4 table indexing format is optimized for documentation, such as knowledge base articles. You don't need to reindex tables that use this format when you change the value of an indexing attribute, such as the weight of a field. If you want to use the BM25 ranking function on a single table, you can convert it to the V4 format.

To enable search across multiple tables, you:

1.  Configure all of your chosen tables to use the V4 index format if they don't already use it.

    **Note:** In new instances, the Catalog Item \[sc\_cat\_item\], Knowledge \[kb\_knowledge\], Social Q&amp;A Questions \[kb\_social\_qa\_question\], and User \[sys\_user\] tables use the V4 index format. If you upgrade your instance from a previous release, the indexing format of these tables remains the same as it was in the older release.

2.  Add the tables to a text index group so they can be indexed and searched together.

    **Note:** You can't add the Task \[task\] table or any tables that extend it to a text index group.


## Procedure

1.  Configure the tables that you want to include in multiple table searches to use the V4 index format.

    **Note:** Upgrading from V3 to V4 is easy. Downgrading from V4 to V3 is more difficult and discouraged.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Text Index Configurations**.

    2.  Open the record for the table that you want to upgrade to the V4 index format.

    3.  If **Format** isn't disabled, select **V4**, select **Submit**, and then skip to step [2](index-multiple-tables.md#create-index-group).

        You can choose index formatting in this step because no index exists for the table.

    4.  If **Format** is disabled, select the **Show index name record** related link.

        The disabled field means that an index already exists for the table and you must explicitly update the index format.

        The Text Index page displays.

    5.  Select the **Upgrade to V4** related link, then select **OK**.

        The system schedules a task to upgrade the text index from V3 to V4, enabling this table to participate in multiple-table indexing.

2.  Create a text index group that specifies the tables you want to index together so you can search them together.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Text Index Groups**.

    2.  Select **New**.

    3.  Enter the following field values:

        |Field|Value|
        |-----|-----|
        |Label|Name for the group of tables that you want to index and search together.|
        |Tables|List of tables that you want to include in the text index group.|

        You can add tables formatted with V3 and V4 to text index groups. If you add V3 tables, the text index group remains inactive.

    4.  Select **Submit**.

3.  Configure the indexing and search attributes on tables in a text index group.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Text Index Configurations**.

    2.  Select **New**.

        The Text Index configuration form displays. If you already have a text index group in the list, skip to step [3.d](index-multiple-tables.md#select-index-group).

    3.  In **Applies to**, select **Index Group**.

    4.  In **Index group**, select the magnifying glass and select the text index group you created, then select **Submit**.

        The only text index groups that display are the ones you have already created.

        The Text Index Configuration table displays.

    5.  Open the record for your text index group.

    6.  On the **Text Index Table Attribute Maps** tab, select **New**.

        The Text Index Table Attribute Map form displays. Attributes pertain to the way Zing indexes or searches individual tables in the text index group.

    7.  In **Table**, select a table to define attributes for.

        Only tables in the specified text index group and their child tables display.

    8.  In **Attribute name**, select the magnifying glass and select an attribute.

        To see the list of attributes, enter `ts_configuration_attribute.list` in the application navigator. For attribute definitions, see [Zing index and search attributes](../reference/index-attributes.md).

    9.  In **Value** enter a value and select **Submit**.

        Valid values depend on the attribute. For information on valid values, see [Zing index and search attributes](../reference/index-attributes.md).

    10. Repeat this procedure to define additional search engine parameters for other tables in the text index group.

    11. Under **Related Links**, select **Generate Text Index**.

4.  Configure search parameters on individual table columns in the text index group.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Text Index Configurations**.

    2.  Open the record for your text index group.

    3.  On the **Text Index Column Attribute Maps** tab, select **New**.

        The Text Index Column Attribute Map form displays. Attributes pertain to the way Zing indexes or searches individual table columns in the text index group.

    4.  In **Table**, select a table to define attributes for.

        Only tables in the text index group and their child tables display.

    5.  In **Attribute name**, select a search engine parameter, enter a value for that parameter in **Value**, and select **Submit**.

        To see the list of attributes, enter `ts_configuration_attribute.list` in the application navigator. For attribute definitions, see [Zing index and search attributes](../reference/index-attributes.md).

    6.  In **Column**, specify the name of the column in the selected table you want to apply the search attribute to.

    7.  In **Value**, specify the attribute's value that governs the search.

    8.  Select **Submit**.

    9.  Repeat this procedure to define additional search engine parameters for table columns in the text index group.

    10. Under **Related Links**, select **Generate Text Index**.

5.  Add a synonym dictionary.

    Specifying a dictionary enables searches on the search term and synonyms of the search term, such as `car` and its synonym `auto`. Zing provides a default synonym dictionary.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Text Index Configurations**.

    2.  Open the record for your text index group.

    3.  On the **Index synonym Dictionaries** tab, select **New**.

    4.  In **Index**, select the table index to add the stop words to.

    5.  In **Synonym dictionary**, select the dictionary to use.

        To add a dictionary, select **New** and follow the procedure in [Create synonym dictionaries](create-synonym-dictionaries.md).

    6.  Select **Submit**.

    7.  Under **Related Links**, select **Generate Text Index**.

6.  Select **Update**.


## What to do next

You can query the tables in the text index group for string matches using the `GlideRecord.addQuery(name, value)` or `GlideRecord.addEncodedQuery(name, value)` methods with the `123TEXTINDEXGROUP321` reserved name. For more information about querying text index groups for string matches, see Querying tables in script.

**Parent Topic:**[Zing indexes words](../concept/zing-indexes-words.md)

**Related topics**  


[Zing indexes punctuation as part of some words](../concept/c_PunctuationForSearchResults.md)

[Zing indexes some HTML elements](../concept/c_SearchingHTMLContent.md)

[Configure a table for indexing and searching](configure-single-table-for-indexing.md#)

[Zing index and search dictionary attributes](../reference/index-attributes.md)

[Regenerate a text index for a table](t_RegenerateATextIndexForATable.md)

[Remove an index](t_RemoveAnIndex.md)

[Remove an index for a specific field](t_RemoveAnIndexForASpecificField.md)

[Remove the text index for a child table](remove-index-child-table.md)

[Change the query mode of an indexed table](configure-table-query-mode.md)

[Enable indexing of text in multi-row variable sets](index-text-multi-row-variable-sets.md)

[Text indexing statistics and status](../reference/r_ViewTextIndexingStatsAndStatus.md)

[Configure tables to use the Japanese tokenizer](configure-tables-japanese-tokenizer.md)

