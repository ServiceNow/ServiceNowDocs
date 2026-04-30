---
title: Checklist Task from Template activity
description: Prompt an agent to complete all items in a task checklist.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Interactive activities, Playbooks reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Checklist Task from Template activity

Prompt an agent to complete all items in a task checklist.

The key input for this activity is the **Checklist Template** field under the [Inputs](checklist-task-activity.md#table_cjj_sr3_plb) section. Before you can provide this input, you must:

-   [Create a checklist](https://www.servicenow.com/docs/access?context=t_CreateAChecklist&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US), and
-   [Create a checklist template for the target task table.](https://www.servicenow.com/docs/access?context=create-checklist-template&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

## Roles and availability

This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

## Common properties

These properties are common to all to activities in Playbooks.

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://www.servicenow.com/docs/access?context=dot-walking-examples&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

<table id="table_sym_wlm_d2c"><thead><tr><th>

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
</table>## Inputs

After configuring the required inputs for your activity, you can also choose to configure additional inputs. In the side panel, select **Show additional options** to display these advanced inputs. For more information, see [Activity experience](../concept/activity-definitions.md#activity-experience).

<table id="table_uym_wlm_d2c"><thead><tr><th>

Input

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Skip Assignment Group

</td><td>

Reference.Group \[sys\_user\_group\]

</td><td>

Group that is allowed to skip this activity when **Can Skip** is enabled.**Note:** If **Can Skip** is enabled, and you do not specify a **Skip Assignment Group**or **Skip Assigned To**, all users will be able to skip this activity.

</td></tr><tr><td>

Skip Assigned To

</td><td>

Reference.User \[sys\_user\]

</td><td>

User that is allowed to skip this activity when **Can Skip** is enabled.**Note:** If **Can Skip** is enabled, and you do not specify a **Skip Assignment Group**or **Skip Assigned To**, all users will be able to skip this activity.

</td></tr><tr><td>

Checklist Template

</td><td>

Reference.Checklist Template \[checklist\_template\]

</td><td>

Template for the checklist to create for each run. Before you can provide this input, you must:-   [Create a checklist](https://www.servicenow.com/docs/access?context=t_CreateAChecklist&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US), and
-   [Create a checklist template for Visual Task Board tasks](https://www.servicenow.com/docs/access?context=create-checklist-template&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

</td></tr><tr><td>

Task

</td><td>

Reference.Task \[task\]

</td><td>

Reference a record to associate with the checklist activity. The checklist is also displayed in the associated task record.

 **Note:** When a specific task record is associated with the checklist, the state of the checklist does not change if you run the playbook again. When you don't provide a specific task record, a new private task record is created for each run.

 ![Checklist in a task record](../images/checklist-task-record.png)

</td></tr><tr><td>

Show SLA

</td><td>

True/False

</td><td>

Option to show SLA countdown details for the task.**Note:** **Show additional options** to see this field.

</td></tr><tr><td>

Can Skip

</td><td>

True/False

</td><td>

Option to allow agents to skip the checklist and to continue through the playbook.

</td></tr></tbody>
</table>## Outputs

These outputs can provide data to other activities in your playbook. You can access this data as activity inputs when you configure your activity:

|Output|Type|Description|
|------|----|-----------|
|Checklist Task|Reference.Task \[task\]|Task record that updates when this activity completes.|

## UI Layouts

Set properties for how the activity renders during a playbook run.

**Parent Topic:**[Interactive activities](../concept/interactive-activities.md)

