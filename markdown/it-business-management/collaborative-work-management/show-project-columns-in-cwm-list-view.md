---
title: Show the Project and Project task columns in a CWM Board
description: Display the Project and Project task columns on a CWM Board List view so that team members can see which project task each work item supports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/show-project-columns-in-cwm-list-view.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 2
keywords: [project column, project task column, CWM List view]
breadcrumb: [Integration with Project Workspace, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Show the Project and Project task columns in a CWM Board

Display the **Project** and **Project task** columns on a CWM Board List view so that team members can see which project task each work item supports.

## Before you begin

Role required: sn\_cwm.cwm\_user

## About this task

The **Project** and **Project task** columns are shown in the default List view of a CWM Board. If the columns have been removed from a personalized view, use column customization to add them back.

The **Project** value is derived from the **Project task** value and updates automatically when the **Project task** value changes. You can also set the **Project** value directly, which clears the **Project task** value. For more information, see [Change or remove the project task connection for a CWM item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/change-project-task-connection-in-cwm.md). You can open a linked project or project task directly from these columns.

## Procedure

1.  Navigate to **Workspaces** &gt; **Collaborative Work Management**.

2.  Open the Space that contains your Board, and then open the Board in the List view.

3.  Select the Personalize icon \(\[Omitted image "icon-personalize.png"\] Alt text: Personalize List and Gantt views.\).

    If the **Project** and **Project task** columns are already visible, skip to the last step.

4.  Select the **Project** and **Project task** columns from the Available columns list to move them to the Active columns list.

    \[Omitted image "cwm-pws-project-columns.png"\] Alt text: Personalize panel with Project and Project task in the Active columns list.

5.  Save the current view so the columns persist for the next session.

    For more information about saving a view, see [Update a CWM Board view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/update-a-cwm-board-view.md).

6.  To open the linked record, select the value in the **Project** or **Project task** column.

    The linked Project Workspace record opens in a new browser tab.


## Result

The **Project** and **Project task** columns display for each work item on the Board. For work items with no connection to a project task, the columns are empty.

**Parent Topic:**[CWM integration with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/connect-project-workspace-cwm.md)

**Related topics**  


[CWM integration with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/connect-project-workspace-cwm.md)

[Change or remove the project task connection for a CWM item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/change-project-task-connection-in-cwm.md)

[Personalize List, Gantt and Kanban display for CWM Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/personalize-cwm-board-views.md)

