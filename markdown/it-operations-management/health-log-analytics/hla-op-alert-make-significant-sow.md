---
title: Mark an alert as significant in Health Log Analytics
description: Make an alert more likely to be included in a Log Analytics group when the associated metric behaves anomalously by labeling the alert as meaningful.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assign higher or lower significance to an alert, Controlling alert generation, prioritization, and anomaly detection, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Mark an alert as significant in Health Log Analytics

Make an alert more likely to be included in a Log Analytics group when the associated metric behaves anomalously by labeling the alert as meaningful.

## Before you begin

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## Procedure

1.  In the Service Operations Workspace, open a Log Analytics alert and then select **Apply ML feedback** &gt; **Mark as significant**.

2.  Confirm the action in the dialog box.

    **Note:** Processing this feedback might take a few seconds.

    The alert is marked as significant. The **Restore ML feedback** button appears instead of the **Apply ML feedback** drop-down list.

3.  Restore the significant alert.

    If you no longer want the significant alert to be treated specially, you can restore normal significance to the alert metric. For more information, see [Restore normal importance to an alert metric in Health Log Analytics](hla-op-alert-restore-user-defined-sow.md).


**Parent Topic:**[Assign higher or lower significance to an alert in Health Log Analytics](../concept/hla-op-alert-significance.md)

