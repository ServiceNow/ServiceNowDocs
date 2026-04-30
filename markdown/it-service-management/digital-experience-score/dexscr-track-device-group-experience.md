---
title: Track experience scores of an individual device group
description: Track and drill down into the quantitative and qualitative data of a device group's metrics to gain a comprehensive view into employee experiences of using the devices.
locale: en-US
release: yokohama
product: Digital Experience Score
classification: digital-experience-score
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Tracking digital experience using Digital Experience Score​ dashboard, Digital Experience Score​, Digital End-User Experience, IT Service Management]
---

# Track experience scores of an individual device group

Track and drill down into the quantitative and qualitative data of a device group's metrics to gain a comprehensive view into employee experiences of using the devices.

## Before you begin

Role required: sn\_dex\_score.digital\_workplace\_leader or sn\_dex\_score.dashboard\_user

## Procedure

1.  Navigate to **All** &gt; **Digital Experience Score** &gt; **Dashboard**.

2.  On the Digital Experience Overview page, determine the time period for which you want to review the experience scores.

    1.  Either accept the default period as **Weekly** or select **Monthly** from the drop-down list.

    2.  Either accept the default values for the current week or month or select a different value from the drop-down list.

    For more information about data collection and when the data is available on the dashboard, see [Data collection frequency for DEX Score metrics](../reference/dexscr-metric-data-load.md).

3.  Display the scores for a specific location by starting to type the location in the search field and selecting it from the drop-down list.

4.  Select the **Device experience** tile.

5.  View the Device groups list page by selecting either a number in the **No. of device groups** column or the **View all device groups** link.

    ![Device groups list page displaying names of operating systems installed on devices, experience scores, and the number of devices on which the operating systems are installed.](../image/dex-score-device-grp-list.png)

6.  Review device experience scores to assess device performance and possible areas of improvement.

    1.  On the Device groups list page, select an operating system from the **Operating system name** column.

    2.  On the device group experience score page, display background information on the metrics by selecting the **See how it's calculated** link:

        -   Definitions of scores
        -   How the experience score is calculated
        -   How normalized scores for application metrics are calculated
    3.  View application health, employee feedback, and service experience scores.

<table id="table_rrv_1cr_dfc"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Device health metrics

</td><td>

The device's performance and overall health.Device health metrics are categorized as Good, Average, or Poor. The **All device health metrics** section provides access to a list of corresponding metrics, metric values and scores, and devices that have average or poor metric values for the selected health category.

The **Suboptimal devices** column shows the number of devices with average or poor metric values. For example, for a device metric in the Poor health category, a suboptimal device count of **3 \(of 3\)** indicates that three out of a total of three devices in the device group have poor metric score.

</td></tr><tr><td>

User sentiment

</td><td>

Employee satisfaction received as responses to surveys sent to them periodically. Identify what is going well and possible areas for improvement for the device.

</td></tr><tr><td>

Service experience

</td><td>

Employee satisfaction with the service desk's quality and speed of support for the device shown through the number of incidents and outages and service level agreement \(SLA\) KPIs.Service experience is categorized as Good, Average, or Poor. Selecting a health category in this section displays a list of corresponding metrics and their values.

</td></tr></tbody>
</table>7.  Review experience scores by device to identify device-specific performance issues.

    1.  On the Device groups list page, select the number in the **No. of devices** column for an operating system.

    2.  On the operating system device list page, view names of devices on which the operating system is installed and the experience score for each device.

    3.  View device health details by selecting a device name in the **Device** column.

        For more information about the device health page, see [Device health page](../../digital-end-user-experience/reference/user-health-card.md).


**Parent Topic:**[Tracking digital experience using Digital Experience Score​ dashboard](../concept/dexscr-using-dex-score.md)

**Related topics**  


[Metric scores in Digital Experience Score​](../concept/dexscr-dex-score-defs.md)

[Track device experience score](dexscr-track-device-experience-score.md)

[Track application experience scores](dexscr-track-app-experience-score.md)

[DEX Score metrics calculation](../reference/dexscr-dex-score-metrics-calc.md)

[DEX Score normalization for metric scores](../reference/dexscr-dex-score-normalization.md)

