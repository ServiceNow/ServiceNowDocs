---
title: Make a Decision-First Match activity
description: Execute rules in a decision table. When this activity runs, it will immediately finish and continue the process execution. The activity returns the result of the first matching decision rule, based on the rank of the rules. To return results from all matching rules, add the decision table to a subflow.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Non-Interactive activities, Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Make a Decision-First Match activity

Execute rules in a decision table. When this activity runs, it will immediately finish and continue the process execution. The activity returns the result of the first matching decision rule, based on the rank of the rules. To return results from all matching rules, add the decision table to a subflow.

## Roles and availability

This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/dot-walking-examples.md).

**Note:** You must select the decision table to run. Any additional inputs and outputs are dynamic based on the decision table.

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

Table Name

</td><td>

Table Name

</td><td>

Table in which you want to create a new record.

</td></tr><tr><td>

Fields

</td><td>

Template Value

</td><td>

Field values to set during record creation.

</td></tr></tbody>
</table>## Outputs

These outputs can provide data to other activities in your playbook. You can access this data as activity inputs when you configure your activity:

|Output|Type|Description|
|------|----|-----------|
|Table Name|Table Name|Table containing new record.|
|Record|Reference.Task \[task\]|Reference to record created.|

