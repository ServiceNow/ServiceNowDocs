---
title: Information on the Overview tab for a Log Analytics group
description: The alert Overview tab in Health Log Analytics helps you understand Log Analytics groups.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Information on the alert Overview tab, Information on the Alert Insight Similar Alerts tab, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Information on the Overview tab for a Log Analytics group

The alert **Overview** tab in Health Log Analytics helps you understand Log Analytics groups.

## Sections on the Overview tab for Log Analytics groups

For a detailed description of Log Analytics groups, see [Types of Health Log Analytics alerts](hla-op-log-analytics-alert-types.md).

-   **Correlations banner**

    During initial analysis, alerts are scored. Each correlation in the alert's log data with another alert contributes to the score. The higher the score, the more likely the alert is to be included as a Log Analytics alert in a Log Analytics alert.

    The following kinds of data are considered when determining whether alerts are correlated:

    -   Time: The events all occurred within a configured time interval.
    -   Metadata: The alerts have matching values in log-line metadata. For example, all alerts involve the same host.
    -   Message text: The message text in the log data is similar or identical between alerts.
    -   Trend: The alerts show a similar tendency in values or rates. For example, a particular metric value is increasing in all alerts.
    Select the **More info** link on the Correlations banner to view the list of correlations that relate the Log Analytics alerts.

    ![Select More info to open the Correlations list.](../image/correlations-banner.png "Correlations banner")

    ![Correlations lists log correlators and Log Analytics alerts per group.](../image/correlation-popup-learn-more.png "Correlations")

    1.  List of correlations: The first correlation in the list is expanded to show the individual Log Analytics alerts that are correlated and the log correlator that the alerts share. The number in parentheses is the number of alerts in the correlation.
    2.  An individual log correlator: The identifier for a group of correlated Log Analytics alerts. The alerts are grouped by the log-line data or metadata that is common to the alerts \(for example, IP address, host name, or user name\). The number in parentheses indicates the number of correlated alerts.
    3.  Log Analytics alerts that are correlated.
-   **Alerts in group**

    For a Log Analytics alert \(Alert0010166 in the example\), the Alerts in group section shows the Log Analytics alerts that are grouped under the Log Analytics alert.

    Select a Log Analytics alert to view its details. To view the full list of Log Analytics alerts, select **View more** or select the **Alerts in group** tab.

    ![Select a Log Analytics alert to view its details.](../image/alerts-in-group-tabs.png "Viewing alert details")

-   **Configuration Items**

    To view more detailed information on the CIs that are associated with the alerts, select the **Configuration Items** tab or select **View more** in the Configuration Items section. See [Operator phase 1: Analyze and acknowledge an alert](../../event-management-operator/task/operator-phase-acknowledge-analyze.md).

-   **Impacted services**

    To view detailed information on the services that are impacted by the alerts, select the **Impacted services** tab. See [Operator phase 1: Analyze and acknowledge an alert](../../event-management-operator/task/operator-phase-acknowledge-analyze.md).


-   **[Log Analytics alerts on the Alerts in group tab](hla-alerts-in-group-ref.md)**  
The table describes the Log Analytics alerts in a Log Analytics group on the **Alerts in group** tab.

**Parent Topic:**[Sections and cards on the alert Overview tab in Health Log Analytics](../../health-log-analytics-admin/concept/hla-alert-overview-tab.md)

