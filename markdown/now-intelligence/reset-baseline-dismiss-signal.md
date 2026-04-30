---
title: Reset baseline or dismiss signal
description: When you get a signal that abnormal variation has occurred, either dismiss the signal or recalculate the parameters.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [KPI Signals, Platform Analytics]
---

# Reset baseline or dismiss signal

When you get a signal that abnormal variation has occurred, either dismiss the signal or recalculate the parameters.

## Before you begin

Role required: You must be a [responsible user](../concept/kpi-signals-responsible-users.md#), unless you have the admin, pa\_admin, or pa\_kpi\_signal\_admin role.

## About this task

Investigate the reason for the variation before deciding to reset the baseline or dismiss the signal. If you determine that the signal represents a "new normal," recalculate the baseline. If you determine that the signal is the result of a temporary circumstance, dismiss the signal.

## Procedure

1.  Open KPI Signals from KPI Details.

    In the KPI Details page for an indicator, you see a notification dot on the KPI Signals tab. This dot tells you that you have a signal for the indicator. ![Open KPI Signals icon with notification dot](../../performance-analytics/image/kpi-signals-notification-dot.png)

    **Note:** KPI Signals can detect signals for an indicator that is filtered on one first-level breakdown element. It does not support multiple elements or second-level breakdowns.

2.  Examine the signal and investigate the business reasons behind this variation in process behavior.

    -   If you determine that the signal shows a temporary change in behavior, click **Dismiss signal**. A temporary change in behavior may be due to a temporary change in circumstances, or due to a problem you are able to quickly correct.
    -   If you determine that the signal shows a long-term, real change in the process behavior, click **Reset baseline**.
3.  If you recalculate the baseline, fill in the following fields:

<table id="table_gby_fyh_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reset from date

</td><td>

The date from which to begin calculating the new baseline. By default, this date is the first date of the signal. If the signal is irregular or followed immediately by more variation, consider a later start date.

</td></tr><tr><td>

Number of scores for baseline calculation

</td><td>

The default number of scores for calculating the baseline depends on the indicator frequency. Do not change this number unless you are confident you have good reasons. The minimum number is five.

</td></tr></tbody>
</table>4.  Whether you dismiss the signal or reset the baseline, give the reason for your decision.

    A required field labeled **What has changed?** appears in the KPI Signals panel. Briefly describe the results of your investigation into the signal.

    The reason for your decision appears when you view **Past** signals. It is key information for deciding whether to revert a signal dismissal or baseline reset.

5.  Click either **Dismiss signal** or **Confirm**, to dismiss the signal, or reset the baseline, respectively.

    In the dialog for resetting the baseline, you can first click **How does it work?** Doing so opens a window with information about what a baseline reset is and when to perform one.

    ![Explanation of a baseline reset including what, why, and when.](../../performance-analytics/image/kpi-signals-understand-reset.png)


## Result

If you reset the baseline, a message appears that the baseline is reset. You also see whether there is a more recent signal than the one you just handled. You can review the signals that you dismissed and your baseline resets in the **Past** tab.

