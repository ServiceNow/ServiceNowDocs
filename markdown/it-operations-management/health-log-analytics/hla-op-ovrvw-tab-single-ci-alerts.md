---
title: Information on the Overview tab for a Log Analytics alert
description: The alert Overview tab in Health Log Analytics helps you understand Log Analytics alerts.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Information on the alert Overview tab, Information on the Alert Insight Similar Alerts tab, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Information on the Overview tab for a Log Analytics alert

The alert **Overview** tab in Health Log Analytics helps you understand Log Analytics alerts.

## Sections and cards on the Overview tab for Log Analytics alerts

For a detailed description of Log Analytics alerts , see [Types of Health Log Analytics alerts](hla-op-log-analytics-alert-types.md).

-   **Identified issue**

    The "identified issue" led to the alert. The issue appears in the title for the alert and on a card on the tab. Information about the alert appears in the banner.

    ![Identified issue appears here and in alert title.](../image/identified-issue-card-loganalytics-alert.png "Identified issue")

    -   Click the information icon \(![Information icon.](../image/icon-info.png)\) to see how the issue was identified.
    -   Click **View surrounding logs** to view the log lines that were generated one minute before and one minute after the alert. See [Analyze log lines around the anomaly to help find the root cause](../task/hla-op-surrounding-logs-view.md).
-   **Configuration Items**

    To view more detailed information on the CI that is associated with the alert, click the **Configuration Items** tab or click **View more** in the Configuration Items section. See [Operator phase 1: Analyze and acknowledge an alert](../../event-management-operator/task/operator-phase-acknowledge-analyze.md).

-   **Impacted services**

    To view detailed information on the services that are impacted by the alerts, click the **Impacted services** tab. See [Operator phase 1: Analyze and acknowledge an alert](../../event-management-operator/task/operator-phase-acknowledge-analyze.md).

-   **Anomaly**

    The Anomaly card illustrates the anomalous activity that led to the alert.

    -   The blue line shows the recent anomalous activity.
    -   On some charts, the lightly shaded area indicates the expected \(learned baseline\) behavior.

        A peach-shaded area represents the baseline values for the same hour one day earlier. A pink-shaded area shows the values for the same period in the previous week.

    -   Click the information icon to see how the anomaly was identified: ![Information icon](../image/icon-info.png).
    In this example, the peach-shaded area shows the same data for the same hour one day earlier. The spike in the metric value \(events per minute\) is clearly visible.

    ![Anomaly card identifies and illustrates anomalous behavior.](../image/anomaly-spike.png "Anomaly card")

    In this example, the pink-shaded area represents the baseline values for the same hour in the previous week.

    ![Baseline values for same hour in previous week.](../image/anomaly-week-earlier.png "Anomaly card with baseline values one week earlier")

    For more information on the kinds of anomalies that you might encounter, see [Types of anomalous behavior in Health Log Analytics](hla-op-anomalous-behavior-types.md).

-   **Meaningful log properties**

    On the Meaningful log properties card, each bar chart shows the distribution of values for a single log property that contributed to the anomaly. Each property value is associated with a color. The length of a color bar correlates to the percentage that the property value holds in comparison with all other values for the property. For the **p\_a5** property in the example, the value **EUR** appeared in 56.12% of log lines, **GBP** in 13.67%, and so on.

    ![Meaningful log properties shows the relative frequency of occurrence for property values.](../image/meaningful-log-properties-card.png "Meaningful log properties")

-   **Top alerts**

    The Top alerts card displays summaries of data from the **Similar alerts** and **Repeated alerts** tabs. The Total results value is the sum of the two values. Click **More details** to open the **Alert Insight Similar Alerts** tab. For details, see [Information on the Alert Insight Similar Alerts tab](hla-op-alrt-inst-simlr-alrts-tab.md).

    ![Top alerts shows counts of total, similar, and repeated alerts.](../image/top-alerts-card.png "Top alerts")

-   **Top incidents**

    The Top incidents card displays summaries of data from the **Incidents on CI** and **Incidents on related CIs** tabs. The Total results value is the sum of the two values. Click **More details** to open the **Incidents on CI** tab.

    ![Top incidents shows counts of total results, incidents on CI, and incidents on related CIs.](../image/top-incidents-card.png "Top incidents")


**Parent Topic:**[Sections and cards on the alert Overview tab in Health Log Analytics](../../health-log-analytics-admin/concept/hla-alert-overview-tab.md)

