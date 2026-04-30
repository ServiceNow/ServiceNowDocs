---
title: Agile work management in CWM
description: Run your agile workflow in Collaborative Work Management \(CWM\), from building and refining a backlog to planning sprints, executing work as stories and scrum tasks, and collaborating with your team.
locale: en-US
release: yokohama
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-03-04"
reading_time_minutes: 7
keywords: [agile, scrum, sprint planning, CWM agile, stories, scrum tasks, backlog]
breadcrumb: [Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Agile work management in CWM

Run your agile workflow in Collaborative Work Management \(CWM\), from building and refining a backlog to planning sprints, executing work as stories and scrum tasks, and collaborating with your team.

CWM is a unified workspace where agile teams can manage their delivery cycle. Teams transitioning to CWM can continue to run the Scrum workflow they’re familiar with, which includes managing a backlog, planning and executing sprints, and tracking daily progress, while also benefiting from CWM's flexible work item model, AI assistance, and broader collaboration features.

## Agile workflow in CWM

The following end-to-end workflow shows how agile teams use CWM to plan and execute work.

![Agile methodology execution workflow in Collaborative Work Management. More details on the workflow follows.](../images/cwm-agile-workflow-cwm-infographic.svg)

-   **Set up your workspace**

    Create a Space and a Board for your team. The Space is where all your work lives. CWM provides Stories, Scrum tasks, and CWM Tasks as default work item types. You can also define custom work item types to reflect your team's terminology, for example, Bugs. For more information, see [Create a Board in CWM](../task/create-boards-in-cwm.md) and [Create and manage custom work item types in CWM](../task/create-custom-work-item-types-in-cwm.md).

-   **Build and maintain your backlog**

    Add work items to your Board through the Sprint Planning view. All unscheduled work appears in the Backlog pane, giving your team a single place to groom, prioritize, and reorder items before pulling them into a sprint. For more information, see [Add work items to Sprint planning Backlog in CWM](../task/add-work-items-to-sprint-planning-backlog-in-cwm.md).

-   **Plan sprints**

    Create sprints by setting a duration, start and end dates, and story point capacity. Drag items from the Backlog into a sprint, or add them directly. Capacity indicators in each sprint section help teams avoid over-committing. For more information, see [Create a sprint in CWM](../task/create-sprints-in-cwm.md) and [Plan work items into sprints in CWM](../task/plan-work-items-into-sprints-in-cwm.md).

-   **Execute and track work**

    Start the sprint and use the Kanban board to track work in progress. Team members move story cards across state lanes to update status. Use quick filters to focus the board on a specific sprint, state, or other columns to stay on top of what matters during the current sprint. For more information, see [Start or complete a sprint in CWM](../task/start-a-sprint-in-cwm.md).

-   **Break stories into scrum tasks**

    For more granular daily execution, break user stories into scrum tasks. Scrum tasks are subtasks linked to a story, which help teams estimate effort, distribute work, and track daily progress. Create them manually from the story's Scrum tasks tab, or use Now Assist to generate them automatically based on the story context. When a story has scrum tasks, an indicator appears on the Kanban card so teams can quickly see stories that have been decomposed. For more information, see [Scrum tasks for stories in CWM](managing-scrum-tasks-for-stories-cwm.md).

-   **Track dependencies**

    Link work items to show how they relate to each other using three relationship types: prerequisite, dependent, and related to. These are informational relationships and don’t block task progress. You can link work items across boards and spaces, enabling visibility into cross-team dependencies without needing to be on the same board. For more information, see [Task dependencies and relationships in CWM](managing-task-dependencies-relationships-cwm.md).

-   **Hold retrospectives**

    At the end of each sprint, create a retrospective board to capture what went well and what to improve for the next sprint. For more information, see [Create a retrospective board for a sprint in CWM](../task/create-a-retrospective-board-for-sprint-cwm.md).


## Bringing in work from other ServiceNow applications

Agile teams often work on more than just stories. Incidents must be resolved, defects must be fixed, and enhancement requests must be delivered. The Connected work feature in CWM lets you bring records from any ServiceNow application into your Board by defining filter conditions. Once connected, you can plan those records into sprints and manage them alongside your stories from a single backlog.

Teams who previously used the Unified Backlog and triage boards in Agile Development 2.0 to manage defects, incidents, and other work records can use Connected work to achieve a similar centralized view in CWM. For more information, see [Connected work in CWM](unified-boards-for-connected-work-in-cwm.md).

## Comparing CWM to Agile Development 2.0

CWM covers the core Scrum workflow, but approaches some functional areas differently. The following describes how key Agile Development 2.0 concepts map to CWM.

<table id="table_agile_cwm_considerations"><thead><tr><th>

Functional area

</th><th>

In Agile Development 2.0

</th><th>

In CWM

</th></tr></thead><tbody><tr><td>

Work item hierarchy

</td><td>

Fixed hierarchy of Products, Epics, Stories, and Scrum Tasks.

</td><td>

Create custom work item types to build a hierarchy that fits your team. There are no built-in Products, Releases, or Themes.

 You can use Spaces to separate product areas and Goals to connect work to business objectives.

</td></tr><tr><td>

Unified backlog and triage

</td><td>

Triage boards filtered records from other apps and automatically created stories for triaged items.

</td><td>

The Connected work feature brings source records directly into the board backlog. So, no separate triage step required. Teams can plan them into sprints and update their status directly from the CWM Board. See [Connected work in CWM](unified-boards-for-connected-work-in-cwm.md).

</td></tr><tr><td>

Multi-team and program planning

</td><td>

Scrum Programs enabled coordination across multiple teams.

</td><td>

CWM is optimized for team-level execution. For program-level planning such as PI planning, use EAP. EAP teams can connect to CWM so teams execute sprint work in CWM while program-level visibility remains in EAP. See [Connecting EAP with Collaborative Work Management](cwm-integration-with-eap.md).

</td></tr></tbody>
</table>-   **[Sprint planning in CWM](agile-sprint-planning-in-cwm.md)**  
Plan, track, and manage work for your teams in the Agile methodology using Sprint planning in Collaborative Work Management.
-   **[Scrum tasks for stories in CWM](managing-scrum-tasks-for-stories-cwm.md)**  
Extend your agile workflow in CWM by breaking user stories into scrum tasks, giving your team the granularity needed to estimate effort, distribute work, and track daily progress through a sprint.
-   **[Task dependencies and relationships in CWM](managing-task-dependencies-relationships-cwm.md)**  
Increase visibility into how work is connected by linking work items directly in Collaborative Work Management \(CWM\), eliminating the need to track dependencies in spreadsheets or notes fields.

**Parent Topic:**[Using Collaborative Work Management](using-collaborative-work-management.md)

**Related topics**  


[Sprint planning in CWM](agile-sprint-planning-in-cwm.md)

[Scrum tasks for stories in CWM](managing-scrum-tasks-for-stories-cwm.md)

[Task dependencies and relationships in CWM](managing-task-dependencies-relationships-cwm.md)

[Connected work in CWM](unified-boards-for-connected-work-in-cwm.md)

[Connecting EAP with Collaborative Work Management](cwm-integration-with-eap.md)

