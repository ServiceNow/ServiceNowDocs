---
title: Decrease sensitivity to similar anomalies in Health Log Analytics
description: Make anomaly detection less sensitive to anomalies like the one that triggered the current Log Analytics alert.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assign higher or lower significance to an alert, Controlling alert generation, prioritization, and anomaly detection, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Decrease sensitivity to similar anomalies in Health Log Analytics

Make anomaly detection less sensitive to anomalies like the one that triggered the current Log Analytics alert.

## Before you begin

**Note:** This functionality is not available for customer alerts and new signal alerts.

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## About this task

Selecting the Raise feedback option raises the threshold for generating alerts when Health Log Analytics identifies future anomalies similar to the one that led to this alert.

## Procedure

1.  In the Service Operations Workspace, open a Log Analytics alert and then select **Apply ML feedback** &gt; **Raise**.

    ![Raise feedback option.](../image/hla-raise-feedback.png)

2.  Confirm the action in the dialog box.

    **Note:** Processing this feedback might take a few seconds.

    Anomaly detection is now less sensitive to anomalies like the one that triggered the current alert. The **Restore ML feedback** button appears instead of the **Apply ML feedback** drop-down list.

3.  Restore normal sensitivity to anomalies like the one that triggered this alert.

    1.  While viewing the alert, select **Restore ML feedback**.

    2.  Confirm the action in the dialog box.


**Parent Topic:**[Assign higher or lower significance to an alert in Health Log Analytics](../concept/hla-op-alert-significance.md)

