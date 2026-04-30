---
title: Set up the State model and Action task model
description: Set up the Vulnerability state model and Action task model to manage the workflow of the Operational vulnerability record. These models define the workflow states and transition conditions for a record type and an action task, respectively. Both the Operational vulnerability record type and the action task adhere to the workflow states configured in their corresponding models.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Setting up the Operational vulnerability module, Completing general administrative tasks, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Set up the State model and Action task model

Set up the Vulnerability state model and Action task model to manage the workflow of the Operational vulnerability record. These models define the workflow states and transition conditions for a record type and an action task, respectively. Both the Operational vulnerability record type and the action task adhere to the workflow states configured in their corresponding models.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

An operational vulnerability typically goes through the following workflow states:

-   **New**: The vulnerability has been opened and it is in the initial stage of review.
-   **Assessment**: The vulnerability is being evaluated to determine the appropriate course of action.
-   **Treatment**: The vulnerability is being actively investigated to gather information and evidence. The course of action and treatment is being decided.
-   **Pending approval**: The vulnerability is being worked on to find a resolution.
-   **Approved**: A review of the vulnerability is being done after it is resolved.
-   **Closed**: The vulnerability is closed and is no longer active.
-   **Canceled**: The vulnerability is canceled and it is no longer being pursued.

When the state transition conditions are satisfied, each vulnerability state gets updated to the next state. For example, the **New** state can be transitioned to the following states as shown in the example:

-   **Assessment**
-   **Treatment**
-   **Pending approval**
-   **Approved**
-   **Closed**
-   **Canceled**

![State transition for New state.](../image/new-state-transition.png)

-   **New to Approved**: Users can select **New to Approved** to view the state transition condition. Once this condition is met, the vulnerability status updates from **New** to **Approved** as shown in the example.

    ![State transition condition.](../image/state-transition-condition.png)

    When all action tasks are closed, the users with write access can update the state as shown in the example.

    ![Tasks to be closed.](../image/state-transition-condition-tasks-to-be-closed.png)

-   **New to Assessment**: Once the state transition condition is met, the vulnerability status updates from **New** to **Assessment**.
-   **New to Canceled**: Once the state transition condition is met, the vulnerability status updates from **New** to **Canceled**. The vulnerability is canceled and it is no longer being pursued.
-   **New to Pending approval**: Once the state transition condition is met, the vulnerability status updates from **New** to **Pending approval**. The vulnerability is being worked on to find a resolution.
-   **New to Treatment**: Once the state transition condition is met, the vulnerability status updates from **New** to **Treatment**. The vulnerability is being actively investigated to gather information and evidence. The course of action and treatment is being decided.

The following model state transitions are displayed in the Model State Transitions related list: These states can vary depending on the organization's vulnerability management process.

Workflow states for an action task are defined as follows:

-   **Draft**: The action task is in the draft stage.
-   **Assigned**: The action task has been assigned to an appropriate user.
-   **Work in progress**: Work on the action task is in progress.
-   **Review**: The action task is in the review stage.
-   **Closed complete**: The action task is in the Closed complete stage.
-   **Closed incomplete**: The action task is in the Closed incomplete stage.
-   **Canceled**: The action task has been canceled.

When the action task transition conditions are satisfied, each action task state gets updated to the next state. For example, the **Draft** state can be transitioned to the **Assigned** and **Canceled** states as shown in the example.

![State transition for the Draft state.](../image/action-task-state-transition.png)

Once the condition is met, the action task is updated from **Draft** to **Assigned** as shown in the example.

![Draft to Assigned.](../image/action-task-state-transition-condition.png)

When the state transition condition is fulfilled, the state gets updated or else an error message is displayed as shown in the example.

![Error message.](../image/action-task-state-transition-condition-fulfilled.png)

## Procedure

1.  Navigate to **All** &gt; **Operational Vulnerability** &gt; **State Models**.

2.  Update the table name.

    |Step|Description|
    |----|-----------|
    |**Configure Vulnerability state model**|Select **New** and select Operational vulnerability \[sn\_oper\_res\_vulnerability\] as the table name.|
    |**Configure Action task model**|Select **New** and select Action task \[sn\_grc\_case\_mgmt\_case\_task\] as the table name.|

    The Action task model is shown in the following example.

    ![Action task model.](../image/action-task-model.png)

3.  On the State model form, fill in the other fields.

    For more information on the fields, see [GRC state model form](../reference/grc-state-model-form-for-op-vul.md).

4.  Select **Submit**.

5.  To copy an existing State model, select it from the state models list and select **Copy Model**.

    You can copy an existing Vulnerability state model as shown in the following example.

    ![State model.](../image/vul-state-model.png)

6.  To update an existing State model, select it from the list and select **Update**.

7.  To delete an existing State model, select it from the list and select **Delete**.


