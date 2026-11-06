---
title: DEX alerts
description: Digital End-User Experience \(DEX\) alerts provide details on the active alerts, their severity, impacted services, and the duration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/dex-alerts.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [dex alert management, active alerts, alert severity, impacted services, impacted devices, impacted users, overview tab, details tab, related records tab, remediate issue on devices, remedial actions, bulk remediation, root cause of alert]
breadcrumb: [Monitor application performance, Manage employee experience, Digital End-User Experience, IT Operations Management]
---

# DEX alerts

Digital End-User Experience \(DEX\) alerts provide details on the active alerts, their severity, impacted services, and the duration.

On the Service Operations Workspace home page, Active alerts, Impacted devices, and Active devices are displayed. The Active alerts section displays the number of active alerts as of that selected time. Select the Active alerts section to view all the active alerts list.

\[Omitted image "active-alerts-list.png"\] Alt text: Active alerts list

By selecting a specific alert, you can find the details of the alert in the tabs listed in the following table. \[Omitted image "active-alerts.png"\] Alt text: Active alert overview window

|Tab name|Description|
|--------|-----------|
|Overview|Provides a summary, impact, and cause of the alert.|
|Details|Provides alert details like the alert name, metric name, history.|
|Related records|Provides details on the affected services, remediation tasks, impacted devices, and possible root causes.|
|Remediate issue on devices|Lists all the available remedial actions for the impacted device.|

View alerts for both your device and its applications in the Alerts section of the Devices page.

**Note:** For details on the active alerts listed see, [Monitor incoming alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/event-management/t_EMUseAlertConsole.md).

## Overview tab

-   Displays an overview of the alert, the summary, impact of the alert, and the cause for the alert created.
-   You can view the impacted devices and impacted users section. When you select the refresh icon on the Impacted devices or Impacted users, refresh the number impacted at that selected time.
-   Details related to the impacted CI are displayed under the impact section and opens up to the related records.
-   Displays any services impacted by the alert.
-   The cause section displays the probable root cause and also shows the number of alerts created due to this cause.

\[Omitted image "alert-overviewtab.png"\] Alt text: Overview tab

## Details tab

Access the **Details** tab to learn more about the history of the alert, metric name, and other metrics.

\[Omitted image "alert-detailstab.png"\] Alt text: Details tab

## Related records tab

-   All the related record information \(Impacted services, configuration items, Impacted devices, Impacted users, repeated alerts, and so on\) is displayed.
-   To access the related lists information displayed on the impacted devices and impacted users tabs, install the latest version \(26.3.1\) of the Service Operations Workspace alert management plugin `(sn_sow_em)`.
-   You can view the history of the bulk remedial action from the related records. All the remedial actions executed and their respective states are displayed.

\[Omitted image "alert-relatedrectab.png"\] Alt text: Related records tab

## Remediate issue on devices

-   Displays all the impacted devices that are up and active for the DEX engineer to remediate issues on multiple devices at once.
-   Categorizes the impacted devices based on the operating system and the status.
-   Displays remedial actions based on the devices selected. If one device is selected, remedial actions applicable for a single device are displayed. If multiple devices are selected, it displays all the available remedial actions for bulk remediation.
-   Enables you to execute a remedial action for a single device or multiple devices. To view the history of remedial action execution, access the **Related records** tab \(remedial action history\).

\[Omitted image "alert-ritab.png"\] Alt text: Remediate issue on devices tab

