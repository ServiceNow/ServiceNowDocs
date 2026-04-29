---
title: Create GRC workflow states
description: Add Governance, Risk, and Compliance workflow states to a state model to define the individual steps in your workflow. Each workflow state represents a phase in the authorization package life cycle and determines what you can do at that stage.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [GRC state model configuration, CAM workflow configuration, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Create GRC workflow states

Add Governance, Risk, and Compliance workflow states to a state model to define the individual steps in your workflow. Each workflow state represents a phase in the authorization package life cycle and determines what you can do at that stage.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **GRC State Models**.

2.  Open the state model record to which you want to add workflow states.

3.  In the **GRC workflow states** section, select **New** to create a workflow state.

4.  On the **GRC workflow state New record** form, fill in the fields.

<table id="table_qt2_4by_thc"><thead><tr><th>

Fields

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

State

</td><td>

Select the state from the drop-down list.

</td></tr><tr><td>

Display type

</td><td>

Select **As node** or **As sub-level** to display how the state appears in the authorization package. **Note:** If the display type for the state is **As sub-level**, then define the state that serves as the parent node for the sublevel.

</td></tr><tr><td>

Stepper Label

</td><td>

Enter the display name of the state that appears in the authorization package.

</td></tr></tbody>
</table>5.  Select **Submit** to add the workflow state to the state model.


## Result

The workflow states appear in the workflow states related list on the state model record. After adding all the required states, you can create state transitions to define valid paths between steps.

## What to do next

[Configure transition between state models](create-state-transitions.md)

