---
title: Define contextual search for record producer
description: Define a record producer to trigger a search based on the text that you enter in a variable field. Search results appear at the bottom of the record producer form.
locale: en-US
release: australia
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Define contextual search for record producer

Define a record producer to trigger a search based on the text that you enter in a variable field. Search results appear at the bottom of the record producer form.

## Before you begin

Role required: admin

## About this task

The base system **Create New Incident** record producer is configured to use contextual search. If you have customized this record producer, you can configure contextual search to link to a specific field on your record producer.

**Note:** Only one variable within a record producer can use contextual search.

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Record Producer Configuration**.

2.  Select **New**.

3.  On the form, fill in the fields.

    ![Record producer configuration form](../image/record-producer-config.png "Record producer configuration form")

    |Field|Description|
    |-----|-----------|
    |Record producer|Unique name of the record producer where you want to add the contextual search.|
    |Search context|Name of the search context to use.|
    |Search variable|Variable within the selected record producer that uses the contextual search.|
    |Title|Title for the search results area that appears in the form.|
    |Active|Option to activate the record producer configuration.|
    |Limit|Maximum number of search results returned.|
    |Results per page|Number of search results to display per page.|
    |Allow expand/collapse|Option to allow expanding or collapsing the search results in the form.|

4.  Select **Submit**.


**Parent Topic:**[Managing contextual search](../concept/working-with-contextual-search.md)

