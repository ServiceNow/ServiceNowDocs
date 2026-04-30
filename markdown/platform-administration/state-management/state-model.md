---
title: State Management
description: State Management enables an administrator to define State Models and State Transitions that control how a record is allowed to transition through a predefined list of states.
locale: en-US
release: zurich
product: State Management
classification: state-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure core features, Administer]
---

# State Management

State Management enables an administrator to define State Models and State Transitions that control how a record is allowed to transition through a predefined list of states.

An example of a state transition is when the **State** field in a facilities request is moved from the **Assigned** state to the **Work In Progress** state.

State Management is active for all instances.

## What is a state model?

A state model is a list of states that describe an expected record workflow through the lifecycle of the record. State models can be defined for any table that extends the task table. State models simplify defining the state transitions allowed for a specific task type.

In the State Model \[sys\_state\_model\] table, define the name of the state model and which task table the state model is applied to. Use the condition builder to specify any conditions for applying the state model to records and any required condition for moving between states.

For example, you could define a state model for a new custom application for airline reservations. The custom application has a Reservation Request \[reservation\_request\] table with 4 states: **Held**, **Confirmed**, **Completed**, and **Canceled**. You could define the state model to target the Reservation Request table, and then define the state transitions for each of the 4 states. When you enable the state model, the choice list for the **State** field includes only the choices allowed by the conditions in the state transitions.

**Note:** State Management includes example state models that are copies of the normal, emergency, and standard change request state models. By default, these examples are not enabled. Use them only as examples to develop a state model and transitions for a task table that does not have a state model. Do not enable these example state models for change requests and then make changes to them. Doing so breaks existing transitions for change requests.

## What is a state transition?

State transitions are a list of conditions for entering or exiting each state defined for a table. In the State Transitions \[sys\_state\_transition\] table, use the condition builder to build a list of conditions required for entering or exiting each state.

To prevent users from choosing an invalid state, any attempt to update a record’s state is denied if it violates the state transitions, whether the attempt is through user input, a script, a Web API such as REST or SOAP, or any other source.

State transitions control the choice list for the **State** field on the target task table and prevent you from choosing any state value that does not adhere to the underlying process or does not meet the defined conditions for the transition.

For example, if the enter condition for the **Completed** state is **State is Confirmed**, only records in the Confirmed state can transition to the Complete state. When a record is in the Confirmed state, the only choice in the **State** field choice list is **Completed**.

