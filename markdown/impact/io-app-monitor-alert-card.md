---
title: Set an alert to monitor the average response time of applications
description: Set an alert to monitor the application performance when the average response time of applications that run on an instance exceeds the configured threshold.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Alerts in Instance Observer, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Set an alert to monitor the average response time of applications

Set an alert to monitor the application performance when the average response time of applications that run on an instance exceeds the configured threshold.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Go to Instance Observer**

2.  Log in to Instance Observer and navigate to **Alerts** &gt; **Configure alerts**.

3.  Select an instance in the **Instance** list.

4.  In the **Search alerts** field, enter `Application monitoring`.

5.  Select the **Application monitoring – Average Response Time** alert card.

6.  In the Edit alert configuration slide on page, set the conditions by setting up a **Snooze time**.

    The minimum snooze time is 15 minutes.

7.  Set the values in the **Average Response Time in seconds for each data point collected over the past mins** fields so that the alert is set when the response time exceeds the time frame for each data point collected over the past minutes that you have configured.

8.  In the **Add applications** section, search from the **Available applications** and select those applications for which you want to trigger the average response time alert.

    All the selected applications appear in the **Selected** section. You can select a maximum of 10 applications and a minimum of one.

9.  Select **Simulate** to get a list of simulated applications.

    The list shows the applications with average response time collected from the data. Setting this alert On with selected applications enables you to monitor their performance.

    ![Setting conditions for average response time alert.](../image/io-alert-config-sim-set.png)

10. Select **Set Notification**.

    To set notification, see the [Set notification step](configuring-io-alerts.md) of [Configure Key Alerts](configuring-io-alerts.md).


**Parent Topic:**[Alerts in Instance Observer](../concept/io-alerts-intro.md)

