---
title: Switch an Agile Team to Kanban in EAP
description: Change the planning methodology of an Agile Team from Scrum to Kanban in Enterprise Agile Planning so that the team works from a continuous backlog instead of Sprints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/enterprise-agile-planning/switch-agile-team-to-kanban-in-eap.html
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Switch an Agile Team to Kanban in EAP

Change the planning methodology of an Agile Team from Scrum to Kanban in Enterprise Agile Planning so that the team works from a continuous backlog instead of Sprints.

## Before you begin

Role required: sn\_apw\_advanced.eap\_admin

## About this task

Each Agile Team follows either the Scrum or the Kanban planning methodology. A Scrum team plans work in Sprints. A Kanban team works from a continuous backlog and doesn't use Sprints. You can choose to switch a team to Kanban when it no longer plans work in Sprints. For more information about how the two types of teams differ, see [Scrum and Kanban teams in an ART in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/scrum-and-kanban-teams-in-eap.md).

**Important:** When you save the team as Kanban, all of its current and future Sprints are cancelled. Sprints that are complete or already cancelled aren't changed.

If the team is connected to Collaborative Work Management \(CWM\) and has a CWM board, you can't switch it while it has active or planned Sprints.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace**.

2.  From the **Settings** menu, select **Agile structure** and navigate to the Agile Team that you want to switch.

3.  On the **Details** tab, in the **Planning methodology** field, select **Kanban**.

    A warning appears on the field: `Switching to Kanban will cancel all current and future sprints for this team.` The warning doesn't appear for teams that are connected to a CWM board.

    \[Omitted image "eap-switch-agile-team-to-kanban.png"\] Alt text: Planning methodology field set to Kanban on the Details tab of an Agile Team, with the sprint cancellation warning shown.

4.  Select **Save**.

    The message `This team has been switched to Kanban and all current and future sprints have been cancelled.` appears.


## Result

The team's planning methodology is set to Kanban, and its current and future Sprints are cancelled. The team can no longer use Sprints.

