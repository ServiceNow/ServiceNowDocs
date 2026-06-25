---
title: Hide per-table search result counts in Next Experience UI
description: Suppress display of per-table search result counts in the Next Experience UI search results page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/hide-result-counts-polaris-ui.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Global search finds records from multiple tables, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Hide per-table search result counts in Next Experience UI

Suppress display of per-table search result counts in the Next Experience UI search results page.

## Before you begin

You must be using Next Experience UI.

Role required: ui\_builder\_admin or admin

## About this task

By default, the search results page displays the total number of search results along with per-table result counts for each searchable table that contains matching records. You can hide the per-table result counts for search users by following this procedure.

## Procedure

1.  Navigate to **All** &gt; **Next Experience Framework** &gt; **UI Builder**.

    UI Builder opens in a new browser tab.

2.  In the list of available experiences, open the **Unified Navigation App** record.

3.  In the Pages and variants listing, open the **Search Results** &gt; **search Default** record.

    UI Builder reloads and displays settings for the Search Results \(search Default\) page.

4.  In the Content pane, select the **Body \(Grid\)** &gt; **Search Result Wrapper 1** component.

    Properties, styles, and events for the selected component appear in the configuration panel.

5.  If a `Different application scope` informational message appears, select **Edit in original scope**.

    The system displays an informational message indicating that you are editing in the application scope.

6.  On the configuration panel's Config tab, enable the **Hide search results count** option.

7.  Select **Save**.


## Result

Per-table search result counts no longer display on the search results page.

**Parent Topic:**[Global search finds records from multiple tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/c_GlobalTextSearch.md)

**Related topics**  


[Global search displays a page of matching results]()

[Text search views control format of global search results for tables]()

[Search settings filter and group global search results by table]()

[Global search displays exact matching records]()

[Global search displays your most recent search queries and results in Next Experience UI]()

[Set global text search properties]()

[Set the preview limit for global or workspace search in Next Experience UI]()

[Add a workspace application to the Unified Navigation search context menu]()

[Global text search suggestions]()

