---
title: Text search views control format of global search results for tables
description: The text\_search view for a table determines how global search displays results from that table.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Global search finds records from multiple tables, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Text search views control format of global search results for tables

The text\_search view for a table determines how global search displays results from that table.

Results displayed by global search include multiple elements. For each search result, the system populates these elements with values of fields included in the table's text\_search list view.

![Sample search result listing in Next Experience UI showing title, field list, and description.](../image/search-result-format-polaris-ui.png "Sample search result listing in Next Experience UI")

![Sample search result listing in Core UI showing title, field list, and description.](../image/jakarta-search-result-formatting.png "Sample search result listing in Core UI")

<table id="table_ypr_txk_rz"><thead><tr><th>

Element

</th><th>

Description

</th><th>

Matching criteria

</th></tr></thead><tbody><tr><td>

1. Title

</td><td>

The title is the first line of the search result block. It links to the matching record of the search result.

</td><td>

Global search uses the first string field in the table's text\_search list view that is not the number field. If there is no matching string field or the contents of the field is empty, the system displays the text "No title" in the session language. For example, in the default text\_search view for the Incident table, the short description field satisfies the title criteria. Global search uses this field as the search result title.

</td></tr><tr><td>

2. Field list

</td><td>

The field list is the second line of the search results. It displays field name-value pairs, separated by the pipe character, for up to 10 fields.

</td><td>

Global search uses the first 10 fields in the table's text\_search list view that don't match the title or description criteria. For example, in the default text\_search view for the Incident table, the number, opened, caller, priority, state, category, and assignment group fields satisfy the field list criteria. Global search displays the names and values for these fields in the search result field list.

</td></tr><tr><td>

3. Description

</td><td>

The description is the third line of the search results. This line is optional and may not appear for all search results.

</td><td>

Global search uses the first string field in the table's text\_search list view that is not the title and is over 100 characters in length. If no field matches these criteria, the search results omit this line. For example, in the default text\_search view for the Incident table, the description field satisfies the description criteria. Global search uses this field as the search result description.

</td></tr></tbody>
</table>By default, the system uses the text\_search list view for a table to format global text search results for that table. If a text\_search view doesn't exist for the table, the system instead formats search results using the table's default form view. Implementers can specify which view the system uses to format search results by modifying the value of the **glide.ui.text\_search.view** system property.

-   **[Default display fields for global search tables](../reference/global-search-default-tables.md)**  
Multiple tables are enabled for global search in the base system. Each global search table has its own set of fields included in the table's default text\_search list view. The system uses fields from this view to format global search results from these tables.

**Parent Topic:**[Global search finds records from multiple tables](c_GlobalTextSearch.md)

**Related topics**  


[Global search displays a page of matching results](global-search-polaris-ui.md#)

[Search settings filter and group global search results by table](search-settings-filter-group-table.md#)

[Global search displays exact matching records](exact-matches-global-search.md#)

[Global search displays your most recent search queries and results in Next Experience UI](global-search-recent-queries-results.md)

[Set global text search properties](../task/set-global-text-search-properties.md)

[Set the preview limit for global or workspace search in Next Experience UI](../task/set-app-preview-limit-polaris-ui.md)

[Hide per-table search result counts in Next Experience UI](../task/hide-result-counts-polaris-ui.md)

[Add a workspace application to the Unified Navigation search context menu](../task/add-app-search-context-polaris-ui.md)

[Global text search suggestions](../reference/r_GlobalTextSearchSuggestions.md)

[Create and delete views](https://www.servicenow.com/docs/access?context=create-delete-view&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

