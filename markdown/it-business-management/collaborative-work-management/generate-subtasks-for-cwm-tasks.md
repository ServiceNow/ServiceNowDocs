---
title: Generate child tasks for CWM tasks
description: Use AI to create child tasks for a large and complex CWM task in the List view. Child tasks are generated from the task's short description and description, reducing manual work breakdown effort.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/generate-subtasks-for-cwm-tasks.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 1
keywords: [subtasks, child tasks, ServiceNow Otto, AI generation, CWM, task, hierarchy, generate]
breadcrumb: [Manage work using Boards, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Generate child tasks for CWM tasks

Use AI to create child tasks for a large and complex CWM task in the List view. Child tasks are generated from the task's short description and description, reducing manual work breakdown effort.

## Before you begin

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

-   Verify that ServiceNow Otto for CWM is active on your instance.
-   A task must exist in the CWM board.

Role required: sn\_cwm\_ai.cwm\_ai\_user

## About this task

AI generates child tasks from any CWM task type by analyzing the task's short description and description. If the task description doesn't provide enough context, child tasks can't be generated. Generated child tasks appear as a hierarchy under the parent task in the List view.

If a task has child tasks, the existing child tasks are analyzed and aren't duplicated when the skill runs.

**Note:** It isn't supported for connected work items, such as incident, change, problem, or demand tasks.

## Procedure

1.  Navigate to **Workspaces** &gt; **Collaborative Work Management**.

2.  From a space, select a Board.

3.  Select the **List** view.

4.  Move the cursor over the short description of the task.

    \[Omitted image "generate-subtasks-cwm.png"\] Alt text: The Generate Subtasks option on a task row in the List view.

    The Generate Subtasks icon appears on the row.

5.  Select the Generate Subtasks icon.

    The icon changes to a loading indicator while AI generates the child tasks, then returns to the original icon when the generation is complete.


## Result

The generated child tasks are inserted as a hierarchy under the parent task in the List view.

**Parent Topic:**[Managing work using Boards in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/cwm-boards.md)

