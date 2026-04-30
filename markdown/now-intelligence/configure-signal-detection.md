---
title: Configure signal detection
description: You can set the start date of the current baseline calculation, the number of scores used to calculate the baseline, and the trend method. You also can deactivate or reactivate KPI Signals monitoring for a KPI.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, KPI Signals, Platform Analytics experience, Platform Analytics]
---

# Configure signal detection

You can set the start date of the current baseline calculation, the number of scores used to calculate the baseline, and the trend method. You also can deactivate or reactivate KPI Signals monitoring for a KPI.

## Before you begin

Role required: admin, or must be a responsible user.

## Procedure

1.  Open KPI Signals for a KPI.

2.  Click the cogwheel to open the Configuration options.

    ![KPI Signals panel showing the cogwheel button for opening configuration settings](../image/kpi-signals-open-settings.png)

3.  Open the Signal Detection tab.

    In this image, you see the Number of open incidents indicator with no breakdowns, and the same indicator with the Priority = 1-Critical breakdown and element. The KPI with the Priority = 1-Critical breakdown has been deactivated. Only KPIs that had been activated at some point appear in this list.

    ![List of KPIs on the same Performance Analytics indicator](../image/kpi-signals-config-kpi-list.png)

4.  Select the KPIs that you want to edit.

5.  Fill in the following fields:

<table id="table_brp_vv3_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active \(check box\)

</td><td>

Deselect to deactivate KPI Signals monitoring of the KPI. The KPI remains in the list afterwards. Select**Active** later to reactivate monitoring on the KPI. If you reactivate monitoring on a KPI, it begins from the date you deactivated monitoring, not the date you reactivated it.

</td></tr><tr><td>

Baseline start

</td><td>

The beginning date of the data points used to calculate the baseline. This date is based on the most recent resolved signal. If there never was a resolved signal, the date was set when monitoring on the KPI was first activated.

</td></tr><tr><td>

Number of scores for baseline calculation

</td><td>

The number of scores, or data points, that the application uses to calculate the baseline. The default number of scores for calculating the baseline depends on the indicator frequency. Do not change this number unless you are confident you have good reasons. The minimum number is five.

</td></tr><tr><td>

Trend method

</td><td>

The statistical method for calculating the baseline. Options are:-   Linear trend, calculated by linear regression
-   No trend, just the average score


</td></tr></tbody>
</table>6.  Click **Save**.


## Linear trend versus no trend

In the following example, the initial linear trend kept resulting in signals despite the average remaining stable. Following the signal in early September, signal detection was changed to "no trend." Following this change, the average remained stable and no further signals were detected.![KPI Signals showing no signal for a KPI: neither a signal nor an anti-signal](../image/kpi-signals-no-signal.png)

**Parent Topic:**[Configuring KPI Signals for an indicator](../concept/configuring-kpi-signals.md)

