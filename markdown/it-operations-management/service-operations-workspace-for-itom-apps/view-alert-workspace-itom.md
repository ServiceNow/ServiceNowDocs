---
title: Alerts in Service Operations Workspace
description: The Service Operations Workspace interface displays an alerts list and details on specific alerts.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Express List in the Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Alerts in Service Operations Workspace

The Service Operations Workspace interface displays an alerts list and details on specific alerts.

When clicking an alert in the alerts list, the **Details** tab of the selected alert appears and the issue that caused the alert \(the identified issue\) appears in the alert title. Only the subtabs relevant to the alert appear on the resulting page. For example, the **Alerts in Group** option appears in the **Related records** tab only for alert groups.

![Details of an open alert.](../image/alert-details-tab-sow.png "Details tab")

The following table describes areas on the alert form.

<table id="table_kjx_2yp_2db"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Header

</td><td>

The header includes these details:

 -   Description: The text from the **Description** field of the alert is displayed.
-   Priority group: Priority group to which the alert belongs.
-   Severity: Severity of the alert.
-   State: The state of the alert.
-   Initial event generation time: Date and time when the initial event was generated.
-   Parent: The primary alert in the group \(relevant only for child alerts in a group\).
-   Group: Group type to which the alert belongs \(relevant only for alerts in a group\).
-   Task: Number of the incident with which the alert is associated.

 The displayed information varies according to the alert type.

</td></tr><tr><td>

Overview tab

</td><td>

When viewing an alert with an assigned CI, this tab opens when selecting the alert. The information displayed varies depending on the type of alert \(grouped, secondary, or primary\).If you have installed the Health Log Analytics app, alert types include Health Log Analytics alerts and component-based alerts.

</td></tr></tbody>
</table>