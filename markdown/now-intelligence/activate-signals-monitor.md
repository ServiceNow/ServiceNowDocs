---
title: Activate KPI Signals monitoring for an indicator \(KPI\)
description: KPI Signals does not monitor indicators by default. You activate monitoring for individual indicators. When you activate KPI Signals for an indicator, you make yourself a responsible user for that indicator.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, KPI Signals, Platform Analytics experience, Platform Analytics]
---

# Activate KPI Signals monitoring for an indicator \(KPI\)

KPI Signals does not monitor indicators by default. You activate monitoring for individual indicators. When you activate KPI Signals for an indicator, you make yourself a responsible user for that indicator.

## Before you begin

**Important:** Data snapshots do not support KPI Signals.

Role required: pa\_kpi\_signal\_admin, pa\_admin, or admin

## Procedure

1.  Open KPI Signals for an indicator, as described in [View KPI Signals](view-kpi-signals.md).

2.  If KPI Signals monitoring for the indicator has not been activated, click **Make me responsible** in the KPI Signals panel.

    ![The Make me Responsible button in the KPI Signals panel](../image/kpi-signals-make-self-responsible.png)

    KPI Signals monitoring cannot be active for a indicator unless there is at least one responsible user. Therefore, when you activate monitoring, you automatically make yourself a responsible user. You can then reassign responsibility. For more information, see [Configure responsibility for KPI Signals](../concept/kpi-signals-responsible-users.md#).

3.  Select a start date from which to evaluate the indicator for signals.

    By default, signals are calculated starting three months before you activate KPI Signals for the indicator. If meaningful data for calculating a baseline begins earlier or later than this date, change the date.

    ![The KPI Signals panel after giving yourself responsibility for a KPI, showing fields for resetting start date and number of points to calculate baseline](../image/kpi-signals-start-date-num-points.png)

4.  Set the number of indicator scores that are used to calculate the baseline.

    The default number of scores for calculating the baseline depends on the indicator frequency. Do not change this number unless you are confident you have good reasons. The minimum number is five.

5.  Click **Confirm**.


## What to do next

After you activate KPI Signals monitoring for an indicator, you can:

-   Deactivate monitoring on the indicator
-   Reactivate monitoring if it was deactivated
-   Reconfigure the number of points for calculating the baseline
-   Change the start date for calculating the baseline
-   Change the type of trend calculation for the baseline

For more information, see [Configure signal detection](configure-signal-detection.md).

**Parent Topic:**[Configuring KPI Signals for an indicator](../concept/configuring-kpi-signals.md)

