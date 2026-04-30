---
title: Create Task activity
description: Create a task record from previously gathered or generated data.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Playbooks reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Create Task activity

Create a task record from previously gathered or generated data.

## Roles and availability

This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://www.servicenow.com/docs/access?context=dot-walking-examples&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

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

</td></tr><tr><td>

Assigned To

</td><td>

Reference.User \[sys\_user\]

</td><td>

User responsible for completing the task associated with the activity.**Note:** **Show additional options** to see this field.

</td></tr><tr><td>

Short Description

</td><td>

String

</td><td>

Summary of the task to complete.

</td></tr><tr><td>

Wait for user input

</td><td>

Choice

</td><td id="wait-process">

Option to pause the playbook until the end user manually completes or skips the activity. Only users with the playbook.admin role can edit this field. By default, the activity waits for user action or data before it completes.

</td></tr></tbody>
</table>## Advanced inputs

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

Task Table

</td><td>

Table Name

</td><td>

Name of the task table extension in which you want to create a task.

</td></tr><tr><td>

Add Field

</td><td>

Template Value

</td><td>

Field values to assign when creating the task record.

</td></tr><tr><td>

Fields to show after creation

</td><td>

String

</td><td>

Comma-separated list of fields to display for a created record.

</td></tr><tr><td>

Wait for Task completion

</td><td>

True/False

</td><td>

Pause the playbook until the created Task record is complete.

</td></tr></tbody>
</table>## Outputs

These outputs can provide data to other activities in your playbook. You can access this data as activity inputs when you configure your activity:

|Output|Type|Description|
|------|----|-----------|
|Table|Table Name|Table containing new record.|
|Record|Reference.Task\[task\]|Reference to record created.|

**Parent Topic:**[Playbooks reference](process-automation-designer-reference.md)

