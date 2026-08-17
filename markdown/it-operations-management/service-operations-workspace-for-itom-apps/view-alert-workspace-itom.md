---
title: Alerts in Service Operations Workspace
description: The Service Operations Workspace interface displays an alerts list and details on specific alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-operations-workspace-for-itom-apps/view-alert-workspace-itom.html
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Express List in SOW for ITOM, Use, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Alerts in Service Operations Workspace

The Service Operations Workspace interface displays an alerts list and details on specific alerts.

When you click an alert in the alerts list, the **Details** tab of the selected alert appears. The issue that caused the alert appears in the alert title. Only the sub tabs relevant to the alert appear on the resulting page. For example, the **Alerts in Group** option appears in the **Related Records** tab only for alert groups.

View the alerts that Azure grouped into the issue in the alert list. The **Source** column displays `A` for these alerts.\[Omitted image "em-related-record-azure-issue.png"\] Alt text: Azure monitor issue alerts

\[Omitted image "alert-details-tab-sow.png"\] Alt text: Details of an open alert.

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

</td></tr><tr><td>

Details tab

</td><td>

Shows the alert's core attributes, including its number, configuration item, class, resource, type, severity, state, and full description of the identified issue. Alongside are assignment fields \(assigned to, assignment group, task, parent\) plus the work notes and a chronological Activity log tracking state changes and system events.

</td></tr><tr><td>

Related Records tab

</td><td>

Displays lists of records linked to the alert, grouped into categories: events, impacted services, service offerings, changes, configuration items, remediation tasks, incidents, and similar alerts.**Note:** ServiceNow represents an Azure Issue as a single alert. You can view the alerts that Azure grouped into the Issue in this tab.

\[Omitted image "em-related-record-preview-azure-issue.png"\] Alt text: Azure monitor issue alert

</td></tr></tbody>
</table>