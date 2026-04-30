---
title: My Work in CWM
description: Manage all your work such as CWM tasks, project tasks, RIDAC items, and Agile stories from a centralized view in the Collaborative Work Management workspace.
locale: en-US
release: xanadu
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Collaborative Work Management, Strategic Portfolio Management]
---

# My Work in CWM

Manage all your work such as CWM tasks, project tasks, RIDAC items, and Agile stories from a centralized view in the Collaborative Work Management workspace.

My Work in CWM consolidates all your tasks across CWM and Strategic Portfolio Management \(SPM\) workspaces, provides visualizations around work such as task grouping by state, priority, and key metrics such as open and overdue items.

Tasks in My Work include all work items for which you are added to the **Assigned to** or **Additional assignee** fields.

![My Work filters in CWM.](../images/cwm-my-work.png "Overview tab of My Work")

My Work page has two views, Overview and List.

-   Overview tab shows multiple widgets that provide information related to the progress of your work. It also enables you to apply filters on the type of tasks that you want to view.
-   List tab shows all open work items assigned to you in a list or grid format, where you can apply the group by and filter options on the columns.

    List view also provides a link back to the source of the work item. For example, if your work item is a Risk, the Source column in the List view provides a navigation to the RIDAC page of the Project Workspace application.


<table id="table_vtn_bhz_bcc"><thead><tr><th>

Widget or option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overall Progress

</td><td>

Percentage of work that is completed

</td></tr><tr><td>

My Open Items

</td><td>

Number of work items that are pending.Clicking the number opens a list view of all work items assigned to you and are in the **Pending** state.

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

</td></tr><tr><td>

Filters

</td><td>

Choose the type of work items that you want to view in My Work. Based on the SPM applications that are installed in your ServiceNow instance, the following types are available to choose from:-   CWM Tasks
-   Project Tasks
-   Demand Tasks
-   Risks
-   Issues
-   Decisions
-   Actions
-   Change Requests
-   Stories
-   Scrum tasks

</td></tr><tr><td>

Date

</td><td>

Filter the tasks by their start and end dates.

</td></tr><tr><td>

Include open items with no dates

</td><td>

Enable display of work items that have no start date, end date, or both.

</td></tr></tbody>
</table>-   CWM tasks or Project tasks that have the **Additional assignee** field set to your name are also shown.
-   Project tasks that are assigned to you from the **Assigned to** or **Resource Assignees** fields are shown.

![List view of work items from My Work.](../images/cwm-my-work-list-view.png "List tab of My Work")

The List view shows all open work items assigned to you. Click the **Short description** of a work item to view its details in a modal pop up. Click the **Source** of a work item to open the work item in a new tab.

**Note:** Connected work items are not shown in the My Work page, unless those items are story, poject task, demand task, or any RIDAC records.

