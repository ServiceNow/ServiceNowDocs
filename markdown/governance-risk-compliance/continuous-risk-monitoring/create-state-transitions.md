---
title: Configure transition between state models
description: Create state model transitions to define valid paths between workflow states. State model transitions control how authorization packages move from one step to another and verify that packages follow the correct sequence through your workflow.
locale: en-US
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-12-06"
reading_time_minutes: 1
breadcrumb: [Create GRC workflow states, GRC state model configuration, CAM workflow configuration, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Configure transition between state models

Create state model transitions to define valid paths between workflow states. State model transitions control how authorization packages move from one step to another and verify that packages follow the correct sequence through your workflow.

## About this task

<table id="simpletable_bhc_q1p_nhc"><thead><tr><th>

Transitions

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Forward transitions

</td><td>

Create forward transitions to move packages to the next step in the workflow sequence.For example, From Prepare \(Order 1\) - To Categorize \(Order 2\).

</td></tr><tr><td>

Backward transitions

</td><td>

Create backward transitions to enable packages to return to previous steps for corrections or updates.For example, From Categorize \(Order 2\) - To Prepare \(Order 1\).

</td></tr></tbody>
</table>## Before you begin

Role required: sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **GRC State Models**.

2.  Open the state model record that contains workflow states.

3.  On the **GRC workflow states** related list, select the workflow state from which you want to create a transition.

4.  On the **Model State Transitions** tab, select **New**.

    ![Selecting Model State Transitions tab.](../image/WF-state-transition1.png)

5.  On the **Model State Transition New record** form, fill in the fields.

    |Fields|Descriptions|
    |------|------------|
    |From|The current state is automatically populated.|
    |To|Select the state that this transition leads to.|

    ![State transition fields.](../image/WF-state-transition2.png)

6.  Select **Submit** to create the state transition to the selected workflow state.

7.  Repeat steps 4–6 for all valid transitions from the current state.

8.  Return to the state model record and repeat steps 3–7 for each workflow state.


## What to do next

[Create GRC model state transition conditions](add-state-transition-conditions.md)

