---
title: Create a Change Model for Design and Assign function
description: Create a Change model and add the model states and model state transitions. You can use this Change model to configure a Design and Assign function.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Design and Assign function, Configure, Telecommunications Network Inventory]
---

# Create a Change Model for Design and Assign function

Create a Change model and add the model states and model state transitions. You can use this Change model to configure a Design and Assign function.

## Before you begin

Role required: admin, sn\_ni\_core.inventory\_admin

## About this task

You create a change model to configure a Design and Assign function for a network service. You must add model states to the change model to move and track change requests through several states.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Change Models**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the Change model.|
    |Active|Option for enabling that this model is available for selection when creating a change request.|

4.  Select **Save**.

    The Model States context menu appears. You can select the states for your Change model.

5.  On the **Model States** tab, select **New**.

6.  On the form, fill in the fields.

<table id="table_aq1_tzn_sdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State

</td><td>

State that you want to include in your Change model. You can add the following state models.-   **Design in progress​**

The activities are in progress.

-   **Design in review​**

The activities are completed and the change request is in review for approval.

-   **Design complete**

The change request is approved.

-   **Closed**

The change request is closed.

You can also add a new model state to the Change model based on the requirements of your Design and Assign function. To learn more, see [add multi-layer model states](https://www.servicenow.com/docs/access?context=t_AddANewState&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

Initial State

</td><td>

Option to enable this state as the initial state for your model. This field is automatically selected when you add the first state to your model. For Design and Assign function, you can set **Design in progress**​ state as initial state.

</td></tr></tbody>
</table>7.  To save the state and return to the Change Model form, select **Submit**.

8.  To add a transition between the states, select the display/hide hierarchical lists icon \(![Hide/display hierarchical Lists Icon](../image/icon-display-hide-hierarchial.png)\) for the model state that you want to apply the transition to.

    The Model State Transitions context menu appears.

9.  Select **New**.

10. On the **Model State Transition** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |From|State that the change request is moving from.|
    |To|State that the change request is moving to.|
    |Automatic Transition|Option for enabling automatic transition to the change request when the defined conditions are met. Selecting this option also helps prevent you from manually selecting the **State** field on the Change request form.|

11. To save the state and return to the Change Model form, select **Submit**.

12. Select **Submit**.


## Result

A Change model is created with the model states and model state transitions.

## What to do next

Create a record producer to configure an activity in the playbook. To learn more, see [Create a record producer for the Design and Assign function](create-record-producer-design-assign-playbook.md).

**Parent Topic:**[Configuring Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

**Related topics**  


[Create a Change model](https://www.servicenow.com/docs/access?context=create-a-change-model&version=australia&pubname=australia-it-service-management&ft:locale=en-US)

[Legacy: State model and transitions](https://www.servicenow.com/docs/access?context=c_ChangeStateModel&version=australia&pubname=australia-it-service-management&ft:locale=en-US)

[Configuring Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

[Configure a Design and Assign function example](../concept/configure-design-assign-playbook-use-case.md)

