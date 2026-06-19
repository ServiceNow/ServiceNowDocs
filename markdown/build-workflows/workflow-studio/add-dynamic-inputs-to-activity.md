---
title: Add dynamic inputs to an activity
description: Configure your activity to show a certain set of fields based on the value of another input, such as a selected catalog item, selected decision table, or even a REST API response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/add-dynamic-inputs-to-activity.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Add dynamic inputs to an activity

Configure your activity to show a certain set of fields based on the value of another input, such as a selected catalog item, selected decision table, or even a REST API response.

## Before you begin

Role required: playbook.admin, pd\_author, action\_designer, flow\_designer, admin

Familiarize yourself with the other Workflow Studio components. [Dynamic inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/getting-started-dynamic-input.md) are created with actions and subflows:

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

    \[Omitted image "playbook-dynamic-inputs-1.png"\] Alt text: Input for a Catalog Item

2.  A user selects **iPad mini** in the Catalog item field.

    \[Omitted image "playbook-dynamic-inputs-2.png"\] Alt text: A user selecting iPad mini as the Catalog item

3.  Two \(2\) additional fields for color and storage options appear in response to the user selecting an iPad mini as the Catalog Item.

    \[Omitted image "playbook-dynamic-inputs-3.png"\] Alt text: Two additional fields for color and storage options appear


## Procedure

1.  Navigate to **All** &gt; **Workflow Studio** and select **Actions**.

2.  [Create an action to add an input.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-data-gathering-action-dynamic-inputs.md)

    The input appears under the **Script step** &gt; **Input Variables** section. The JSON under the **Script** section should include the new input.

3.  In the **Outputs** section, click **Edit Outputs** to make sure that the value of the **Name** field is **output**, and that **JSON** is the selected in the **Type** drop-down field.

4.  [Create a subflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-subflow.md) with the new input.

5.  Navigate to **All** &gt; **Process Automation Administration** &gt; **Activity Definitions**.

6.  Open or [create the activity definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-activity-definition.md) to add the new input to.

7.  Under the **Automation Plan** tab, make sure the action or flow you created with the new input is the underlying **Flow or Action**, and that the new input appears in the **Variables** section.

8.  Change the visibility of the new input from **Show as additional property** to **Always show**.

9.  Save your changes.

    Once your activity definition is created, Playbooks authors can add and configure activities with the dynamic inputs.


**Parent Topic:**[Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md)

