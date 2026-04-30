---
title: Create a calendar report visualization in the Visualization Designer
description: Create calendar report visualizations to show and highlight date-driven events.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [Create calendar report, Create calendar visualization]
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create a calendar report visualization in the Visualization Designer

Create calendar report visualizations to show and highlight date-driven events.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. If you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

For information about the use of the Calendar report visualizations on dashboards, see [the Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/shared-components/sn-par-calendar-connected/usage). This site gives information about Calendar report components in the UI Builder, and some configuration options may differ from the Visualization Designer.

## About this task

The calendar visualization is used to show activity over the course of a longer span of time than most data visualizations. Use them when you want to condense date-specific information into a small space.

**Note:** Calendar visualizations that are migrated from Core UI require a start time in the **Start date** field and an end time in the **End date** field. These fields are not required in Core UI, but are required in Platform Analytics experience.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select **New**.

3.  Select the Calendar Report \(![calendar icon](../image/inline-data-vis-calendar-days.png)\) visualization type.

4.  In the configuration panel, configure the **Component header**.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Component title

</td><td>

A title for the calendar report visualization that reflects the information being shared.

</td></tr><tr><td>

Use large font size

</td><td>

Defines the styles used to render the calendar title. When true, the non-bold Title-tertiary font is used. Otherwise, the bold Header-secondary font is used.Default: false

</td></tr><tr><td>

Component description

</td><td>

Description you enter for the component. This field has a limit of 250 characters.

</td></tr><tr><td>

Show description

</td><td>

Adds an information icon \(![Information icon](../image/icon-info.png)\) to the visualization. This icon opens the component description in a popup.

</td></tr></tbody>
</table>5.  In the **Data** section, specify the source table, predefined condition, date range, and filter options.

<table id="table_tbv_xgb_ptb"><thead><tr><th>

Data fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Select the table or [database view](../../performance-analytics/concept/performance-analytics-glossary.md#) to report calendar events from.Default value: task

</td></tr><tr><td>

Predefined conditions

</td><td>

Predefined conditions from the Report Source \[sys\_report\_source\] table for filtering event records.

</td></tr><tr><td>

Edit filter table

</td><td>

Conditions for filtering event records. This filter is applied when the end user views the calendar. Users can filter further if a filter component is added to the page. **Note:** This property adds a filter condition in addition to the table and predefined conditions, if any are applied.

</td></tr><tr><td>

Start date field

</td><td>

Field from the record to display as the starting event. You must select a date field. Default value: Opened

</td></tr><tr><td>

End date field

</td><td>

Field to report on as the ending event. You must select a date field. Default value: Closed \[closed\_at\]

</td></tr><tr><td>

Event display fields

</td><td>

One or more fields you select to appear on all calendar events.Default value: number,short\_description

</td></tr></tbody>
</table>6.  In the **Additional Settings** section you have some miscellaneous options.

<table id="table_cfz_d1b_tdc"><thead><tr><th>

Data fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Follow filters

</td><td>

When enabled, the visualization follows all filters in the same dashboard tab or on the whole dashboard.

</td></tr><tr><td>

Show filter overview

</td><td>

Shows a filter icon that opens a filter panel. This panel shows the configuration filters, such as "Active is true" and any filters followed on the dashboard. Does not show predefined conditions.

</td></tr><tr><td>

Default view

</td><td>

The calendar view format to apply as the default. Choose from:-   Day
-   Week
-   Work Week
-   Month
Default value: Month

</td></tr></tbody>
</table>7.  Select **Save**.

    Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** to return to the Data Visualization list.


## What to do next

-   [Add a visualization to a dashboard from the Visualization Designer](add-dv-new-db.md)
-   [Share a data visualization in the Visualization Designer](share-dv-ac.md#)
-   [Bookmark a visualization in the Visualization Designer](../../dashboards/task/bookmark-dv-ac.md)

**Parent Topic:**[Creating data visualizations](../concept/creating-data-visualizations.md)

