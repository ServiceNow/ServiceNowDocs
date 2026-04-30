---
title: Questionnaire activity
description: Collects inputs from a user during a playbook run to use later in the playbook.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Stages and activities, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Questionnaire activity

Collects inputs from a user during a playbook run to use later in the playbook.

The questionnaire activity replaces the Collect User Data activity, but does not require you to create a data definition. Use the questionnaire activity if:

-   You don't have a table already,
-   You don't need to run reports on the collected data,
-   And you don't need to use the data outside of the playbook.

If you already have a table to store the collected data, use the [User Form activity](user-form-activity.md).

## Roles and availability

This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

During a playbook run, you can use data definitions to potentially:

-   Collect a shipping address, then reference the address when generating a shipping label.
-   Ask the user "yes" or "no" questions, and determine subsequent activities based on the user's responses.

## Common properties

These properties are common to all to activities in Playbooks.

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://www.servicenow.com/docs/access?context=dot-walking-examples&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

<table id="table_ajt_sr3_plb"><thead><tr><th>

Input

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

String

</td><td>

Title to display as activity and playbook card.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Information to display about activity usage or outcome.

</td></tr><tr><td>

Run condition

</td><td>

Condition Builder

</td><td>

Conditions that must be met to run an activity or stage. You can use data from prior activities to build conditions.**Note:** **Show additional options** to see this field.

</td></tr><tr><td>

Start Rule

</td><td>

Choice

</td><td>

Under **Schedule** &gt; **Start Rule**, select a start rule for when your stage should start running:-   **When process starts**: Your stage starts running as soon as the playbook starts.
-   **After specific stages**: Your stage starts running after specified stage\(s\) have finished running.

Under Schedule &gt; Start Rule, select a start rule for when your activity should start running:-   **When stage starts**: Your activity starts running as soon as its stage starts running. Your stage starts running when your playbook is triggered.
-   **After specific activities**: Your activity starts running after specified activities have finished running.

</td></tr><tr><td>

Start with delay

</td><td>

True/False

</td><td>

Option to wait for a duration of time before running an activity or stage. When enabled, this input displays the [Start with delay input properties](start-with-delay-properties.md).**Note:** **Show additional options** to see this field.

</td></tr></tbody>
</table>## Questionnaire

In the **Questionnaire** tab, you can:

-   Add questions for agents to respond to,
-   Edit existing questionnaires.

To learn more about adding or configuring questions, see [Create a new questionnaire](../task/create-questionnaire.md).

## Inputs

Many of these inputs are common to activities in Playbooks.

After configuring the required inputs for your activity, you can also choose to configure additional inputs. In the side panel, select **Show additional options** to display these advanced inputs. For more information, see [Activity experience](../concept/activity-definitions.md#activity-experience).

<table><thead><tr><th>

Input

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment Group for this Process Step

</td><td>

Reference.Group \[sys\_user\_group\]

</td><td>

Assignment group allowed to perform this playbook activity. If you don't set any values for **Assignment Group** or **Assigned To**, any user can read and edit the collected data. The Assignment group and Assigned to fields limit who has access to do so. To specify only individual users, use the **Assigned To** field. The same users do not need to be specified in both fields.**Note:** By default, these fields are mapped to the **Assignment Group** and **Assigned To** fields of the trigger record. This means that users assigned to work on the parent record have access to submit, view and edit the collected data by default.

</td></tr><tr><td>

Assigned to this Process Step

</td><td>

Reference.User \[sys\_user\]

</td><td>

User allowed to perform this playbook activity. If you don't set any values for **Assignment Group** or **Assigned To**, any user can read and edit the collected data. The Assignment group and Assigned to fields limit who has access to do so. To specify only individual users, use the **Assigned To** field. The same users do not need to be specified in both fields.**Note:** By default, these fields are mapped to the **Assignment Group** and **Assigned To** fields of the trigger record. This means that users assigned to work on the parent record have access to submit, view and edit the collected data by default.

</td></tr></tbody>
</table>## Outputs

These outputs can provide data to other activities in your playbook. You can access this data as activity inputs when you configure your activity:

|Output|Type|Description|
|------|----|-----------|
|Record|Reference.Flow Data|Reference to record containing collected data. Use the pill-picker to dot-walk to **Outputs** &gt; **Record** &gt; **Vars** to see all collected data. To learn more about the pill-picker, see [Dot-walking examples](https://www.servicenow.com/docs/access?context=dot-walking-examples&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).|

-   **[Create a questionnaire](../task/create-questionnaire.md)**  
Create and insert a new questionnaire for agents to respond to.

**Parent Topic:**[Stages and activities](../concept/process-automation-designer-lanes-activities.md)

**Related topics**  


[Add and configure a stage in a playbook](../task/add-configure-stage.md)

[Activity definitions](../concept/activity-definitions.md)

[Add and configure an activity in a playbook](../task/add-configure-activity.md)

[Automation Assets](../concept/automation-assets.md)

[Start with delay input properties](start-with-delay-properties.md)

[Optional activities](../concept/optional-activities.md#)

[Decision activities](../task/create-a-decision-activity.md)

[Parallel branches](../task/create-parallel-activity.md)

[Add dynamic inputs to an activity](../task/add-dynamic-inputs-to-activity.md)

