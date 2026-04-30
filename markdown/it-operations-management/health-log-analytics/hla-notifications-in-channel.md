---
title: Set up Health Log Analytics alert notifications in channels
description: Set up notifications for new Health Log Analytics anomaly alerts in either a Slack or Microsoft Teams channel.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Receive alert notification in Slack or Microsoft Teams channels, Administer HLA, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up Health Log Analytics alert notifications in channels

Set up notifications for new Health Log Analytics anomaly alerts in either a Slack or Microsoft Teams channel.

## Before you begin

Starting with Version 33.0.27 - August 2024, Health Log Analytics uses the Microsoft Teams Graph spoke application to send notifications for new anomaly alerts. The new application replaces the Microsoft Teams spoke plugin, which will be deprecated. If you're using an HLA version earlier than 33.0.27, follow the setup procedure below. Otherwise, refer to [Set up Health Log Analytics alert notifications in a Microsoft Teams channel](hla-notifications-in-ms-teams.md).

**Note:** If you upgrade from an earlier version to Version 33.0.27 - August 2024 or later, redo the setup using the procedure in [Set up Health Log Analytics alert notifications in a Microsoft Teams channel](hla-notifications-in-ms-teams.md).

For alert notifications in Slack channels, verify that the plugin Slack Webhooks Spoke for ServiceNow Integration Hub \(com.sn.slack.ah\) is installed:

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.
2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel. For more information, see [Request a plugin](https://www.servicenow.com/docs/access?context=t_RequestAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).


Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## Procedure

1.  Create a Webhook URL for a channel in Slack or Microsoft Teams.

    Health Log Analytics uses the Webhook to notify about the alerts in the channel.

    Perform the appropriate procedure:

    -   Create a Webhook URL for a channel in Slack
    -   Create a Webhook URL for a channel in Microsoft Teams
2.  Map the Webhook URL for the channel to the service instance associated with the alert.

    1.  Navigate to **Health Log Analytics Administration** &gt; **Webhook Notification**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

<table id="table_pwk_njy_xtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Webhook

</td><td>

The Webhook URL that you created for the channel.

</td></tr><tr><td>

Active

</td><td>

Select to activate the Webhook.

</td></tr><tr><td>

Configuration item

</td><td>

The service instance associated with the alert.If this field is empty, the system uses the default property for the channel: default.slack.webhook.url for Slack or default.teams.webhook.url for Microsoft Teams.

</td></tr></tbody>
</table>    4.  Select **Submit**.

3.  Activate the Health Log Analytics Alert Management rule for submitting alerts to the appropriate channel.

    1.  Navigate to **Event Management** &gt; **Rules** &gt; **Alert Management Rules**.

    2.  Locate the appropriate rule:

        -   For Slack: Submit HLA alerts to slack.
        -   For Microsoft Teams: Submit HLA alerts to teams.
    3.  In the **Active** column for the rule, set the value to `true`.

4.  Filter the alerts on which notifications will be sent to the channel.

    1.  In the Alert Management Rules table, select the rule for your channel.

    2.  Select **Alert Filter**.

    3.  On the form, set the conditions that must be met for sending a notification on the alert to the channel.

    4.  Select **Update**.


**Parent Topic:**[Health Log Analytics alert notification in Slack or Microsoft Teams channels](../concept/hla-alert-notification-in-channel.md)

