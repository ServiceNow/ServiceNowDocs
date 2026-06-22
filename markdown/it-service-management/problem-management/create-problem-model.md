---
title: Create a problem model
description: Create custom Problem Management models with states and transitions tailored to your use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/problem-management/create-problem-model.html
release: zurich
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Problem Management, IT Service Management]
---

# Create a problem model

Create custom Problem Management models with states and transitions tailored to your use cases.

## Before you begin

See considerations for enabling Problem Management models at [Problem Management models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/problem-management/problem-mgmt-models.md).

Role required: admin

## Procedure

1.  Open the Problem Models table in one of the following ways.

    -   In the navigation filter, enter `prb_model.list`.
    -   Navigate to **All** &gt; **Problem** &gt; **Administration** &gt; **Problem Models**.

        **Note:** For more information about enabling menu items for Problem Management models, see [Enable or disable an application menu or module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-user-experiences/t_EnDisableAppMenuOrMod.md).

    1.  Select **New**.

    2.  On the Problem Model form, fill in the fields.

        For more information, see [Problem model form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/problem-management/problem-model-form.md).

2.  Choose the states for your custom model by selecting **Save** from the form context menu icon \(\[Omitted image "form-context-menu.png"\] Alt text: Form context menu icon.\).

    1.  From the Model States context menu that appears, select **New**.

    2.  On the Model State form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |State|State that you want to include in your model.|
        |Initial state|Option to enable this state as the initial state for your model. This field is automatically selected when you add the first state to your model.|

    3.  Select **Submit** for each state you choose.

3.  Apply a transition to each model state by selecting the display/hide hierarchical lists icon \(\[Omitted image "display-hide-hierarchial-lists.png"\] Alt text: Display/hide hierarchical lists icon.\).

    1.  From the Model State Transitions context menu, select **New**.

    2.  On the Model State Transitions form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |From|State that the problem record is moving from.|
        |To|State that the problem record is moving to.|
        |Automatic transition|Option for enabling automatic transition to the problem record when the defined conditions are met. Selecting this option also prevents you from manually selecting the **State** field on the problem record.|

    3.  Select **Submit** for each model state transition that you add.

4.  Apply transition conditions by selecting any of your model state transitions.

    1.  From the Transition Conditions context menu, select **New**.

    2.  On the Model State Transition Condition form, fill in the fields.

        For more information, see [Problem Management model state transition condition form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/problem-management/problem-model-state-transition-condition.md).

    3.  Select **Submit** for each transition condition you add.


## Result

If you selected the **Default problem model** option in the Problem Model form, your custom problem model is used when new problems are created.

**Parent Topic:**[Configuring Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/problem-management/configuring-problem-mgmt.md)

**Previous topic:**[Enable Problem Management models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/problem-management/enable-problem-mgmt-models.md)

**Next topic:**[Create a problem task model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/problem-management/create-problem-task-model.md)

