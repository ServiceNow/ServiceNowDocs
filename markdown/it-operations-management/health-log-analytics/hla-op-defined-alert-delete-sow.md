---
title: Delete a Log Analytics alert rule in Health Log Analytics
description: Delete a Log Analytics alert rule that you have defined if it is no longer necessary.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Health Log Analytics, log analytics alert rule, delete alert rule, remove alert rule, defined alerts, Log viewer, Defined alerts table, alert rule management, alert configuration, custom alert rules, alert rule deletion, alert cleanup, unnecessary alerts]
breadcrumb: [Use alert rules to control when HLA generates alerts, Controlling alert generation, prioritization, and anomaly detection, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Delete a Log Analytics alert rule in Health Log Analytics

Delete a Log Analytics alert rule that you have defined if it is no longer necessary.

## Before you begin

For background information, see [About Log Analytics alert rules](../../health-log-analytics-admin/concept/hla-custom-alert-rules.md).

This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, and the Health Log Analytics Viewer application, Version 20.0.4 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## Procedure

1.  Open the **Log Viewer** using one of the following methods:

    -   Navigate to **Workspaces** &gt; **Service Operations Workspace** and select the Log Viewer icon \(![Log Viewer icon.](../image/icon-log-viewer-sow.png)\).
    -   While viewing log entries for an alert on the **Surrounding logs** tab, select **Log Viewer**.
2.  Open a defined alert.

    1.  Select the selection icon \(![Selection icon.](../image/icon-selection-sow.png)\) at the top right of the **Log viewer** tab, and then choose **Manage my defined alerts** from the drop-down list.

    2.  From the **Defined alerts** table, select the alert that you want to delete.

3.  Select **Delete**.


**Related topics**  


[Define a Log Analytics alert rule in Health Log Analytics](hla-op-alert-rule-add-sow.md)

[Change a Log Analytics alert rule in Health Log Analytics](hla-op-defined-alert-modify-sow.md)

