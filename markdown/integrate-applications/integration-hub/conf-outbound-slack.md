---
title: Configure outbound configurations in ServiceNow instance
description: Specify events in ServiceNow instance for which actions must be performed on your Slack spoke application.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up Slack spoke, Slack Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Configure outbound configurations in ServiceNow instance

Specify events in ServiceNow instance for which actions must be performed on your Slack spoke application.

## Before you begin

Role required: admin

## About this task

The outbound configurations provide a template to the Post Actionable Message and Post Approval Message actions and subflows. You can customise the default outbound configurations or create outbound configuration as per your requirement.

## Procedure

1.  Navigate to **All** &gt; **Slack** &gt; **Outbound Configurations**.

2.  Click **New** to create a outbound configuration template or click the default outbound configuration to configure it.

3.  On the Outbound Configuration form, fill these values.

<table id="table_kzl_yh4_3mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the outbound configuration record.

</td></tr><tr><td>

Message Title

</td><td>

Title of message that is posted in the Slack spoke channel. For example, `Pending approvals for {0}`.

</td></tr><tr><td>

Target Table

</td><td>

ServiceNow table from which the record details are retrieved.

</td></tr><tr><td>

Fields

</td><td>

Fields from the ServiceNow table whose values must be displayed in the message that is posted in the Slack spoke channel.

</td></tr><tr><td>

Buttons

</td><td>

Buttons for the relevant users to take action in the Slack spoke channel. For example, **Approve** or **Reject** a request. For more information about buttons and their styling, see [Button element](https://api.slack.com/reference/block-kit/block-elements#button).**Note:** Users must have the required permissions to perform the necessary actions. For example, user must have the required permissions to approve or reject a request. These permissions are based on user roles assigned to users in your ServiceNow instance.

</td></tr><tr><td>

Choice List

</td><td>

Slack outbound choices such as, Reject. These options are displayed as a list in the Slack channel.

</td></tr><tr><td>

Action ID

</td><td>

Unique identifier of the outbound configuration.**Note:** **Action ID** of the outbound configuration must be used in the relevant inbound decision to complete the flow. For example, **Action ID** of the Approval Message outbound configuration is provided in the Approval Decision inbound decision. This ensures that upon the request approval or rejection, update is made to the relevant record in your ServiceNow instance.

</td></tr></tbody>
</table>4.  Click **Submit**.


