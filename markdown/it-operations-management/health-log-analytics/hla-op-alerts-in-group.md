---
title: View the list of Log Analytics alerts in a Log Analytics group
description: View the list of all Log Analytics alerts in a Log Analytics group on the Alerts in group tab.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Information on the Overview tab for a Log Analytics group, Sections and cards on the alert Overview tab in Health Log Analytics, Health Log Analytics reference, Health Log Analytics, ITOM Health, IT Operations Management]
---

# View the list of Log Analytics alerts in a Log Analytics group

View the list of all Log Analytics alerts in a Log Analytics group on the **Alerts in group** tab.

## Before you begin

Role required: evt\_mgmt\_operator, or evt\_mgmt\_user, or evt\_mgmt\_admin

## About this task

For a detailed description of Log Analytics groups and Log Analytics alerts, see [Types of Health Log Analytics alerts](../reference/hla-op-log-analytics-alert-types.md).

## Procedure

1.  Use one of the following methods to view the list of Log Analytics alerts:

    -   While viewing a Log Analytics group on the **Overview** tab in the Operator Workspace, click **View more** in the Alerts in group section.
    -   While viewing a Log Analytics group in the Service Operations Workspace, click the **Alerts in group** tab to view the full list of alerts in the parent group for the alert.
<table id="table_egk_qqf_tmb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The number of the alert that appears in the list of alerts on the Operator Workspace dashboard. To view detailed information for an alert on the **Details** tab, click the alert number.

 This field is automatically set.

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
**Parent Topic:**[Information on the Overview tab for a Log Analytics group](../reference/hla-op-ovrvw-tab-log-anltcs-alerts.md)

