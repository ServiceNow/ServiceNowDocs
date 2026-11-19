---
title: Monitor and track work using dashboards in CWM Boards
description: The Dashboard view displays a collection of widgets that visualize CWM Board data, giving teams an at-a-glance summary of task progress, priorities, and assignments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/collaborative-work-management/cwm-board-dashboards.html
release: zurich
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-08-20"
reading_time_minutes: 5
keywords: [Dashboard view, CWM, board dashboards, widgets, empty state]
breadcrumb: [Manage work using Boards, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Monitor and track work using dashboards in CWM Boards

The Dashboard view displays a collection of widgets that visualize CWM Board data, giving teams an at-a-glance summary of task progress, priorities, and assignments.

## Dashboard overview

The Dashboard view is one of the views available on a CWM Board, alongside List, Gantt, Kanban, and Sprint planning. It displays widgets, such as charts and score dials, that summarize the work items on the Board without requiring you to open individual records.

Every Board is provisioned with two predefined shared dashboards with a set of predefined widgets configured for each.

-   Team progress dashboard. See [Team progress dashboard in Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/cwm-team-progress-dashboard.md).

    \[Omitted image "cwm-team-progress-dashboard.png"\] Alt text: Team progress dashboard.

-   Team sprint tracker dashboard. See [Team sprint tracker dashboard in Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/cwm-team-sprint-tracker-dashboard.md).

    \[Omitted image "cwm-team-sprint-tracker-dashboard.png"\] Alt text: Team sprint tracker dashboard.


Existing Boards are configured with both predefined dashboards when your instance is upgraded.

Each Board can have multiple dashboards. Owners and editors can create dashboards and add predefined or custom widgets to them. They can also rename, duplicate, and delete dashboards. The predefined dashboards can't be renamed or deleted. All dashboards are shared with everyone who has access to the Board.

The dashboard selector in the dashboard header lets you switch between dashboards. The selector shows the name of the currently selected dashboard and lists the shared dashboards available on the Board. Widget data refreshes when you switch dashboards using the dashboard selector or reload the dashboard page. Widget data isn't updated in real-time while you're viewing a dashboard.

\[Omitted image "cwm-dashboard-selector.png"\] Alt text: Dashboard selector shows the current dashboard name.

## Benefits of dashboards

The benefits of Dashboards in CWM Boards are:

-   Dashboards show the current and updated data points at any point in time.
-   Teams don't have to leave the CWM Board for analysis, minimizing context switching.
-   Custom widgets can be created for the CWM custom columns.

## Access required for managing dashboards

|Action|Role required|
|------|-------------|
|Create a dashboard|Space owners and editors|
|Add predefined or custom widgets to a dashboard|Space owners and editors|
|View a dashboard and its widgets|Space viewers|
|Rename or duplicate a dashboard|Space owners and editors|
|Delete a dashboard|Space owners and dashboard creators|

## Predefined widgets

Widgets are the building blocks of a dashboard. They visualize Board data as charts, score dials, and other categories. Each category includes predefined widgets and, for some categories, a custom option, and are available in the Add widgets or Manage widgets panel of a dashboard.

Widgets are organized into six chart-type categories. Some categories include both predefined widgets and a custom option that you can configure with your columns and data.

-   Bar chart: Custom bar chart, Task by assignee, Sprint tasks by state, Sprint workload by assignee, Sprint spillover
-   Pie chart: Custom pie chart, Tasks by priority
-   Single score: Overdue tasks, Open tasks, Sprint tasks missing estimates
-   Dial score: Sprint progress, Task progress
-   Sprint charts: Sprint burndown, Sprint burnup, Sprint velocity chart

## Custom widgets

Custom widgets let you chart any column on the Board, including custom columns and columns from Connected Work items. You can create a custom bar or pie widget and bind it to the column of your choice.

The column picker lists columns from three sources, with no restriction on which type of column you can chart:

-   Predefined columns common to CWM task types, such as assigned to or assignment group.
-   Custom columns you have added to the Board.
-   Columns from Connected Work items on the Board, such as caller on an incident.

## Shareable dashboard links

A dashboard link can be shared with users who have at least viewing permissions to the Board where the dashboard is. A **Copy link** option is available under the Dashboard options menu. Selecting it copies the shareable link and displays a confirmation message.

Users without access can request access directly from the link. If the Dashboard tab is hidden from the recipient's view when they open the link, they land on the Board's default List view instead. Opening the link takes the recipient to the Board's Dashboard tab with that dashboard preselected, regardless of which dashboard they last viewed.

\[Omitted image "cwm-dashboard-copy-link.png"\] Alt text: The Copy Link option under Dashboard options.

-   **[Team progress dashboard in Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/cwm-team-progress-dashboard.md)**  
The Team progress dashboard supports waterfall use cases and includes widgets that visualize task completion and workload for the whole Board.
-   **[Team sprint tracker dashboard in Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/cwm-team-sprint-tracker-dashboard.md)**  
The Team sprint tracker dashboard supports agile use cases with widgets that visualize sprint progress, workload, and trend data for agile teams.
-   **[Create a dashboard for a CWM Board in Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/creating-dashboards-in-cwm.md)**  
Create a dashboard for a CWM Board to visualize work data using predefined or custom widgets. Track progress and spot issues without reviewing individual tasks or stories.
-   **[Add widgets to a dashboard in Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/add-a-widget-to-cwm-dashboard.md)**  
Add predefined or custom widgets to an empty state or existing dashboard on a CWM Board to visualize task and sprint data.
-   **[Rename a dashboard in Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/rename-a-dashboard-in-cwm.md)**  
Rename a dashboard in a CWM Board so your team can easily identify it among shared dashboards for any specific requirement.
-   **[Duplicate a dashboard in Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/duplicate-a-dashboard-in-cwm.md)**  
Duplicate a dashboard in a CWM Board to reuse an existing set of widgets in a new dashboard. This avoids rebuilding the same layout from scratch.
-   **[Remove widgets from a dashboard in Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/remove-a-widget-from-a-dashboard.md)**  
Remove widgets from a dashboard in a CWM Board to keep the dashboard focused on the metrics that still matter.
-   **[Delete a dashboard in Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/delete-a-dashboard-in-cwm.md)**  
Delete a dashboard in a CWM Board when your team no longer needs it.

**Parent Topic:**[Managing work using Boards in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/cwm-boards.md)

