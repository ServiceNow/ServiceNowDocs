---
title: Creating similar tasks groups
description: In BCM, when the same plan is activated multiple times, it can result in multiple redundant tasks. Starting with BCM release 9.0.x, the Similar tasks groups tab in events helps you to eliminate redundant tasks by grouping duplicate tasks from multiple plans for similar scenarios. This functionality streamlines event task management and reduces duplication of efforts.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Creating similar tasks groups

In BCM, when the same plan is activated multiple times, it can result in multiple redundant tasks. Starting with BCM release 9.0.x, the **Similar tasks groups** tab in events helps you to eliminate redundant tasks by grouping duplicate tasks from multiple plans for similar scenarios. This functionality streamlines event task management and reduces duplication of efforts.

## Progression of original and duplicate tasks

The Similar tasks group functionality enables event users to group similar tasks from multiple plans aimed at resolving specific situations. The system automatically designates an original task within a group and the duplicate tasks are moved to the **On hold** state. Upon completing the original task, event users mark it as closed. The duplicate tasks are then marked as Closed duplicates.

The progression of both original and duplicate tasks is as follows:

-   **Initial task state**

    When a task is part of a group, it initially moves to the **On hold** state instead of the **Open** state. The first task to enter the **On hold** state is automatically designated as the original task.

-   **Transition to the Open state**

    The original task in a group is then moved to the **Open** state when all the other tasks are moved to the **On hold** state.

-   **Handling duplicate tasks**

    Duplicate tasks remain on hold until the original task is closed and are not assigned to users. When the original task is completed, the duplicate tasks in the group are automatically marked as **Closed duplicate**.

-   **Modifying duplicate tasks**

    Duplicate tasks cannot be modified directly; to take any action on them, you must first remove them from their associated group.

-   **Reporting and time calculation**

    For duplicate tasks, the original task's state and time fields are used to roll up to the activated plans and assets. The time taken by duplicate tasks is not included in the **Total effort** field on the activated plans and assets.

-   **Re-triggering original tasks**

    If the original task is re-triggered, the duplicate task remains in the **Closed duplicate** state, unaffected by the change of status of the original task.

-   **Task grouping rules**

    Tasks with similar recovery task references are automatically grouped together by the system. Tasks that have internal dependencies cannot be grouped together, but they can be added to different groups. Tasks that trigger related plans cannot be added to the Similar tasks group.


## Flexibility and control

You can unlink tasks from a similar task group or remove tasks from the event tasks.

By eliminating redundant task execution and enhancing task management, this feature significantly improves operational efficiency during complex exercises or events.

-   **[Create a similar tasks group](../task/create-similar-tasks-group.md)**  
Identify similar or duplicate event tasks associated with an event and add them to a similar tasks group by grouping them in the **Similar tasks groups** tab. It helps you to streamline event task management and reduce duplication of efforts.
-   **[State changes for event tasks in groups](transition-states-of-event-task.md)**  
The original and duplicate event tasks in the Similar tasks group move through different states until the original task is closed.

**Parent Topic:**[Structured workflows for exercises](performing-tasks-to-manage-exercise-events.md)

