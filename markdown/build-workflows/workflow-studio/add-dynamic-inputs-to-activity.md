---
title: Add dynamic inputs to an activity
description: Configure your activity to show a certain set of fields based on the value of another input, such as a selected catalog item, selected decision table, or even a REST API response.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Add dynamic inputs to an activity

Configure your activity to show a certain set of fields based on the value of another input, such as a selected catalog item, selected decision table, or even a REST API response.

## Before you begin

Role required: playbook.admin, pd\_author, action\_designer, flow\_designer, admin

Familiarize yourself with the other Workflow Studio components. [Dynamic inputs](../../flow-designer/task/getting-started-dynamic-input.md#) are created with actions and subflows:

1.  In the ServiceNow AI Platform, you will create a new data definition for the dynamic input fields you want to add to an activity.
2.  In Workflow Studio, you will create a data gathering action.
3.  Still in Workflow Studio, you will create a subflow or another action with a dynamic input to consume the first action. This subflow or new action creates a JSON schema that represents the field\(s\) you want to add to an activity.
4.  In the ServiceNow AI Platform, you will create an activity definition using the subflow or action with the dynamic input.

Once your activity definition is created, Playbooks authors can add and configure activities with the dynamic inputs.

## About this task

A dynamic input is an input that changes based on another input. In Workflow Studio Playbooks, you can present multiple dynamic inputs based on another input.

## Example

When a user requests catalog items, you can dynamically present a list of catalog variables based on the selected catalog item.

1.  The first input required is for the Catalog Item field.

    ![Input for a Catalog Item](../images/playbook-dynamic-inputs-1.png)

2.  A user selects **iPad mini** in the Catalog item field.

    ![A user selecting iPad mini as the Catalog item](../images/playbook-dynamic-inputs-2.png)

3.  Two \(2\) additional fields for color and storage options appear in response to the user selecting an iPad mini as the Catalog Item.

    ![Two additional fields for color and storage options appear](../images/playbook-dynamic-inputs-3.png)


## Procedure

1.  Navigate to **All** &gt; **Workflow Studio** and select **Actions**.

2.  [Create an action to add an input.](../../flow-designer/task/create-data-gathering-action-dynamic-inputs.md)

    The input appears under the **Script step** &gt; **Input Variables** section. The JSON under the **Script** section should include the new input.

3.  In the **Outputs** section, click **Edit Outputs** to make sure that the value of the **Name** field is **output**, and that **JSON** is the selected in the **Type** drop-down field.

4.  [Create a subflow](../../flow-designer/task/create-subflow.md) with the new input.

5.  Navigate to **All** &gt; **Process Automation Administration** &gt; **Activity Definitions**.

6.  Open or [create the activity definition](create-activity-definition.md) to add the new input to.

7.  Under the **Automation Plan** tab, make sure the action or flow you created with the new input is the underlying **Flow or Action**, and that the new input appears in the **Variables** section.

8.  Change the visibility of the new input from **Show as additional property** to **Always show**.

9.  Save your changes.

    Once your activity definition is created, Playbooks authors can add and configure activities with the dynamic inputs.


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

[Decision stages](create-decision-stage.md)

[Questionnaire activity](../reference/questionnaire-activity.md)

[Parallel branches](create-parallel-activity.md)

[Playbook activity state mapping](../../workspace/concept/playbook-activity-state-mapping.md)

