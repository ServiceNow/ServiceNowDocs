---
title: Remove an index for a specific field
description: You can remove the index for a specific field in a table if you no longer want the search engine to return results for that field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/t\_RemoveAnIndexForASpecificField.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Remove an index for a specific field

You can remove the index for a specific field in a table if you no longer want the search engine to return results for that field.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Open the dictionary record for the table field.

    The dictionary record for a table field is the record with **Table** matching the table's name and **Column name** matching the field's name, as shown in the following example image.

    \[Omitted image "table-field-dictionary-record.png"\] Alt text: Dictionary Entry table showing a table field's dictionary record with matching Table and Column name.

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

**Parent Topic:**[Zing indexes words](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/zing-indexes-words.md)

**Related topics**  


[Zing indexes punctuation as part of some words]()

[Zing indexes some HTML elements]()

[Configure a table for indexing and searching]()

[Configure a text index group to search across multiple tables]()

[Zing index and search dictionary attributes]()

[Regenerate a text index for a table]()

[Remove an index]()

[Remove the text index for a child table]()

[Change the query mode of an indexed table]()

[Enable indexing of text in multi-row variable sets]()

[Text indexing statistics and status]()

[Configure tables to use the Japanese tokenizer]()

