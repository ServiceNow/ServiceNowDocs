---
title: Time constraints in parent-child relationships
description: Parent-child task relationships have several effects on task time constraints.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Parent-child task relationships, Project task relationships and dependencies, Project tasks, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Time constraints in parent-child relationships

Parent-child task relationships have several effects on task time constraints.

-   **When a child task is set to __Start ASAP__**

    The child task starts at the same time as the parent task. If Project itself is set as a parent, the **Start ASAP** tasks starts on the same date as set in the **Constraint Date** field, as long as it does not have dependencies with other child tasks.

-   **When a parent task is set to __Start ASAP__ and child tasks are set to __Start on specific date__:**
    -   The earliest child task start date determines the start date of the parent, assuming no other dependencies.
    -   In this case, the **Time constraint** field of the parent remains **Start ASAP**, but the actual start date is changed to the start date of the earliest child task.
-   **When a parent task is set to __Start ASAP__ and child tasks are set to __Start on specific date__:**

    Child precedence also applies to end dates. If the estimated end date of the child task is later than the end date of the parent task, the estimated end date extends to cover the child. For actual values, a parent has the same start date as the earliest start date of its children. The latest actual end date is the latest end date of its children. Assuming the child tasks are **Closed Complete**. If the child tasks are not in the **Closed Complete** state, the actual end date of the parent is empty.

    For the planned start date of the parent task:

    -   The planned start date is the earliest planned start date of all the children that do not have an actual start date.
    -   If all child tasks have actual start dates, the planned start date of the parent task is set to the actual start date.
    For the planned end date of the parent task: The latest planned end date or actual end date of the child tasks determines the planned end date of the parent.

    A task with **Start no later than** or **Start on specific date** time constraint cannot be a parent task. When a new child task is added to a task with these time constraints, the time constraint for the parent task is changed to **Start ASAP**.


**Parent Topic:**[Parent-child task relationships](../concept/c_Parent-ChildTaskRelationships.md)

