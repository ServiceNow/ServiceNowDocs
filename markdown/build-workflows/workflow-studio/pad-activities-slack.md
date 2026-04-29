---
title: Slack activities
description: Enable agents and fulfillers to send direct messages and post in Slack channels during a playbook run, via Workflow Data Fabric's Slack spoke.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Interactive activities, Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Slack activities

Enable agents and fulfillers to send direct messages and post in Slack channels during a playbook run, via Workflow Data Fabric's Slack spoke.

## Roles and availability

-   These activities are available as an application in the ServiceNow Store. Users with the playbook.admin or pd\_author role can add these activities to a playbook.
-   You must have access to Workflow Data Fabric's Slack spoke.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://www.servicenow.com/docs/access?context=dot-walking-examples&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

<table id="table_qcb_5jc_35b"><thead><tr><th>

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

</td></tr><tr id="activity-input-channel-member-id"><td>

Channel/Member ID

</td><td>

String

</td><td>

Slack channel or member that the message is sent to.

</td></tr><tr><td>

Message

</td><td>

String

</td><td>

Message text to display to end users.

</td></tr><tr id="activity-input-username"><td>

Blocks

</td><td>

String

</td><td>

Code blocks to include in the message to end users.

</td></tr><tr><td>

Username

</td><td>

String

</td><td>

Sender of the Slack message.

</td></tr><tr id="activity-input-icon"><td>

Icon

</td><td>

String

</td><td>

Slack user profile icon of the sender.

</td></tr><tr><td>

Collect data from user

</td><td>

True/False

</td><td>

Option to pause the playbook until the end user manually completes or skips the activity. Only users with the playbook.admin role can edit this field. By default, the activity waits for user action or data before it completes.

</td></tr></tbody>
</table>## Outputs

Your message posted in a Slack channel or sent as a direct message.

