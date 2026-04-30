---
title: Decision activities
description: Create and define branches with different conditions for different paths between activities.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Stages and activities, Building playbooks, Use, Workflow Studio, Build workflows]
---

# Decision activities

Create and define branches with different conditions for different paths between activities.

## Before you begin

Role required: playbook.admin

## About this task

Add a decision activity to create a decision tree between activities so that agents in Playbook Experience can troubleshoot if-then situations during runtime. Branches are the different paths with different conditions that agents can follow. For example, in a credit card approval playbook:

![Playbook decisions credit card approval example in Diagram view in Workflow Studio](../images/playbook-decisions-example.png)

In this example, an agent can take different actions for different credit scores during a decision activity to assess the risk of a credit card applicant.

Decisions are also supported for stages. To learn more, see [Decision stages](create-decision-stage.md).

## Procedure

1.  In Diagram view, hover on the object that you want to insert a decision activity next to, and select the **+** icon to add an activity.

    **Note:** Decision activities can only be added in Diagram view, but can be modified and viewed in Board view.

    The mini-picker displays.

2.  Select the diamond icon ![Diamond decision icon in Diagram view mini-picker.](../images/diagram-decision-icon.png) to add a decision.

    A decision is added with two branches and the side panel opens for configuration.

3.  Under the **Details** tab, fill in the following fields.

<table id="table_jpj_mfx_c1c"><tbody><tr><td>

**Label**

</td><td>

Enter a unique name for your activity. This name appears in your playbook during runtime.

</td></tr><tr><td>

**Description**

</td><td>

Optionally, enter some descriptive details about your activity.

</td></tr><tr><td>

**Start Rule**

</td><td>

Choose when you want your activity to start running. Options include:-   **When stage starts**: Your activity starts running as soon as its stage starts running. Your stage starts running when your playbook is triggered.
-   **After specific activities**: Your activity starts running after specified activities have finished running.


</td></tr><tr><td>

**Display order**

</td><td>

Define the order in which this activity will appear during a playbook run.

</td></tr><tr><td>

**Run condition**

</td><td>

After the activity starts, the activity runs only if specific conditions are met.

</td></tr><tr><td>

**Start with delay**

</td><td>

Specify a duration of time to wait before running an activity whose start rule and conditions have been met. Give users a specific amount of time to complete actions. For more information, see [Start with delay input properties](../reference/start-with-delay-properties.md).

</td></tr><tr><td>

**Restart rules**

</td><td>

Choose what this activity does when a playbook is restarted:-   **Skip on restart**: Skip this activity when the playbook run is due to a restart.
-   **Run always**: Always run this activity, including first runs.
-   **Skip on first run**: Skip this activity during the first run.
For more information, see [Restart a playbook](restart-a-playbook.md).

</td></tr></tbody>
</table>4.  Under the **Branches** tab, select your new branch to begin configuring it.

    1.  Give your branch a unique label.

    2.  Select the **Add Condition** button.

        The [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) displays.

        **Note:** Branches can only be added in the side panel.

        ![Playbook decision activity side panel](../images/playbook-decisions-side-panel.png)

    3.  Select or enter a field, operator, and value.

5.  Add more branches as needed.

    Branches can only be added via the side panel.

6.  If you add two or more branches, select whether to process all branches with conditions that are met, or just to process the first listed branch with conditions met.

7.  If you selected to **Process only the first one that is true**, drag and drop the branch that you want to be evaluated to the top.

    ![Drag and drop branches in the side panel](../images/playbook-decision-branch-order.gif)


## Result

You've added and configured decision branches between activities.

**Parent Topic:**[Stages and activities](../concept/process-automation-designer-lanes-activities.md)

**Related topics**  


[Add and configure a stage in a playbook](add-configure-stage.md)

[Activity definitions](../concept/activity-definitions.md)

[Add and configure an activity in a playbook](add-configure-activity.md)

[Use AI agent as an activity](ai-agent-as-activity.md)

[Automation Assets](../concept/automation-assets.md)

[Start with delay input properties](../reference/start-with-delay-properties.md)

[Optional activities](../concept/optional-activities.md#)

[Decision stages](create-decision-stage.md)

[Questionnaire activity](../reference/questionnaire-activity.md)

[Parallel branches](create-parallel-activity.md)

[Add dynamic inputs to an activity](add-dynamic-inputs-to-activity.md)

[Playbook activity state mapping](../../workspace/concept/playbook-activity-state-mapping.md)

