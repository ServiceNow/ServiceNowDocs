---
title: Track instance performance with the top six timely alerts – Guided users
description: Use the Instance Observer alerting feature to receive notifications on the performance of your instance. Monitor the alerts that are system driven.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Alerts in Instance Observer, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Track instance performance with the top six timely alerts – Guided users

Use the Instance Observer alerting feature to receive notifications on the performance of your instance. Monitor the alerts that are system driven.

## Before you begin

Role required: admin

## About this task

If you’re an Impact Guided tier customer, then the important top 6 and commonly used alerts are available for you. You can configure alerts and customize the types of notifications on instances to receive timely alerts that enable you to monitor the instance performance.

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Go to Instance Observer**.

2.  Log in to Instance Observer and navigate to **Alerts** &gt; **Configure Alerts**.

    The alert cards listed are:

    1.  Response Time – Instance
    2.  Event Queue
    3.  Database Response Time
    4.  Default Semaphore \(Mean\)
    5.  Default Semaphore \(Queue Depth\)
    6.  Long Running Jobs
3.  To configure an alert, select the alert name.

4.  In the **Configure Alert Condition** section of the slider page, select a value from the **Conditions** list to configure alert condition.

    You can select the conditions, set the threshold, duration to monitor the condition, and the snooze time in increments of five minutes.

5.  To simulate the configured conditions, select **Simulate Chart**.

6.  To set a notification rule, select **Set Notification** and select a rule.

7.  To create a notification rule, navigate to **Alerts** &gt; **Configure Notification** and select **Create Rule**.

    You can create a **New Rule** by giving a name and description. You can configure the **Notification Type** by selecting one or more from the options available such as Email, SMS, ServiceNow Integration, and third party integrations. If there are third-party integrations such as AWS, Google Cloud, or Azure an automated notification is sent to the specific URL as a webhook alert.

    You can set the rule conditions as default, which take precedence over all other conditions of a default rule.

    You can also select your users to whom you want the notifications to be sent by selecting the **Add custom recipients** option.

8.  Select **Save**.

    For more information on configuring alerts and setting notifications, see [Configure Key Alerts](configuring-io-alerts.md).


**Parent Topic:**[Alerts in Instance Observer](../concept/io-alerts-intro.md)

