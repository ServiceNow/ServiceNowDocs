---
title: Connected CWM work on the project planning page
description: Understand how the connected Collaborative Work Management \(CWM\) tasks are displayed on your project's planning page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/project-workspace/connected-cwm-work-in-planner-pw.html
release: zurich
product: Project Workspace
classification: project-workspace
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 2
keywords: [CWM connected tasks, planning page, date conflict, connected work]
breadcrumb: [Integration with CWM, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Connected CWM work on the project planning page

Understand how the connected Collaborative Work Management \(CWM\) tasks are displayed on your project's planning page.

When CWM is active in your instance, CWM tasks and stories linked to your project tasks appear inline as child rows under each project task on the planning page. Project managers can see execution activity from the team without leaving Project Workspace.

Only the first level of the CWM hierarchy is displayed under a project task. Nested children within CWM aren't shown on the planning page.

## Inline display and editing of connected work

Each connected CWM item appears with standard columns for name, assignee, status, and dates. A Board icon marks each connected CWM row so that you can distinguish it from project tasks. The rows are collapsible under their parent project task.

The display of connected items is controlled by a per-user setting. To turn the display on or off, see [Show or hide connected CWM tasks on the planning page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/show-hide-connected-tasks-in-planner-pw.md).

Inline editing is not supported for connected CWM rows on the planning page. To edit a connected item, open it either in the side panel of the Project planning page or in CWM. To edit a CWM task, you need the sn\_cwm.cwm\_user role.

## Date conflict indicator

A red warning icon appears in the WBS column of a connected CWM row when its planned dates fall outside the parent project task's planned dates. Hovering over the icon shows a tooltip that describes the specific conflict.

The tooltip displays one of the following messages:

-   **start date is before parent planned start date** when the connected item starts before the parent project task starts.
-   **end date exceeds parent planned end date** when the connected item ends after the parent project task ends.
-   **dates outside parent planned dates** when the connected item starts before and ends after the parent, or falls entirely outside the parent's date range.

The indicator clears automatically when the dates are corrected to fit within the parent project task's planned dates.

## What team members see in CWM

Team members work with the same connected items from within CWM Boards, list views, and My Work. For details on the CWM side of the integration, see .

**Parent Topic:**[Project Workspace integration with CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/cwm-integration-pw.md)

