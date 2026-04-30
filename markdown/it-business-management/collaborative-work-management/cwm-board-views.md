---
title: List, Gantt, and Kanban views in CWM
description: Switch between List, Gantt, and Kanban views to manage and visualize work on a CWM Board in the way that best fits your team's workflow.
locale: en-US
release: yokohama
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-03-04"
reading_time_minutes: 4
keywords: [board views, List view, Gantt view, Kanban view, CWM, quick filters, scrum tasks, sprint tracking]
breadcrumb: [Board views in CWM, Manage work using Boards, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# List, Gantt, and Kanban views in CWM

Switch between List, Gantt, and Kanban views to manage and visualize work on a CWM Board in the way that best fits your team's workflow.

Each CWM Board supports three views: List, Gantt, and Kanban. You can switch between views at any time without losing data, and each view can be personalized to show the columns and attributes most relevant to your team. For more information, see [Personalize List, Gantt and Kanban display for CWM Boards](../task/personalize-cwm-board-views.md).

## List view

The List view displays all work items on a Board in a grid format. Use this view to review the status of work items at a glance, update fields inline, or assign items to team members quickly. The List view displays up to 1,000 work items by default.

![List view of a Board in the CWM workspace showing work items in a grid format.](../images/cwm-additional-assignee-list-view.png)

## Gantt view

The Gantt view displays work items in a grid alongside a calendar timeline, making it easy to visualize schedules and reschedule items based on changing priorities. The Gantt view displays up to 1,000 work items by default.

![Gantt view of a Board in the CWM workspace showing work items alongside a calendar timeline.](../images/cwm-board-gantt.png)

## Kanban view

The Kanban view organizes work items into columns and rows based on attributes you choose, such as **State** and **Assigned to**. Vertical lanes represent one attribute and horizontal swimlanes represent another, giving teams a visual overview of work distribution and status. Each axis supports up to 50 lanes by default.

![Kanban view showing task cards with scrum task and relationship indicators on the cards.](../images/cwm-relationships-cards.png)

-   **Quick filters**

    Use quick filters to focus the Kanban board on a specific sprint, state, or other column attribute. Multiple filters can be active at the same time, and a counter at the top of the board shows the number of active filters. For example, use quick filters for sprint-specific information during daily standups or sprint reviews.

    ![The Kanban board with quick filters applied, showing the active filter counter at the top of the board.](../images/cwm-kanban-filters.png)

    You can save these filters to a Board view of your choice and when you save this Board as a template, these filters get saved in the template.

-   **Work item indicators on Kanban cards**

    Kanban cards display indicators that give teams at-a-glance visibility into scrum tasks and relationships associated with a work item, without opening the item.

    -   **Scrum task indicator:** Appears on a story card when the story has one or more scrum tasks. Selecting the indicator opens the right side panel showing the scrum tasks for that story. For more information, see [Scrum tasks for stories in CWM](managing-scrum-tasks-for-stories-cwm.md).
    -   **Relationship indicator:** Appears on a work item card when the item has one or more linked relationships, such as a prerequisite, dependent, or related-to item. Selecting the indicator opens the right side panel showing the related work items and their relationship types. For more information, see [Task dependencies and relationships in CWM](managing-task-dependencies-relationships-cwm.md).
-   **Kanban card layout options**

    Personalize Kanban cards to surface the information most relevant to your team using card layout settings. Select up to five fields to display on each card. Use the Compact layout to show only the work item name for a focused view, or the Full layout to show all selected fields for more context directly on the card.

    ![Kanban card layout settings panel showing field selection and layout options.](../images/cwm-kanban-card-layout.png)

-   **Kanban view with Connected work**

    If the Board includes Connected work items, you can use vertical and horizontal lane combinations to group and filter them. For example:

    -   Set the vertical lane to **State** and the horizontal lane to **Task type** to view all epics grouped by state, then filter to show only epics.
    -   Set the vertical lane to **Sprint** and the horizontal lane to **Task type** to view connected stories grouped by sprint.

-   **[Personalize List, Gantt and Kanban display for CWM Boards](../task/personalize-cwm-board-views.md)**  
Show, hide, or rearrange columns and apply sorting or filters to personalize the way data is displayed in Collaborative Work Management Boards based on your workflow.

**Parent Topic:**[Board views in CWM](board-views-in-cwm.md)

**Related topics**  


[Personalize List, Gantt and Kanban display for CWM Boards](../task/personalize-cwm-board-views.md)

[Scrum tasks for stories in CWM](managing-scrum-tasks-for-stories-cwm.md)

[Task dependencies and relationships in CWM](managing-task-dependencies-relationships-cwm.md)

