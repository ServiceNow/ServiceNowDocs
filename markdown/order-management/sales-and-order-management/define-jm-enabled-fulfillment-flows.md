---
title: Define Jeopardy-enabled fulfillment workflows
description: Create jeopardy-enabled fulfillment workflows using Workflow Studio. The workflows enable Jeopardy Management to track task completion times and manage risk.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 2
breadcrumb: [Configuring Jeopardy Management, Order management, Configure, Sales Customer Relationship Management]
---

# Define Jeopardy-enabled fulfillment workflows

Create jeopardy-enabled fulfillment workflows using Workflow Studio. The workflows enable Jeopardy Management to track task completion times and manage risk.

## Before you begin

Role required: admin

## About this task

Creating fulfillment flows starts with defining subflows in Workflow Studio using unique actions developed for Jeopardy Management.

The following Workflow Studio actions are used to create Jeopardy Management flows:

-   Create Order Planned Task
-   All Place Holder Tasks Created for Domain Order
-   Set Task Relationships
-   All Relationships Created for Order Tasks on Domain Order
-   Set Order Task State

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    Workflow Studio opens in a separate window.

2.  Select **Subflows** and do one of the following:

    -   Search for existing subflows that you want to edit.
    -   Start a new flow by selecting **New** &gt; **Subflow**.
3.  Give the subflow a name and provide any additional information.

4.  Select the **Build subflow** action.

    ![The figure shows a Jeopardy Management subflow using the Create Order Planned Task action in Workflow Studio.](../image/jm-create-order-planned-task.png)

5.  Build the Jeopardy Management subflow using the following actions:

6.  <table id="table_ykg_nwz_dyb"><thead><tr><th>

Order flow action

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Create Order Planned Task

</td><td>

Creates an order task and provides the option to establish task relationship with an existing order task. The Create Order Planned Task action extends planned tasks to Jeopardy Management.

</td></tr><tr><td>

All Placeholder Tasks Created for Domain Order

</td><td>

Sets the domain order stage to all order tasks created, so order tasks created by other subflows can have relationships created with current flow order tasks.

</td></tr><tr><td>

Set Task Relationship

</td><td>

Sets the relationship between two order tasks by creating a record in the planned\_task\_rel\_planned\_task table. The table calculates the order line item runtime and the order task jeopardy calculations.

</td></tr><tr><td>

All Relationships Created for Order Tasks on Domain Orders

</td><td>

Introduces the domain order all\_relationship\_set and sets the field to true in the subflow when all task relationships are established.

</td></tr><tr><td>

Set Task Order State

</td><td>

The flow action checks if an order task has a previous state value and uses the previous state to update the order task state during inflight state change.

 The Set the Order Task State action checks to see if an order task has a previous state value and uses the previous state to update the order task state during inflight state changes.

</td></tr></tbody>
</table>    **Note:** For more information about building subflows, see [Building subflows](https://www.servicenow.com/docs/access?context=subflows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

7.  Test the flow by selecting **Test**.

8.  Publish the flow by selecting **Publish**.


## What to do next

[Configure the Order Task Duration Assignment Policy](configure-order-task-duration-assignment-policy.md).

