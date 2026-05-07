---
title: Sections and cards on the Overview tab for a Log Analytics group in Health Log Analytics
description: The Overview tab in the Service Operations Workspace helps you understand Log Analytics groups.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Start remediation of a Log Analytics alert, Log Analytics in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Sections and cards on the Overview tab for a Log Analytics group in Health Log Analytics

The **Overview** tab in the Service Operations Workspace helps you understand Log Analytics groups.

For a detailed description of Log Analytics groups, see [Types of Health Log Analytics alerts](hla-op-log-analytics-alert-types.md).

## Summary

-   **Identified issue**

    This card describes the issue that led to the alert. The identified issue appears on the card and in the title for the alert. Information about the alert appears in the banner.

    ![Identified issue appears here and in alert title.](../image/identified-issue-card-comp-based-sow.png "Identified issue")

    Select **View correlations** to view the list of correlations that relate the Log Analytics alerts.

-   **Correlations list**

    During initial analysis, alerts are scored. Each correlation in the alert's log data with another alert contributes to the score. The higher the score, the more likely the alert is to be included as a Log Analytics alert in a Log Analytics group.

    The following kinds of data are considered when determining whether alerts are correlated:

    -   Time: The events all occurred within a configured time interval.
    -   Metadata: The alerts have matching values in log-line metadata. For example, all alerts involve the same host.
    -   Message text: The message text in the log data is similar or identical between alerts.
    -   Trend: The alerts show a similar tendency in values or rates. For example, a particular metric value is increasing in all alerts.
    ![Correlations lists log correlators and Log Analytics alerts per group.](../image/correlation-popup-learn-more-sow.png "Correlations")

    1.  List of correlations: The first correlation in the list is expanded to show the individual Log Analytics alerts that are correlated and the log correlator that the alerts share.
    2.  An individual log correlator: The identifier for a group of correlated Log Analytics alerts. The alerts are grouped by the log-line data or metadata that is common to the alerts \(for example, IP address, host name, or user name\). The number in the blue square indicates the number of correlated alerts.
    3.  Log Analytics alerts that are correlated.
-   **Alerts in group**

    For a Log Analytics alert, the Alerts in group card shows the Log Analytics alerts that are grouped under the Log Analytics alert. Select a Log Analytics alert to view its details.

    ![Select a Log Analytics alert to view its details.](../image/alerts-in-group-sow.png "Alerts in group")

    Select **View all** to the view the list of all Log Analytics alerts in the group and relevant information about them. You can also view the Alerts in group list by selecting the **Related records** tab and then selecting **Alerts in group**. For more information, see [View the Log Analytics alerts in a Log Analytics group in Health Log Analytics](../task/hla-op-alerts-in-group-sow.md)


## Impact

-   **Configuration Items**

    This card provides information about the CIs that are impacted by the alert.

-   **Impacted services**

    This card provides information about the services that are impacted by the alert.

    ![Impact section provides information on the impacted CIs and services.](../image/hla-ovrvw-tab-impact-sow.png "Impact section")


-   **[View the Log Analytics alerts in a Log Analytics group in Health Log Analytics](../task/hla-op-alerts-in-group-sow.md)**  
View a list of all Log Analytics alerts in a Log Analytics group on the **Related records** tab.

**Parent Topic:**[Start remediation of a Log Analytics alert from the Overview tab](../task/hla-op-overview-tab-view-sow.md)

