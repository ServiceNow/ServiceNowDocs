---
title: Request Manager Approval activity
description: Enable agents and fulfillers to submit an approval request to a manager during a playbook run.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Interactive activities, Playbooks reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Request Manager Approval activity

Enable agents and fulfillers to submit an approval request to a manager during a playbook run.

## Roles and availability

These activities are available as an application in the ServiceNow Store. Users with the playbook.admin or pd\_author role can add these activities to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://www.servicenow.com/docs/access?context=dot-walking-examples&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

<table id="table_ibc_1bk_35b"><thead><tr><th>

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

Table name

</td><td>

Choice

</td><td>

Table that you want to choose the associated record from.

</td></tr><tr><td>

Record

</td><td>

Choice

</td><td>

Associated record for the approval request.

</td></tr><tr><td>

Approver

</td><td>

Choice

</td><td>

Individual user that will receive approval requests.

</td></tr><tr><td>

Due date

</td><td>

Date/Time

</td><td>

Date the approval is due by.

</td></tr><tr><td>

Comments

</td><td>

String

</td><td>

Option for the approver to add comments in the approval request.

</td></tr></tbody>
</table>## Outputs

Record of your approval request.

**Parent Topic:**[Interactive activities](../concept/interactive-activities.md)

