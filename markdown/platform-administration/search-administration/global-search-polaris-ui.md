---
title: Global search displays a page of matching results
description: Global search displays a page of results that match your search, grouped by table.Global search displays a Search Results page containing results that match your search terms, grouped by search source. Results appear when the search is complete.Use the search context menu to view and open results for your current search in workspace applications.Global text search displays a page of results that match your search terms. Search results appear dynamically on this page as Zing generates them.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Global search finds records from multiple tables, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Global search displays a page of matching results

Global search displays a page of results that match your search, grouped by table.

The elements included on the search results page differ by UI, as described in the following sections.

**Parent Topic:**[Global search finds records from multiple tables](c_GlobalTextSearch.md)

**Related topics**  


[Text search views control format of global search results for tables](text-search-view-formats-results.md)

[Search settings filter and group global search results by table](search-settings-filter-group-table.md#)

[Global search displays exact matching records](exact-matches-global-search.md#)

[Global search displays your most recent search queries and results in Next Experience UI](global-search-recent-queries-results.md)

[Set global text search properties](../task/set-global-text-search-properties.md)

[Set the preview limit for global or workspace search in Next Experience UI](../task/set-app-preview-limit-polaris-ui.md)

[Hide per-table search result counts in Next Experience UI](../task/hide-result-counts-polaris-ui.md)

[Add a workspace application to the Unified Navigation search context menu](../task/add-app-search-context-polaris-ui.md)

[Global text search suggestions](../reference/r_GlobalTextSearchSuggestions.md)

## Search results page in Next Experience UI

Global search displays a Search Results page containing results that match your search terms, grouped by search source. Results appear when the search is complete.

![Results for email permissions search showing total results, search groups, and list of all results for navigation.](../image/global-search-ui-example-polaris.png "Search Results page in Next Experience UI")

Zing displays global search results in a dedicated page consisting of these elements.

<table id="table_syy_ntr_fz"><thead><tr><th>

UI element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Search Results page title

</td><td>

Contextual app pill for the search results page.

</td></tr><tr><td>

2. Global search field

</td><td>

Field displaying your current search terms. If you edit these terms, refresh the results page by selecting the **View results** link that appears in a panel below the search field.

</td></tr><tr><td>

3. Contextual return link

</td><td>

Link to return to the page you were on when you performed the search. The title of this link depends on which page you searched from.

</td></tr><tr><td>

4. Total result count

</td><td>

Total number of records matching your search.

</td></tr><tr><td>

5. Search source table name and result count

</td><td>

Name of a search source table and the number of previewed and total matching records in that table. Users with the admin or ui\_builder\_admin roles can hide the per-table counts of matching records. For details on making this change, see [Hide per-table search result counts in Next Experience UI](../task/hide-result-counts-polaris-ui.md).

</td></tr><tr><td>

6. Preview of matching records for table

</td><td>

Partial list of matching records for the specified table, with maximum count controlled by the preview limit. By default, the system displays up to 10 matching records per table, sorted from highest to lowest document score. The system displays a separate list for each table in the search source. By default, the system displays fields from the table's text\_search list view for each search result. If this view doesn't exist for the table, it instead displays fields from the default list view. For more details on the text\_search list view and the format of individual result listings, see [Text search views control format of global search results for tables](text-search-view-formats-results.md).

 Users with the admin role can override the preview results limit for a search application by modifying the application's record in the Workspace Global Search Configuration \[sys\_aw\_global\_search\_config\] table. For more details on this procedure, see [Set the preview limit for global or workspace search in Next Experience UI](../task/set-app-preview-limit-polaris-ui.md).

 Administrators can also modify the search results table list view by modifying the value of the **glide.ui.text\_search.view** system property. For details on changing this value, see [Set global text search properties](../task/set-global-text-search-properties.md).

</td></tr><tr><td>

7. Table filter

</td><td>

Icon indicating that a filter was applied to results from this search source table. Pointing to the information icon displays a pop-up containing the search filter applied.

</td></tr><tr><td>

8. Link to all table results

</td><td>

Link to all matching records from the searched table. Select the link to launch a filtered list view based on the query. This link only displays when the total number of matching records in the table exceeds the preview limit.

</td></tr><tr><td>

9. Results summary

</td><td>

List of search source tables, showing the number of matching search results per table. Select the search source table name to display the associated preview list results. Search source tables with no matching results don't appear in this list. Users with the admin or ui\_builder\_admin roles can hide the per-table counts of matching records. For details on making this change, see [Hide per-table search result counts in Next Experience UI](../task/hide-result-counts-polaris-ui.md).

</td></tr></tbody>
</table>## View and open search results using workspace applications in Next Experience Unified Navigation

Use the search context menu to view and open results for your current search in workspace applications.

### Before you begin

You must be using Next Experience UI.

Role required: none

### About this task

In addition to global search, you may have access to workspace search applications, such as CSM/FSM Configurable Workspace. If you have access to multiple search applications, the search field's drop-down search context menu displays all available search applications, with the current application preselected. To view and open search results in another application, select it from the search context menu.

Users with the administrator role can add workspace applications to the search context menu. For details on this procedure, see [Add a workspace application to the Unified Navigation search context menu](../task/add-app-search-context-polaris-ui.md).

### Procedure

1.  Use the search field to perform a search and view search results.

2.  To open the search context menu, select the **Choose search context** icon ![](../image/polaris-ui-search-field-arrow-icon.png) in the search field.

    **Note:** If the **Choose search context** icon isn't displayed in the search field, the current search applications is the only one available. You can't switch search applications.

    A drop-down menu of available search applications displays, with the current search applications preselected.

    ![Global search field displaying search context menu.](../../../get-started/servicenow-overview/image/pol-search-context.png)

3.  Select an alternate search application from the drop-down menu.

    The drop-down menu disappears and the **View results** link appears.

4.  To view search results in the selected application, select **View results** or press Enter.


### Result

The page reloads and displays results for your current search from the selected search application. If you select a previewed matching record, it opens in the selected search application.

## Search results page in Core UI and UI15

Global text search displays a page of results that match your search terms. Search results appear dynamically on this page as Zing generates them.

![Results for "email" search showing total results, search groups, and list of all results for navigation.](../image/jakarta-global-search-ui.png "Global text search results page in Core UI")

Zing displays global text search results in a dedicated page consisting of these elements.

<table id="table_syy_ntr_fz"><thead><tr><th>

UI element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Search terms

</td><td>

Field displaying your current search terms. If you edit these terms, refresh the results page by selecting the search icon ![](../../ai-search/image/ui16-search-icon.png) or pressing Enter.**Note:** If you delete your search terms and select the search icon or press Enter, the search results page doesn't refresh. To refresh the page, enter search terms, then select the search icon or press Enter.

</td></tr><tr><td>

2. Total results

</td><td>

Total number of records matching your search.

</td></tr><tr><td>

3. Search group name

</td><td>

Name of the search group that includes the table with matching records.

</td></tr><tr><td>

4. Preview of matching records

</td><td>

Partial list of matching records for the specified table, with maximum count controlled by the preview limit. By default, the system displays up to 10 matching records per table, sorted from highest to lowest document score. The system displays a separate list for each table in the search group. By default, the system uses the table's text\_search list view if available. Otherwise, it displays fields with the default list view.

 Users with the admin role can modify the default preview results limit and search results table list view by changing the values of the **glide.ui.text\_search.rowcount** and **glide.ui.text\_search.view** system properties. For more details on these properties, see [Set global text search properties](../task/set-global-text-search-properties.md).

</td></tr><tr><td>

5. Table name

</td><td>

Name of the search group table and the number of matching records in the table. Click the link to launch a filtered list view based on the query. Users with the admin role can hide matching record counts by setting the **sn\_global\_searchui.hide\_results\_count** property to **true** in the [System Property](../../reference-pages/reference/r_AvailableSystemProperties.md#) table.

</td></tr><tr><td>

6. Table filter

</td><td>

Current filter applied to search results from this table. Pointing to the information icon displays a pop-up containing the search filter applied. For information on applying a table filter to a search group, see [Add a search group for Core UI](search-settings-filter-group-table.md#).

</td></tr><tr><td>

7. Progress bar

</td><td>

Current percentage of tables searched. The system hides this element after the search is complete.

</td></tr><tr><td>

8. Link to all table results

</td><td>

Link to see all matching records from the search group table. Click the link to launch a filtered list view based on the query.

</td></tr><tr><td>

9. Global search field

</td><td>

Global search field.**Note:** If you delete your search terms and select the search icon or press Enter, the search results page refreshes, displaying zero search results.

</td></tr><tr><td>

10. Results summary

</td><td>

List of search groups and tables with the number of search results per group and table. Select the table name to display the associated preview list results.

</td></tr></tbody>
</table>