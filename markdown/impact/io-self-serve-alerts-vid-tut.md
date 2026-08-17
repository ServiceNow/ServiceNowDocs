---
title: Configure notifications in IO
description: Configure notifications and alerts to monitor your Instance Observer instance and receive alerts when specified conditions are met.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-self-serve-alerts-vid-tut.html
release: australia
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 2
breadcrumb: [Key alerts and notifications, Use alerts to monitor your instance, Monitor instance performance, Platform Health, Using Impact, Impact]
---

# Configure notifications in IO

Configure notifications and alerts to monitor your Instance Observer instance and receive alerts when specified conditions are met.

## Before you begin

Role required: admin

## About this task

Use this procedure to set up self-serve alerts that notify you when specific conditions occur on your Instance Observer instance. By configuring notification rules and alert criteria, you can monitor instance health proactively and ensure that the right people receive alerts through their preferred channels. The configuration process takes approximately 10-15 minutes.

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Monitor**.

2.  Log in to **Instance Observer** and navigate to **Alerts** &gt; **Configuration Notification**.

    This tab displays how many notification rules you have and also allows you to create notification rules. These rules notify you when an alert is triggered, determine who receives alerts, and through which communication channels.

3.  Select **Create Rule** to create a notification rule.

4.  On the form, fill in the fields.

<table id="table_zlm_fvk_vjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the notification rule.For example, Database Performance Alerts or Critical Instance Issues.

</td></tr><tr><td>

Description

</td><td>

Description explaining when this notification rule triggers and who should receive the alerts.

</td></tr><tr><td>

Notification Type

</td><td>

Notification channel for the notification type.-   Advanced customers can receive Email notification only.
-   Total customers can receive Email, SMS, ServiceNow, and third-party notifications.
Your available options depend on your impact tier. For more information, see Impact Benefits page in the Impact Portal.

</td></tr><tr><td>

All provisioned users

</td><td>

Option for all users who have access to Instance Observer to be notified when the alert triggers.

</td></tr><tr><td>

ServiceNow Otto for SAM

</td><td>

Option to be notified ifServiceNow Otto for SAM is affiliated with your account.

</td></tr><tr><td>

Add customer recipients

</td><td>

Option to enter custom email addresses for email notification.

</td></tr><tr><td>

SMS

</td><td>

SMS to **All provisioned users** and **Specific Users**. If you select specific users, you can add their telephone numbers.

</td></tr><tr><td>

ServiceNow

</td><td>

Option to utilize the ServiceNow implementation webhook to initiate a workflow on a specific instance.

</td></tr><tr><td>

Webhook

</td><td>

Option to integrate Instance Observer with a third-party monitoring tool.

</td></tr></tbody>
</table>    You can add multiple notification alerts which can be set as enabled default, or turned off entirely.

    **Note:** You must configure a notification first otherwise you won't be able to create an alert. For alerts must be tied to a notification.


## What to do next

[Set notifications for configured key alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configuring-io-alerts.md)

**Parent Topic:**[Key alerts and notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/io-alerts.md)

