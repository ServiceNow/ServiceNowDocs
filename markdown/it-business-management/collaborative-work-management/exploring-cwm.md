---
title: Exploring Collaborative Work Management
description: Collaborative Work Management \(CWM\) is a work management tool that centralizes tasks, documentation, and planning in a single workspace, helping knowledge workers, project managers, and agile teams manage work without switching between applications.
locale: en-US
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-04-02"
reading_time_minutes: 8
breadcrumb: [Collaborative Work Management, Strategic Portfolio Management]
---

# Exploring Collaborative Work Management

Collaborative Work Management \(CWM\) is a work management tool that centralizes tasks, documentation, and planning in a single workspace, helping knowledge workers, project managers, and agile teams manage work without switching between applications.

## Collaborative Work Management overview

Teams managing work across disconnected tools often lose context, duplicate effort, and struggle to maintain a clear picture of progress. Tasks live in one tool, documentation in another, and sprint planning in a third, with dependencies tracked in spreadsheets and status updates shared over email or chat.

CWM solves this by bringing tasks, documentation, and planning into a single workspace organized around Spaces. Each Space contains Boards for task and project management and Docs for documentation, so everything related to a team's work stays connected and accessible from one place.

Teams can choose how they work within CWM. Use a custom workflow for general task management, or run sprints end-to-end using the built-in Agile capabilities, including sprint planning, scrum tasks, and cross-team dependencies. Boards are highly configurable without admin involvement, and generative AI features help reduce manual overhead on task creation, formula building, and content generation.

CWM integrates with the broader ServiceNow AI Platform, connecting to other ServiceNow applications, records, and the Strategic Planning workspace so that team-level execution stays aligned with organizational goals.

## Collaborative Work Management users

|User|Description|
|----|-----------|
|Knowledge worker/Team member|Creates and manages tasks on Boards, collaborates on Docs, and tracks personal work in My Space. Uses [Now Assist for Collaborative Work Management \(CWM\)](../../now-assist-cwm/concept/now-assist-for-cwm-landing.md) to reduce manual overhead in task creation and formula building.|
|Project manager|Organizes work into Spaces and Boards, tracks progress across teams, and connects work to business goals and the Strategic Planning workspace.|
|Agile practitioner|Plans and runs sprints, manages backlogs, generates scrum tasks from user stories, and tracks cross-team dependencies.|
|SPM team member|Views and updates project and demand tasks from Project Workspace and Next Experience for Demand Management directly in CWM using the team member read or team member read-write role.|

## Collaborative Work Management benefits

<table id="table_wry_fs5_rzb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Keep all team work in one place by organizing Boards and Docs into shared Spaces. Your team gets a single location to find tasks, documentation, and status without switching between tools.

 Use **My Space** as a personal space to manage any work assigned to you.

</td><td>

[Spaces](cwm-spaces.md)

</td><td>

All users

</td></tr><tr><td>

Get started without admin involvement by configuring your own workflow and organizing work the way your team needs it.

-   Create custom fields for task records.
-   Switch between List, Gantt, and Kanban views.
-   Create custom work item types.
-   Add a list of additional assignees to a task.

</td><td>

[Boards](cwm-boards.md)

</td><td>

All users

</td></tr><tr><td>

Create and collaborate on meeting notes, technical specifications, or feature requirements directly within your workspace, keeping documentation connected to the work it supports.

 -   Create rich text docs and add action items to users from within and outside the team.
-   Collaborate on docs in real-time with multiple concurrent editors.
-   Use AI to summarize page content for quick insights, generate and refine content using custom prompts, or generate tasks directly from the information in your Doc and add them to Boards.

</td><td>

[Docs](cwm-docs.md)

</td><td>

Knowledge worker/Team member

</td></tr><tr><td>

Reduce repetitive setup and ensure consistency across your team by starting from predefined templates for Spaces, Boards, and Docs.

</td><td>

[Templates for Spaces, Boards, and Docs](templates-in-cwm-for-spaces-boards-and-docs.md)

</td><td>

All users

</td></tr><tr><td>

Run sprints end-to-end in CWM without switching to a separate Agile tool. Plan work into sprints, manage backlogs, track progress through the sprint lifecycle, and conduct retrospectives, all within your Board.

</td><td>

[Sprint planning in CWM](agile-sprint-planning-in-cwm.md)

</td><td>

Agile practitioner

</td></tr><tr><td>

Break user stories into granular scrum tasks to improve sprint execution and estimation. Assign tasks to team members and track daily progress through a sprint.

 Using Now Assist to accelerate sprint preparation, you can generate acceptance criteria for your stories from the story description, then generate an initial set of scrum tasks based on that description and criteria. Review and refine both before adding them to your sprint, or create scrum tasks manually from the story form.

</td><td>

[Scrum tasks](managing-scrum-tasks-for-stories-cwm.md)

</td><td>

Agile practitioner

</td></tr><tr><td>

Link work items as prerequisites, dependents, or related to surface dependencies directly in CWM without tracking them in spreadsheets or notes. Blocked items are visible at a glance on the Kanban board to help teams spot bottlenecks and plan work in the right sequence.

</td><td>

[Task dependencies and relationships](managing-task-dependencies-relationships-cwm.md)

</td><td>

Agile practitioner

</td></tr><tr><td>

Switch between List, Gantt, and Kanban view modes to visualize work in the format that fits your team's workflow. Save personalized views or create shared views to give the whole team a consistent starting point.

</td><td>

[Board views](board-views-in-cwm.md)

</td><td>

All users

</td></tr><tr><td>

Add calculated columns to the List view that automatically compute values from your task data, such as totaling story points, calculating date differences, or deriving custom metrics. Build formulas manually using the Formula Builder panel.

 You can also describe your calculation in plain language and let AI generate the formula for you.

</td><td>

[Formula columns](../task/add-formula-column-cwm-boards.md)

</td><td>

Knowledge worker/team member, Project manager

</td></tr><tr><td>

Reduce manual overhead by automating repetitive processes such as sending notifications, reassigning tasks, or updating task priority when conditions are met, without involving an admin.

</td><td>

[Automations](implementing-automations-in-collaborative-work-management.md)

</td><td>

Project manager

</td></tr><tr><td>

Bring work from across your ServiceNow AI Platform applications onto a single CWM Board, giving your team one place to plan and manage cross-functional work without switching between applications.

</td><td>

[Connected work in CWM](unified-boards-for-connected-work-in-cwm.md)

</td><td>

Project manager, SPM team member

</td></tr><tr><td>

Access and update project and demand tasks directly in CWM without requiring access to Project Workspace or Next Experience for Demand Management. View assigned work in **My Work** or pull tasks into a Board using **Connected Work**.

</td><td>

[Team member roles for project work](cwm-team-member-roles.md)

</td><td>

SPM team member

</td></tr><tr><td>

Connect team execution to organizational strategy by surfacing CWM Boards in Strategic Planning portfolio plans, where work can be prioritized and roadmapped alongside other investments.

</td><td>

[Connecting CWM with Strategic Planning or Portfolio Planning](connect-cwm-spw.md#)

</td><td>

Project manager

</td></tr><tr><td>

Reference live ServiceNow AI Platform records such as Incidents, Risks, or Issues directly in CWM Docs. References update automatically to reflect the latest record data, keeping documentation accurate without manual updates.

</td><td>

[Enable ServiceNow AI Platform records in CWM Docs](../task/enable-now-platform-servicenow-records-cwm-docs.md)

</td><td>

Knowledge worker/Team member

</td></tr><tr><td>

Share Board data with stakeholders outside CWM or prepare for offline analysis and presentations by exporting to CSV or Microsoft Excel.

</td><td>

[Export Board as CSV or Excel](../task/export-a-board-in-cwm-to-csv-or-excel.md)

</td><td>

Project manager

</td></tr><tr><td>

Share Doc content with stakeholders who don't have access to CWM by exporting pages to PDF.

</td><td>

[Export Doc as PDF](../task/export-a-doc-in-cwm-to-a-pdf-file.md)

</td><td>

Knowledge worker

</td></tr></tbody>
</table>**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## What to explore next

To learn more about configuring and using Collaborative Work Management, see:

-   [Configuring Collaborative Work Management](configuring-cwm.md)
-   [Using Collaborative Work Management](using-collaborative-work-management.md)
-   [Collaborative Work Management reference](reference-cwm.md)

