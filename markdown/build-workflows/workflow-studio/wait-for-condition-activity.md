---
title: Wait For Condition activity
description: Pause the playbook until a record has field values that match a set of conditions.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Interactive activities, Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Wait For Condition activity

Pause the playbook until a record has field values that match a set of conditions.

## Roles and availability

-   This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/dot-walking-examples.md).

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

Reference to the record that pauses the playbook until conditions match.

</td></tr><tr><td>

Table

</td><td>

Table Name

</td><td>

Table containing the record to update.

</td></tr><tr><td>

Conditions

</td><td>

Template Value

</td><td>

Criteria that a record must meet for the playbook to continue.

</td></tr></tbody>
</table>## Advanced inputs

After configuring the required inputs for your activity, you can also choose to configure additional inputs. In the side panel, select **Show additional options** to display these advanced inputs. For more information, see [Activity experience](../concept/activity-definitions.md#activity-experience).

|Input|Type|Description|
|-----|----|-----------|
|Enable timeout|Choice|Option to time out the Wait for Condition activity if the conditions aren't met after a specified Duration.|
|Duration|Date/Time|Amount of time to wait before the activity times out and its state is set to Skipped. This input requires setting the Enable timeout input.|
|Schedule|Choice|Schedule used to compute duration values. This input requires setting the Enable timeout input.|

## Outputs

The Wait for Condition activity has no outputs.

