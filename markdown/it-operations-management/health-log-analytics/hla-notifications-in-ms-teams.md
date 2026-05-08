---
title: Set up Health Log Analytics alert notifications in a Microsoft Teams channel
description: Set up notifications for new Health Log Analytics anomaly alerts in a Microsoft Teams channel.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Receive alert notification in Slack or Microsoft Teams channels, Administer HLA, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up Health Log Analytics alert notifications in a Microsoft Teams channel

Set up notifications for new Health Log Analytics anomaly alerts in a Microsoft Teams channel.

## Before you begin

Starting with Version 33.0.27 - August 2024, Health Log Analytics uses the Microsoft Teams Graph spoke application to send notifications on new anomaly alerts. For more information, see Microsoft Teams Graph Spoke. If you're using an HLA version earlier than 33.0.27, refer to the setup procedure in [Set up Health Log Analytics alert notifications in channels](hla-notifications-in-channel.md).

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## Procedure

1.  Install the latest version of the Microsoft Teams Graph spoke from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

2.  Set up the Microsoft Teams Graph spoke.

    For instructions, see: Set up the.

3.  Activate the Health Log Analytics Alert Management rule for submitting alerts to the Microsoft Teams channel.

    1.  Navigate to **Event Management** &gt; **Rules** &gt; **Alert Management Rules**.

    2.  Locate the appropriate rule: Submit HLA alerts to teams.

    3.  In the **Active** column for the rule, set the value to `true`.

4.  Map the service instance to the Microsoft Teams channel.

    1.  In the **All** navigation menu, type `sn_occ_teams_alert_notification_config` and then press Enter.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        **Note:**

        -   You can obtain the Teams ID and Channel ID from the Microsoft Teams channel.
        -   The **Configuration Item** field must correspond to the Service instance. If no CI is needed, leave this field empty. In this case, the record is used for alerts when there's no record that matches their CI.
    4.  Select **Submit**.

    5.  Repeat steps 1 to 4 to add additional configurations.


**Parent Topic:**[Health Log Analytics alert notification in Slack or Microsoft Teams channels](../concept/hla-alert-notification-in-channel.md)

