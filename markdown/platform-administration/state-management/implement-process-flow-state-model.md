---
title: Implement process flow and UI actions with a state model
description: You can implement a process flow and UI actions with a state model.
locale: en-US
release: australia
product: State Management
classification: state-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [State Management, Configure core features, Administer the ServiceNow AI Platform]
---

# Implement process flow and UI actions with a state model

You can implement a process flow and UI actions with a state model.

## Before you begin

Role required: state\_model\_admin or admin

## About this task

State models provide a way to limit the choices for moving between states in a form. If you set up only a state model, users manually change states in the form. Additional steps are required to add the process flow or UI actions, as illustrated in the following example.

![Change Request form highlighting the UI Action and Process Flow.](../image/change-form-ui-actions-process.png)

## Procedure

1.  Verify the choices for the **State** field for the table and ensure that you created transitions for them.

    For more information about how to add **State** field choices, see [Best practices for state field choice values](../../field-administration/concept/c_BPForStateFieldChoiceValues.md#).

2.  After creating the state model, define the process flow.

    For more information about process flows, see [Process flow formatter](../../form-administration/reference/r_ProcessFlowFormatter.md#).

3.  Define UI actions as desired to move between states.

    For more information about UI actions, see [UI actions](../../list-administration/concept/c_UIActions.md).


## Result

After the state model is enabled, only the defined state transitions are included in the choice list for the **State** field, and the process flow and UI actions are implemented.

