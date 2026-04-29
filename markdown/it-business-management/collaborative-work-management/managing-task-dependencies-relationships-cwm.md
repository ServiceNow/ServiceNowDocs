---
title: Task dependencies and relationships in CWM
description: Increase visibility into how work is connected by linking work items directly in Collaborative Work Management \(CWM\), eliminating the need to track dependencies in spreadsheets or notes fields.
locale: en-US
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [dependencies, relationships, prerequisite, dependent, related to, CWM, work items, agile]
breadcrumb: [Agile in CWM, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Task dependencies and relationships in CWM

Increase visibility into how work is connected by linking work items directly in Collaborative Work Management \(CWM\), eliminating the need to track dependencies in spreadsheets or notes fields.

In CWM, you can link any task-type work item to another to show how pieces of work relate to each other. Relationships are informational and team members can progress on a work item regardless of the state of its linked items. Relationships can be created across Boards and Spaces, giving teams visibility into cross-team dependencies for their work.

## Relationship types

Work items in CWM support three relationship types.

-   **Prerequisite**

    Indicates that another work item must be completed before this item can begin. Use this relationship to communicate sequencing and upstream dependencies to your team. Only task-type work items extending the Task \[task\] table and CWM tasks can be added as prerequisites. Planning items such as Epics aren’t supported.

-   **Dependent**

    Indicates that this work item must be completed before work on another item can begin. This is the inverse of a prerequisite relationship and communicates downstream impact to your team.

-   **Related**

    Indicates a general connection between two work items without implying a specific order of execution. Use this relationship when items share context, overlap in scope, or are otherwise connected without one blocking the other.

    ![A Kanban board showing a work item card with the relationships indicator, and the side panel open listing the related work items and their relationship types.](../images/cwm-relationships-kanban.png)


## Linking work items across boards and spaces

You can link any task-type work item to another across the ServiceNow AI Platform, regardless of which Board or Space it belongs to. To create a relationship, search for the work item by name and attach it. The search covers all task type work items that you have permission to view.

**Note:** Work items brought onto a Board through the Connected work feature don’t display relationships on their original source record unless the relationship is added directly on that record.

## Relationships on the Kanban board

When a work item has one or more relationships, a relationships indicator icon appears on its Kanban card. Selecting the icon opens the right side panel showing the related work items and their relationship types, so team members can view dependency details without leaving the board.

![Kanban view showing task cards with scrum task and relationship indicators on the cards.](../images/cwm-relationships-cards.png)

## Task dependency considerations and limitations

-   Planning items such as Epics can’t be added as prerequisites because they aren’t derived from the Task \[task\] table.
-   You can add a work item as a dependency on if you have permission to view that item.
-   Relationships have no effect on percent complete calculations for CWM Tasks or Boards in Strategic Planning Workspace.
-   If a story in the Story \[rm\_story\] table already has prerequisite and dependent stories associated to it, those details are shown in CWM.
-   Adding a story-type work item as a relationship to another story syncs with the prerequisite and dependent fields in the Story \[rm\_story\] table.
-   Adding a non-story-type work item as a relationship to a story does not sync with the Story \[rm\_story\] table.

-   **[Add a dependency to a work item in CWM](../task/add-a-dependency-to-a-work-item-cwm.md)**  
Link a work item to another in Collaborative Work Management \(CWM\) to show how they relate, whether one is a prerequisite for another or they are generally connected.
-   **[Remove a dependency from a work item in CWM](../task/remove-a-dependency-from-a-work-item-cwm.md)**  
Unlink a relationship between work items in Collaborative Work Management \(CWM\) when it is no longer relevant or was added incorrectly.

**Parent Topic:**[Agile work management in CWM](agile-in-cwm.md)

**Related topics**  


[Agile work management in CWM](agile-in-cwm.md)

[Scrum tasks for stories in CWM](managing-scrum-tasks-for-stories-cwm.md)

