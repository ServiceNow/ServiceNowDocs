---
title: Configuring search in Next Experience
description: Administrators can customize Next Experience search settings. Add new searchable tables, modify the fields displayed for search results from a table, or add workspace applications to the search context menu for users.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Configuring search in Next Experience

Administrators can customize Next Experience search settings. Add new searchable tables, modify the fields displayed for search results from a table, or add workspace applications to the search context menu for users.

Next Experience search is enabled by default in the Unified Navigation.

## Add a searchable table

A search source specifies a table to include in Next Experience search. The search results page displays matching records and their counts on a per-table basis. Users can select a table to filter their search results, displaying only matching records from the selected table.

![Table filter list from search results page.](../../../get-started/servicenow-overview/image/pol-search-general-filter.png)

To make a table searchable in Next Experience, add it as a new search source. For details on this procedure, see [Add a search source for Next Experience](https://www.servicenow.com/docs/access?context=search-settings-filter-group-table&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

For the list of tables searchable by default in the base system, see [Default global search sources for Next Experience](https://www.servicenow.com/docs/access?context=search-settings-filter-group-table&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Modify the fields displayed for each search result from a table

The text\_search list view for a searchable table determines which fields the system uses to populate the title, field list, and description for each result from that table.

![Sample search result listing in Next Experience UI showing result's title, field list, and description.](../../../get-started/servicenow-overview/image/pol-search-result-fields.png)

To learn how the system uses fields in the text\_search list view to populate search result entries, see [Text search views control format of global search results for tables](https://www.servicenow.com/docs/access?context=text-search-view-formats-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

For the list of fields included in the base system's text\_search list views for the default searchable tables, see [Default display fields for global search tables](https://www.servicenow.com/docs/access?context=global-search-default-tables&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Add a workspace application to the search context menu

The search context menu enables users to view and open search results in available workspace applications as well as in global search.

![Search context menu displayed beneath Unified Navigation search field.](../../../get-started/servicenow-overview/image/pol-search-context.png)

To add a workspace application to the search context menu, see [Add a workspace application to the Unified Navigation search context menu](https://www.servicenow.com/docs/access?context=add-app-search-context-polaris-ui&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

For details on using the search context menu, see [View and open search results using workspace applications in Next Experience Unified Navigation](https://www.servicenow.com/docs/access?context=global-search-polaris-ui&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

For more information on configuring search settings in Next Experience, see [Global search finds records from multiple tables](https://www.servicenow.com/docs/access?context=c_GlobalTextSearch&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Parent Topic:**[Configuring the Next Experience UI](next-experience-ui-admin.md)

