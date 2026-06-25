---
title: Configure tables to use the Japanese tokenizer
description: Improve search results in Japanese language searches by configuring individual tables to use the Japanese tokenizer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/configure-tables-japanese-tokenizer.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure tables to use the Japanese tokenizer

Improve search results in Japanese language searches by configuring individual tables to use the Japanese tokenizer.

## Before you begin

Role required: admin

## About this task

Japanese language searches use the Kuromoji Japanese tokenizer in Zing. The Japanese tokenizer attribute is active by default, but you must configure individual tables to use it and then regenerate the text index.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Search for the table name.

3.  In the search results, open the table, which is the list item that has an empty **Column name** and a **Type** of **Collection**.

4.  Scroll down the page and select the **Attributes** tab, and then select **New**.

5.  Fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Attribute|Enter **Text index tokenizer language**.|
    |Dictionary entry|Defaults to the name of the table.|
    |Value|Enter **ja** for the Japanese tokenizer.|

6.  Select **Submit**.

7.  [Regenerate a text index for a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/t_RegenerateATextIndexForATable.md).

    **Note:** Text indexing can be a resource-intensive task that may take a while to complete. You may notice performance degradation or incomplete search results during index generation. To estimate text indexing duration, you can view historical [statistics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/r_ViewTextIndexingStatsAndStatus.md).


## Result

When the text index is generated and you go to the table you configured, the table now uses the Japanese tokenizer.

**Parent Topic:**[Zing indexes words](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/zing-indexes-words.md)

**Related topics**  


[Zing indexes punctuation as part of some words]()

[Zing indexes some HTML elements]()

[Configure a table for indexing and searching]()

[Configure a text index group to search across multiple tables]()

[Zing index and search dictionary attributes]()

[Regenerate a text index for a table]()

[Remove an index]()

[Remove an index for a specific field]()

[Remove the text index for a child table]()

[Change the query mode of an indexed table]()

[Enable indexing of text in multi-row variable sets]()

[Text indexing statistics and status]()

