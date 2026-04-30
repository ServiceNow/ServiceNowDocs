---
title: Scrum tasks for stories in CWM
description: Extend your agile workflow in CWM by breaking user stories into scrum tasks, giving your team the granularity needed to estimate effort, distribute work, and track daily progress through a sprint.
locale: en-US
release: zurich
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [scrum tasks, stories, agile, CWM, sprint, Kanban, Now Assist, AI generation]
breadcrumb: [Agile in CWM, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Scrum tasks for stories in CWM

Extend your agile workflow in CWM by breaking user stories into scrum tasks, giving your team the granularity needed to estimate effort, distribute work, and track daily progress through a sprint.

In CWM, scrum tasks represent the individual units of work that make up a user story. While stories capture a feature or requirement from the user's perspective, scrum tasks break that story into steps that team members can pick up and complete independently during a sprint. Scrum tasks are always associated with a parent story and aren't a standalone work items on the board.

## Creating scrum tasks

You can create scrum tasks manually or use Now Assist to generate them based on the story content.

-   **Manual creation**

    After a story is saved, a Scrum Tasks tab is available on the story form. From this tab, you can add tasks by entering a title and any relevant details directly on the story. You can also create scrum tasks for stories inline from the List and Sprint planning views. For more information, see [Add scrum tasks to a story in CWM](../task/add-scrum-tasks-to-a-story-cwm.md).

    ![The Scrum tasks tab on a story form showing the option to add a scrum task from the side panel.](../images/cwm-scrum-tasks-add.png)

-   **AI-generated scrum tasks**

    Now Assist can analyze the story description and context to suggest a set of scrum tasks. The **Create with Now Assist** button on the story form and the inline sparkle button on the **Scrum tasks** tab both trigger generation. You can review the suggestions, regenerate if the results don’t fit the story, and then insert the tasks. AI-generated tasks serve as a starting point and can be edited after they're created. For more information, see [Generate scrum tasks for a story with Now Assist for CWM](../../now-assist-cwm/task/generate-scrum-tasks-for-stories-cwm.md).


## Scrum tasks on the Kanban board

When a story has one or more scrum tasks, a scrum task indicator icon appears on the story's Kanban card. Selecting the icon opens a side panel that shows the scrum tasks for that story, so team members can view task details without leaving the board.![A Kanban board showing a story card with the scrum task indicator, and the side panel open with the associated scrum tasks listed.](../images/cwm-scrum-tasks-kanban-indicator.png)

Quick filters on the Kanban board let teams focus on specific sprints, states, or other columns. Multiple filters can be active at the same time, and a counter at the top of the board shows how many filters are currently applied. This makes it easier to track sprint-specific work during daily stand-ups and sprint execution.

## Scrum task considerations and limitations

-   Scrum tasks belong to a parent story and can’t exist independently as standalone work items on the board.
    -   When a story is moved from one sprint to another, the child scrum tasks also move to the new sprint.
    -   You can reorder scrum tasks only within its parent story.
    -   Scrum tasks can't be moved \(drag and drop\) or copied outside its parent story.
-   Percent complete isn’t rolled up from scrum tasks to the parent story. Percent complete is tracked only for CWM tasks.
-   When a story is imported through Connected work, its associated scrum tasks are brought in automatically along with it. Scrum tasks can’t be imported directly through Connected work.
-   Scrum tasks can’t be assigned to a sprint independently. They inherit the sprint of their parent story. When you change the sprint for a story, all associated scrum tasks move to the new sprint automatically.
-   Scrum tasks aren’t displayed in the Backlog section of the Sprint planning view. They’re shown only in the sprint section.
-   Sprint information can't be edited on a scrum task record.
-   Deleting a scrum task in CWM doesn’t delete the underlying record. It’s only removed from viewing in CWM.
-   You can’t add scrum tasks if the scrum task work type is disabled in your ServiceNow instance.
-   You can’t add scrum tasks if you have just the Viewer access to the CWM Board.
-   If scrum tasks were previously imported through Connected work before upgrading to v9.0.0, and stories are then imported through Connected work after the upgrade, duplicate scrum tasks may appear on the board. To resolve this, remove the existing configuration for scrum tasks in Connected work for your Board.

-   **[Add scrum tasks to a story in CWM](../task/add-scrum-tasks-to-a-story-cwm.md)**  
Break down a user story into scrum tasks in Collaborative Work Management \(CWM\) to distribute work across team members and track daily progress during a sprint.

**Parent Topic:**[Agile work management in CWM](agile-in-cwm.md)

**Related topics**  


[Agile work management in CWM](agile-in-cwm.md)

[Task dependencies and relationships in CWM](managing-task-dependencies-relationships-cwm.md)

