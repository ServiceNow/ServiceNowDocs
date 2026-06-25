---
title: Remove an index
description: You can remove the index for a table if you no longer want the search engine to return results for that table. This procedure also removes the index for all tables that extend the specified table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/t\_RemoveAnIndex.html
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

    \[Omitted image "table-dictionary-record.png"\] Alt text: Dictionary Entry table showing a table's dictionary record with matching Table name, empty Column name and Type value of Collection.

3.  If the **Text index** option field is hidden, configure the form layout to show it.

    For details on showing and hiding fields on a form, see [Configuring the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md).

4.  Clear the record's **Text index** option, then select **Update**.


## Result

The system no longer indexes text from the specified table or queries it for text search results. This change also disables text indexing and search for all tables that extend the specified table.

**Parent Topic:**[Zing indexes words](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/zing-indexes-words.md)

**Related topics**  


[Zing indexes punctuation as part of some words]()

[Zing indexes some HTML elements]()

[Configure a table for indexing and searching]()

[Configure a text index group to search across multiple tables]()

[Zing index and search dictionary attributes]()

[Regenerate a text index for a table]()

[Remove an index for a specific field]()

[Remove the text index for a child table]()

[Change the query mode of an indexed table]()

[Enable indexing of text in multi-row variable sets]()

[Text indexing statistics and status]()

[Configure tables to use the Japanese tokenizer]()

