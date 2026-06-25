---
title: Search work order tasks
description: Minimize scrolling and filter tasks that show in the task panel. Quickly search by keyword, or see all the tasks assigned to a group or territory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/search-work-order-tasks.html
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Dispatcher Workspace, Assigning tasks from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Search work order tasks

Minimize scrolling and filter tasks that show in the task panel. Quickly search by keyword, or see all the tasks assigned to a group or territory.

## Before you begin

Role required: wm\_dispatcher

## About this task

You can search work order tasks using the following criteria:

-   Keyword
-   Match calendar dates
-   Work order task state

You can also filter and sort work order tasks based on the fields that are configured by the administrator.

If you add a work order task number to the work notes of another work order task, when you search for the work order task number that was added to the work notes both the tasks show up. This happens because it's a keyword search that causes both the work order tasks show up. For example if you add WOT123 to the notes of WOT456, then when you search for WOT123, both WOT123 and WOT456 show up.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select **Dispatcher Workspace**.

3.  In the task panel, search for a work order task.

<table id="table_ttg_rsh_wkb"><thead><tr><th>

Search criteria

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Keyword

</td><td>

Type the search term in the search field and select the Search icon \( \[Omitted image "search\_icon.png"\] Alt text: Search icon.\).**Note:** To clear the search and display all tasks, delete the search term and press the Enter key.

</td></tr><tr><td>

Calendar dates

</td><td>

Select the **Turn on filter tasks by calendar dates** \(\[Omitted image "filter-calendar-date.png"\] Alt text: Turn on filter tasks by calendar dates.\) icon to display tasks associated with the calendar dates in addition to the selected filter.**Note:** The task panel displays tasks based on dates as follows:

-   If the window start and window end dates of a task fall within the dates currently shown on the calendar.
-   If the window end field is empty, then the task appears if the calendar is displaying a date beyond the task's window start date.
-   If the window start field is empty, then the task appears if the calendar shows a date before the task's window end date.
-   If both the window start and window end fields are empty, then the task panel's task appears when Match calendar dates are enabled.
-   If the calendar display window is modified, the task panel is updated to display only tasks that match the new date range.


</td></tr><tr><td>

Assignment group/ Territory task filter

</td><td>

Select the **Turn ON assignment group/ territory-matching task filtering** \(\[Omitted image "assignment-group-matching.png"\] Alt text:\) icon to limit the task panel to only display tasks that belong to your selected assignment groups or territories.

</td></tr><tr><td>

State

</td><td>

Select the filter from the list of default filters. The default fields that appear in the **Filter by** list are configured by the administrator.

</td></tr><tr><td>

Sort options

</td><td>

Select the Sort icon \(\[Omitted image "sort\_options.png"\] Alt text: Sort icon.\) to sort tasks. The default sort options that appear are configured by the administrator.

</td></tr></tbody>
</table>
## Result

The tasks that meet the search requirements are displayed in the task panel.

**Related topics**  


[Search for appropriate Field Service agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/search-agents-tasks.md)

[Assign work order tasks to agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/manage-work-order-tasks-dw.md)

