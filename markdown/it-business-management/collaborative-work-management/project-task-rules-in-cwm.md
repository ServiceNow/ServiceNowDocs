---
title: Project task hierarchy and permissions in CWM
description: Learn how assignee, hierarchy, and item-type conditions determine which project tasks accept CWM children and who can add or move them on a Board.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/project-task-rules-in-cwm.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 3
keywords: [project task, assignee, permission, hierarchy, project phase]
breadcrumb: [Integration with Project Workspace, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Project task hierarchy and permissions in CWM

Learn how assignee, hierarchy, and item-type conditions determine which project tasks accept CWM children and who can add or move them on a Board.

Adding or moving a CWM task or story under a project task is subject to assignee, hierarchy, and item-type rules. These rules determine which context menu options appear, which project tasks are available in the **Project task** column dropdown, and whether an action completes or displays an inline notification.

## Project task assignees

A user counts as an assignee of a project task when at least one of the following is true:

-   The user is listed in the **Assigned to** field on the project task.
-   The user is listed as a resource assignee on the project task.
-   The user is part of a resource assignment group on the project task.

Only assignees can create, indent, or drop CWM items under a project task. The **Add child CWM task** and **Add child story** options still appear for non-assignees, but selecting one displays an inline error notification instead of creating the item.

## Hierarchy restriction on CWM child tasks

A project task can't accept CWM child tasks when the project task already has child project tasks. This rule applies to all users, including assignees. To see the existing child project tasks for a project task, open it in Project Workspace.

The **Project task** column dropdown on a Board excludes project tasks that already have child project tasks. So, those project tasks can't be selected as a new parent when a CWM item is moved.

## Child task and story creation availability

Both the **Add child CWM task** and **Add child story** options appear on every project task, regardless of its phase type. Whether the action completes depends on the phase type:

-   On an agile project phase, both **Add child CWM task** and **Add child story** complete successfully.
-   On a project task with any other phase type, only **Add child CWM task** completes. Selecting **Add child story** displays an error notification instead of creating the story.

## Restriction signals on the Board

Restrictions are surfaced in one of three ways, depending on the rule and the action:

-   **Error notifications for non-assignees**

    For non-assignees, the **Add child CWM task** and **Add child story** options still appear, but selecting one displays an inline error notification instead of creating the item.

-   **Dropdown exclusions**

    While associating a CWM task with a project and project task, the **Project task** column dropdown shows only those project tasks that don't already have child project tasks.

-   **Inline notifications**

    If a project task already has child project tasks, then you can't associate additional CWM tasks or stories.


**Parent Topic:**[CWM integration with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/connect-project-workspace-cwm.md)

**Related topics**  


[Create a CWM task or story under a project task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/create-cwm-work-under-project-task.md)

[Change or remove the project task connection for a CWM item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/change-project-task-connection-in-cwm.md)

[CWM integration with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/connect-project-workspace-cwm.md)

