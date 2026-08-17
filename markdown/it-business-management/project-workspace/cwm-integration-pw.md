---
title: Project Workspace integration with CWM
description: Track team execution alongside your project plan by displaying Collaborative Work Management \(CWM\) tasks and stories linked to your project tasks directly on the planning page. Team members continue working in CWM, while you keep visibility in Project Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-workspace/cwm-integration-pw.html
release: australia
product: Project Workspace
classification: project-workspace
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 3
keywords: [CWM integration, connected work, project execution, team collaboration]
breadcrumb: [Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Project Workspace integration with CWM

Track team execution alongside your project plan by displaying Collaborative Work Management \(CWM\) tasks and stories linked to your project tasks directly on the planning page. Team members continue working in CWM, while you keep visibility in Project Workspace.

The integration between Project Workspace and Collaborative Work Management \(CWM\) gives project managers and team members a shared view of the same work. Team members create, update, and manage CWM tasks and stories linked to a project task from within CWM Boards and My Work. Project managers see those same items inline on the planning page, alongside the regular project tasks.

## Enabling the integration

The integration is available when both applications are installed and active in your instance.

-   Collaborative Work Management \(CWM\) v10.2.0 and later. For installation, see [Install Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/install-cwm.md).
-   Project Workspace v7.5.0 and later. For installation, see [Install Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/install-project-workspace.md).

When both applications are active, the **Show connected tasks** toggle is available in Settings on the planning page of a Project. Turning this toggle on displays the connected CWM tasks and stories within their parent project tasks.

## Project execution with CWM integration

The integration is designed so that project managers and team members can work in their preferred tools without losing visibility into each other's activity.

-   **Track team execution in one place**

    Project managers see the CWM tasks and stories that a team is executing under each project task, with standard columns for name, assignee, status, and dates. Only the first level of the CWM hierarchy is displayed, so the planning page stays focused on the project plan.

-   **Catch schedule risks earlier**

    A date-conflict indicator appears on a connected CWM row when its planned dates fall outside the parent project task's planned dates. Project managers can address the conflict with the team before it rolls up into a slippage on the project plan.

-   **Enable teams work in their preferred tool**

    Team members break down a project task or phase by creating additional CWM tasks and stories under it from CWM Boards. The connection to the project task is preserved automatically, so any child items they create are displayed on the planning page appropriately.

-   **Grant access through project permissions**

    Users with read or write access to a project or project task can view and edit the linked CWM tasks, even without membership in the Board's Space. Project security carries across the two applications without separate Board access for every project team member.


## Display of CWM tasks on the project Planning page

Connected CWM tasks and stories appear as child rows under each project task. The display is controlled by a per-user setting that is enabled by default. For more details, see the following:

-   [Show or hide connected CWM tasks on the planning page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/show-hide-connected-tasks-in-planner-pw.md).
-   [Show or hide connected CWM tasks on the planning page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/show-hide-connected-tasks-in-planner-pw.md).

## Team member view in CWM

Team members work with the same connected items from within CWM. For details on the CWM side of the integration, such as creating, moving, and viewing connected work, see [CWM integration with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/connect-project-workspace-cwm.md).

-   **[Connected CWM work on the project planning page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/connected-cwm-work-in-planner-pw.md)**  
Understand how the connected Collaborative Work Management \(CWM\) tasks are displayed on your project's planning page.
-   **[Show or hide connected CWM tasks on the planning page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/show-hide-connected-tasks-in-planner-pw.md)**  
Enable or disable the display of connected Collaborative Work Management \(CWM\) tasks and stories on the Project planning page.

**Parent Topic:**[Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/project-workspace-landing-page.md)

