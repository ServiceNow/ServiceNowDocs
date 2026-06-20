---
title: Manage automation tasks
description: Manage all tasks associated with the automation requests from one location from the Task Board in the Automation Center Kanban board.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/automation-center/manage-task-board.html
release: zurich
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Kanban board, Explore, Automation Center, Workflow Data Fabric]
---

# Manage automation tasks

Manage all tasks associated with the automation requests from one location from the Task Board in the Automation Center Kanban board.

## Before you begin

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Automation Center Workspace**.

    The Automation Center dashboard is displayed.

2.  Select the Kanban board icon \[Omitted image "icon-kanban.png"\] Alt text: kanban board icon.

    The Kanban board is displayed with the Request Board in view.

3.  Select **Task Board** from the list view.

    \[Omitted image "task-board.png"\] Alt text: Task board

    The Task Board is displayed with all available tasks and their states.

    **Note:** A maximum of 2000 tasks are available on the Task Board. This value can be changed only by the System Administrator.

    Also, anyone with the sn\_ac.automation\_admin or sn\_ac.automation\_technical\_user role can reorder different states \(columns\) on the Task Board to set the lifecycle or process flow direction according to their requirement by editing the vtb\_board table.

    \[Omitted image "task-board-ui.png"\] Alt text: Task Board

4.  You can do multiple actions on the Task Board.

    -   Filter the tasks to match your need.

        Filter the tasks based on the following:

        -   **Date**: Select any date range to view tasks created during that period.
        -   **Type**: Select one or more types of tasks to view tasks that belong to the selected types.
        -   **Priority**: Select one or more priority values to view tasks with those priority values.
        -   **User**: Select one or more users to view tasks assigned to only those users. Only users who have been assigned a task are available for selection.
    -   Sort the tasks for ease of use.

        \[Omitted image "sort-task.png"\] Alt text: Task board sort

        Select **Name**, **Priority**, or **Score** from the **Sort by** field.

        Select **Ascending** or **Descending** from the **Sort Direction** field.

        The tasks are sorted based on the selected sorting options.

    -   Change the state of a task.

        To move a task from one state to another, drag the card to the required state column.

        If a sorting is applied, the task card is placed according to the sorting. If no sorting is applied, the task card is placed based on the creation date.

    -   Create a task from the automation task card.

        Select the **Add Task** icon.

        The **Create New Automation Task** form is displayed. For more information, see [Automation task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/automation-center/automation-task-form.md).

        Verify that the associated automation request is either in the **Planned** or **In Progress** state.


**Parent Topic:**[Automation Center Kanban board](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/automation-center/kanban.md)

