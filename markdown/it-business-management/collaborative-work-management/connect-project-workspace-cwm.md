---
title: CWM integration with Project Workspace
description: View and manage project tasks alongside CWM work without switching applications. Team members can see assigned project tasks, break down work, and manage connections while project managers track execution in Project Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/connect-project-workspace-cwm.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 7
keywords: [Project Workspace, project task, connected work, PWS integration]
breadcrumb: [Use, Collaborative Work Management, Strategic Portfolio Management]
---

# CWM integration with Project Workspace

View and manage project tasks alongside CWM work without switching applications. Team members can see assigned project tasks, break down work, and manage connections while project managers track execution in Project Workspace.

The Project Workspace integration with Collaborative Work Management \(CWM\) gives project managers and team members a shared view of work across both applications. Team members work inside CWM using Boards and My Work. Project managers track that same work inside Project Workspace.

Each CWM task or story can be linked to a project and a project task.

## Enabling the integration

Both applications must be installed and active in your instance to use the integration.

-   Collaborative Work Management \(CWM\) v10.2.0 and later. For installation, see [Install Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/install-cwm.md).
-   Project Workspace v7.5.0 and later. For installation, see [Install Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/install-project-workspace.md).

When both are active, the **Project** and **Project task** fields are available on CWM task records. The related row context menu options, such as **Add child CWM task** and **Add child story**, also are available in the List view.

## Bring project tasks onto a Board

If a project task isn't already on your Board, you can add it as connected work. For the steps, see [Connect work from other ServiceNow apps to CWM Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/connect-work-to-cwm-boards.md).

Adding a project task to a Board doesn't bring across the CWM tasks or stories that are already linked to that project task. Each Board can have its own set of connected work items for the same project task. In Project Workspace, all of these connected items appear together under the project task.

## How the integration supports collaborative work

The integration is designed so that team members and project managers can work in their preferred tools without losing visibility into each other's activity.

-   **Stay in CWM for daily work**

    Create, update, and move CWM tasks and stories linked to a project task from Boards, list views, and My Work. You can also see which project task each work item supports without opening Project Workspace.

-   **Break down work assigned to you**

    If you are an assignee on a project task, you can create additional CWM tasks and stories under it directly from a Board. New items are automatically linked to the project task and its project.

-   **Give project managers direct visibility**

    Project managers see the CWM tasks and stories your team is executing directly under each project task on the planning page. They don't need Board access to review status, and a date-conflict indicator flags when a CWM item's planned dates fall outside the parent project task.

-   **Share access through project permissions**

    Users with read or write access to a project or project task can view and edit the linked CWM tasks, even without Board membership. Team leads and project stakeholders can act on connected work without being added to every Board.


## When a project or project task is deleted

Deleting a project or a project task doesn't delete the CWM tasks or stories connected to it. The connected CWM items stay on their Boards. Only the **Project** and **Project task** column values are cleared, and each affected item returns to the initial level on the Board.

A connected item doesn't automatically return to its earlier parent. For example, in a Website rebuild project, the CWM task **Draft homepage copy** starts as a child of another CWM task, **Content planning**. You then reconnect **Draft homepage copy** to the project task **Prepare launch content**. If **Prepare launch content** is later deleted, **Draft homepage copy** stays on the Board but moves to the initial level as an independent task. It doesn't return under **Content planning**.

## What team members do in CWM

From within CWM, team members can perform the following actions:

-   See the **Project** and **Project task** that each work item supports. For more information, see [Show the Project and Project task columns in a CWM Board](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/show-project-columns-in-cwm-list-view.md).
-   Track project tasks assigned to them or to a group they belong to in My Work. For more information, see [View project tasks assigned to you in CWM My Work](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/view-project-tasks-in-cwm-my-work.md).
-   Create additional CWM tasks and stories under a project task they are assigned to. For more information, see [Create a CWM task or story under a project task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/create-cwm-work-under-project-task.md).
-   Change or remove the project task connection on a CWM item. For more information, see [Change or remove the project task connection for a CWM item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/change-project-task-connection-in-cwm.md).

Not every action is available on every project task. Assignee, hierarchy, and item-type conditions determine what's allowed. For details, see [Project task hierarchy and permissions in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/project-task-rules-in-cwm.md).

## What the project manager sees in Project Workspace

Project managers can enable the display of connected tasks in the Planner tab of a project in Project Workspace. When connected tasks display is enabled, the CWM tasks and stories linked to project tasks are shown as child items under each project task in the Planner. However, inline editing of these CWM child rows is not supported. Only the first level of the CWM hierarchy appears in the Planner.

When a linked CWM task has a start date earlier or an end date later than the project task, the date conflict is indicated in red on the connected task row. The indicator clears when the dates are corrected.

For information on enabling and using these views, see [Project Workspace integration with CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/cwm-integration-pw.md).

## Access through project permissions

Users who have read or write access to a project or a project task, and have the **sn\_cwm.cwm\_user** role, can view and edit the connected CWM tasks. For more information, see [Project task access in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/cwm-access-via-project-permissions.md).

-   **[Project task hierarchy and permissions in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/project-task-rules-in-cwm.md)**  
Learn how assignee, hierarchy, and item-type conditions determine which project tasks accept CWM children and who can add or move them on a Board.
-   **[Show the Project and Project task columns in a CWM Board](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/show-project-columns-in-cwm-list-view.md)**  
Display the **Project** and **Project task** columns on a CWM Board List view so that team members can see which project task each work item supports.
-   **[View project tasks assigned to you in CWM My Work](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/view-project-tasks-in-cwm-my-work.md)**  
Track project tasks alongside your other CWM work from a single view in My Work. Project tasks show up when you're assigned to them directly or through a group.
-   **[Create a CWM task or story under a project task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/create-cwm-work-under-project-task.md)**  
Break down a project task by creating child CWM tasks or stories under it on a Board. New child items are automatically linked to the parent project task and to its project.
-   **[Change or remove the project task connection for a CWM item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/change-project-task-connection-in-cwm.md)**  
Reassign a CWM task or story to a different project task, or break the connection to a project task entirely, from the List view of the CWM Board.

**Parent Topic:**[Using Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/using-collaborative-work-management.md)

