---
title: Add and configure an activity in a playbook
description: Add and configure an activity in your playbook.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Add and configure an activity in a playbook

Add and configure an activity in your playbook.

## Before you begin

Role required: playbook.admin or pd\_author

Review [Stages and activities](../concept/process-automation-designer-lanes-activities.md).

## Procedure

1.  Add an activity.

<table id="choicetable_e2d_3mv_21c"><thead><tr><th align="left" id="d178165e73">

View

</th><th align="left" id="d178165e76">

Steps

</th></tr></thead><tbody><tr><td id="d178165e82">

**Diagram**

</td><td>

1.  Select the **+** icon in the first stage.
2.  In the mini-picker, select the square icon ![Square activity icon in Diagram view mini-picker.](../images/diagram-activity-icon.png) to add an activity.
3.  In the activity picker, search for an activity to add.

**Note:** Select the application first, and then the activity from the resulting list.

</td></tr><tr><td id="d178165e114">

**Board**

</td><td>

1.  Select **+ Add activity** in the first stage.
2.  In the activity picker, search for an activity to add.

**Note:** Select the application first, and then the activity from the resulting list.

</td></tr></tbody>
</table>    Your new activity appears in the stage, and the Activity properties panel appears.

2.  Under the **Details** tab, fill in the details of your activity.

    1.  Provide the basic details of the activity.

<table id="table_lwk_5mv_21c"><tbody><tr><td>

**Label**

</td><td>

Enter a unique, user-facing name for your activity. This name appears to agents and fulfillers during runtime of your playbook.

</td></tr><tr><td>

**Description**

</td><td>

Optionally, enter some descriptive details about your activity.

</td></tr><tr><td>

**Start Rule**

</td><td>

Choose when you want your activity to start running. Options include:-   **When stage starts**: Your activity starts running as soon as its stage starts running. Your stage starts running when your playbook is triggered.
-   **After specific activities**: Your activity starts running after specified activities have finished running.


</td></tr></tbody>
</table>    1.  **Show additional options** the activity for [even more granular control](../reference/advanced-instruction-activity.md).

        **Warning:** Changing the advanced property fields of an activity can potentially break your automation. Make sure you understand how the playbook and its activities flow before you make changes.

<table id="choicetable_n4l_ydt_vlb"><tbody><tr><td id="d178165e269">

**Display order**

</td><td>

Define the order in which this activity will appear during a playbook run.

</td></tr><tr><td id="d178165e281">

**Run condition**

</td><td>

After the activity starts, the activity runs only if specific conditions are met.

</td></tr><tr><td id="d178165e290">

**Start with delay**

</td><td>

Specify a duration of time to wait before running an activity whose start rule and conditions have been met. For more information, see [Start with delay input properties](../reference/start-with-delay-properties.md).

</td></tr><tr><td id="d178165e310">

**Restart rules**

</td><td>

Choose what this activity does when a playbook is restarted:-   **Skip on restart**: Skip this activity when the run is due to a restart.
-   **Run always**: Always run this activity, including first runs.
-   **Skip on first run**: Skip this activity during the first run.
For more information, see [Configure restart for Playbooks](enable-define-restart.md).

</td></tr></tbody>
</table>3.  Open the **Automation** tab.

    Automation, inputs, and outputs sections appear.

    -   **Automation**

        See or open the action, subflow, or flow that drives the activity.

    -   **Inputs**

        Configure inputs for the action, subflow, or flow that is driving the activity. Not all activities require user input.

    -   **Outputs**

        Outputs of the action, subflow, or flow that is driving the activity.

4.  Under the **Inputs** section, define the values of the activity's inputs.

    Configure inputs with a hardcoded value, or by dot-walking to a data pill \(![Data pill picker icon](../images/data-pill-picker-icon.png)\) to use data from previous activities, the playbook trigger, from the playbook parent table, or from the playbook inputs.

    **Tip:** You can use both text and multiple pills in any other rich text or HTML input fields.

5.  Open the **UI Layout** tab.

    Depending on the UI Layout associated with the activity, different sections and fields appear under the activity definition's Activity Experience. These sections and fields let you set up the activity data that renders during the runtime Playbook Experience.

    **Note:** All UI Layouts, except for Record generator, display an Associated Record section. For information on how to set up or edit the Associated Record section in an activity definition, see [Create an activity definition](create-activity-definition.md).

6.  Specify if an AI Agent performs the activity, and how.

    To learn more, see [Configuring Agentic Playbooks](configure-agentic-playbooks.md).

7.  Click **Save and close** to save the details of your activity.

    At any point while in the Playbooks builder, you can add more activities to a stage as described in the previous steps.

8.  If the activity you want to add is not in the activity picker, create the activity definition.

    1.  Under your stage, click **+ Add activity**.

        The activity picker appears.

    2.  Click the **Create a new activity** button.

    3.  Fill in the following fields.

<table id="choicetable_cf4_jqb_g5b"><tbody><tr><td id="d178165e553">

**Label**

</td><td>

Enter a unique, user-facing name for your activity. This name appears to agents and fulfillers during runtime of your playbook.

</td></tr><tr><td id="d178165e565">

**Accessible From**

</td><td>

Where the activity is accessible from. Make the activity accessible to other applications by setting the **Accessible from** field to **All application scopes**. Restrict access by setting the field to **This Application Scope Only**.

</td></tr><tr><td id="d178165e583">

**Table**

</td><td>

Optionally, set to the table associated with the activity.

</td></tr><tr><td id="d178165e592">

**Application**

</td><td>

Read-only field that indicates which applications can use this activity.

</td></tr><tr><td id="d178165e601">

**Description**

</td><td>

Optionally, enter some descriptive details about your activity.

</td></tr><tr><td id="d178165e611">

**Automation Plan**

</td><td>

Select the subflow or action that you want to use to automate your activity.

</td></tr><tr><td id="d178165e620">

**Activity Experience**

</td><td>

Optionally, set the activity's experience type, which helps to define how the activity renders in user-facing views of a playbook card at runtime.

</td></tr></tbody>
</table>9.  Click **Submit** to finish creating your activity definition.

    Your activity is defined.


## What to do next

Set up the Playbook Experience for you agents and fulfillers.

**Parent Topic:**[Stages and activities](../concept/process-automation-designer-lanes-activities.md)

**Related topics**  


[Add and configure a stage in a playbook](add-configure-stage.md)

[Activity definitions](../concept/activity-definitions.md)

[Use AI agent as an activity](ai-agent-as-activity.md)

[Automation Assets](../concept/automation-assets.md)

[Start with delay input properties](../reference/start-with-delay-properties.md)

[Optional activities](../concept/optional-activities.md#)

[Decision activities](create-a-decision-activity.md)

[Decision stages](create-decision-stage.md)

[Questionnaire activity](../reference/questionnaire-activity.md)

[Parallel branches](create-parallel-activity.md)

[Add dynamic inputs to an activity](add-dynamic-inputs-to-activity.md)

[Playbook activity state mapping](../../workspace/concept/playbook-activity-state-mapping.md)

