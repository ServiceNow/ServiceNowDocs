---
title: Take action on a Health Log Analytics alert from the Overview tab
description: Start the remediation process from the Overview tab in the Service Operations Workspace. This tab provides information on alerts, log data that is associated with the anomalous behavior, CIs that generated the triggering metric, and services that are impacted by the alerts.
locale: en-US
release: yokohama
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Service Operations Workspace for ITOM Log Analytics, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Take action on a Health Log Analytics alert from the Overview tab

Start the remediation process from the **Overview** tab in the Service Operations Workspace. This tab provides information on alerts, log data that is associated with the anomalous behavior, CIs that generated the triggering metric, and services that are impacted by the alerts.

## Before you begin

Role required: evt\_mgmt\_operator, or evt\_mgmt\_user, or evt\_mgmt\_admin

## Procedure

1.  In the Service Operations Workspace, select the lists icon \(![Lists icon.](../image/icon-lists-sow.png)\).

2.  Select the appropriate list in the Alerts sublist and navigate to the desired alert or group.

    All Health Log Analytics alerts have the value **Log Analytics** in the **Source** column. The value in the **Group** column identifies the type of Log Analytics alert. See [Types of Health Log Analytics alerts](../reference/hla-op-log-analytics-alert-types.md) for a more detailed description of each type of alert or group.

    **Tip:** To preview an alert in the list, click its info icon \(![Info icon.](../../agent-client-collector/image/icon-info.png)\).

3.  Select the alert number.

    The **Overview** tab displays.

4.  View the section of the **Overview** tab that provides the information that you need.

    For a description of the sections and cards, see [Sections and cards on the alert Overview tab in Health Log Analytics](../../health-log-analytics-admin/concept/hla-alert-overview-tab.md).

    **Note:** Because some sections on the **Overview** tab show only a portion of the information, many sections include a link that displays different or more complete information.


-   **[Sections and cards on the Overview tab for a Component-based alert](../reference/hla-op-ovrvw-tab-comp-based-alerts-sow.md)**  
The **Overview** tab in the Service Operations Workspace helps you understand Component-based alerts.
-   **[Sections and cards on the Overview tab for a Log Analytics group](../reference/hla-op-ovrvw-tab-log-anltcs-alerts-sow.md)**  
The **Overview** tab in the Service Operations Workspace helps you understand Log Analytics groups.
-   **[Information on the Overview tab for a Log Analytics alert](../reference/hla-op-ovrvw-tab-single-ci-alerts-sow.md)**  
The **Overview** tab in the Service Operations Workspace helps you understand Log Analytics alerts.

**Parent Topic:**[Using Service Operations Workspace for ITOM Log Analytics](../concept/hla-op-binder-sow.md)

