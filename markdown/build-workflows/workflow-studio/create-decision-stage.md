---
title: Decision stages
description: Create and define branches with different conditions for different paths between stages.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Decision stages

Create and define branches with different conditions for different paths between stages.

## Before you begin

Role required: playbook.admin

## About this task

Add a decision node between stages to determine which stage to run next, based on runtime conditions. For example, in a recruitment playbook, you can have multiple stages for each interview round and one disqualification stage. After each interview stage, you can add a decision to automatically select whether to run the next interview round or proceed to disqualification based on the completed stage.

![A playbook with decision between stages.](../images/decision-stages.png)

Adding decision between stages help you achieve the following benefits:

-   **Simplified authoring**

    Reduces the need to copy run conditions across stages.

-   **Improved transparency**

    Makes branching logic more visible and easier to manage.

-   **Enhanced runtime experience**

    Displays only the relevant stages to the end user, improving performance and clarity.


## Procedure

1.  In Diagram view, select the **+** icon.

2.  From the mini-picker, select the diamond icon ![Diamond decision icon in Diagram view mini-picker.](../images/diagram-decision-icon.png) to add a decision.

    A decision is added with two branches and the side panel opens for configuration.

3.  Under the **Details** tab, fill in the following fields.

<table id="table_jpj_mfx_c1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Label**

</td><td>

Enter a unique name for the decision.

</td></tr><tr><td>

**Description**

</td><td>

Enter some descriptive details about the decision.

</td></tr><tr><td>

**Start Rule**

</td><td>

Choose when you want to evaluate the decision. Options include:-   **When playbook starts**: The decision starts running as soon as the playbook starts.
-   **After specific stages**: The decision starts running after specified stages have finished running.


</td></tr></tbody>
</table>4.  Select **Show additional options** to specify the following optional fields:

<table id="table_ajv_h3m_2hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Display order**

</td><td>

When multiple stages run at the same time, define the order in which stages appear during a playbook run.**Note:** In Workflow Studio, this can also be helpful when viewing parallel stages and activities in Diagram view.

</td></tr><tr><td>

**Start with delay**

</td><td>

Specify a duration of time to wait before running a stage whose start rule and conditions have been met. For more information, see [Start with delay input properties](../reference/start-with-delay-properties.md).

</td></tr><tr><td>

**Restart rules**

</td><td>

Choose what this activity does when a playbook is restarted:-   **Skip on restart**: Skip this stage when the run is due to a restart.
-   **Run always**: Always run this stage, including first runs.
-   **Skip on first run**: Skip this stage during the first run.
For more information, see [Configure restart for Playbooks](enable-define-restart.md).

</td></tr></tbody>
</table>5.  Under the **Branches** tab, select your new branch to begin configuring it.

    1.  Give your branch a unique label.

    2.  Select the **Add Condition** button.

        The condition builder displays.

    3.  Select or enter a field, operator, and value.

6.  Add more branches as needed.

    Branches can only be added via the side panel.

7.  If you add two or more branches, select whether to process all branches with conditions that are met, or just to process the first listed branch with conditions met.

8.  If you selected to **Process only the first one that is true**, drag and drop the branch that you want to be evaluated to the top.

9.  Select **Save and close**.


## Result

You've added and configured decision branches between stages.

## What to do next

Complete and test the playbook. For more information, see [Test a playbook](test-process.md).

**Parent Topic:**[Stages and activities](../concept/process-automation-designer-lanes-activities.md)

**Related topics**  


[Add and configure a stage in a playbook](add-configure-stage.md)

[Activity definitions](../concept/activity-definitions.md)

[Add and configure an activity in a playbook](add-configure-activity.md)

[Use AI agent as an activity](ai-agent-as-activity.md)

[Automation Assets](../concept/automation-assets.md)

[Start with delay input properties](../reference/start-with-delay-properties.md)

[Optional activities](../concept/optional-activities.md#)

[Decision activities](create-a-decision-activity.md)

[Questionnaire activity](../reference/questionnaire-activity.md)

[Parallel branches](create-parallel-activity.md)

[Add dynamic inputs to an activity](add-dynamic-inputs-to-activity.md)

[Playbook activity state mapping](../../workspace/concept/playbook-activity-state-mapping.md)

