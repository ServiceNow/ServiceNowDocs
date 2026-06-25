---
title: Configure a table-specific stop word
description: You can configure stop words for a specific table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/t\_ConfigureATableSpecificStopWord.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Zing removes stop words from queries, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
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

    You must regenerate indexes whenever words may be missing from an index. For example, if you delete or change a stop word for which the mode was Neither Index nor Query, the word may be missing from the index. An after [Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/c_BusinessRules.md) checks these conditions and generates the notification message when index regeneration is necessary.

    **Note:** Text search uses the global list plus the table-specific list of stop words when indexing the table.

    \[Omitted image "TableSpecificStopWords.png"\] Alt text: Notification to regenerate table's text index after removing a table-specific stop word.


**Parent Topic:**[Zing removes stop words from queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/stop-words-removed-from-queries.md)

**Related topics**  


[Configure a global stop word]()

[Enable automatic stop words for a table]()

[Disable a stop word in Zing]()

