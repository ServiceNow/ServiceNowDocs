---
title: Define the model state transitions for a privacy case
description: Define the transition conditions to control how a compliance case traverses through the different workflow states by using the Privacy Case Management application.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Privacy Case Management, Privacy Management, Governance, Risk, and Compliance]
---

# Define the model state transitions for a privacy case

Define the transition conditions to control how a compliance case traverses through the different workflow states by using the Privacy Case Management application.

## Before you begin

Role required: sn\_privacy\_case.privacy\_case\_admin

## About this task

The state transitions are a list of conditions for entering or exiting each state that is defined for a table. In the State Transitions table, use the condition builder to build a list of required conditions for entering or exiting each state.

## Procedure

1.  Navigate to **All** &gt; **Privacy Case Management** &gt; **State Models**.

2.  Open the state model that you want to define the model state transition for.

3.  To define the model state transition, select the required workflow state.

4.  On the Model State Transitions context menu, select **New**.

5.  Select the state that you want to move to from the selected state.

6.  To enable the automatic transition of the workflow state, select the **Automatic transition** option.

7.  Open the form context menu and select **Save**.

    The GRC model state transition conditions related list appears.

8.  On the GRC model state transition conditions context menu, select **New**.

9.  On the form, fill in the fields.

    For a description of the field values on the GRC model state transition form, see [GRC model state transition condition form](../reference/pcm-state-model-transition-condition-form.md).

10. Select **Submit**.


-   **[GRC model state transition condition form](../reference/pcm-state-model-transition-condition-form.md)**  
Use the GRC Model State Transition Condition form to define the transition conditions to control how a compliance case traverses through the different workflow states by using the Privacy Case Management application.

**Parent Topic:**[Configuring Privacy Case Management](../concept/configuring-privacy-case-management.md)

