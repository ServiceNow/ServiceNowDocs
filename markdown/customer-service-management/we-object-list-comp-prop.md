---
title: Component properties for the Object list
description: Component property enables you to configure the behavior of the Object list component on a third-party website.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Web Embeddables component properties, Web Embeddables reference, Reference, Customer Service Management]
---

# Component properties for the Object list

Component property enables you to configure the behavior of the Object list component on a third-party website.

|Component property|Description|
|------------------|-----------|
|Type|All Records shows the complete list with options to edit, filter, and take bulk actions. Top Records shows a prioritized, read-only list with a view all link.|
|Table|Table data to display in the list.|
|Edit query|Query filters to refine the list results. These filters cannot be modified.|
|Edit default filter|Users can edit or remove this filter. When a query is set, it adds more conditions to narrow down the displayed records.|
|Columns|Select columns to be displayed. If both columns and List view are chosen, columns take priority.|
|List view|Uses preconfigured columns from the UI view table. If both columns and a list view are selected, columns take priority.|
|Nest by|Column used to define the hierarchy. If this property is not set, the list is displayed as a flat list.|
|Default group by|Group records by a specific column. User can choose to group by another column.|
|Hide when empty|Enable to hide the component when there are no records to show for the user.|

<table id="table_tbp_lcv_zfc"><thead><tr><th>

Component property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide header

</td><td>

Option to show or hide the header.

</td></tr><tr><td>

Title

</td><td>

Displays the title of the list. You can set a custom title or use the table name as the default title.

</td></tr><tr><td>

Subtitle

</td><td>

Subtitle to display near the title. When empty, no subtitle will be displayed.

</td></tr><tr><td>

Hide record count

</td><td>

Option to show or hide the count badge on the header.

</td></tr><tr><td>

Hide search

</td><td>

Option to show or hide the search bar. Search works only for indexed tables.

</td></tr><tr><td>

Hide filters

</td><td>

Option to show or hide the filter with condition-builder.

</td></tr><tr><td>

Disable column selection

</td><td>

Option to disable or enable column selection and arrangement.

</td></tr><tr><td>

Hide actions

</td><td>

Option to show or hide the action buttons.

</td></tr><tr><td>

Action config

</td><td>

Global actions and actions set at the table or view level will automatically be displayed.To display additional actions specific to this component, select an **Action Config** record.

</td></tr></tbody>
</table>|Component property|Description|
|------------------|-----------|
|Disable clickable records|When unchecked, values in the first column appear as clickable links to open record details.|
|Enable clickable reference records|When checked, values in the reference column appear as clickable links to open the related record details.|
|Disable column highlighting|When unchecked, column values are highlighted.|
|Highlighted value config|Select UX Highlighted Value Configuration record that defines which fields and values to highlight.|

|Component property|Description|
|------------------|-----------|
|Disable quick edit|When unchecked, users with required permissions can edit the records.|

|Component property|Description|
|------------------|-----------|
|Disable cell wrapping|When unchecked, automatically moves content to a new line within a cell when it exceeds the cell’s width. Long text may still be truncated.|
|Max cell characters|Displays number of characters in each cell before truncation.|
|Disable cell editing|Option to allow inline editing of cell.|

|Component property|Description|
|------------------|-----------|
|Records per page|Allows user to choose the number of records displayed on each page.|
|Visible page range|Sets how many page numbers are shown between navigation arrows.|
|Limit records fetched|Limit the total records fetched across all pages to improve component performance. Higher values may increase load times. Leave it empty to fetch all records.|
|Hide errors|Option to show or hide the error messages from end user when the component fails to load initially.|

**Related topics**  


[Configure the Object list component instance](../task/we-config-object-list-comp.md)

[Embed the Object list component on the third-party website](../task/we-embed-object-list-comp-on-thirdparty-web.md)

[Event handlers in the Object list component](we-event-handlers-object-list.md)

[Sample code for the Object list component](we-object-list-sample-code.md)

