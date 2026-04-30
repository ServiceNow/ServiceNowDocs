---
title: Timeline sub item
description: Use the Timeline Sub Items related list to define child spans for the timeline, based on records in a table that references the parent timeline's table.
locale: en-US
release: zurich
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Timeline pages, Viewing record information over time, Reference, Time configuration, Configure core features, Administer]
---

# Timeline sub item

Use the Timeline Sub Items related list to define child spans for the timeline, based on records in a table that references the parent timeline's table.

## About this task

You can create a timeline sub item generate a hierarchical relationship, starting from a timeline page to any number of levels. For example, if there is a timeline page for a release, the sub item might be sprints, and the sprint might have stories as a sub item.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Timeline Pages**.

2.  Open the timeline page for which you want to add a sub item.

3.  Go to the Timeline Sub Items related list and click **New**.

4.  Fill in the form \(see table for field descriptions\) and click **Submit**.

<table id="table_eh5_xgc_np"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Parent

</td><td>

\[Read-only\] Identifies the parent of the timeline sub item.

</td></tr><tr><td>

Name

</td><td>

Enter a unique name that describes the function of this timeline. For example, Sprints for late Priority Changes.

</td></tr><tr><td>

Table

</td><td>

Select the table called by this timeline. The selected table must contain at least one field that references the table you selected for the parent timeline page. For example, if the parent timeline page uses the Scrum Release \[rm\_release\_scrum\] table, you might choose the Sprint \[rm\_sprint\] table for a timeline sub item.

</td></tr><tr><td>

Start date field

</td><td>

Select a time-related field from the specified table to use as the start date for the timeline. For example, Planned start date.

</td></tr><tr><td>

End date field

</td><td>

Select a time-related field from the specified table to use as the end date for the timeline. For example, Planned end date.

</td></tr><tr><td>

Parent Reference Column

</td><td>

Select a reference field on which to base the timeline connection between the sub item records and the parent records. -   If multiple reference fields are available, choose the reference field that forms part of the hierarchy modeled by this timeline.
-   If this list is blank, the sub item table contains no reference fields to the parent table. In this case, you must choose a different table for the sub item.
 ServiceNow uses the parent reference column to determine which records appear at each level of the timeline.

</td></tr><tr><td class="sub-head" colspan="2">

**Display Options**

</td></tr><tr><td>

CSS span color

</td><td>

Enter a custom span color using any CSS color format, such as RGB or hexadecimal. If this field is blank, it uses the default span color, light blue. The dark blue color indicates tasks with a planned start date only, with no planned end date. Adding a planned end date updates the color to light blue.

</td></tr><tr><td>

Span text fields

</td><td>

Select fields from the specified table to have those values appear as span labels. For example, you might select **Number** and **Short description**. If the timeline displays the left pane, span labels also appear in the left pane

</td></tr><tr><td>

Tooltip text fields

</td><td>

Select fields from the specified table to have those values appear as tooltips. For example, you might select **Category**, **Assigned to**, and **Due date**.

</td></tr><tr><td class="sub-head" colspan="2">

Filtering and Sorting

</td></tr><tr><td>

Condition builder

</td><td>

Create a condition to filter the results that appear in the sub item. For example, you might create a condition that displays only active, high priority incidents.

</td></tr><tr><td>

Perform custom sort

</td><td>

Select this check box to enable custom sorting. Configure the sort order by selecting fields in the **Sort by** and**Sort by order** fields.

</td></tr><tr><td>

Sort by

</td><td>

Select any field in the list for sorting the spans in the timeline. Common practice is to select either the **Start date field** or the **End date field** as the sorting field. If you select a different sorting field, also include that field in the list of tooltip text fields to give users a way of discovering the sort criteria.

</td></tr><tr><td>

Sort by order

</td><td>

Select the sort order for the sorting fields selected.

</td></tr><tr><td class="sub-head" colspan="2">

Interactive options

</td></tr><tr><td>

Allow horizontal moving?

</td><td>

Select this check box to permit users to drag timeline spans horizontally. Dragging changes the start and end dates and updates the record.

</td></tr><tr><td>

Allow start time dragging?

</td><td>

Select this check box to permit users to update the record by dragging the start time of a span.

</td></tr><tr><td>

Allow end time dragging?

</td><td>

Select this check box to permit users to update the record by dragging the end time of a span.

</td></tr><tr><td>

Restriction

</td><td>

Specify the behavior when you drag a child span. This option is available only if you did not specify **Range calculator** for the parent timeline page.-   **None**: No restriction is in place.
-   **Restrict by parent**: Move the child span only within the time frame defined by the parent span.
-   **Update parent**: Update the span when you move the child span outside the time frame defined by the parent span.


</td></tr></tbody>
</table>
**Parent Topic:**[Timeline pages](../concept/c_TimelinePages.md)

