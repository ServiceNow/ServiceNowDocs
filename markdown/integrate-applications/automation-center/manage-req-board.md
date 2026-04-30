---
title: Manage automation requests
description: Manage all automation requests from one location from the Request Board in the Automation Center Kanban board.
locale: en-US
release: xanadu
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Automation Center Kanban board, Exploring Automation Center, Automation Center, Creating integrations with applications]
---

# Manage automation requests

Manage all automation requests from one location from the Request Board in the Automation Center Kanban board.

## Before you begin

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Automation Center Workspace**.

    The Automation Center dashboard is displayed.

2.  Select the Kanban board icon ![kanban board icon](../images/icon-kanban.png).

    The Kanban board is displayed with the Request Board in view. You can view all the available automation requests with their states.

    **Note:** A maximum of 200 automation requests are available on the Request Board. This value can be changed only by someone with the sn\_ac.automation\_admin or sn\_ac.automation\_technical\_user role.

    Also, anyone with the sn\_ac.automation\_admin or sn\_ac.automation\_technical\_user role can reorder different states \(columns\) on the Request Board to set the lifecycle or process flow direction according to their requirement by editing the vtb\_board table.

    ![Request board](../images/req-board.png)

3.  You can do multiple actions on the Request Board.

    -   Filter the automation requests to match your need.

        Filter the automation requests based on the following:

        -   **Date**: Select any date range to view automation requests created during that period.
        -   **Request type**: Select the type of request you want to view. You can choose to view automation requests, action requests, or review requests.
        -   **Priority**: Select one or more priority values to view automation requests with those priority value.
        -   **Department**: Select one or more departments to view automation requests that belong to the selected departments.
    -   Sort the automation requests for ease of use.

        ![Request board sort](../images/kanban-sort.png)

        Select **Name**, **Priority**, or **Score** from the **Sort by** field.

        Select **Ascending** or **Descending** from the **Sort Direction** field.

        The automation requests are sorted based on the selected sorting options.

    -   Change the state of an automation request.

        To move an automation request from one state to another, drag the card to the required state column.

        When you don’t follow the happy path, error messages are displayed and you're guided to fix the issue.

        If a sorting is applied, the automation request card is placed according to the sorting. If no sorting is applied, the automation request card is placed based on the creation date.

    -   Create a task from the automation request card.

        1.  Select the task icon \(![Task icon](../images/icon-task.png)\) from the automation task card.

            The Contextual Task Board for the automation request is displayed.

        2.  Select the **Add Task** icon.

            The **Create New Automation Task** form is displayed. For more information, see [Automation task form](../reference/automation-task-form.md).

            Verify that the associated automation request is either in the **Planned** or **In Progress** state.

    -   View if an automation request has a task assigned to it. If yes, then how many tasks have been completed.
    -   View if an automation request has automations associated with it.

**Parent Topic:**[Automation Center Kanban board](../concept/kanban.md)

