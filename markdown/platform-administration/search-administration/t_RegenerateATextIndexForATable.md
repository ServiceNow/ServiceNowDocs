---
title: Regenerate a text index for a table
description: You can regenerate a table text index when you change table stop words or display values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/t\_RegenerateATextIndexForATable.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Zing indexes words, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Regenerate a text index for a table

You can regenerate a table text index when you change table stop words or display values.

## Before you begin

The table that you want to regenerate the text index for must already be configured for indexing and searching. For details on this configuration process, see [Configure a table for indexing and searching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-single-table-for-indexing.md).

Role required: ts\_admin or admin

## About this task

By default, the system maintains text indexes on a daily schedule. Typically, you only need to manually regenerate a text index when you change these values.

-   You change the list of table-specific stop words.
-   You change the display value of a record such as changing a user or group name. Until you regenerate the index, text searches for old display values will still produce results and searches for the new display value won't show results.

You can also regenerate a text index if you observe incorrect search results for the indexed table. This is rare and usually only occurs if text indexing was interrupted.

Text indexing can be a resource-intensive task that may take a while to complete. You may notice performance degradation or incomplete search results during index generation. To estimate text indexing duration, you can view historical [statistics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/r_ViewTextIndexingStatsAndStatus.md).

**Note:** This index regeneration process purges the existing text search index for the table before it regenerates it. While it's processing, no search results are returned if you perform a text search before the regeneration is complete. An alternate method is available that doesn't impact use of text searches for the table while the regeneration is in process. See [Reindex a table without impacting text search results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/real-time-reindexing.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Text Indexes**.

2.  Open the text index for the table.

    For example, select **task**.

    The system displays the Text Index record for the table.

3.  Select the **Regenerate Text Index** related link, then select **OK**.

    \[Omitted image "regenerate-text-index.png"\] Alt text: Regenerate the text index for the task table.


## Result

The system schedules the selected table for text indexing.

-   **[Reindex a table without impacting text search results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/real-time-reindexing.md)**  
Rebuild text search indexes without adversely impacting search results. You can continue to perform text searches on a table while the index regeneration takes place.
-   **[Regenerate the text index for a single record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/regenerate-text-index-one-record.md)**  
Update the text search index for a single record. Use this approach to quickly verify whether text indexing is the cause of a search issue without rebuilding the full text index for an entire table.

**Parent Topic:**[Zing indexes words](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/zing-indexes-words.md)

**Related topics**  


[Zing indexes punctuation as part of some words]()

[Zing indexes some HTML elements]()

[Configure a table for indexing and searching]()

[Configure a text index group to search across multiple tables]()

[Zing index and search dictionary attributes]()

[Remove an index]()

[Remove an index for a specific field]()

[Remove the text index for a child table]()

[Change the query mode of an indexed table]()

[Enable indexing of text in multi-row variable sets]()

[Text indexing statistics and status]()

[Configure tables to use the Japanese tokenizer]()

