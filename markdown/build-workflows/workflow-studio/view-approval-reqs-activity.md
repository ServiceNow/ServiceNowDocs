---
title: View Approval Requests activity
description: Display a list of approval requests from within Playbook Experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/view-approval-reqs-activity.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Interactive activities, Playbooks reference, Reference, Workflow Studio, Build workflows]
---

# View Approval Requests activity

Display a list of approval requests from within Playbook Experience.

## Roles and availability

Users with the playbook.admin or pd\_author role can add these activities to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/dot-walking-examples.md).

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

Conditions that must be met to run an activity or stage. You can use data from prior activities to build conditions.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Start Rule

</td><td>

Choice

</td><td>

Under **Schedule** &gt; **Start Rule**, select a start rule for when the activity should start running:-   **When stage starts**: The activity starts running as soon as its stage starts running.
-   **After specific activities**: The activity starts running after specified activities have finished running. You can select one more activities from the available activities. By default, the previous activity is selected.

</td></tr><tr><td>

Start with delay

</td><td>

True/False

</td><td>

Option to wait for a duration of time before running an activity or stage. When enabled, this input displays the [Start with delay input properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/start-with-delay-properties.md).**Note:** Select **Show additional options** to see this field.

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

After configuring the required inputs for your activity, you can also choose to configure additional inputs. In the side panel, select **Show additional options** to display these advanced inputs. For more information, see [Activity experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/activity-definitions.md).

|Input|Type|Description|
|-----|----|-----------|
|Order by|String|Field you want to use to sort a list of records.|
|Sort Type|Choice|Option to sort records alphabetically or reverse alphabetically.|
|Max Results|Integer|Maximum number of results to display to end users.|

**Parent Topic:**[Interactive activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/interactive-activities.md)

