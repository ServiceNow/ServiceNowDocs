---
title: Create a list visualization in the Visualization Designer
description: Create a expandable list of table records that can be drilled down to from chart interactions. List reports display data in the form of an expandable list. For example, an incident report grouped by priority displays only the priority names and a number of records that display if the user selects the priority.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create a list visualization in the Visualization Designer

Create a expandable list of table records that can be drilled down to from chart interactions. List reports display data in the form of an expandable list. For example, an incident report grouped by priority displays only the priority names and a number of records that display if the user selects the priority.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## About this task

In the Zurich release, this List replaces the simple list visualization. Upon migration, all simple lists are migrated to the new List.

**Note:**

-   You can include Spotlight information in a list visualization. Configure the list to display information from the Spotlight \[spotlight\] table. For more information, see [Spotlights on Platform Analytics dashboards](../../performance-analytics/concept/spotlights-configurable-workspaces.md). For general information about the Spotlight feature, see [Ranking records with Spotlight](../../performance-analytics/concept/spotlight.md).
-   It is not possible to configure auto refresh on the List visualization. To refresh a List visualization on a dashboard, select the More Options icon ![Context menu icon](../../dashboards/image/icon-vert-3dot-p.png) and choose **Refresh**.
-   The option to show the total number of records is not available in the new List visualization.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

2.  Select **Create data visualization**.

3.  Select the List \(![List visualization icon](../../../reuse/icons/product-icons/list-outline-24.svg)\) visualization type from the category labeled **Other**.

4.  Select **Add data source**.

    You can only select Table data sources, such as the Incident \[incident\] table.

5.  Configure the **Header and border**. Header and border options are the same for all data sources.

<table id="table_ly5_djk_c5b"><thead><tr><th>

Header and border fields

</th><th>

Description

</th></tr></thead><tbody><tr id="ac-dv-showheader"><td>

Show header

</td><td>

The visualization header, including title and icons.

</td></tr><tr id="ac-dv-showheadersep"><td>

Show header separator

</td><td>

Option to display a line separating the header from the rest of the component.

</td></tr><tr id="ac-dv-charttitle"><td>

Chart title

</td><td>

Title of the visualization.

</td></tr><tr id="ac-dv-chartdesc"><td>

Description

</td><td>

A short overview about the visualization that the end user sees. Descriptions help users find the visualization.

</td></tr><tr id="ac-dv-wraptitle"><td>

Wrap title

</td><td>

Option to wrap long titles onto a second line. If false, displays an ellipsis to truncate long titles.

</td></tr><tr id="ac-dv-showborder"><td>

Show border

</td><td>

Option to display a line around the component.

</td></tr><tr id="ac-dv-bare"><td>

Bare

</td><td>

Option to remove padding around data visualization to provide more compact positioning on the page. Only available when **Show border** is turned off.

</td></tr><tr><td>

Header background color

</td><td>

Specify the color behind the title of the visualization.

</td></tr><tr><td>

Title color

</td><td>

Specify the text color. The default title color is black, but you can choose a color that contrasts better with the header background.

</td></tr><tr id="group-by-heading"><td class="sub-head" colspan="2">

Group by

</td></tr><tr id="row_group-by-field"><td>

Group by \(optional\)

</td><td>

The field to group by. For example, in an incident report grouped by **Assignment group**, all incidents that belong to Software, Service Desk, and Network are placed in separate groups. If the table contains variables or question fields, you have the option to group by one of them at the end of the list of fields.**Note:**

-   It is not possible to group or stack data by the **Tags** field, or by certain field types, such as MEDIUMTEXT.
-   If you want to group by a field with continuous values, such as date or integer, the values are automatically grouped according to any report ranges that are defined for the data. For more information, see [Report ranges](../concept/c_ReportRanges.md#).


</td></tr><tr id="alternative-group-by"><td>

Add alternative group by

</td><td>

This selection opens a dialog in which you select additional items that the data in the visualization may be grouped by. The viewer of the visualization can then select which of these items to group the data by. The viewer toggles the visibility of the selector in the visualization's More actions menu. In the additional items dialog, you can set whether this selector is visible by default by toggling **Selector visible by default**.If you select a value in **Group by**, that is the default group-by value. You do not have to select a **Group by** value to specify alternative group-by values. In this case, no default group-by value is used.

For more information about the viewer experience selecting from alternative group-by values, see [Select a group-by value in a data visualization as a viewer](../../performance-analytics/concept/select-group-runtime.md).

**Important:**

-   Only up to three metrics on one visualization support alternative group-by.
-   Alternative group-by does not support data binding on the data source


</td></tr><tr id="data-update-heading"><td class="sub-head" colspan="2">

Data update

</td></tr><tr id="ac-dv-followfilters"><td>

Follow filters

</td><td>

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

</td></tr><tr id="ac-dv-showfiltericon"><td>

Show filter icon

</td><td>

Option to show the filter icon and the number of filters impacting the visualization. If a filter is not selected to apply to a visualization, the icon does not show. Toggle off to hide the filter icon and number of filters applied.

</td></tr><tr id="no-data-message-ss-table-uxa"><td class="sub-head" colspan="2">

Info messages

</td></tr><tr id="enable-custom-empty-state"><td>

Set custom message when no data

</td><td>

Option to configure a custom message that displays when no data is returned.

</td></tr><tr id="empty-state-illustration"><td>

Illustration

</td><td>

An illustration to include in the message.

</td></tr><tr id="empty-state-heading"><td>

Heading

</td><td>

Header text of the message that describes why no data was returned.

</td></tr><tr id="empty-state-heading-level"><td>

Heading level

</td><td>

Header text size for the message that describes why no data was returned.

</td></tr><tr id="empty-state-content"><td>

Content

</td><td>

Secondary text of the message that provides additional detail.

</td></tr><tr id="empty-state-alignment"><td>

Alignment

</td><td>

The alignment of the illustration and text in the message.

</td></tr><tr id="presentation"><td class="sub-head" colspan="2">

Presentation

</td></tr><tr id="columns-and-rows"><td class="sub-head" colspan="2">

Columns and rows

</td></tr><tr><td>

Columns

</td><td>

Select the columns from the table that you want to display in the visualization.**Note:** The List shows some columns by default. These columns are not included as selected columns in the configuration panel until you save the data visualization for the first time.

This feature to show default columns as selected cannot be used with List visualizations that were created before Platform Analytics experience bundle 7.2.1 was installed.

</td></tr><tr><td>

Maximum rows

</td><td>

Specify the maximum number of rows to show. When there are more rows in the visualization, it will be divided into pages \(if **Allow list pagination** is selected in display settings\).

</td></tr><tr><td>

Number of displayed columns

</td><td>

For a view with too many columns, you can set the maximum number that are displayed.

</td></tr><tr><td>

Maximum characters

</td><td>

Specify the number of characters to show in a cell before it is truncated.

</td></tr><tr><td>

Show option to personalize columns

</td><td>

Enable the ability to add, remove, and change the order of columns in the list at runtime.

</td></tr><tr><td>

Disable dotwalk

</td><td>

Disable the dotwalk capability in personalized lists. Available only if Show option to personalize columns is selected.

</td></tr><tr><td>

Show option to drag-and-drop columns

</td><td>

Enable users to reorder the columns at runtime.

</td></tr><tr><td>

Show option to group records

</td><td>

Enable users to group the list by column entries at runtime.

</td></tr><tr><td>

Show column resizing

</td><td>

Enable users to resize column widths at runtime.

</td></tr><tr><td>

Show column filtering

</td><td>

Enable users to apply filters from column headings at runtime.

</td></tr><tr><td>

Show column sorting

</td><td>

Enable users to sort the column values in ascending or descending order at runtime.

</td></tr><tr><td class="sub-head" colspan="2">

Display settings

</td></tr><tr><td>

Show inline editing

</td><td>

Allows users to edit values in the list by double-clicking them. Security restrictions including ACLs apply.**Note:** Users cannot edit fields of the journal\_input type. These fields include the following:

-   Work Notes
-   Additional Comments
-   Approval Comments
-   Change request notes
-   Problem Notes


</td></tr><tr><td>

Show links

</td><td>

Select to show all links in the list. When cleared, reference fields and links render as plain text.

</td></tr><tr><td>

Wrap cell content

</td><td>

Enable multiple lines of text per cell across the table. Text may still be truncated, based on the value of the **Maximum characters** option.

</td></tr><tr><td>

Show 'view all' footer

</td><td>

Enables the user to view all the rows in the visualization, not just the maximum number specified.

</td></tr><tr><td>

Allow list pagination

</td><td>

Enables the list to be divided across multiple pages. When cleared, list pagination is hidden.

</td></tr></tbody>
</table>
-   **[Create a list visualization with variable columns](create-list-dv-with-var-col.md)**  
You can create a list visualization with variables columns based on a data source or table that has variables associated with it. For example, if an item has a variable called **Storage**, you can create a list report that has a column for the values in this variable.

**Parent Topic:**[Creating data visualizations](../concept/creating-data-visualizations.md)

