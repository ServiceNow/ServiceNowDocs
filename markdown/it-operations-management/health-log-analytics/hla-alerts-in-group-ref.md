---
title: Log Analytics alerts in the Alerts in group tab
description: The table describes the Log Analytics alerts in a Log Analytics group on the Alerts in group tab.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Information on the Overview tab for a Log Analytics group, Sections and cards on the alert Overview tab in Health Log Analytics, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Log Analytics alerts in the Alerts in group tab

The table describes the Log Analytics alerts in a Log Analytics group on the **Alerts in group** tab.

<table id="table_egk_qqf_tmb"><thead><tr><th>

Column

</th><th>

Description

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
</table>**Parent Topic:**[Information on the Overview tab for a Log Analytics group](hla-op-ovrvw-tab-log-anltcs-alerts.md)

