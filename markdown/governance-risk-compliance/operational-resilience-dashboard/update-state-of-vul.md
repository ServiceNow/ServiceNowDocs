---
title: Update the state of the operational vulnerability
description: Update the state of the Operational vulnerability record to the Assessment or Treatment state. At this stage, the vulnerability is being evaluated to determine the best course of action and create an action task accordingly.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing Operational vulnerability, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Update the state of the operational vulnerability

Update the state of the Operational vulnerability record to the **Assessment** or **Treatment** state. At this stage, the vulnerability is being evaluated to determine the best course of action and create an action task accordingly.

## Before you begin

Role required: sn\_oper\_res.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **All Operational Vulnerabilities**.

2.  Open the vulnerability record from the list.

    The Operational vulnerability record is in the **New** state.

    ![New state.](../image/op-vul-new-state.png)

3.  Select **Update state** UI action.

    The **New** state can be transitioned to the following states as shown in the example:

    -   **Assessment**
    -   **Treatment**
    -   **Pending approval**
    -   **Approved**
    -   **Closed**
    -   **Canceled**
    ![State transition for New state.](../image/new-state-transition.png)

    For more information on the state transition model, see [Set up the State model and Action task model](establish-state-model-record.md).

4.  Update the state of the vulnerability record.

    |Step|Description|
    |----|-----------|
    |**Select __Update state__ UI action, select __Assessment__, add comments in __Additional comments__, and select __Submit__.**|This action updates the state of the vulnerability record to the **Assessment** state.|
    |**Select __Update state__ UI action, select __Treatment__, add comments in __Additional comments__, and select __Submit__.**|This action updates the state of the vulnerability record to the **Treatment** state.|

    The Update state window is shown in the example.

    ![Assessment.](../image/op-vul-update-state.png)

    When the state is updated to **Assessment**, the state of the Operational vulnerability record is updated to the **Assessment in progress** state as shown in the example.

    ![Assessment in progress.](../image/op-vul-assmt-in-progress.png)


## What to do next

When the vulnerability record is in the **Assessment** state, the task owner creates an assessment-type action task. For more information, see [Manage an assessment-type action task](create-action-task-op-vul.md).

When the vulnerability record is in the **Treatment** state, the task owner creates an investigation-type action task. For more information, see [Manage an investigation-type action task](update-state-of-action-task.md).

