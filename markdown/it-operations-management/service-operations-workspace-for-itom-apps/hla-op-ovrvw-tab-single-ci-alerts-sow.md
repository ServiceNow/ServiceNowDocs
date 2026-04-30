---
title: Information on the Overview tab for a Log Analytics alert in Health Log Analytics
description: The Overview tab in the Service Operations Workspace helps you understand Log Analytics alerts.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Start remediation of a Log Analytics alert, Log Analytics in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Information on the Overview tab for a Log Analytics alert in Health Log Analytics

The **Overview** tab in the Service Operations Workspace helps you understand Log Analytics alerts.

For a detailed description of Log Analytics alerts, see [Types of Health Log Analytics alerts](hla-op-log-analytics-alert-types.md).

## Summary

-   **Identified issue**

    This card describes the issue that led to the alert. The identified issue appears on the card and in the title for the alert. Information about the alert appears in the banner.

    ![Identified issue appears here and in alert title.](../image/identified-issue-card-loganalytics-alert-sow.png "Identified issue")

    Select **View surrounding logs** to view the log lines that were generated one minute before and one minute after the alert. See [Analyze log lines around the anomaly to help find the root cause](../task/hla-op-surrounding-logs-view.md).

-   **Anomaly**

    This card illustrates the anomalous activity that led to the alert.

    -   The blue line shows the recent anomalous activity.
    -   On some charts, the lightly shaded area indicates the expected \(learned baseline\) behavior.

        A peach-shaded area represents the baseline values for the same hour one day earlier. A pink-shaded area shows the values for the same period in the previous week.

    In this example, the peach-shaded area shows the data for the same hour one day earlier. The drop in the metric value \(events per minute\) is clearly visible.

    ![Anomaly card identifies and illustrates anomalous behavior.](../image/anomaly-day-earlier-sow.png "Anomaly card")

    For more information on the kinds of anomalies that you might encounter, see [Types of anomalous behavior in Health Log Analytics](hla-op-anomalous-behavior-types.md).


## Impact

-   **Configuration Items**

    This card provides information about the CIs that are impacted by the alert.

-   **Impacted services**

    This card provides information about the services that are impacted by the alert.

    ![Impact section provides information on the impacted CIs and services.](../image/hla-ovrvw-tab-impact-single-sow.png "Impact section")


## Cause

-   **Meaningful log properties**

    On this card, each bar chart shows the distribution of values for a single log property that contributed to the anomaly. Each property value is associated with a color. The length of a color bar correlates to the percentage that the property value holds in comparison with all other values for the property.

    ![Meaningful log properties shows relative frequency of occurrence for property values.](../image/meaningful-log-properties-card-sow.png "Meaningful log properties")


**Parent Topic:**[Take action on a Log Analytics alert from the Overview tab](../task/hla-op-overview-tab-view-sow.md)

