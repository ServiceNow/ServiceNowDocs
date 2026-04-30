---
title: Configure a global stop word
description: Configure stop words that shouldn't be indexed by the search.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Zing removes stop words from queries, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure a global stop word

Configure stop words that shouldn't be indexed by the search.

## Before you begin

Role required: ts\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Text Index Stop Words**.

2.  Add or remove stop words from the list.

3.  If a message appears at the top of the list, contact Technical Support to regenerate all indexes.

    You must regenerate indexes whenever words may be missing from an index. For example, if you delete, inactivate, or change an active global stop word, the word may be missing from the index. An after business rule checks these conditions and generates the notification message when index regeneration is necessary.

    ![Notification to regenerate all indexes after removing a stop word.](../image/NotificationToRegenerateAllIndexes.png)


**Parent Topic:**[Zing removes stop words from queries](../concept/stop-words-removed-from-queries.md)

**Related topics**  


[Configure a table-specific stop word](t_ConfigureATableSpecificStopWord.md)

[Enable automatic stop words for a table](t_ConfigureAnAutomaticStopWord.md)

[Disable a stop word in Zing](disable-stop-word-zing.md)

