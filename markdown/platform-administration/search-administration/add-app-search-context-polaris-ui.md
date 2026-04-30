---
title: Add a workspace application to the Unified Navigation search context menu
description: Enable users to view results for their Unified Navigation searches in workspace applications as well as in global search.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-02-04"
reading_time_minutes: 5
breadcrumb: [Global search finds records from multiple tables, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Add a workspace application to the Unified Navigation search context menu

Enable users to view results for their Unified Navigation searches in workspace applications as well as in global search.

## Before you begin

You must be using Next Experience UI.

The workspace application that you want to add to the search context menu must be installed. A search application configuration record must exist for the workspace, with AI Search specified as the search engine. If you need to create a new search application configuration record for the workspace, see [Create a search application configuration for AI Search](../../ai-search/task/create-search-app-config-ais.md).

Role required: admin

## About this task

You can add a workspace application, such as CSM/FSM Configurable Workspace, to the Unified Navigation search context menu. Adding the workspace application to the search context menu enables users to switch between global search results and search results from the specified workspace.

## Procedure

1.  Copy the sys\_id of the record for the search application configuration for the chosen workspace:

    1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

    2.  Open the record for the chosen workspace's search application configuration.

        As an example, for Agent Workspace, open the **Agent Workspace Search Config** record.

    3.  Select the Additional actions icon ![](../../ai-search/image/polaris-ui-form-context-menu-icon.png), then select **Copy sys\_id**.

2.  Define a globalSearchDataConfigId UX page property to map the search application configuration record to the workspace's UX application:

    1.  Navigate to the UX Page Property \[sys\_ux\_page\_property\] table's list view by selecting **All**, entering `sys_ux_page_property.list` in the **Filter** field, and pressing Enter.

    2.  Select **New**.

    3.  On the UX Page Property form, fill in the fields as follows:

        |Field|Description|
        |-----|-----------|
        |Page|Use the Lookup using list icon ![](../../ai-search/image/icon-lookup-using-list.png) to select the UX Application record for your workspace.|
        |Name|Enter `globalSearchDataConfigId`.|
        |Type|Select **string**.|
        |Value|Enter the search application configuration record sys\_id that you copied in step [1.c](add-app-search-context-polaris-ui.md#copy_srch_app_cfg_sys_id).|

    4.  Select **Submit**.

3.  Copy the sys\_id of the record for the Workspace Global Search Configuration that you want workspace search to use:

    1.  Navigate to the Workspace Global Search Configuration \[sys\_aw\_global\_search\_config\] table's list view by selecting **All**, entering `sys_aw_global_search_config.list` in the navigation filter, and pressing Enter.

    2.  Open the record for the Workspace Global Search Configuration that you want workspace search to use.

        If you have a custom Workspace Global Search Configuration record that you want to use, open that record. Otherwise, open the Workspace search settings record.

    3.  Select the Additional actions icon ![](../../ai-search/image/polaris-ui-form-context-menu-icon.png), then select **Copy sys\_id**.

4.  Define a global\_search\_configurations UX page property to configure the workspace's search settings:

    1.  Navigate to the UX Page Property \[sys\_ux\_page\_property\] table's list view by selecting **All**, entering `sys_ux_page_property.list` in the **Filter** field, and pressing Enter.

    2.  Select **New**.

    3.  On the UX Page Property form, fill in the fields as follows:

<table id="table_xkh_gd3_fxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Page

</td><td>

Use the Lookup using list icon ![](../../ai-search/image/icon-lookup-using-list.png) to select the UX Application record for your workspace.

</td></tr><tr><td>

Name

</td><td>

Enter `global_search_configurations`.

</td></tr><tr><td>

Type

</td><td>

Select **json**.

</td></tr><tr><td>

Value

</td><td>

Enter the following JSON:```json
{
  "globalSearchViewConfigId": "00000000000000000000000000000000",
  "globalSearchRoute": "search"
}
```

 Replace the `globalSearchViewConfigId` value of `00000000000000000000000000000000` with the Workspace Global Search Configuration record sys\_id that you copied in step [3.c](add-app-search-context-polaris-ui.md#copy_ws_srch_config_sys_id). For example, if you selected the Workspace search settings record, replace the value with `97a574ea53c0130084acddeeff7b12a6`.

</td></tr></tbody>
</table>    4.  Select **Submit**.

5.  Enable Unified Navigation search for the chosen workspace:

    1.  Navigate to the UX Page Property \[sys\_ux\_page\_property\] table's list view by selecting **All**, entering `sys_ux_page_property.list` in the **Filter** field, and pressing Enter.

    2.  Look for a UX Page Property record with name **chrome\_header** and page matching the chosen workspace.

        As an example, for Asset Workspace, look for a record with name **chrome\_header** and page **Asset Workspace**.

    3.  If a **chrome\_header** record exists for the workspace, edit it and change the **searchEnabled** JSON element to true in its **Value** field, then select **Update**.

    4.  If no **chrome\_header** record exists for the workspace, select **New** and fill in the UX Page Property form fields as follows, then select **Submit**.

<table id="table_krt_5n3_fxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Page

</td><td>

Use the Lookup using list icon ![](../../ai-search/image/icon-lookup-using-list.png) to select the UX Application record for your workspace.

</td></tr><tr><td>

Name

</td><td>

Enter `chrome_header`.

</td></tr><tr><td>

Type

</td><td>

Select **json**.

</td></tr><tr><td>

Value

</td><td>

Enter the following JSON:```json
{
  "privatePage": {
    "searchEnabled": true
  }
}
```

</td></tr></tbody>
</table>6.  Refresh your browser tab to reload the ServiceNow AI Platform®.

7.  Clear your instance's system cache by entering `<instance-name>.service-now.com/cache.do` in your browser's address bar and pressing Enter.

    **Important:** Clearing the system cache can affect overall performance and degrade system response times. Don't run cache flushes during business hours, and don't trigger cache flushes automatically.


## Result

The chosen workspace appears as an option in the Unified Navigation search context menu for users who have it assigned. Users can switch to the workspace's search context. For more details on using the search context menu to switch application contexts, see [View and open search results using workspace applications in Next Experience Unified Navigation](../concept/global-search-polaris-ui.md#).

**Parent Topic:**[Global search finds records from multiple tables](../concept/c_GlobalTextSearch.md)

**Related topics**  


[Global search displays a page of matching results](../concept/global-search-polaris-ui.md#)

[Text search views control format of global search results for tables](../concept/text-search-view-formats-results.md)

[Search settings filter and group global search results by table](../concept/search-settings-filter-group-table.md#)

[Global search displays exact matching records](../concept/exact-matches-global-search.md#)

[Global search displays your most recent search queries and results in Next Experience UI](../concept/global-search-recent-queries-results.md)

[Set global text search properties](set-global-text-search-properties.md)

[Set the preview limit for global or workspace search in Next Experience UI](set-app-preview-limit-polaris-ui.md)

[Hide per-table search result counts in Next Experience UI](hide-result-counts-polaris-ui.md)

[Global text search suggestions](../reference/r_GlobalTextSearchSuggestions.md)

