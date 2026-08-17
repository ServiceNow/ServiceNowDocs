---
title: Create a CWM task or story under a project task
description: Break down a project task by creating child CWM tasks or stories under it on a Board. New child items are automatically linked to the parent project task and to its project.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/create-cwm-work-under-project-task.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 2
keywords: [project task, child task, add child, context menu]
breadcrumb: [Integration with Project Workspace, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Create a CWM task or story under a project task

Break down a project task by creating child CWM tasks or stories under it on a Board. New child items are automatically linked to the parent project task and to its project.

## Before you begin

You must be an assignee of the project task through one of the following:

-   Listed in the **Assigned to** field on the project task.
-   Listed as a resource assignee on the project task.
-   A member of a group that is listed as a group resource assignee on the project task.

The project task must not already have child project tasks. When a project task has child project tasks, adding CWM child items is blocked for all users. For details on assignee and hierarchy rules, see [Project task hierarchy and permissions in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/project-task-rules-in-cwm.md).

Role required: sn\_cwm.cwm\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Collaborative Work Management**.

2.  Open the Board that shows the project task, and switch to the List view.

3.  Open the context menu for the project task row.

4.  Select one of the following options:

    -   **Add child CWM task** to create a task.
    -   **Add child story** to create a story.
    Both **Add child CWM task** and **Add child story** appear to all users, whether or not you're an assignee. The child item is created only if you're an assignee of the project task, and the project task doesn't already have child project tasks. Otherwise, selecting either option displays an inline error notification instead of creating the child.

    **Add child story** completes only when the project task's phase type is Agile. On a project task with any other phase type, selecting **Add child story** displays an error notification instead of creating the story.

    For the full assignee and hierarchy rules, see [Project task hierarchy and permissions in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/project-task-rules-in-cwm.md).

5.  Enter the details for the new task or story inline.

6.  Press the **Enter** key or click anywhere outside the row to save the new item.

    The new child item is created with the **Project task** field set to the parent project task and the **Project** field set to that project task's project.


## Result

The new CWM task or story is displayed as a child row under the project task. The child item inherits the connection to the project task's project.

**Parent Topic:**[CWM integration with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/connect-project-workspace-cwm.md)

**Related topics**  


[CWM integration with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/connect-project-workspace-cwm.md)

[Change or remove the project task connection for a CWM item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/change-project-task-connection-in-cwm.md)

[Project task hierarchy and permissions in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/project-task-rules-in-cwm.md)

