---
title: My Work in CWM
description: Manage your work from all ServiceNow applications from a centralized view in the Collaborative Work Management workspace.
locale: en-US
release: yokohama
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use, Collaborative Work Management, Strategic Portfolio Management]
---

# My Work in CWM

Manage your work from all ServiceNow applications from a centralized view in the Collaborative Work Management workspace.

My Work provides a centralized view of all your assigned tasks, including project tasks, problems, and incidents. It also offers visualizations that group items by state, priority, and status, such as open or overdue.

Work items from all ServiceNow applications assigned to you’re displayed in My Work. If you receive a work item on the CWM Board via Connected Work, those items appear here as well. This ensures you have a single source for all assigned work without the need to switch between applications.

**Note:**

-   Any task record created in a table that doesn’t extend the Task \[task\] table, such as VTask, won't show up in My Work.
-   If you’re added as **Additional assignee** to a task, work with your admin to enable the display of such tasks in My Work. See [Properties installed with CWM](../reference/properties-installed-with-cwm.md).

![My Work filters in CWM.](../images/cwm-my-work.png "Overview tab of My Work")

The following are the filters available on My Work:

-   Task type filter displays a list of all task types that are assigned to you currently.
-   Date filter lets you select predefined or custom date ranges.
-   You can choose to include open items that don't have start or end dates.

My Work page has two views, Overview and List.

-   Overview tab shows multiple widgets that provide information related to the progress of your work. It also enables you to apply filters on the type of tasks that you want to view.
-   List tab shows all open work items assigned to you in a list or grid format, where you can apply the group by and filter options on the columns.

    List view also provides a link back to the source of the work item. For example, if your work item is a Risk, the Source column in the List view provides a navigation to the RIDAC page of the Project Workspace application.


<table id="table_vtn_bhz_bcc"><thead><tr><th>

Widget or option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work item type filter

</td><td>

Choose the type of work items that you want to view in My Work.For example, if your current assignments consist of CWM tasks, Projects, and Incidents, then the Task type filter only shows these three options to select from.

Also, CWM tasks of all types, including custom CWM tasks, will be grouped as **CWM Tasks** type.

</td></tr><tr><td>

Date

</td><td>

Filter the tasks by their start and end dates.

</td></tr><tr><td>

Include open items with no dates

</td><td>

Enable display of work items that have no start date, end date, or both.

</td></tr><tr><td>

Overall Progress

</td><td>

Percentage of work that is completed

</td></tr><tr><td>

My Open Items

</td><td>

Number of work items that are pending.SelectingClicking the number opens a list view of all work items assigned to you and are in the **Pending** state.

</td></tr><tr><td>

My Overdue Items

</td><td>

Number of work items that are overdue.Clicking the number opens a list view of all work items assigned to you that are past their due date.

</td></tr><tr><td>

Completed

</td><td>

Number of work items that are complete.Clicking the number opens a list view of all work items assigned to you that are in the **Closed Complete** state.

</td></tr><tr><td>

Task by State

</td><td>

Bar chart that groups all work items assigned to you by their current state. Clicking a bar opens a list of tasks that meet the filter criteria for the corresponding bar.For more information on how the tasks are grouped by state, see [Grouping of tasks in status reports of CWM My Work](../reference/grouping-of-tasks-in-status-reports-of-cwm-my-work.md).

</td></tr><tr><td>

Task by Priority

</td><td>

Bar chart that groups all work items assigned to you by their priority. Clicking a bar opens a list of tasks that meet the filter criteria for the corresponding bar.For more information on how the tasks are grouped by priority, see [Grouping of tasks in status reports of CWM My Work](../reference/grouping-of-tasks-in-status-reports-of-cwm-my-work.md).

</td></tr></tbody>
</table>![List view of work items from My Work.](../images/cwm-my-work-list-view.png "List tab of My Work")

The List view shows all open work items assigned to you. Select the **Short description** of a work item to view its details in a modal pop-up. Select the **Source** of a work item to open the work item in a new tab.

**Note:**

-   The list view displays all the tasks with start or end dates that fall within the range of the date filter.
-   Any closed task that doesn't have dates populated isn’t shown in My Work.
-   You can't perform bulk editing of state, priority, or date values of the tasks through My Work.

**Parent Topic:**[Using Collaborative Work Management](using-collaborative-work-management.md)

