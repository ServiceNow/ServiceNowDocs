---
title: Create a problem task model in Service Operations Workspace
description: Create custom Problem Management models with states and transitions tailored to your use cases.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Problem Management in Service Operations Workspace, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Create a problem task model in Service Operations Workspace

Create custom Problem Management models with states and transitions tailored to your use cases.

## Before you begin

See considerations for enabling Problem Management models at [Problem Management models in Service Operations Workspace](../concept/problem-mgmt-models-sow.md).

Enable the system property **com.snc.problem\_management.models.enabled**. For more information, see [Enable Problem Management models in Service Operations Workspace](enable-problem-mgmt-models-sow.md).

Role required: admin

## Procedure

1.  Open the Problem Task Models table in one of the following ways.

    -   In the navigation filter, enter `prb_task_model.list`.
    -   Navigate to **All** &gt; **Problem** &gt; **Administration** &gt; **Problem Task Models**.

        **Note:** For more information about enabling menu items for Problem Management models, see [Enable or disable an application menu or module](https://www.servicenow.com/docs/access?context=t_EnDisableAppMenuOrMod&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

2.  Create a task model.

    1.  Select **New**.

    2.  On the Problem Task Model form, fill in the fields.

        For more information, see [Problem task model form](../../problem-management/reference/problem-task-model-form.md).

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
        |From|State that the problem task record is moving from.|
        |To|State that the problem task record is moving to.|
        |Automatic transition|Option for enabling automatic transition to the problem task record when the defined conditions are met. Selecting this option also prevents you from manually selecting the **State** field on the problem task record.|

    3.  Select **Submit** for each model state transition that you add.

5.  Apply transition conditions by selecting any of your model state transitions.

    1.  From the Transition Conditions context menu, select **New**.

    2.  On the Model State Transition Condition form, fill in the fields.

        For more information, see [Problem Management model state transition condition form](../../problem-management/reference/problem-model-state-transition-condition.md).

    3.  Select **Submit** for each transition condition that you add.

6.  Create an interceptor for your model by entering `sn_sow_interceptor_record_type_selector.list` in the navigation filter.

    1.  From the Applies to column, search for `=problem_task`.

    2.  Select **New**.

    3.  On the Record Type Selector form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Applies to|Set to **Problem Task \[problem-task\]** for creating problem task models.|
        |Order|Order in which the associated model is displayed.|
        |Title|Name of the model displayed on the button when creating problem tasks.|
        |Description|Description of the model displayed on the button when creating problem task.|
        |Active|Option to make the record type selector active.|

    4.  From the drop-down **Values** list, select **Model**.

    5.  Select the search icon \(![search icon](../../configurable-workforce-optimization-itsm/image/search_icon.png)\) and select your custom problem task model from the list.

    6.  From the Condition list, select **Show Related Fields** at the bottom of the list.

    7.  From the Condition list of related fields, select **Problem → Problem fields**.

    8.  From the Condition list of **Problem → Problem fields** fields, select **Model**.

    9.  From the Condition list of operators, select **is not empty**.

    10. Select **Submit**.


## Result

Your custom problem task model is available as a choice in Service Operations Workspace for the roles specified in your model.

