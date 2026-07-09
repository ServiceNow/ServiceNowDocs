---
title: Overview tab sections for Log Analytics alert groups
description: The Overview tab in the Service Operations Workspace helps you understand Log Analytics groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-operations-workspace-for-itom-apps/hla-op-ovrvw-tab-log-anltcs-alerts-sow.html
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Start remediation of a Log Analytics alert, Log Analytics in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Overview tab sections for Log Analytics alert groups

The **Overview** tab in the Service Operations Workspace helps you understand Log Analytics groups.

For a detailed description of Log Analytics groups, see [Types of Health Log Analytics alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-op-log-analytics-alert-types.md).

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
    \[Omitted image "correlation-popup-learn-more-sow.png"\] Alt text: Correlations lists log correlators and Log Analytics alerts per group.

    1.  List of correlations: The first correlation in the list is expanded to show the individual Log Analytics alerts that are correlated and the log correlator that the alerts share.
    2.  An individual log correlator: The identifier for a group of correlated Log Analytics alerts. The alerts are grouped by the log-line data or metadata that is common to the alerts \(for example, IP address, host name, or user name\). The number in the blue square indicates the number of correlated alerts.
    3.  Log Analytics alerts that are correlated.
-   **Alerts in group**

    For a Log Analytics alert, the Alerts in group card shows the Log Analytics alerts that are grouped under the Log Analytics alert. Select a Log Analytics alert to view its details.

    \[Omitted image "alerts-in-group-sow.png"\] Alt text: Select a Log Analytics alert to view its details.

    Select **View all** to the view the list of all Log Analytics alerts in the group and relevant information about them. You can also view the Alerts in group list by selecting the **Related records** tab and then selecting **Alerts in group**. For more information, see [View the Log Analytics alerts in a Log Analytics group in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/hla-op-alerts-in-group-sow.md)


## Impact

-   **Configuration Items**

    This card provides information about the CIs that are impacted by the alert.

-   **Impacted services**

    This card provides information about the services that are impacted by the alert.

    \[Omitted image "hla-ovrvw-tab-impact-sow.png"\] Alt text: Impact section provides information on the impacted CIs and services.


-   **[View the Log Analytics alerts in a Log Analytics group in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/hla-op-alerts-in-group-sow.md)**  
View a list of all Log Analytics alerts in a Log Analytics group on the **Related records** tab.

**Parent Topic:**[Take action on a Log Analytics alert from the Overview tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/hla-op-overview-tab-view-sow.md)

