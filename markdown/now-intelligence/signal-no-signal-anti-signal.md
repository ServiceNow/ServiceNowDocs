---
title: Signal, no signal, and anti-signal
description: When KPI Signals detects abnormal variation in the scores of a KPI, it generates a signal. When KPI Signals does not detect abnormal variation for a significant amount of time, it generates an "anti-signal." The anti-signal lets you know that your workflow is under control.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, KPI Signals, Platform Analytics experience, Platform Analytics]
---

# Signal, no signal, and anti-signal

When KPI Signals detects abnormal variation in the scores of a KPI, it generates a signal. When KPI Signals does not detect abnormal variation for a significant amount of time, it generates an "anti-signal." The anti-signal lets you know that your workflow is under control.

Both the presence and absence of signals conveys information:

-   The presence of signals lets you know that a workflow has changed, or at least is not statistically stable.
-   The long-term absence of signals indicates that a workflow is statistically stable. With this information you can decide to launch a process improvement initiative, for example.

**Note:** By default, dashboards that show indicators with KPI Signals enabled have insight cards for signals that get generated. For more information, see [Proactive analytics insights on dashboards](proactive-analytics.md).

## Signals

The KPI Signals application considers the following behaviors to 'signal' special cause variation:

-   **Outlier**

    Every score beyond a three standard deviation \(3-sigma\) upper or lower limit.

-   **Short run**

    Four consecutive scores on the same side of the central line, with three of the scores close to the upper or lower limit. "Close to the limit" is defined as outside two standard deviations.

-   **Long run**

    Seven consecutive scores on the same side of the central line. That is, seven scores in a row all greater than or all less than the average value.


**Note:** The KPI Signals app counts outliers \(dismissed or not\) when calculating whether a short or long run has occurred.

In the following example, you see a "Long run" signal: seven consecutive scores above or below the central line.

![KPI Signals panel open on the KPI Details tab, showing a Long Run signal of seven consecutive scores all greater than or all less than the average value.](../image/kpi-signals-signal.png)

**Note:** The KPI Signals application can detect signals for an indicator with no more than one first-level [breakdown element](../../performance-analytics/concept/performance-analytics-glossary.md#). The application does not support multiple breakdown elements or a second-level breakdown.

## Anti-signals

The application issues an anti-signal when it has not detected a signal for a length of time equal to the following formula:

```
Length of time to calculate the baseline for the KPI * Anti-signal factor
```

The application takes 14 days by default to calculate the baseline for a daily indicator. The default anti-signal factor is two. Thus, the default length of time to detect an anti-signal on a daily indicator is 28 days. For more information about setting the time to calculate a baseline, see [Configure signal detection](../task/configure-signal-detection.md). For more information about setting the anti-signal factor, see [Configure signal notifications](../task/configure-signal-notifications.md).

In this example, the default configuration values apply to a daily indicator. The application has not detected a signal for 28 days, so it shows a 28-day anti-signal.

![KPI Signals showing an anti-signal, where no signals have been detected for an extended period of time](../image/kpi-signals-anti-signal.png)

Although responsible users are notified when an anti-signal is generated, no action is required.

## No signal

Usually no signal is detected for a shorter amount of time than it takes to detect an anti-signal. In this case, the application shows a simple "No signal" message. No notifications are sent and no action is necessary.

In the following example, no signal is detected for five days after the baseline was most recently reset. The baseline has been reset three times in the period being shown.

![KPI Signals showing no signal for a KPI: neither a signal nor an anti-signal](../image/kpi-signals-no-signal.png)

**Parent Topic:**[Exploring KPI Signals](exploring-kpi-signals.md)

