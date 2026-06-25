---
title: Sections and cards on the Overview tab for a Log Analytics alert in Health Log Analytics
description: The Overview tab in Health Log Analytics helps you understand Log Analytics alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/hla-op-ovrvw-tab-single-ci-alerts-sow.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Health Log Analytics, Overview tab, log analytics alerts, Service Operations Workspace, anomaly detection, identified issue, configuration items, impacted services, meaningful log properties, anomalous behavior, alert investigation, surrounding logs]
breadcrumb: [Information on the alert Overview tab, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Sections and cards on the Overview tab for a Log Analytics alert in Health Log Analytics

The **Overview** tab in Health Log Analytics helps you understand Log Analytics alerts.

For a detailed description of Log Analytics alerts, see [Types of Health Log Analytics alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-op-log-analytics-alert-types.md).

## Summary

-   **Identified issue**

    This card describes the issue that led to the alert. The identified issue appears on the card and in the title for the alert. Information about the alert appears in the banner.

    \[Omitted image "identified-issue-card-loganalytics-alert-sow.png"\] Alt text: Identified issue appears here and in alert title.

    Select **Details** for more information about the alert.

    Select **View surrounding logs** to view the log lines that were generated one minute before and one minute after the alert. See [Analyze log lines that surround an anomaly in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-op-surrounding-logs-view-sow.md).

-   **Anomaly**

    This card illustrates the anomalous activity that led to the alert.

    The chart shows:

    -   Recent anomalous activity
    -   Expected behavior \(the learned baseline\)
    -   Baseline values from one day earlier
    -   Baseline values from the previous week
    In this example, the system tracks the baseline rate \(the average number of events per minute\) for a specific log pattern. When this typically inactive log generates a spike in events, the system detects the deviation from the baseline and generates an alert.

    \[Omitted image "anomaly-spike.png"\] Alt text: Anomaly card identifies and illustrates anomalous behavior.

    In this example, the blue line represents the current average number of events per minute. The orange-shaded area represents the baseline values for the same hour in the previous week.

    \[Omitted image "anomaly-week-earlier.png"\] Alt text: Baseline values for same hour in previous week.

    For more information on the kinds of anomalies that you might encounter, see [Types of anomalous behavior in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-op-anomalous-behavior-types.md).


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


**Parent Topic:**[Sections and cards on the alert Overview tab in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-alert-overview-tab.md)

