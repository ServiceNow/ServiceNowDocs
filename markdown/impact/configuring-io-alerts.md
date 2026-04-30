---
title: Configure Key Alerts
description: Follow these steps to configure Key Alerts on an instance where critical alerts have not yet been configured.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Key alerts – activation and notifications, Alerts in Instance Observer, Impact Instance Observer, Platform Health, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Configure Key Alerts

Follow these steps to configure Key Alerts on an instance where critical alerts have not yet been configured.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Go to Instance Observer**

2.  Log in to Instance Observer and navigate to **Alerts** &gt; **Configure alerts**.

    ![Shows the Configure Alerts banner to begin alert configuration.](../image/config-alert-banner.png)

    A notification banner displays.

3.  Select **Configure your alerts!**.

    Alerts for metrics chosen by the system display.

4.  Select up to five alerts from the **Max alerts per day / per metric** drop-down to receive for each metric per day.

    The maximum number of alerts selected pertains to each of the six available system metrics. If you choose a maximum of two alerts for each metric, then you receive 12 alerts, as the maximum alert count each day, for example \(2 alerts\) X \(6 metrics\) = 12 alerts. The alert count resets daily at 00:00 UTC.![Shows the alert configuration drop-down selector.](../image/alert-max-threshold.png)

5.  Select **Set Notification**.

    The Alert configuration page loads and the **Default** notification rule is automatically selected.![The Alert Notification screen with the Default alert selected. How to Configure Notification Rules and Configure Notification links are also available.](../image/alert-config-io.png)

6.  Select **Configure Notification** to create a custom rule.

    The **How to Configure Notification Rules** link contains information on custom notification creation. Rule options include Rule Name, Recipients, and Notification Methods.

7.  Select **Review &amp; Create** to display the summary of the alerts to be configured and the notification rule.

    ![Shows the list of alerts to be configured and the confirmation button.](../image/create-io-alert.png)

8.  Select **Create Alert** or **Set Notification** to return to the notifications configuration page.

    A notification appears to confirm the alert configuration.

    ![Shows the alert configuration confirmation message.](../image/alert-confirmation.png)


## Result

After the request submission, all six alerts will be enabled automatically, no manual intervention is required. If you want to see the alert threshold, navigate to **Edit Alert configuration** to access the **IO recommended** condition.

**Note:** If one or more alerts out of the six available aren’t enabled automatically, then a threshold wasn’t available for that specific metric due to limited use in the instance.

## What to do next

[Manage Instance Observer alerts](manage-io-alerts.md)

