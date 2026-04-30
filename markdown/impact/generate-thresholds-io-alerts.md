---
title: Generate thresholds for key alerts
description: For an instance where critical alerts have already been configured you can obtain improved thresholds to receive enhanced or minimal alerts.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Key alerts – activation and notifications, Alerts in Instance Observer, Overview of Instance Observer, Platform Health, Using Impact, Impact]
---

# Generate thresholds for key alerts

For an instance where critical alerts have already been configured you can obtain improved thresholds to receive enhanced or minimal alerts.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Instance Observer** &gt; **Alerts** &gt; **Configure alerts**.

    ![Shows the Generate Threshold button in the Configure Alerts banner.](../image/threshold-banner-io.png)

    A notification banner displays. If the banner prompts to configure alerts, see [Configure Key Alerts](configuring-io-alerts.md).

2.  Select **Generate Threshold**.

3.  Select up to five alerts from the **Max alerts per day / per metric** drop-down to receive for each metric per day.

    The maximum number of alerts selected pertains to each of the six available system metrics. If you choose a maximum of two alerts for each metric, then you receive 12 alerts, as the maximum alert count each day, for example \(2 alerts\) X \(6 metrics\) = 12 alerts. The alert count resets daily at 00:00 UTC.![Shows the alerts threshold configuration screen.](../image/threshold-alerts.png)

4.  Select **Submit**.

    A confirmation message displays.

    ![Shows the alert confirmation screen.](../image/threshold-saved.png)

5.  Navigate to **Edit Alert Configuration**.

    An informational blue banner displays with a recommended alert configuration.

    ![Shows the Alert Condition Configuration screen.](../image/config-alert-condition.png)

6.  Select the **Configure Alert Condition** banner.

7.  Select **Save**.

8.  Repeat these steps for the remaining alerts.

    **Note:** If an alert condition banner isn’t available for any of the six alert conditions, then threshold data aren’t available for that specific metric at this time. Thresholds are regularly refreshed, and the recommendations become available.

9.  After alerts are enabled with the recommended thresholds, the details can be updated manually.
10. Select **Configure Alert Condition** for a selected metric.

11. While editing an Alert Configuration, select **Change Alert Count**.![Shows the Change Alert Count option.](../image/change-alert-count.png)

12. Select a maximum alert value of up to five and select **Submit**.![The Change alert count metrics option.](../image/change-alert-count-config.png)

    After the change is submitted, the pre-calculated threshold is fetched based on the new maximum alert count for the specific metric. You’re returned to the Edit Alert Configuration window.

13. Select **Save** on the Edit Alert Configuration window to apply the changes.

14. Repeat the same process for each alert to edit additional metrics alert configurations.

    **Note:** If you choose three max alerts per day, then you may receive up to three Alerts notification per day for that specific metric. The alert count resets daily at 00:00 UTC.


