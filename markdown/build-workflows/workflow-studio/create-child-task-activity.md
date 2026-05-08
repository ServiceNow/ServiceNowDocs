---
title: Create Child Task activity
description: Enable agents and fulfillers to create a child task during a playbook run.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Interactive activities, Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Create Child Task activity

Enable agents and fulfillers to create a child task during a playbook run.

## Roles and availability

These activities are available as an application in the ServiceNow Store. Users with the playbook.admin or pd\_author role can add these activities to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see Dot-walking examples.

<table id="table_kyw_4nj_35b"><thead><tr><th>

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

</td></tr><tr><td>

Parent

</td><td>

Choice

</td><td>

Parent record of the child task.

</td></tr><tr><td>

Assignment Group

</td><td>

Choice

</td><td>

User group that the child task is assigned to.

</td></tr><tr><td>

Assigned To

</td><td>

Choice

</td><td>

User that the child task is assigned to.

</td></tr><tr><td>

Short Description

</td><td>

String

</td><td>

Summary of the child task.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Detailed information to display about the child task.

</td></tr><tr><td>

Priority

</td><td>

Choice

</td><td>

Prioritization level of the child task.

</td></tr><tr><td>

Collect data from user

</td><td>

True/False

</td><td>

Option to pause the playbook until the end user manually completes or skips the activity. Only users with the playbook.admin role can edit this field. By default, the activity waits for user action or data before it completes.

</td></tr></tbody>
</table>## Outputs

Your child task record.

