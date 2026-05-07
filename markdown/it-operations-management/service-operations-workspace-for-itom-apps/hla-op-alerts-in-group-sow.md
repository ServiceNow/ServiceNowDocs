---
title: View the Log Analytics alerts in a Log Analytics group in Health Log Analytics
description: View a list of all Log Analytics alerts in a Log Analytics group on the Related records tab.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Overview tab for a Log Analytics group, Start remediation of a Log Analytics alert, Log Analytics in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View the Log Analytics alerts in a Log Analytics group in Health Log Analytics

View a list of all Log Analytics alerts in a Log Analytics group on the **Related records** tab.

## Before you begin

Role required: evt\_mgmt\_operator, or evt\_mgmt\_user, or evt\_mgmt\_admin

## About this task

For a detailed description of Log Analytics groups and Log Analytics alerts, see [Types of Health Log Analytics alerts](../reference/hla-op-log-analytics-alert-types.md).

## Procedure

1.  On the **Overview** tab for a Log Analytics alert, go to the **Alerts in group** card and select the **View all** link.

    The **Alerts in group** section on the **Related records** tab displays.

    ![Alerts in group section on the Related records tab.](../image/alerts-in-group-list-sow.png "Alerts in group section on the Related records tab")

2.  For each Log Analytics alert in the Log Analytics group, the information described in the table is available.

<table id="table_bcp_syz_4tb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The number of the alert. Select the number to view detailed information for an alert.

 This field is automatically set.

</td></tr><tr><td>

Initial event generation time

</td><td>

The time when the event that generated the alert first occurred.**Note:** Time here is the ServiceNow processing time, not the source system time.

</td></tr><tr><td>

Group

</td><td>

Type of group that the alert belongs to: a standalone Log Analytics alert or a Component-based alert.

</td></tr><tr><td>

Description

</td><td>

Anomalous pattern or metric that caused the alert to be generated.

</td></tr><tr><td>

Severity

</td><td>

Severity value for the alert. The available values are: -   **Critical**: Immediate action is required. Either the resource is not functional or critical problems are imminent.
-   **Major**: Major functionality is severely impaired or performance has degraded.
-   **Minor**: Either performance has degraded or there is a partial, non-critical loss of functionality.
-   **Warning**: Attention is required even though the resource is still functional.
-   **Info**: An informational message. An alert is created, but the resource is still functional.
-   **Clear or Resolved**: No action is required. An alert is not created from this event. Existing alerts are closed.


</td></tr><tr><td>

Priority group

</td><td>

Priority group that indicates the order in which to resolve alerts. Choices are as follows:-   **Urgent**
-   **High**
-   **Moderate**
-   **Low**
The priority group value is more important than severity alone. For example, a high priority and low severity alert should be addressed before a low priority and high severity alert. For information on how priority is calculated, see [Alert priority](../../event-management/concept/alert-priority.md).

</td></tr><tr><td>

State

</td><td>

Processing state of the alert. A newly generated alert is in the **Open** state. Other states are as follows:-   **Reopen**: A previously closed alert is open again, and it requires your attention.
-   **Flapping**: The alert is receiving identical events from the same source at high frequency. This state can cause an alert to re-open from the Closed state, resulting in a high frequency of changes between Open and Closed states.
-   **Closed**: The alert is closed and does not require any further action. You close an alert when it is remediated.


</td></tr><tr><td>

Configuration item

</td><td>

CI in the CMDB. The CI is applied to by the alert.

</td></tr><tr><td>

Node

</td><td>

Node field that is received in the log message. The event described in the log message occurred on this node. Often, the node is the name of the CI that is associated with the alert. For example, a computer name, IP address, FQDN, or MAC address.

</td></tr><tr><td>

Source

</td><td>

All Health Log Analytics alerts have the value **Log Analytics** in the **Source** column to indicate that the Health Log Analytics app generated the alert.

</td></tr><tr><td>

Metric name

</td><td>

Name of the metric whose anomalous behavior led to the alert. For example, the **I/O request** in the case that the I/O request took longer than 15000 ms to complete.

</td></tr><tr><td>

Updated

</td><td>

Most recent time when the alert information or state was updated.

</td></tr></tbody>
</table>
**Parent Topic:**[Sections and cards on the Overview tab for a Log Analytics group in Health Log Analytics](../reference/hla-op-ovrvw-tab-log-anltcs-alerts-sow.md)

