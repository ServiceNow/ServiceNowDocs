---
title: Configure a table-specific stop word
description: You can configure stop words for a specific table.
locale: en-US
release: zurich
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Zing removes stop words from queries, Zing text indexing and search engine, Search administration, Configure core features, Administer]
---

# Configure a table-specific stop word

You can configure stop words for a specific table.

## Before you begin

Role required: ts\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Text Indexes**.

2.  Open the text index entry for the table.

3.  Add or remove stop words from the **Index Stop Words** related list.

    For each word, select the desired **Stop mode** \(Not a Stop Word \(inactivates the stop word\), Neither Index nor Query, or Index but do not Query\).

4.  If a message appears at the top of the form, select **Regenerate Text Index**, then select **OK**.

    You must regenerate indexes whenever words may be missing from an index. For example, if you delete or change a stop word for which the mode was Neither Index nor Query, the word may be missing from the index. An after [Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) checks these conditions and generates the notification message when index regeneration is necessary.

    **Note:** Text search uses the global list plus the table-specific list of stop words when indexing the table.

    ![Notification to regenerate table's text index after removing a table-specific stop word.](../image/TableSpecificStopWords.png)


**Parent Topic:**[Zing removes stop words from queries](../concept/stop-words-removed-from-queries.md)

**Related topics**  


[Configure a global stop word](t_ConfigureAGlobalStopWord.md)

[Enable automatic stop words for a table](t_ConfigureAnAutomaticStopWord.md)

[Disable a stop word in Zing](disable-stop-word-zing.md)

