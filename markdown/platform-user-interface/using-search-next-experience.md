---
title: Using search in Next Experience
description: Global search enables you to search multiple record types at once from the Next Experience Unified Navigation search field. Search returns the results that are most relevant to you, grouped by source, or takes you directly to a record that exactly matches your search query. You can switch between global search results and results from workspace applications that you have access to.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [global search, next experience global search]
breadcrumb: [Using the Unified Navigation, Working in Next Experience, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Using search in Next Experience

Global search enables you to search multiple record types at once from the Next Experience Unified Navigation search field. Search returns the results that are most relevant to you, grouped by source, or takes you directly to a record that exactly matches your search query. You can switch between global search results and results from workspace applications that you have access to.

## Search in the Unified Navigation search field

To perform a global search, enter your search query in the Unified Navigation search field, then select **View results** or press Enter.

![Unified Navigation search field.](../image/pol-nav-global-search.png)

![Unified Navigation search field with search terms entered, showing the View results link.](../image/pol-nav-global-search-terms.png)

The search results page reports the total number of records that matched your search and previews a selection of results from each searchable table that contains matching records. You can open any search result record by selecting it in the preview list.

![Global search results page showing results for an email permissions search query.](../image/pol-search-results-page.png)

For more details on the contents of the Next Experience search results page, see [Search results page in Next Experience](https://www.servicenow.com/docs/access?context=global-search-polaris-ui&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Narrow your search by source on the search results page

The search results page includes a list of source tables showing the number of matching records each contains. Select an entry to see search results from the specified source table.

![Global search results page list of source tables.](../image/pol-search-general-filter.png)

When there are more matching records from a source table than can be previewed, the results page displays a **View all** link next to the table title. Select this link to view all matching records from the specified table.

![Detail of global search results page showing previews of records and View all link for the Knowledge table.](../image/pol-search-results-table.png)

## Return to your starting point from the search results page

To return to the page where you initiated your search, select the link with a left arrow that appears above the total results count on the search results page. The title of this link indicates the page it returns you to. For example, if you searched from the Home page, the link text would be **Home**, but if you searched from the Dashboards page, the link text would be **Dashboards Overview**.

## Search for a specific record using Exact Match

Enter a record number into the Unified Navigation search field but don't press Enter or select **View results**. The search field displays a preview of the record with an **Exact Match** tag. Select the preview to go directly to the matching record, bypassing the search results page.

![Global search field displaying exact match record preview.](../image/pol-search-record.png)

## Access your most recent search queries and results

When you select the empty Unified Navigation search field, the system displays lists showing your most recent search queries and your most recently viewed search results. Select a **Recently Searched** query to repeat it, or select a **Recently Viewed** search result record to navigate to it.

![Unified Navigation search field showing Recently Searched and Recently Viewed lists.](../image/pol-search-recent-srch-view.png)

## View results for your search in an available workspace application

If you have access to search in workspace applications, an arrow appears at the right of the Unified Navigation search field after you search that enables you to switch between the results in global search and in your workspace applications.

![Global search field displaying search context menu.](../image/pol-search-context.png)

For example, if the context menu in the illustration was available after you performed a global search, you could select **CSM/FSM Configurable Workspace** from the context menu to view results for the search in CSM/FSM Configurable Workspace.

Exact matches open in the selected workspace application. For example, if you selected **CSM/FSM Configurable Workspace**, entered a record number, and selected the record preview in the search results, the record would open in CSM/FSM Configurable Workspace.

For information adding a workspace to the Unified Navigation search menu, see [Add a workspace application to the Unified Navigation search context menu](https://www.servicenow.com/docs/access?context=add-app-search-context-polaris-ui&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

