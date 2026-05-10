---
title: Microsoft Teams activities
description: Enable agents and fulfillers to send direct messages and post in Microsoft Teams channels during a playbook run, via Workflow Data Fabric's Microsoft Teams spoke.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Interactive activities, Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Microsoft Teams activities

Enable agents and fulfillers to send direct messages and post in Microsoft Teams channels during a playbook run, via Workflow Data Fabric's Microsoft Teams spoke.

## Roles and availability

-   These activities are available as an application in the ServiceNow Store. Users with the playbook.admin or pd\_author role can add these activities to a playbook.
-   You must have access to Workflow Data Fabric's Microsoft Teams spoke.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/dot-walking-examples.md).

<table id="table_zlc_4nc_35b"><thead><tr><th>

Input

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="activity-input-label"><td>

Label

</td><td>

String

</td><td>

Title to display as activity and playbook card.

</td></tr><tr id="activity-input-description"><td>

Description

</td><td>

String

</td><td>

Information to display about activity usage or outcome.

</td></tr><tr id="activity-input-condition-to-run"><td>

Condition to run

</td><td>

Condition Builder

</td><td>

Criteria that must be met to run the activity. You can use the output data from prior activities to build the conditions to run this activity.

</td></tr><tr id="activity-input-when-to-start"><td>

When to start

</td><td>

Choice

</td><td>

Option to specify when the activity runs. Options include-   With Previous - the activity runs at the same time as the previous activity
-   After Previous - the activity only runs after the previous activity completes running
-   Immediately - the activity runs immediately without waiting for other activities

</td></tr><tr><td>

Start with delay

</td><td>

True/False

</td><td>

Option to wait for a duration of time before running an activity or stage. When enabled, this input displays the [Start with delay input properties](start-with-delay-properties.md).**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Chat type

</td><td>

Choice

</td><td>

Choose whether to post to a Microsoft Teams channel or direct message.

</td></tr><tr><td>

Message

</td><td>

String

</td><td>

Message text to display to end users.

</td></tr><tr><td>

Team ID

</td><td>

String

</td><td>

Sender of the Microsoft Teams message.

</td></tr><tr><td>

Channel name

</td><td>

String

</td><td>

Microsoft Teams channel that the message is posted in.

</td></tr><tr><td>

To members

</td><td>

String

</td><td>

Microsoft Teams user that the message is sent to.

</td></tr></tbody>
</table>## Outputs

Your message posted in a Microsoft Teams channel or sent as a direct message.

