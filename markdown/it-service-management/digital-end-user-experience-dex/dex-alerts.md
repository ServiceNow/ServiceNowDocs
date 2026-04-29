---
title: DEX Alerts
description: Digital End-User Experience \(DEX\) Alerts provide details on the active alerts, their severity, impacted services, and the duration.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Digital End-User Experience, IT Service Management]
---

# DEX Alerts

Digital End-User Experience \(DEX\) Alerts provide details on the active alerts, their severity, impacted services, and the duration.

On the Service Operations Workspace home page, Active alerts, Impacted devices, and Active devices are displayed. The Active alerts section displays the number of active alerts as of that selected time. Select the Active alerts section to view all the active alerts list.

![Active alerts list](../image/active-alerts-list.png)

By selecting a specific alert, you can find the details of the alert in different tabs that are listed in the table. ![Active alert overview window](../image/active-alerts.png)

|Tab name|Description|
|--------|-----------|
|**The Overview tab**|Provides a summary, impact, and cause of the alert.|
|**The Details tab**|Provides alert details like the alert name, metric name, history.|
|**The Related records**|Provides details on the affected services, remediation tasks, impacted devices, and possible root causes.|
|**The Remediate issue on devices**|Lists all the available remedial actions for the impacted device.|

View alerts for both your device and its applications in the Alerts section of the Devices page.

**Note:** For details on the active alerts listed see, [Monitor incoming alerts](https://www.servicenow.com/docs/access?context=t_EMUseAlertConsole&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).

## The Overview tab

-   Displays an overview of the alert, the summary, impact of the alert, and the cause for the alert created.
-   You can view the impacted devices and impacted users section. When you select the refresh icon on the Impacted devices or Impacted users, refresh the number impacted at that selected time.
-   Details related to the impacted Configuration Item \(CI\) are displayed under the impact section and opens up to the related records.
-   It displays any impacted services caused due to the alert.
-   The cause section displays the probable root cause and also shows the number of alerts created due to this cause.

![Overview tab](../image/alert-overviewtab.png)

## The Details tab

Access the Details tab to learn more about the history of the alert, metric name, and other metrics.

![Details tab](../image/alert-detailstab.png)

## Related records tab

-   All the related record information \(Impacted services, configuration items, Impacted devices, Impacted users, repeated alerts, and so on\) is displayed.
-   To access the related lists information displayed on the impacted devices and impacted users tabs, install the latest version \(26.3.1\) of the Service Operations Workspace alert management plugin `(sn_sow_em)` store plugin.
-   You can view the history of the bulk remedial action from the related records. All the remedial actions executed and their respective states are displayed.

![Related records tab](../image/alert-relatedrectab.png)

## Remediate issue on devices

-   Displays all the impacted devices that are up and active for the DEX engineer to remediate issues on multiple devices at once.
-   Categorizes the impacted devices based on the operating system and the status.
-   Based on the device selected. If one device is selected, remedial actions applicable for a single device are displayed. If multiple devices are selected, it displays all the available remedial actions for bulk remediation.
-   Enables you to execute a remedial action for a single device or multiple devices. To view the history of remedial action execution, access the related records tab \(remedial action history\).

![Remediate issue on devices tab](../image/alert-ritab.png)

