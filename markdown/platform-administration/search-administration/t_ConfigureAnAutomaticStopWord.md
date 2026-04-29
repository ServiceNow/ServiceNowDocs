---
title: Enable automatic stop words for a table
description: The system can identify and generate stop words when a search term exceeds an occurrence threshold.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Zing removes stop words from queries, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable automatic stop words for a table

The system can identify and generate stop words when a search term exceeds an occurrence threshold.

## Before you begin

Enable text indexing for the table.

Role required: ts\_admin or admin

## About this task

By default, the TS Index Stats scheduled job identifies and creates stop words for tables with text indexes on a nightly basis. Automatically adding stop words improves your search results by removing search terms that return too many search results.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Text Indexes**.

2.  Open the text index entry for the table.

3.  Select the **Auto stop** check box.

4.  In **Auto threshold**, enter the maximum number of occurrences a search term can have in search results.

    When a search term generates more search results than the threshold, the system automatically creates a stop word for the search term.

    For example, to create stop words for the task table, see the blog post [Configuring auto stop words and regenerating text indexes](https://community.servicenow.com/community?id=community_blog&sys_id=83bc6e25dbd0dbc01dcaf3231f961963&view_source=searchResult) from a ServiceNow employee on the ServiceNow Community.

5.  Select **Update**.


## Result

The job identifies and creates stop words for the table with a **Stop mode** value of *Index but do not Query* and inserts a **Comment** to indicate that the stop word was generated automatically.

**Parent Topic:**[Zing removes stop words from queries](../concept/stop-words-removed-from-queries.md)

**Related topics**  


[Configure a global stop word](t_ConfigureAGlobalStopWord.md)

[Configure a table-specific stop word](t_ConfigureATableSpecificStopWord.md)

[Disable a stop word in Zing](disable-stop-word-zing.md)

