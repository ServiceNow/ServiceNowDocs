---
title: Change or remove the project task connection for a CWM item
description: Reassign a CWM task or story to a different project task, or break the connection to a project task entirely, from the List view of the CWM Board.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/change-project-task-connection-in-cwm.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 2
keywords: [project task connection, break connection, move task, un-indent]
breadcrumb: [Integration with Project Workspace, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Change or remove the project task connection for a CWM item

Reassign a CWM task or story to a different project task, or break the connection to a project task entirely, from the List view of the CWM Board.

## Before you begin

The target project task must not have child project tasks. When a project task has child project tasks, moving a CWM item under it is blocked for all users. For details on assignee and hierarchy rules, see [Project task hierarchy and permissions in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/project-task-rules-in-cwm.md).

Role required: sn\_cwm.cwm\_user

## About this task

Use one of the following approaches based on what you want to change:

-   To move a CWM item to a different project task, update the **Project task** column value from the List view.
-   To remove the connection to a project task without moving the item elsewhere, use the un-indent option from the context menu.

The **Project task** column dropdown lists only project tasks that do not have child project tasks. Project tasks with children are excluded because they cannot accept CWM child items.

## Procedure

1.  Navigate to **Workspaces** &gt; **Collaborative Work Management**.

2.  Open the Board that contains the item, and switch to the List view.

3.  To move the item to a different project task, in the **Project task** column for the item, select the new project task from the dropdown.

    The item is re-parented on the Board under the new project task. The **Project** column updates automatically to reflect the new parent's project.

4.  To change only the project without selecting a new project task, in the **Project** column, select a different project.

    When the project changes, the **Project task** value is cleared for the item.

5.  To break the connection entirely, open the context menu for the child item and select **Un-indent item**.

    The **Project task**, **Project**, and parent fields are cleared. The item is no longer displayed under a project task on the Board.


**Parent Topic:**[CWM integration with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/connect-project-workspace-cwm.md)

**Related topics**  


[CWM integration with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/connect-project-workspace-cwm.md)

[Create a CWM task or story under a project task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/create-cwm-work-under-project-task.md)

[Show the Project and Project task columns in a CWM Board](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/show-project-columns-in-cwm-list-view.md)

[Project task hierarchy and permissions in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/project-task-rules-in-cwm.md)

