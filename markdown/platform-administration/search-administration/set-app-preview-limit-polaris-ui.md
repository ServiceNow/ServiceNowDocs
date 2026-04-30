---
title: Set the preview limit for global or workspace search in Next Experience UI
description: Override the default limit of 5 preview results per search source on the Next Experience UI search results page for global or workspace search.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Global search finds records from multiple tables, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set the preview limit for global or workspace search in Next Experience UI

Override the default limit of 5 preview results per search source on the Next Experience UI search results page for global or workspace search.

## Before you begin

You must be using Next Experience UI.

Role required: workspace\_admin

## About this task

The preview limit for a search application specifies how many preview results can appear for each search source on the search results page. By default, the system displays up to 5 preview results per search source. Workspace administrators can override this default limit separately for global search and for all workspace searches.

## Procedure

1.  Navigate to the Workspace Global Search Configuration \[sys\_aw\_global\_search\_config\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_aw_global_search_config.list`.

    3.  Press Enter.

2.  Open the configuration record for the search application that you want to modify the preview limit for:

    -   To modify the preview limit for global search, open the **Now Experience Search Configuration** record.
    -   To modify the preview limit for a workspace application, open the **Workspace search settings** record.
3.  On the Workspace Global Search Configuration form, enter your desired preview limit into the **Tab overview items per section** field, then select **Update**.


## Result

The search results page for global or workspace search displays preview results up to the new limit for each search source.

**Parent Topic:**[Global search finds records from multiple tables](../concept/c_GlobalTextSearch.md)

**Related topics**  


[Global search displays a page of matching results](../concept/global-search-polaris-ui.md#)

[Text search views control format of global search results for tables](../concept/text-search-view-formats-results.md)

[Search settings filter and group global search results by table](../concept/search-settings-filter-group-table.md#)

[Global search displays exact matching records](../concept/exact-matches-global-search.md#)

[Global search displays your most recent search queries and results in Next Experience UI](../concept/global-search-recent-queries-results.md)

[Set global text search properties](set-global-text-search-properties.md)

[Hide per-table search result counts in Next Experience UI](hide-result-counts-polaris-ui.md)

[Add a workspace application to the Unified Navigation search context menu](add-app-search-context-polaris-ui.md)

[Global text search suggestions](../reference/r_GlobalTextSearchSuggestions.md)

