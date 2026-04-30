---
title: Mark an alert as significant
description: Make an alert more likely to be included in a Log Analytics group when the associated metric behaves anomalously by labeling the alert as meaningful.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Assigning higher or lower significance to an alert in Health Log Analytics, Using Service Operations Workspace for ITOM Log Analytics, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Mark an alert as significant

Make an alert more likely to be included in a Log Analytics group when the associated metric behaves anomalously by labeling the alert as meaningful.

## Before you begin

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## Procedure

1.  In the Service Operations Workspace, open a Log Analytics alert and then select **Apply ML feedback** &gt; **Mark as significant**.

2.  Confirm the action in the dialog box.

    **Note:** Processing this feedback might take a few seconds.

3.  Restore the significant alert.

    If you no longer want the significant alert to be treated specially, you can restore normal significance to the alert metric. For more information, see [Restore normal importance to an alert metric](hla-op-alert-restore-user-defined-sow.md).


**Parent Topic:**[Assigning higher or lower significance to an alert in Health Log Analytics](../../service-operations-workspace-itom/concept/hla-op-alert-significance-sow-itom.md)

