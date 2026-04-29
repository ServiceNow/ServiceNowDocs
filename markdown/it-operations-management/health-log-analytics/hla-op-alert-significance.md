---
title: Assign higher or lower significance to an alert in Health Log Analytics
description: Label an alert in Health Log Analytics as meaningful or insignificant, or restore normal importance to the metric involved in generating it.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Controlling alert generation, prioritization, and anomaly detection, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Assign higher or lower significance to an alert in Health Log Analytics

Label an alert in Health Log Analytics as meaningful or insignificant, or restore normal importance to the metric involved in generating it.

Assigning higher or lower significance to an alert helps you prioritize the alerts Health Log Analytics generates. Here are some common use cases for adjusting the importance of an alert:

-   Labeling alerts as meaningful: You can make a significant alert more likely to be included in a Log Analytics group when its associated metric behaves anomalously. This ensures that important alerts receive appropriate attention.
-   Muting distracting alerts: You can mute alerts for insignificant issues to reduce noise and avoid being overwhelmed by alerts for minor problems. This enables you to focus on more critical alerts. You can view a list of muted metrics to ensure you are aware of metrics that are no longer generating alerts.
-   Reducing sensitivity to certain anomalies: You can lower the sensitivity of anomaly detection to a specific anomaly. This can help you focus on more significant anomalies.
-   Restoring normal significance: If you previously marked an alert as significant, muted it, or if you lowered sensitivity to certain anomalies, you can return the associated metric to its normal significance. This is useful when you no longer want to treat the alert specially.

You can do the following to adjust the importance of an alert or reduce sensitivity to specific anomalies:

-   [Mark an alert as significant in Health Log Analytics](../task/hla-op-alert-make-significant-sow.md)

    Make an alert more likely to be included in a Log Analytics group when the associated metric behaves anomalously by labeling the alert as meaningful.

-   [Mute an unimportant alert in Health Log Analytics](../task/hla-op-alert-mute-sow.md)

    Eliminate distracting new alerts for insignificant issues by muting them. [View the list of metrics that were muted](../task/hla-op-alert-view-ignored-list.md) and no longer generate alerts.

-   [Decrease sensitivity to similar anomalies in Health Log Analytics](../task/hla-op-alert-raise-feedback-sow.md)

    Make Health Log Analytics anomaly detection less sensitive to anomalies like the one that triggered the current Log Analytics alert.

-   [Restore normal importance to an alert metric in Health Log Analytics](../task/hla-op-alert-restore-user-defined-sow.md)

    Return normal significance to the metric involved in generating a Log Analytics alert.


For detailed information about alert metrics, see [How Health Log Analytics generates alerts](hla-op-anomalies-detecting.md).

-   **[Mark an alert as significant in Health Log Analytics](../task/hla-op-alert-make-significant.md)**  
Make an alert more likely to be included in a Log Analytics group when the associated metric behaves anomalously by labeling the alert as meaningful.
-   **[Mute an unimportant alert in Health Log Analytics](../task/hla-op-alert-mute.md)**  
Eliminate distracting new alerts for insignificant issues by muting them.
-   **[Restore normal importance to an alert metric in Health Log Analytics](../task/hla-op-alert-restore-user-defined.md)**  
If you no longer want a muted alert or an alert that was marked as significant to be treated specially, you can restore normal importance to the metric involved in generating it.

**Parent Topic:**[ITOM AIOps](../../it-operations-management/reference/itom-health-landing-page.md)

