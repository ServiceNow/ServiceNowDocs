---
title: Remove the text index for a child table
description: You can remove the text index for a child table if you no longer want the search engine to return results for that child table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/remove-index-child-table.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Remove the text index for a child table

You can remove the text index for a child table if you no longer want the search engine to return results for that child table.

## Before you begin

Role required: admin

## About this task

The **Text index** option for a table is inherited by all of that table's child tables. Clearing this option for an individual child table has no effect.

For example, **Text index** is selected for the Task table in the base system. This setting enables text indexing for the Task table. All tables that extend Task, such as Catalog Task, Incident, and Request, inherit this option. Clearing the **Text index** option in the Incident child table doesn't disable text indexing for Incident records.

To disable text indexing for a specific child table, set that table's **No text index** attribute. This attribute overrides the table's inherited **Text index** option without affecting indexing behavior for other tables in its hierarchy.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Open the dictionary record for the child table.

    The dictionary record for a table is the record with an empty column name and a **Type** value of **Collection**, as shown in the following example image.

    \[Omitted image "table-dictionary-record.png"\] Alt text: Dictionary Entry table showing a table's dictionary record with empty Column name and Type value of Collection.

3.  In the Attributes related list, select **New**.

4.  On the Dictionary Attribute form, fill in the fields:

    |Field|Value|
    |-----|-----|
    |Attribute|No text index|
    |Value|true|

5.  Select **Submit**.

6.  Select **Update**.


## Result

The system no longer indexes or queries the child table for text search results. Indexing continues for other tables in the table's hierarchy.

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

[Change the query mode of an indexed table]()

[Enable indexing of text in multi-row variable sets]()

[Text indexing statistics and status]()

[Configure tables to use the Japanese tokenizer]()

