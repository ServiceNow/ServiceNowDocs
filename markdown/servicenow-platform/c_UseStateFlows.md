---
title: Use state flows
description: You can create custom state flows for any table that uses states.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [State flows, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Use state flows

You can create custom state flows for any table that uses states.

Make state transitions occur in any order or skip specific states according to your business practices. State flows can manage the behavior of fields and field visibility on a task form. State flows can also trigger system events that perform work such as sending [Email and SMS notifications](https://www.servicenow.com/docs/access?context=c_EmailNotifications&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Administrators can configure state flows to:

-   Limit the [choice list](../task/t_CreateAStateFlow.md) for the **State** field to contain only those states that are valid for the flow.
-   Define the [behavior and visibility](c_StateFlows.md) of specific fields on a task form when state transitions occur and for certain end states.
-   Configure [events that are triggered when a task changes states](c_StateFlows.md).
-   [Set up](../task/t_CreateAStateFlow.md) UI actions and business rules to implement certain state transitions, or while the task is in certain states.

The State Flow plugin installs records used by work management to control state transitions for work orders and work order tasks. For detailed information about using work management state flows, see [State flow customization](https://www.servicenow.com/docs/access?context=c_StateFlowCustomization&version=australia&pubname=australia-service-management-for-the-enterprise&ft:locale=en-US).

Creating and customizing state flows requires scripting knowledge. Users with the admin role can create state flow records.

## Dictionary overrides for state flows

A dictionary override in a state flow defines the starting state for all new records in a specific table.

You set an override in tables that extend a base table only, so that your customizations are applied only to the extended table.

1.  In a state flow record, select an **Ending state**.

    This is the override value which becomes the starting state for all new records in the table named.

2.  Click **Create Default Value**.

    The system populates the Dictionary override field with a value of state, which is the field in the task table affected by the override. The Dictionary override field is read-only. After the override is created, the system hides the **Create Default Value** button on all subsequent state flow forms for that table.


## Events triggered on state changes

You can configure a state flow to trigger a registered system event when a task transitions from a starting state to a specified end state.

For example, you can use events to trigger email notifications and create script actions. When you attach an event to a state flow, the system creates a business rule called State Flow Events for &lt;table name&gt; for the table specified in the state flow. If you specify a start and end state, the business rule executes when the record transitions from the start state to the end state. If the state flow only specifies an end state, the business rule executes whenever that end state is reached. The system creates one business rule for all state flows containing events on a single table. When all events or all state flows on a table are deleted, the system deletes the business rule.

## Field controls

You can define controls for individual fields that are enforced when a record transitions between states.

Settings in the Field Controls section of the State Flow form enable you to apply field controls when the system detects a specified state transition or when the end state is the current state when the form is opened. The control is applied only to existing fields on the form. State flows cannot add fields to the form.

For example, you might want the Problem field to be visible when an incident moves to the Awaiting Problem state. If the incident state changes to Awaiting User Info, you hide the Problem field and make the Caller field mandatory.

When creating field controls, configure state flow records with an ending state only and to create the correct behavior for every ending state you want to control. This configuration ensures that the field controls are set properly when the user selects a new state, and also when the user returns a record's State field to the original state. Only specify a full state transition, with both a starting and ending state, when you want a particular behavior for that precise state transition.

**Note:** State flows use client scripts to enforce field controls. It is possible that your settings can be changed by existing UI policies, which execute after client scripts.

The system creates the following objects, as needed, to enforce field properties in state flows:

|Type|Name|Description|
|----|----|-----------|
|Business rule|State Flow Notes for &lt;table name&gt;|Enforces mandatory fields for the table on which that field behavior is defined.|
|Client script \(onLoad\)|&lt;table name&gt; state flow|Sets possible states and initial mandatory, read-only, and visible properties when a record is loaded.|
|Client script \(onChange\)|&lt;table name&gt; change state flow|Sets updated mandatory, read-only, and visible properties when a record is changed.|

## Rebuild state flows

You can rebuild state flows when a mismatch between existing and new sys\_ids occurs.

When you use an XML file to import a state flow record into an instance, the system attempts to match the incoming states with existing states by comparing sys\_ids. Because the sys\_ids of items in a choice list can vary between instances, the system can fail to match the states, even though they are otherwise identical.

When matching fails, the start and end states of affected records are left blank or contain numeric values. To repair these records navigate to **State Flows** &gt; **Admin** &gt; **Rebuild State Flows**. This module runs a script that compares the numerical value of each item in the **State** field choice list until it finds a match in the imported state flow record.

## State flow cleanup



## Work notes



-   **[Create a state flow](../task/t_CreateAStateFlow.md)**  
Creating State Flows.
-   **[State flow cleanup](c_StateFlowCleanup.md)**  
The business rules, client scripts, and UI actions that the system creates automatically to perform custom transitions exist only while the state flow records that use them are present.
-   **[Work notes](c_WorkNotes.md)**  
Work notes are an important part of the state flow process and are used to communicate information about state transitions.

**Parent Topic:**[State flows](c_StateFlows.md)

**Related topics**  


[Use state flows](c_UseStateFlows.md)

[Create a state flow](../task/t_CreateAStateFlow.md)

