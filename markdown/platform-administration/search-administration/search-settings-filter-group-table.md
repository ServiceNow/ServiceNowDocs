---
title: Search settings filter and group global search results by table
description: Global search filters and groups matching results by table. You can configure search sources \(in Next Experience UI\) or search groups to define tables and groups for global search.Global search in Next Experience UI displays search results broken out by search source. A search source is a collection of global search settings for a ServiceNow AI Platform table.The base system includes these default search sources for global search in Next Experience UI.Add a new search source to make a table searchable by global search or workspace search in Next Experience UI.Global text search in Core UI displays search results broken out by search group. A search group is a collection of related searchable tables.The base system includes these default text search groups for global text search in Core UI.Add a new text search group to filter global text search results by table in Core UI.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Global search finds records from multiple tables, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Search settings filter and group global search results by table

Global search filters and groups matching results by table. You can configure search sources \(in Next Experience UI\) or search groups to define tables and groups for global search.

The configuration settings for table-based filtering and grouping of global search results differ by UI, as described in the following sections.

**Parent Topic:**[Global search finds records from multiple tables](c_GlobalTextSearch.md)

**Related topics**  


[Global search displays a page of matching results](global-search-polaris-ui.md#)

[Text search views control format of global search results for tables](text-search-view-formats-results.md)

[Global search displays exact matching records](exact-matches-global-search.md#)

[Global search displays your most recent search queries and results in Next Experience UI](global-search-recent-queries-results.md)

[Set global text search properties](../task/set-global-text-search-properties.md)

[Set the preview limit for global or workspace search in Next Experience UI](../task/set-app-preview-limit-polaris-ui.md)

[Hide per-table search result counts in Next Experience UI](../task/hide-result-counts-polaris-ui.md)

[Add a workspace application to the Unified Navigation search context menu](../task/add-app-search-context-polaris-ui.md)

[Global text search suggestions](../reference/r_GlobalTextSearchSuggestions.md)

## Search sources filter global search results by table in Next Experience UI

Global search in Next Experience UI displays search results broken out by search source. A search source is a collection of global search settings for a ServiceNow AI Platform® table.

A user must have read access to a table to see search results for it.

### Default global search sources for Next Experience UI

The base system includes these default search sources for global search in Next Experience UI.

When Next Experience UI is activated, the following search sources are defined for global search. These search sources appear in the Application Search Sources related list for the **Now Experience Search Configuration** record in the Search Application Configuration \[sys\_search\_context\_config\] table.

|Search source|Table searched|
|-------------|--------------|
|Tasks - Incidents|Incident \[incident\]|
|Tasks - Change Requests|Change Request \[change\_request\]|
|Tasks - Change Tasks|Change Task \[change\_task\]|
|Tasks - Problems|Problem \[problem\]|
|Tasks - Requests|Request \[sc\_request\]|
|Tasks - Catalog Tasks|Catalog Task \[sc\_task\]|
|People &amp; Places - Users|User \[sys\_user\]|
|Tasks - Requested Items|Requested Item \[sc\_req\_item\]|
|People &amp; Places - Groups|Group \[sys\_user\_group\]|
|Knowledge &amp; Catalog - Knowledge|Knowledge \[kb\_knowledge\]|
|People &amp; Places - Companies|Company \[core\_company\]|
|Knowledge &amp; Catalog - Catalog Items|Catalog Item \[sc\_cat\_item\]|

**Note:** Search sources only affect filtering of global search results in Next Experience UI. In Core UI, global text search filters results based on settings defined in text search groups. For details on these settings, see [Search groups filter global text search results by table in Core UI](search-settings-filter-group-table.md#).

### Add a search source for Next Experience UI

Add a new search source to make a table searchable by global search or workspace search in Next Experience UI.

#### Before you begin

You must be using Next Experience UI.

**Note:** You can configure tables for global text search in Core UI by adding new text search groups. For more details, see [Add a search group for Core UI](search-settings-filter-group-table.md#).

The tables you want to include in the search group must have text indexing enabled. To enable text indexing for a table, see [Configure a table for indexing and searching](../task/configure-single-table-for-indexing.md#).

Role required: search\_application\_admin or workspace\_admin

#### About this task

A search source defines a table that is searchable by global or workspace search in Next Experience UI. Define new search sources to add to the default set of tables configured for global search or your workspace search. For the list of global search sources included in the base system, see [Default global search sources for Next Experience UI](search-settings-filter-group-table.md#).

#### Procedure

1.  Define the new search source in the Search Source \[sys\_search\_source\] table.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_search_source.list`.

    3.  Press Enter.

    4.  Select **New**.

    5.  On the Search Source form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name to display for the search source in the global search results page.|
        |Table|Table to make searchable for global search.|
        |Conditions|Filter conditions that table records must satisfy to be searchable.|
        |Application|Application scope for the search source. This field is automatically set.|

    6.  Select **Submit**.

2.  Link the new search source to the record for the global or workspace search application in the Search Application Configurations \[m2m\_search\_context\_config\_search\_source\] table.

    1.  Select **All**.

    2.  In the **Filter** field, enter `m2m_search_context_config_search_source.list`.

    3.  Press Enter.

    4.  Select **New**.

    5.  Select the additional actions icon ![](../../ai-search/image/polaris-ui-form-context-menu-icon.png), then select **Configure** &gt; **Form Layout**.

    6.  Use the slushbucket to add the Search context config field to the selected field list, then select **Save**.

    7.  On the Application Search Sources form, fill in the fields.

<table id="table_lvj_k1k_5rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

Name to display for the search source in the global search results page.

</td></tr><tr><td>

Order

</td><td>

Order of appearance for the search source in the search application configuration context.

</td></tr><tr><td>

Application

</td><td>

Application scope for the search source. This field is automatically set.

</td></tr><tr><td>

Search context config

</td><td>

Record for the global or workspace search application in the Search Application Configuration \[sys\_search\_context\_config\] table. To add the search source for global search, select the **Now Experience Search Configuration** record.

 To add the search source for a workspace application, select the record for that application. For example, to add a search source for Agent Workspace, select the **Agent Workspace Search Config** record.

</td></tr></tbody>
</table>    8.  Select **Submit**.

3.  Reorder search sources for the global or workspace search application.

    1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

    2.  Open the record for the search application.

        **Note:** For global search, open the **Now Experience Search Configuration** record. For a workspace application, open the record for that application, such as the **Agent Workspace Search Config** record for Agent Workspace.

    3.  In the Application Search Sources related list, edit the **Order** values for search source records to alter the display order for table filters on the application's search results page.


#### Result

The new search source appears in global or workspace search results.

## Search groups filter global text search results by table in Core UI

Global text search in Core UI displays search results broken out by search group. A search group is a collection of related searchable tables.

Within each search group, the system divides search results by table. A user must have read access to a table to see search results for it.

### Displaying search results by group

The system displays knowledge and service catalog search results within their respective search results pages. The system displays other results in list format.

For exact match searches, the system only returns records from the Task \(task\) and Knowledge \(kb\_knowledge\) tables.

**Note:** The system filters global search results to display only knowledge articles that are in the same language as the preferred language setting.

![Search results showing Tasks search group name and Incidents table name.](../image/ExampleGlobalSearchResults.png "Example global text search results")

### Options for administrators

Administrators can customize these search group settings for all users:

-   Specifying which tables are part of the group.
-   Specifying whether the search group is available for use.
-   Specifying whether searches include results from this search group by default.
-   Creating new search groups.

Enabling a search group allows users to see records from the search group's tables. Disabling a search group hides records from the search group's tables.

### Default global text search groups for Core UI

The base system includes these default text search groups for global text search in Core UI.

<table id="table_vfr_hnw_pp"><thead><tr><th>

Search group

</th><th>

Tables searched

</th></tr></thead><tbody><tr><td>

Tasks

</td><td>

-   Incident \[incident\]
-   Change Request \[change\_request\]
-   Change Task \[change\_task\]
-   Problem \[problem\]
-   Request \[sc\_request\]
-   Catalog Task \[sc\_task\]
-   Requested Item \[sc\_req\_item\]

</td></tr><tr><td>

People &amp; Places

</td><td>

-   User \[sys\_user\]
-   Group \[sys\_user\_group\]
-   Company \[core\_company\]

</td></tr><tr><td>

Knowledge &amp; Catalog

</td><td>

-   Knowledge \[kb\_knowledge\]
-   Catalog Item \[sc\_cat\_item\]

</td></tr></tbody>
</table>**Note:** Text search groups only affect filtering of global text search results in Core UI and UI15. In Next Experience UI, global search filters results based on search sources linked to the **Now Experience Search Configuration** record in the Search Application Configuration \[sys\_search\_context\_config\] table. For details on the search sources included in the base system, see [Default global search sources for Next Experience UI](search-settings-filter-group-table.md#).

### Add a search group for Core UI

Add a new text search group to filter global text search results by table in Core UI.

#### Before you begin

You must be using Core UI.

**Note:** You can configure tables for global search in Next Experience UI by adding new search sources. For more details, see [Add a search source for Next Experience UI](search-settings-filter-group-table.md#).

The tables you want to include in the search group must have text indexing enabled. To enable text indexing for a table, see [Configure a table for indexing and searching](../task/configure-single-table-for-indexing.md#).

Role required: text\_search\_admin

#### About this task

A text search group defines a set of tables to use as filters for global text search results in Core UI. Define new search groups to add to the default set of text search groups configured for global text search.

For the list of text search groups included in the base system, see [Default global text search groups for Core UI](search-settings-filter-group-table.md#).

#### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Search Groups**.

2.  Select **New**.

3.  On the Text Search Groups form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name for the search group.|
    |Roles|Select one or more user roles if you want to restrict access to the search group to those roles.|
    |User group|Select a user group if you want to restrict access to the search group to users in that user group.|
    |Description|Enter text to display as a tooltip for the search group.|
    |Active|Ensure the check box is selected to make the search group available.|
    |Searched|Clear the check box if you want to exclude results from this search group.|
    |Order|Enter a number to determine the order in which this search group is listed relative to other search groups.|

4.  Select the additional actions icon ![](../../ai-search/image/polaris-ui-form-context-menu-icon.png), then select **Save**.

5.  For each table that you want to add to the search group, perform the following steps.

    1.  In the search group record's Text Search Tables related list, select **New**.

    2.  On the Text Search Table form, fill in the fields.

<table id="table_cpf_3p1_ks"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search group

</td><td>

The search group that you want to add a table to.

</td></tr><tr><td>

Table

</td><td>

Select the table to include in the search group.**Note:** You can select any table not excluded by [the **glide.ui.no\_text\_search** system property](../task/set-global-text-search-properties.md), but global search only displays search results for tables that have text indexing enabled.

</td></tr><tr><td>

Application

</td><td>

Application scope for the text search table record. This field is automatically set.

</td></tr><tr><td>

Active

</td><td>

Option to search the table as part of the search group.

</td></tr><tr><td>

Searched

</td><td>

If you want to exclude results from this table by default, clear this option. A user can manually choose to show results from this table on the search results page.

</td></tr><tr><td>

Order

</td><td>

Order in which this table is listed relative to other tables in the search group.

</td></tr><tr><td>

Conditions

</td><td>

Select one or more conditions to determine which records on the selected **Table** are searched.

</td></tr></tbody>
</table>    3.  Select **Submit**.


