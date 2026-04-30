---
title: Create a simple list visualization in the Visualization Designer
description: List reports display data in the form of an expandable list. For example, an incident report grouped by priority displays only the priority names and a number of records that display if the user selects the priority. You can configure whether lists display expanded or collapsed.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-04-09"
reading_time_minutes: 6
breadcrumb: [Data visualizations in Platform Analytics, Platform Analytics]
---

# Create a simple list visualization in the Visualization Designer

List reports display data in the form of an expandable list. For example, an incident report grouped by priority displays only the priority names and a number of records that display if the user selects the priority. You can configure whether lists display expanded or collapsed.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. If you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## About this task

For information about the use of a Simple List in a dashboard, see [the Developer Site](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/shared-components/now-record-list-connected-snapshot/usage). This site gives information for the Simple List component in UI Builder, and some configuration options may differ from the Visualization Designer.

The simple list differs from other visualizations in several ways:

-   No unified header configuration
-   No unified data source selection configuration
-   No unified group by
-   No option to export the List from dashboards
-   No option to paginate the records instead of using the **View all** link

**Note:** You can include Spotlight information in a simple list. Configure the list to display information from the Spotlight \[spotlight\] table. For more information, see [Spotlights on Platform Analytics dashboards](../../performance-analytics/concept/spotlights-configurable-workspaces.md). For general information about the Spotlight feature, see [Ranking records with Spotlight](../../performance-analytics/concept/spotlight.md).

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select **New**.

3.  Select the List-Simple \(![Simple list visualization icon](../../../reuse/icons/product-icons/list-outline-24.svg)\) visualization type.

4.  Configure the title, filters, visible columns, and highlighted values.

<table id="table_tbv_xgb_ptb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Select the source table of your simple list report.

</td></tr><tr><td>

Edit fixed filter

</td><td>

Apply query conditions to the table. The conditions you specify here can’t be changed at runtime.

</td></tr><tr><td>

Follow filters

</td><td>

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

</td></tr><tr><td>

Columns

</td><td>

Choose the columns that will be visible.

</td></tr><tr><td>

Number of displayed columns

</td><td>

If the view that you selected has too many columns, you can set the maximum number of columns to be displayed.

</td></tr><tr><td>

Edit filter

</td><td>

Provide additional filter conditions on the visualization. These conditions can be changed by the viewer in runtime.

</td></tr><tr><td>

Group by

</td><td>

Choose a field to group the list by. At runtime, this field is collapsed and users can expand it. For example, if you group by priority, users see only the priority names, and can select the name to see all the records of that priority.

</td></tr><tr><td>

Maximum rows

</td><td>

Specify the maximum number of visible rows. This value input overrides user preferences. For example, if the value input is set to 10, the list always displays 10 records regardless of user preference. To honor user preferences, leave the field blank.

</td></tr><tr><td>

Hide "View all" footer

</td><td>

By default, the Simple list has a **View all** link that opens the standard list of table records in the Core UI for the subject table. None of the filters in this Simple list component apply in that view. To prevent viewers from navigating to that link, turn this option on.

</td></tr><tr><td>

Hide highlighted values

</td><td>

Prevents value highlighting from the Highlighted Values \[sys\_ux\_highlighted\_value\_config\] table from being applied.

</td></tr><tr><td>

Highlighted values

</td><td>

Select highlighting rules from the Highlighted Values \[sys\_ux\_highlighted\_value\_config\] table to apply. Available only when **Hide highlighted values** is false.

</td></tr><tr><td>

Hide highlighted content

</td><td>

Disables the user's ability to highlight text. Use this property in conjunction with search results.

</td></tr><tr><td>

Highlighted content

</td><td>

JSON properties defining which content to highlight and what colors to use. Available only when **Hide highlighted content** is false.

</td></tr><tr><td>

Hide links

</td><td>

Removes all the links in the list. Reference fields and links will render as plain text.

</td></tr><tr><td>

Enable word wrap

</td><td>

When turned on, the text wraps in all columns of the list.

</td></tr><tr><td>

Override word wrap user preference

</td><td>

Overrides word wrap configured in user preferences with the value of **Enable word wrap**.

</td></tr><tr><td>

Maximum characters

</td><td>

Integer that determines the maximum characters allowed in a grid row cell. Text exceeding this limit truncates.Default: 4000

</td></tr><tr><td>

Hide empty state image

</td><td>

When turned on, the empty state image for the list component is not displayed.

</td></tr></tbody>
</table>5.  Configure **End user capabilities**.

    Move the toggle switch to hide these capabilities.

    |Field|Description|
    |-----|-----------|
    |Hide option to personalize columns|Disable the ability to add, remove, and change the order of columns|
    |Disable dotwalk|Disable dotwalk capability in list personalization. \(Only effective when **Hide option to personalize columns** is off.\)|
    |Hide option to drag and drop columns|When off, users can reorder the list's columns at runtime.|
    |Hide option to group records|When off, users can group the list by the values of any of the available columns.|
    |Hide column resizing|When off, users can drag columns to resize their widths.|
    |Hide column filtering|When off, users can filter the content of a list from the column headers.|
    |Hide column sorting|When off, users can sort the list content from the column headers.|

6.  Set border and spacing.

    |Field|Description|
    |-----|-----------|
    |Show border|Displays a border around the list.|
    |Bare|When turned on, removes padding around list to provide more compact positioning on the page.|

7.  Configure the header.

    Move the toggle switch to hide these capabilities.

    |Field|Description|
    |-----|-----------|
    |Hide header|Removes all header content, including the visualization title, number of records, last fresh time, and refresh option.|
    |Hide title|Removes the title of the visualization|
    |Title|Provide a name for your list visualization.|
    |Hide total number of records|Removes the number of records, usually found next to the title.|
    |Hide last refresh information|Hides the indication of when the visualization was last refreshed.|
    |Hide option to refresh|Removes the refresh icon \(![Refresh icon](../../dashboards/image/icon-db-refresh.png)\) from the visualization.|

8.  Set advanced options.

    These options require expertise and usually do not need to be set.

<table id="table_b5b_51c_kvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide inline editing

</td><td>

When turned on, prevents viewers from editing the list.**Note:** Users cannot edit fields of the journal\_input type. These fields include the following:

-   Work Notes
-   Additional Comments
-   Approval Comments
-   Change request notes
-   Problem Notes


</td></tr><tr><td>

Include in landmark keyboard shortcut

</td><td>

When turned on, the component is included in the landmark keyboard shortcut cycling behavior, allowing users to quickly jump focus back-and-forth between the main elements on the page.

</td></tr><tr><td>

Refresh requested

</td><td>

Object containing a timestamp that can be passed down to trigger a refresh.

</td></tr><tr><td>

Column preference key

</td><td>

The key to use for sourcing and saving a user preference which specifies the columns to show and in what order. This is meant to be used as a fallback in situations where the component can not correctly determine the default key to be used to save a user preference.

</td></tr></tbody>
</table>9.  Select **Save**.

    Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** to return to the Data Visualization list.


## What to do next

-   [Add a visualization to a dashboard from the Visualization Designer](add-dv-new-db.md)
-   [Share a data visualization in the Visualization Designer](share-dv-ac.md#)
-   [Bookmark a visualization in the Visualization Designer](../../dashboards/task/bookmark-dv-ac.md)

