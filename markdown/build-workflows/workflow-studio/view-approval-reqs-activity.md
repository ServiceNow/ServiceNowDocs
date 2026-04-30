---
title: View Approval Requests activity
description: Display a list of approval requests from within Playbook Experience.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Interactive activities, Playbooks reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# View Approval Requests activity

Display a list of approval requests from within Playbook Experience.

## Roles and availability

These activities are available as an application in the ServiceNow Store. Users with the playbook.admin or pd\_author role can add these activities to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://www.servicenow.com/docs/access?context=dot-walking-examples&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

<table id="table_zyd_zdk_35b"><thead><tr><th>

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

Table

</td><td>

Choice

</td><td>

Table that you want to choose the approval requests from.

</td></tr><tr><td>

Conditions

</td><td>

Condition Builder

</td><td>

Criteria that you want your list of approval requests to meet.

</td></tr></tbody>
</table>## Advanced Inputs

After configuring the required inputs for your activity, you can also choose to configure additional inputs. In the side panel, select **Show additional options** to display these advanced inputs. For more information, see [Activity experience](../concept/activity-definitions.md#activity-experience).

|Input|Type|Description|
|-----|----|-----------|
|Order by|String|Field you want to use to sort a list of records.|
|Sort Type|Choice|Option to sort records alphabetically or reverse alphabetically.|
|Max Results|Integer|Maximum number of results to display to end users.|

**Parent Topic:**[Interactive activities](../concept/interactive-activities.md)

