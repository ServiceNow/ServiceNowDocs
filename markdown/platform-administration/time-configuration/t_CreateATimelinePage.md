---
title: Create a timeline page
description: Create a timeline page to track any activity bounded by two dates.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Timeline pages, Viewing record information over time, Reference, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a timeline page

Create a timeline page to track any activity bounded by two dates.

## Procedure

1.  Navigate to **System UI** &gt; **Timeline Pages** and create a new record \(see table for field descriptions\).

    |Field|Description|
    |-----|-----------|
    |Name|Unique name that describes the function of this timeline. For example, `High Priority Change Requests`.|
    |Table|Name of the table associated with this timeline, such as Change Request `[change_request]`.|
    |Start date field|Time-related field from the specified table to use as the start date for the timeline. The timeline begins with the span for the record with the earliest start date from this field, after it applies the filter and sort order. For example, you can select **Updated** as the start date field. It then starts the span for each active change request on the date it was updated to a high priority.|
    |End date field|Time-related field from the specified table to use as the end date for the timeline. The timeline ends with the span for the record with the latest date from this field, after it applies the filter and sort order. For example, you can select **Closed** as the end date field and display all high priority change requests by the date on which they were closed.|
    |**Display Options**|
    |Show grid lines|Select this check box to show horizontal background shading to highlight alternate spans.|
    |Show left pane|Select this check box to show label text in a pane on the left of the timeline. The text that appears in this pane is defined in **Span text fields**.|
    |Show summary pane|Select this check box to show the pink, perspective slider at the bottom of the timeline. Move the slider from right to left to scroll across the chart. Adjust the end points of the slider to change the magnification. A narrow slider zooms in on the spans and provides a more detailed view. A wide slider pulls the view out and makes more of the timeline visible on the screen.|
    |Auto refresh|Select an automatic refresh interval or disable automatic refresh. When auto refresh is disabled, the timeline adjusts only when the browser is manually refreshed or when a start or end date field is updated in a record.|
    |CSS span color|Enter a custom span color using any CSS color format, such as RGB or hexadecimal. If this field is blank, the default span color, light blue, is used. The dark blue color indicates tasks that have a planned start date only, with no planned end date. Adding a planned end date updates the color to light blue.|
    |Show span text|Select this check box to display the content of the **Span text fields** as labels below each span.|
    |Span text fields|Select fields from the specified table to have those values appear as span labels. For example, you might select **Number** and **Short description**. The span labels also appear in the left pane if the left pane is visible.|
    |Show tooltips|Select this check box to display tooltips when the cursor rests on a span.|
    |Tooltip text fields|Select from the specified table the fields whose values appear as tooltips. For example, you might select **Category**, **Assigned to**, and **Due date**.|
    |Filtering and Sorting|
    |Condition|Create a condition to filter the results that appear in the timeline. For example, a condition that displays only active, high priority incidents. [Add the condition count to a condition field](../../field-administration/task/t_AddingTheConditionCountWidget.md) to preview what records will be returned by this condition set.|
    |Perform custom sort?|Select this check box to enable custom sorting. Configure the sort order by selecting fields in the **Sort by** and **Sort by order** fields.|
    |Sort by|Select any field in the list for sorting the spans in the timeline. Common practice is to select either the **Start date field** or the **End date field** as the sorting field. If you select a different sorting field, also include that field in the list of **Tooltip text fields** to give users a way of discovering the sort criteria.|
    |Sort by order|Select the sort order for the sorting fields selected.|
    |Interactive Options|
    |Allow horizontal moving?|Select this check box to permit users to drag timeline spans horizontally. Dragging changes the start and end dates and updates the record.|
    |Allow start time dragging?|Select this check box to permit users to update the record by dragging the start time of a span.|
    |Allow end time dragging?|Select this check box to permit users to update the record by dragging the end time of a span.|
    |Range calculator|Specify a script include that Using DurationCalculator to calculate a due date range restrictions and processes parent updates, if appropriate.|


**Parent Topic:**[Timeline pages](../concept/c_TimelinePages.md)

