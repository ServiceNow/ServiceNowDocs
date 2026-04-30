---
title: Decrease sensitivity to similar anomalies
description: Make Health Log Analytics anomaly detection less sensitive to anomalies like the one that triggered the current Log Analytics alert.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Assigning higher or lower significance to an alert in Health Log Analytics, Using Service Operations Workspace for ITOM Log Analytics, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Decrease sensitivity to similar anomalies

Make Health Log Analytics anomaly detection less sensitive to anomalies like the one that triggered the current Log Analytics alert.

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

3.  Restore normal sensitivity to anomalies like the one that triggered this alert.

    1.  While viewing the alert, select **Remove feedback**.

    2.  Confirm the action in the dialog box.


**Parent Topic:**[Assigning higher or lower significance to an alert in Health Log Analytics](../../service-operations-workspace-itom/concept/hla-op-alert-significance-sow-itom.md)

