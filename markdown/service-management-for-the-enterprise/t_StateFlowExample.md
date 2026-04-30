---
title: State flow example
description: Your business processes might require work order tasks to be accepted automatically when dispatched to an agent.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Service management states, Service Management]
---

# State flow example

Your business processes might require work order tasks to be accepted automatically when dispatched to an agent.

## Before you begin

Role required: admin

## About this task

Create a new state flow record that automates the transition from Pending Dispatch to Accepted and bypasses the Assigned state in which agents can reject tasks. This prevents the system from running the manual script associated with UI actions. The automatic script performs the jobs that the manual script performed, such as updating the date and time the task was dispatched, or to do additional work such as sending a notification.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **State Flows** &gt; **Work Task Flows**.

2.  Open the **Assigned** record that defines a task transition from a starting state of **Pending Dispatch** to an ending state of **Assigned**.

    This is an automatic state change that occurs when an agent's name is added to the Assigned to field and the task is updated.

3.  Change the name of the state flow.

    In this example, change the name to **Skip Agent Acceptance**.

4.  Change the value in the **Ending state** field to **Accepted**.

    This transition allows you to bypass the **Accept** state flow record that enables agents to reject tasks.

5.  Set up the condition criteria in the following fields:

    -   **Automatic condition string**: This condition ensures that the current state is at **Pending Dispatch** and the value in the **Assigned to** field changes. For example, `current.state == 10 && current.assigned_to.changes()`.
    -   **Automatic condition**: The condition **\[Assigned to\] \[is not empty\]**ensures that all dispatched tasks are accepted automatically.
    -   **Automatic script**:\] The automatic script sets the time the task was dispatched. For example, use method: `current.dispatched_on = gs.nowDateTime();`.
    **Note:** The previous two condition statements have an **\[and\]** relationship. In this example, the business rule runs when a task in a state of **Pending Dispatch** is assigned to any agent.

6.  Copy the record using the **Insert and Stay** command.

    This action increments the record number and clears the **Business rule** field. The system automatically creates a new business rule, using the name of the new state flow record. The Skip Agent Acceptance business rule moves the task from **Pending Dispatch** to **Accepted** automatically when a dispatcher enters a user name in the **Assigned to** field. Note that any changes you make to this state flow record in the future are executed by this business rule.

7.  Ensure that the **Active** check box is selected.

8.  In the Work Task Flows list, locate the **Accept** state flow record and change the **Active** status to **false**.

    This action deactivates the transition that allows agents to accept tasks and moves the state flow directly from **Pending Dispatch** to **Accepted**.


**Parent Topic:**[Service management states](../concept/c_ServiceManagementStates.md)

