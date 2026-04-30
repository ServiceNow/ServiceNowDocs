---
title: Select synonym dictionaries for a table
description: Search administrators can specify one or more synonym dictionaries available to a particular table.
locale: en-US
release: xanadu
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Zing can expand search results with synonyms, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Select synonym dictionaries for a table

Search administrators can specify one or more synonym dictionaries available to a particular table.

## Before you begin

Role required: ts\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Text Indexes**.

2.  Select the table for which you want to change search behavior.

    The system displays the Text index record for the table.

3.  Select the **Index Synonym Dictionaries** tab.

4.  Select **New**.

5.  Select a synonym dictionary in the **Synonym Dictionary** field on the **Index Synonym Dictionary** form.

6.  Select **Submit**.


## Result

Text searches on this table use the selected synonym dictionaries.

**Parent Topic:**[Zing can expand search results with synonyms](../concept/search-synonyms-expand-results.md)

**Related topics**  


[Enable search synonyms](enable-text-index-synonyms.md)

[Create synonym dictionaries](create-synonym-dictionaries.md)

[Disable synonyms for a table](disable-synonyms-for-a-table.md)

[Debug synonym searches](debug-synonym-searches.md)

