---
title: Sections and cards on the Overview tab for a Log Analytics group in Health Log Analytics
description: The alert Overview tab in Health Log Analytics helps you understand Log Analytics groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/hla-op-ovrvw-tab-log-anltcs-alerts-sow.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Overview tab, Log Analytics group, Log Analytics alerts, alert correlations, log correlator, alerts in group, identified issue, impacted services, configuration items, Service Operations Workspace]
breadcrumb: [Information on the alert Overview tab, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Sections and cards on the Overview tab for a Log Analytics group in Health Log Analytics

The alert **Overview** tab in Health Log Analytics helps you understand Log Analytics groups.

For a detailed description of Log Analytics groups, see [Types of Health Log Analytics alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-op-log-analytics-alert-types.md).

## Summary

-   **Identified issue**

    This card describes the issue that led to the alert. The identified issue appears on the card and in the title for the alert. Information about the alert appears in the banner.

    \[Omitted image "identified-issue-card-comp-based-sow.png"\] Alt text: Identified issue appears here and in alert title.

    Select **View correlations** to view the list of correlations that relate the Log Analytics alerts.

-   **Correlations list**

    During initial analysis, alerts are scored. Each correlation in the alert's log data with another alert contributes to the score. The higher the score, the more likely the alert is to be included as a Log Analytics alert in a Log Analytics group.

    The following kinds of data are considered when determining whether alerts are correlated:

    -   Time: The events all occurred within a configured time interval.
    -   Metadata: The alerts have matching values in log-line metadata. For example, all alerts involve the same host.
    -   Message text: The message text in the log data is similar or identical between alerts.
    -   Trend: The alerts show a similar tendency in values or rates. For example, a particular metric value is increasing in all alerts.
    \[Omitted image "correlation-popup-learn-more.png"\] Alt text: Correlations lists log correlators and Log Analytics alerts per group.

    1.  List of correlations: The first correlation in the list is expanded to show the individual Log Analytics alerts that are correlated and the log correlator that the alerts share.
    2.  An individual log correlator: The identifier for a group of correlated Log Analytics alerts. The alerts are grouped by the log-line data or metadata that is common to the alerts \(for example, IP address, host name, or user name\). The number in the blue square indicates the number of correlated alerts.
    3.  Log Analytics alerts that are correlated.
-   **Alerts in group**

    For a Log Analytics alert, the Alerts in group card shows the Log Analytics alerts that are grouped under the Log Analytics alert. Select a Log Analytics alert to view its details.

    \[Omitted image "alerts-in-group-tabs.png"\] Alt text: Select a Log Analytics alert to view its details.

    Select **View all** to the view the list of all Log Analytics alerts in the group and relevant information about them. You can also view the Alerts in group list by selecting the **Related records** tab and then selecting **Alerts in group**.

    For each Log Analytics alert in the group, the following information is available.

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
The priority group value is more important than severity alone. For example, a high priority and low severity alert should be addressed before a low priority and high severity alert. For information on how priority is calculated, see [Alert priority](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/alert-priority.md).

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
## Impact

-   **Configuration Items**

    This card provides information about the CIs that are impacted by the alert.

-   **Impacted services**

    This card provides information about the services that are impacted by the alert.

    \[Omitted image "hla-ovrvw-tab-impact-sow.png"\] Alt text: Impact section provides information on the impacted CIs and services.


**Parent Topic:**[Sections and cards on the alert Overview tab in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-alert-overview-tab.md)

