---
title: Overview tab sections for Log Analytics alerts
description: The Overview tab in the Service Operations Workspace helps you understand Log Analytics alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-operations-workspace-for-itom-apps/hla-op-ovrvw-tab-single-ci-alerts-sow.html
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Start remediation of a Log Analytics alert, Log Analytics in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Overview tab sections for Log Analytics alerts

The **Overview** tab in the Service Operations Workspace helps you understand Log Analytics alerts.

For a detailed description of Log Analytics alerts, see [Types of Health Log Analytics alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-op-log-analytics-alert-types.md).

## Summary

-   **Identified issue**

    This card describes the issue that led to the alert. The identified issue appears on the card and in the title for the alert. Information about the alert appears in the banner.

    \[Omitted image "identified-issue-card-loganalytics-alert-sow.png"\] Alt text: Identified issue appears here and in alert title.

    Select **View surrounding logs** to view the log lines that were generated one minute before and one minute after the alert. See [Analyze log lines surrounding an anomaly](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-op-surrounding-logs-view.md).

-   **Anomaly**

    This card illustrates the anomalous activity that led to the alert.

    -   The blue line shows the recent anomalous activity.
    -   On some charts, the lightly shaded area indicates the expected \(learned baseline\) behavior.

        A peach-shaded area represents the baseline values for the same hour one day earlier. A pink-shaded area shows the values for the same period in the previous week.

    In this example, the peach-shaded area shows the data for the same hour one day earlier. The drop in the metric value \(events per minute\) is clearly visible.

    \[Omitted image "anomaly-day-earlier-sow.png"\] Alt text: Anomaly card identifies and illustrates anomalous behavior.

    For more information on the kinds of anomalies that you might encounter, see [Types of anomalous behavior in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-op-anomalous-behavior-types.md).


## Impact

-   **Configuration Items**

    This card provides information about the CIs that are impacted by the alert.

-   **Impacted services**

    This card provides information about the services that are impacted by the alert.

    \[Omitted image "hla-ovrvw-tab-impact-single-sow.png"\] Alt text: Impact section provides information on the impacted CIs and services.


## Cause

-   **Meaningful log properties**

    On this card, each bar chart shows the distribution of values for a single log property that contributed to the anomaly. Each property value is associated with a color. The length of a color bar correlates to the percentage that the property value holds in comparison with all other values for the property.

    \[Omitted image "meaningful-log-properties-card-sow.png"\] Alt text: Meaningful log properties shows relative frequency of occurrence for property values.


**Parent Topic:**[Take action on a Log Analytics alert from the Overview tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/hla-op-overview-tab-view-sow.md)

