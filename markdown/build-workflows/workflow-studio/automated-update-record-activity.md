---
title: Automated Update Record activity
description: Update a record without pausing the playbook to ask for user input. When the activity runs, it immediately updates the record and continues to the next activity in the playbook. The record must meet server-side validation rules such as data policies, business rules and dictionary-defined mandatory fields but ignores UI policies.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Non-Interactive activities, Playbooks reference, Reference, Workflow Studio, Build workflows]
---

# Automated Update Record activity

Update a record without pausing the playbook to ask for user input. When the activity runs, it immediately updates the record and continues to the next activity in the playbook. The record must meet server-side validation rules such as data policies, business rules and dictionary-defined mandatory fields but ignores UI policies.

## Roles and availability

-   This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://www.servicenow.com/docs/access?context=dot-walking-examples&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

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

</td></tr><tr><td>

Record

</td><td>

Reference

</td><td>

Reference to the record you want to update.

</td></tr><tr><td>

Table

</td><td>

Table Name

</td><td>

Table containing the record to update.

</td></tr><tr><td>

Fields

</td><td>

Template Value

</td><td>

Field values to change during record update.

</td></tr></tbody>
</table>## Outputs

These outputs can provide data to other activities in your playbook. You can access this data as activity inputs when you configure your activity:

|Output|Type|Description|
|------|----|-----------|
|Table|Table Name|Table containing updated record.|
|Record|Reference.Task\[task\]|Reference to record updated.|

**Parent Topic:**[Non-Interactive activities](../concept/non-interactive-activities.md)

