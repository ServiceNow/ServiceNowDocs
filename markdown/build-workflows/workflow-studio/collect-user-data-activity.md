---
title: Collect User Data activity
description: Collects inputs from a user during a playbook run to use later in the playbook.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Interactive activities, Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Collect User Data activity

Collects inputs from a user during a playbook run to use later in the playbook.

**Important:** As of the 26.1 release, the **Collect user data** activity is no longer available in the activity picker. The activity will continue to function wherever it is used, but for new activities use the **Questionnaire** activity instead. The **Questionnaire** activity does not require you to create a data definition. To learn more about the **Questionnaire** activity, see [Questionnaire activity](questionnaire-activity.md).

Use the Collect User Data activity if:

-   You don't have a table already,
-   You don't need to run reports on the collected data,
-   And you don't need to use the data outside of the playbook.

If you already have a table to store the collected data, use the [User Form activity](user-form-activity.md).

The key input for this activity is the **User form for data collection** field, under the [Inputs](collect-user-data-activity.md#collect-user-data_inputs) section. To provide this input, you must [create a data definition](../task/create-data-definition.md) first.

## Roles and availability

This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

During a playbook run, you can use data definitions to potentially:

-   Collect a shipping address, then reference the address when generating a shipping label.
-   Ask the user "yes" or "no" questions, and determine subsequent activities based on the user's responses.

## Common properties

These properties are common to all to activities in Playbooks.

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see Dot-walking examples.

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

Conditions that must be met to run an activity or stage. You can use data from prior activities to build conditions.**Note:** Select **Show additional options** to see this field.

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

Option to wait for a duration of time before running an activity or stage. When enabled, this input displays the [Start with delay input properties](start-with-delay-properties.md).**Note:** Select **Show additional options** to see this field.

</td></tr></tbody>
</table>## Inputs

Many of these inputs are common to activities in Playbooks. The key input for this activity is **User form for data collection** field.

After configuring the required inputs for your activity, you can also choose to configure additional inputs. In the side panel, select **Show additional options** to display these advanced inputs. For more information, see [Activity experience](../concept/activity-definitions.md#activity-experience).

<table id="table_cjj_sr3_plb"><thead><tr><th>

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

</td></tr><tr><td>

User form for data collection

</td><td>

Choice

</td><td>

Type of input form used to collect data. Playbook authors define the data that they want agents or fulfillers to collect during a playbook run in the `sys_flow_data_definition` table. When the information is collected, it is stored in the `sys_flow_data` table for use later in the playbook run, instead of in the record table. To define the data you want an agent or fulfiller to collect, see [Create a Data Definition](../task/create-data-definition.md).

</td></tr><tr><td>

Wait for user input

</td><td>

Choice

</td><td id="wait-process">

Option to pause the playbook until the end user manually completes or skips the activity. Only users with the playbook.admin role can edit this field. By default, the activity waits for user action or data before it completes.

</td></tr></tbody>
</table>## Outputs

These outputs can provide data to other activities in your playbook. You can access this data as activity inputs when you configure your activity:

|Output|Type|Description|
|------|----|-----------|
|Record|Reference.Flow Data|Reference to record containing collected data. Use the pill-picker to dot-walk to **Outputs** &gt; **Record** &gt; **Vars** to see all collected data. To learn more about the pill-picker, see Dot-walking examples.|

## UI Layouts

Set properties for how the activity renders during a playbook run.

