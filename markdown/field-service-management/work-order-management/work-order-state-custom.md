---
title: Customizing state flows
description: State flows control the sequence in which records transition between states in the Field Service Management applications.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Configuring work orders, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Customizing state flows

State flows control the sequence in which records transition between states in the Field Service Management applications.

## How Field Service Management task state flows work

State flows replace the standard process that controls how requests and their associated tasks move between states. The ServiceNow system creates business rules, client scripts, and UI actions that perform the transitions and field controls you specify. These programming elements remain in use while the state flow records that use them are present. When state flows on the Field Service Management table are deleted, the system attempts to delete any unnecessary programming elements that were created on that table. You can limit the selections for the State field to valid states for the transition, based on the starting state.

**Important:** Creating custom state flows requires scripting knowledge.

State flows provide the following controls:

-   **Manual transitions:** A UI action, created automatically by the system when you provide a condition or a script, initiates a transition.
-   **Automatic transitions:** A business rule, created automatically by the system when you provide a condition and a script, initiates a transition when changes are made to a request or task.

Users with the wm\_admin role can perform the following tasks:

-   Create, read, add, update, or delete work order flows and work task flows.
-   Trigger events on particular state transitions.
-   Transition to another state automatically when data in a request or its task changes, or change states manually when the user selects a button.
-   Limit the choice list for the State field to those end states that are valid transitions from the given start state.
-   Control the visibility and behavior of selected fields on a target table when records in that table change states.
-   Create custom state flows. Turn off the **State flows are enabled** option on the configuration screen.

## Features available with state flows

-   **Custom transitions:** Customize the order in which states can change for requests and task records.
-   **Field controls:** Control the behavior and visibility of specific fields when a task changes states or reaches a specified end state.
-   **State choice list:** Limit the values offered in a task record State field to valid states for that transition. This is the same client script that the system creates to manage field controls for state transitions.
-   **Events:** Trigger events when a state transition occurs or when a record reaches a specific end state.

## Start and end states

Users with the wm\_admin role can create a custom state flow for processing that occurs when a task record makes a specific transition from one state to another. These records require a starting state and an ending state, and processing occurs during the transition between states. To perform some processing when a task record reaches a particular end state, you must define the end state. In some cases a state flow can have a starting state only, like when you perform some type of cleanup after a task is canceled. A state flow might have no starting or ending state if the processing in the record applies to more than one state transition. The solution is to store the business rule or client script in a state flow record and create a condition to trigger processing for any state change that requires it.

An example of this in Field Service Management is the Roll Up Changes business rule on the Work Order Task \[wm\_task\] table. This business rule rolls up state changes that occur in tasks to the parent work order.

## Configuration overview

The steps for setting up state flow customizations are:

1.  [Configure state flows for work orders and work order tasks](../task/configure-state-flow.md)

    Configure the states that work orders, and work order tasks move between. This can be helpful if you have a specific sequence of states that help track work.

2.  \(Optional\) [State flow dictionary overrides](../task/state-flow-overrides.md)

    Define the starting state for all new work orders and work order tasks with dictionary overrides.

3.  \(Optional\) [Work notes in state flows](work-notes-in-states.md)

    Add customized work notes to work order tasks when they reach a certain state. For example, you might include the note, "Task rejected by agent" in the Reject state flow.

4.  \(Optional\) [Field controls in state flows](state-flow-field-controls.md)

    Determine what happens if the system detects a specified state transition. For example, you might want the Problem field to be visible when an incident moves to the Awaiting Problem state.

5.  \(Optional\) [Trigger events on state changes](../task/trigger-events-on-states.md)

    Configure a state flow to trigger a registered system event when a task transitions from a starting state to a specified end state. For example, you can use events to trigger email notifications and create script actions.

6.  \(Optional\) [Rebuild state flows](rebuild-state.md)

    Rebuild state flows when a mismatch between existing and new sys\_ids occurs.

7.  \(Optional\) [State flow cleanup](state-flow-cleanup.md)

    Cleanup the business rules, client scripts, and UI actions that the system creates to perform custom transitions that only exist while the state flow records that use them are present.


