---
title: Configure Security Metrics to send email when thresholds are triggered
description: Learn how to configure Security Metrics so that your instance generates an email notification when a threshold is triggered.
locale: en-US
release: yokohama
product: Security Center
classification: security-center
topic_type: task
last_updated: "2025-04-21"
reading_time_minutes: 1
breadcrumb: [Security metrics, Security monitoring console, Security Center, Platform Security]
---

# Configure Security Metrics to send email when thresholds are triggered

Learn how to configure Security Metrics so that your instance generates an email notification when a threshold is triggered.

## Before you begin

Role required: admin

## Procedure

1.  In the Security Center, navigate to **metrics**.

2.  Select a metric that you want to set a threshold for in your organization.

    To manage failed logins, you can set a threshold. When the number of failed logins reach this threshold, admins or security experts in your organization are notified. The appropriate Security Metric to target in this case is **users** &gt; **failed logins**.

3.  Select the **Thresholds** icon.

4.  Select the **plus \(+\)** icon on the thresholds panel to configure the form.

    The options available are to set the visibility, threshold type, and threshold value.

    1.  For visibility, select **for everyone** if you want everyone to receive the notification, or **for me** if you only want to receive a notification.

    2.  In **threshold type**, select **all time high**.

        This field triggers the threshold notification.

        **Note:** A threshold value must only be entered when the **Threshold Type** is set to **Less than** or **More than**.

5.  Select **save** to create the threshold.

    Next, the notification must be set up.

6.  Select **all**, and enter **system notification**.

7.  Navigate to **email** &gt; **notifications**.

8.  In the **name** column, enter `*pa thre`.

    The threshold notifications are event-based, and they’re set up in the PA Thresholds Notification table.

9.  Select **PA Thresholds Notification**.

    There are three tabs in the results:

    -   When to send: Specifies what must occur to send the email notification. In this example, once the threshold you previously set is reached, the email is triggered.
    -   Who will receive: Specifies which users receive the notification. You can add users and groups.
    -   What it will contain: Specifies the script action that a user can modify to customize the message that users and the group will receive. To learn more about creating script actions, see [Script actions](https://www.servicenow.com/docs/access?context=r_ScriptActions&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

**Parent Topic:**[Security metrics](../concept/sc-metrics.md)

