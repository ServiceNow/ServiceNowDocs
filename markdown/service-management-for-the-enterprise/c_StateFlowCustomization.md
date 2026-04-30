---
title: State flow customization
description: State flows control the sequence in which records transition between states in Service Management applications.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Service management states, Service Management]
---

# State flow customization

State flows control the sequence in which records transition between states in Service Management applications.

An administrator can perform the following tasks:

-   Add or delete states.
-   Trigger events on particular state transitions.
-   Transition to another state automatically when data in a request or its task changes, or change states manually when the user clicks a button.
-   Limit the choice list for the State field to those end states that are valid transitions from the given start state.
-   Control the visibility and behavior of selected fields on a target table when records in that table change states.
-   Create custom state flows. Turn off the **State flows are enabled** option on the configuration screen. Creating custom state flows requires scripting knowledge.

**Note:** Users with the wm\_admin role can create, read, update, and delete only work order flows and work task flows. Users with the facilities\_admin role can create, read, update, and delete only facilities request flows and request task flows. Users with the wm\_admin role cannot manipulate facilities records, and users with the facilities\_admin role cannot manipulate work order records.

## How SM request and task state flows work

State flows replace the standard process that controls how requests and their associated tasks move between states. The ServiceNow system creates business rules, client scripts, and UI actions that perform the transitions and field controls you specify. These programming elements remain in use while the state flow records that use them are present. When state flows on an SM application table are deleted, the system attempts to delete any unnecessary programming elements that were created on that table. You can limit the selections for the State field to valid states for the transition, based on the starting state.

State flows provide the following controls:

-   **Manual transitions:**A UI action, created automatically by the system when you provide a condition or a script, initiates a transition.
-   **Automatic transitions:**A business rule, created automatically by the system when you provide a condition and a script, initiates a transition when changes are made to a request or task.

## Features available with state flows

-   **Custom transitions:** Customize the order in which states can change for requests and task records.
-   **Field controls:** Control the behavior and visibility of specific fields when a task changes states or reaches a specified end state.
-   **State choice list:**Limit the values offered in a task record State field to valid states for that transition. This is the same client script that the system creates to manage field controls for state transitions.
-   **Events:**Trigger events when a state transition occurs or when a record reaches a specific end state.

## Start and end states

You can create a custom state flow for processing that must occur when a task record makes a specific transition from one state to another. These records require a starting state and an ending state, and processing occurs during the transition between states. To perform some processing when a task record reaches a particular end state, you only need to define the end state. In some cases a state flow can have a starting state only, such as when you need to perform some type of cleanup after a task is canceled. A state flow might have no starting or ending state if the processing in the record applies to more than one state transition.

The solution is to store the business rule or client script in a state flow record and create a condition to trigger processing for any state change that requires it. An example of this in field service management is the Roll Up Changes business rule on the Work Order Task \[wm\_task\] table. This business rule rolls up state changes that occur in tasks to the parent work order.

-   **[State flow dictionary overrides](../task/t_StateFlowDictionaryOverrides.md)**  
A dictionary override in a state flow defines the starting state for all new records in a specific table. You set an override in tables that extend a base table only, so that your customizations are applied only to the extended table.
-   **[Work notes in state flows](c_WorkNotesInStateFlows.md)**  
Work notes are an important part of the state flow process and are used to communicate information about state transitions.
-   **[Field controls in state flows](c_FieldControlsInStateFlows.md)**  
You can define controls for individual fields that are enforced when a record transitions between states.
-   **[Trigger events on state changes](../task/t_TriggerEventsOnStateChanges.md)**  
You can configure a state flow to trigger a registered system event when a task transitions from a starting state to a specified end state. For example, you can use events to trigger email notifications and create script actions.
-   **[Rebuild state flows](c_RebuildStateFlows.md)**  
You can rebuild state flows when a mismatch between existing and new sys\_ids occurs.
-   **[State flow cleanup](../reference/r_StateFlowCleanup.md)**  
The business rules, client scripts, and UI actions that the system creates automatically to perform custom transitions exist only while the state flow records that use them are present.

**Parent Topic:**[Service management states](c_ServiceManagementStates.md)

