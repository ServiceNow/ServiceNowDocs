---
title: Create a problem model in Service Operations Workspace
description: Create custom Problem Management models with states and transitions tailored to your use cases.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Problem Management in Service Operations Workspace, Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Create a problem model in Service Operations Workspace

Create custom Problem Management models with states and transitions tailored to your use cases.

## Before you begin

See considerations for enabling Problem Management models at [Problem Management models in Service Operations Workspace](../concept/problem-mgmt-models-sow.md).

Enable the system property **com.snc.problem\_management.models.enabled**. For more information, see [Enable Problem Management models in Service Operations Workspace](enable-problem-mgmt-models-sow.md).

Role required: admin

## Procedure

1.  Open the Problem Models table in one of the following ways.

    -   In the navigation filter, enter `prb_model.list`.
    -   Navigate to **All** &gt; **Problem** &gt; **Administration** &gt; **Problem Models**.

        **Note:** For more information about enabling menu items for Problem Management models, see [Enable or disable an application menu or module](https://www.servicenow.com/docs/access?context=t_EnDisableAppMenuOrMod&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

2.  Create a problem model.

    1.  Select **New**.

    2.  On the Problem Model form, fill in the fields.

        For more information, see [Problem model form](../../problem-management/reference/problem-model-form.md).

3.  Choose the states for your custom model by selecting **Save** from the form context menu icon \(![Form context menu icon.](../../change-management/image/form-context-menu.png)\).

    1.  From the Model States context menu that appears, select **New**.

    2.  On the Model State form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |State|State that you want to include in your model.|
        |Initial state|Option to enable this state as the initial state for your model. This field is automatically selected when you add the first state to your model.|

    3.  Select **Submit** for each state you choose.

4.  Apply a transition to each model state by selecting the display/hide hierarchical lists icon \(![Display/hide hierarchical lists icon.](../../change-management/image/display-hide-hierarchial-lists.png)\).

    1.  From the Model State Transitions context menu, select **New**.

    2.  On the Model State Transitions form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |From|State that the problem record is moving from.|
        |To|State that the problem record is moving to.|
        |Automatic transition|Option for enabling automatic transition to the problem record when the defined conditions are met. Selecting this option also prevents you from manually selecting the **State** field on the problem record.|

    3.  Select **Submit** for each model state transition that you add.

5.  Apply transition conditions by selecting any of your model state transitions.

    1.  From the Transition Conditions context menu, select **New**.

    2.  On the Model State Transition Condition form, fill in the fields.

        For more information, see [Problem Management model state transition condition form](../../problem-management/reference/problem-model-state-transition-condition.md).

    3.  Select **Submit** for each transition condition that you add.


## Result

If you selected the **Default problem model** option in the Problem Model form, your custom problem model is used when new problems are created.

