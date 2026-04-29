---
title: Update a type-ahead suggestion
description: The knowledge base and global text searches provide suggestions as you type. These type-ahead suggestions are compiled on a nightly basis by a scheduled job.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Global text search suggestions, Global search finds records from multiple tables, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Update a type-ahead suggestion

The knowledge base and global text searches provide suggestions as you type. These type-ahead suggestions are compiled on a nightly basis by a scheduled job.

## Before you begin

The type-ahead search suggestions feature is only available in the UI15 interface.

Role required: admin

## About this task

Use the following procedure if you need to refresh the type-ahead suggestions list before the next run of the scheduled job.

**Note:** Type-ahead suggestions aren't configurable. For more about how suggestions are generated and maintained, see the blog post [Global Text Search Suggestions](https://www.servicenow.com/community/in-other-news/global-text-search-suggestions/ba-p/2294604) by a ServiceNow Technical Support Engineer in the ServiceNow Community.

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs**.

2.  Open **TS Search Stats**.

3.  Run the scheduled job.


**Parent Topic:**[Global text search suggestions](../reference/r_GlobalTextSearchSuggestions.md)

**Related topics**  


[Configure "Did you mean?" suggestions](t_ConfigureADidYouMeanSuggestion.md)

