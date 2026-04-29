---
title: Mute an unimportant alert in Health Log Analytics
description: Eliminate distracting new alerts for insignificant issues by muting them.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assigning higher or lower significance to an alert in Health Log Analytics, Log Analytics in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Mute an unimportant alert in Health Log Analytics

Eliminate distracting new alerts for insignificant issues by muting them.

## Before you begin

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## About this task

When you mute an alert that is based on the keyword metric or the pattern severity metric, the system mutes the metric in the dominant pattern. The dominant pattern is the main pattern that contributes to the anomaly. For the specified source only, anomalous behavior for the metric that is associated with the muted alert no longer generates alerts. You can also mute the metric that is associated with an unimportant alert for all components of the Application Service. A component can be multiple CIs that perform the same function.

## Procedure

1.  In the Service Operations Workspace, open the Log Analytics alert that you don't want to see again.

2.  Select **Apply ML feedback**

3.  Mute the metric associated with the alert by doing one of the following:

    -   Select **Mute alert metric** to mute the metric for the specified source only.
    -   Select **Mute alert metric for all components** to mute the metric for all components of the Application Service.
4.  Confirm the action in the dialog box.

    **Note:** Processing this feedback might take a few seconds.

5.  Restore the muted alert.

    If you no longer want the muted alert to be treated specially, you can restore normal significance to the alert metric. For more information, see [Restore normal importance to an alert metric in Health Log Analytics](hla-op-alert-restore-user-defined-sow.md).


**Parent Topic:**[Assigning higher or lower significance to an alert in Health Log Analytics](../../service-operations-workspace-itom/concept/hla-op-alert-significance-sow-itom.md)

**Related topics**  


[View the list of muted metrics in Health Log Analytics](hla-op-alert-view-ignored-list.md)

