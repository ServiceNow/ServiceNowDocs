---
title: Create a problem task model
description: Create custom Problem Management models with states and transitions tailored to your use cases.
locale: en-US
release: zurich
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Problem Management, IT Service Management]
---

# Create a problem task model

Create custom Problem Management models with states and transitions tailored to your use cases.

## Before you begin

See considerations for enabling Problem Management models at [Problem Management models](../concept/problem-mgmt-models.md).

Role required: admin

## Procedure

1.  Open the Problem Task Models table in one of the following ways.

    -   In the navigation filter, enter `prb_task_model.list`.
    -   Navigate to **All** &gt; **Problem** &gt; **Administration** &gt; **Problem Task Models**.

        **Note:** For more information about enabling menu items for Problem Management models, see [Enable or disable an application menu or module](https://www.servicenow.com/docs/access?context=t_EnDisableAppMenuOrMod&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

    1.  Select **New**.

    2.  Save the sys\_id for creating an interceptor \(as described in later steps\) by selecting **Copy sys\_id** from the form context menu icon \(![Form context menu icon.](../../change-management/image/form-context-menu.png)\).

    3.  On the Problem Task Model form, fill in the fields.

        For more information, see [Problem task model form](../reference/problem-task-model-form.md).

2.  Choose the states for your custom model by selecting **Save** from the form context menu icon \(![Form context menu icon.](../../change-management/image/form-context-menu.png)\).

    1.  From the Model States context menu that appears, select **New**.

    2.  On the Model State form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |State|State that you want to include in your model.|
        |Initial state|Option to enable this state as the initial state for your model. This field is automatically selected when you add the first state to your model.|

    3.  Select **Submit** for each state you choose.

3.  Apply a transition to each model state by selecting the display/hide hierarchical lists icon \(![Display/hide hierarchical lists icon.](../../change-management/image/display-hide-hierarchial-lists.png)\).

    1.  From the Model State Transitions context menu, select **New**.

    2.  On the Model State Transitions form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |From|State that the problem task record is moving from.|
        |To|State that the problem task record is moving to.|
        |Automatic transition|Option for enabling automatic transition to the problem task record when the defined conditions are met. Selecting this option also prevents you from manually selecting the **State** field on the problem task record.|

    3.  Select **Submit** for each model state transition that you add.

4.  Apply transition conditions by selecting any of your model state transitions.

    1.  From the Transition Conditions context menu, select **New**.

    2.  On the Model State Transition Condition form, fill in the fields.

        For more information, see [Problem Management model state transition condition form](../reference/problem-model-state-transition-condition.md).

    3.  Select **Submit** for each transition condition you add.

5.  Create an interceptor for your model by navigating to **All** &gt; **System Definition** &gt; **Interceptors**.

    1.  From the Name column, search for `*models`.

    2.  Select **Problem Task Models** from the list.

    3.  From the interceptor list for problem task models, select **New**.

    4.  Select **Simple question to redirect the URL**.

    5.  On the Interceptor Answer form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name for the intercept.|
        |Order|Order in which the associated model is displayed.|
        |Active|Option to make the intercept active.|
        |User Prompt|Name of the model that your user sees.|
        |Roles|Option to define the roles to select the problem task model.|

        **Note:** In the **Target URL** field, specify your model's sys\_id in the following format:

        `problem_task.do?sys_id=-1&sysparm_query=prb_task_model=[sys_id]`.

    6.  Select **Submit**.


## Result

Your custom problem task model is available as a choice for the roles specified in your interceptor.

**Parent Topic:**[Configuring Problem Management](../concept/configuring-problem-mgmt.md)

**Previous topic:**[Create a problem model](create-problem-model.md)

**Next topic:**[Applying CSDM guidelines to Problem Management](../concept/pm-use-case-product-view.md)

