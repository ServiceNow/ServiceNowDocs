---
title: Plan work for an ART in EAP
description: Plan work across all teams in an ART for multiple Planning Intervals, coordinate with different teams to manage dependencies and resolve blockers in real-time using the Planning board in Enterprise Agile Planning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/enterprise-agile-planning/plan-work-for-teams-using-planning-board-in-eap.html
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Perform PI planning, Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Plan work for an ART in EAP

Plan work across all teams in an ART for multiple Planning Intervals, coordinate with different teams to manage dependencies and resolve blockers in real-time using the Planning board in Enterprise Agile Planning.

## Before you begin

Role required: sn\_apw\_advanced.eap\_user

## About this task

This task is explained using an Agile Release Train \(ART\) that has a Planning Interval \(PI\) as its calendar. This ART has child teams associated with it, which have Sprints defined for them.

On the board, move the story cards into different lanes or add new stories for the teams during planning meetings. Enable the **Dependencies** toggle to view dependencies and blockers across work for the teams.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.

2.  From the Agile structure section of the left navigation panel, choose an ART and select **Planning Board**.

    -   The planning board shows the current iteration for the ART by default. You can select a different iteration.

        \[Omitted image "eap-planning-board-change-pi-art.png"\] Alt text: Planning Interval selection in EAP Planning Board.

    -   Based on the scheduling of work done in the Backlog page, story cards are displayed in the Sprint lanes.
3.  Enable the **Dependencies** toggle to view dependencies between stories.

    Based on how dependencies are created, the stories sometimes need rescheduling. For more information on story dependencies, see [Create and manage dependencies between work items in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/enterprise-agile-planning/create-dependencies-between-work-items-in-eap.md).

4.  Enable the **Capacity** toggle to view the workload of the teams for each Sprint.

    The color of the capacity bar acts as a visual indicator of the workload:

    -   Red: Team is overloaded.
    -   Grey: Team is at 100% capacity.
    -   Blue: Team is at less that 100% capacity.
    \[Omitted image "eap-team-capacity-bar.png"\] Alt text: Team workload utilization in EAP planning board.

5.  Collaborate with the teams on stories by clicking a card open in the side panel.

    During the planning meetings, collaborate with multiple teams and update story information such as priority, story points, or blocked reason.

    You can also upload files in the Attachments tab and add notes and @-mention team members in the Comments tab of the side panel.

    If you want to access additional information of the story such as scrum tasks, select **Full details** from the side panel.

6.  Reschedule a story into a different Sprint or reassign it to a different team by dragging the cards into the respective lanes.


## What to do next

For the work that you assigned and scheduled, track the progress at different levels of your Agile structure using EAP dashboards. See [EAP reports and dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/enterprise-agile-planning/using-eap-dashboard.md).

**Parent Topic:**[Perform PI planning in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/enterprise-agile-planning/pi-planning-eap.md)

