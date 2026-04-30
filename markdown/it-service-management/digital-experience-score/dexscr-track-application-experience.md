---
title: Track experience scores of an individual application
description: Track and drill down into the quantitative and qualitative data of an application's metrics to gain a comprehensive view into employee experiences of using it.
locale: en-US
release: yokohama
product: Digital Experience Score
classification: digital-experience-score
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Tracking digital experience using Digital Experience Score​ dashboard, Digital Experience Score​, Digital End-User Experience, IT Service Management]
---

# Track experience scores of an individual application

Track and drill down into the quantitative and qualitative data of an application's metrics to gain a comprehensive view into employee experiences of using it.

## Before you begin

Role required: sn\_dex\_score.digital\_workplace\_leader or sn\_dex\_score.dashboard\_user

## Procedure

1.  Navigate to **All** &gt; **Digital Experience Score** &gt; **Dashboard**.

2.  On the Digital Experience Overview page, determine the time period for which you want to review the experience scores.

    1.  Either accept the default period as **Weekly** or select **Monthly** from the drop-down list.

    2.  Either accept the default values for the current week or month or select a different value from the drop-down list.

    For more information about data collection and when the data is available on the dashboard, see [Data collection frequency for DEX Score metrics](../reference/dexscr-metric-data-load.md).

3.  Display the values for a specific location by starting to type the location in the search field and selecting it from the drop-down list.

4.  Select the **Application experience** tile.

5.  On the Application Experience Overview page in the **Application by experience** section, access a list of applications by selecting either a number in the **No. of applications** column or the **View all applications** link.

    ![Applications list page displaying the installed and web applications, application experience scores, and the number of devices on which applications are installed.](../image/dex-score-app-list.png)

6.  Review the experience scores for an application to assess application performance and possible areas of improvement.

    1.  On the Applications list page, select either the **Installed applications** or **Web applications** tab.

    2.  Select an application from the **Application name** column.

    3.  On the application experience score overview page, display background information on the metrics by selecting the **See how it's calculated** link:

        -   Definitions of scores
        -   How the experience score is calculated
        -   How normalized scores for application metrics are calculated
    4.  View application health, employee feedback, and service experience scores.

<table id="table_rsl_f1p_cfc"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application health metrics

</td><td>

The application's performance and overall health.Application health metrics are categorized as Good, Average, or Poor. The **All application health metrics** section provides access to a list of corresponding metrics, metric values and scores, and devices that have average or poor metric values for the selected health category.

The **Suboptimal devices** column shows the number of devices with average or poor metric values. For example, for CPU usage metric in the Average health category, a suboptimal device count of **40 \(of 50\)** indicates that of the 50 devices on which the application is installed, 40 devices have average or poor CPU usage metrics.

</td></tr><tr><td>

User sentiment

</td><td>

Employee satisfaction received as responses to surveys sent to them periodically. Identify what is going well for employees and possible areas for improvement for the application.

</td></tr><tr><td>

Service experience

</td><td>

Employee satisfaction with the service desk's quality and speed of support for the application shown through the number of incidents and outages and service level agreement \(SLA\) KPIs.Service experience is categorized as Good, Average, or Poor. Selecting a health category in this section displays a list of corresponding metrics and their values.

</td></tr></tbody>
</table>7.  Review application experience scores by device to identify device-specific performance issues.

    1.  On the Applications list page, select the number in the **No. of devices** column for an application.

    2.  On the application device list page, view the names of devices on which the application is installed and the application experience score for each device.

    3.  View device health details by selecting a device name in the **Device** column.

        For more information about the device health page, see [Device health page](../../digital-end-user-experience/reference/user-health-card.md).


**Parent Topic:**[Tracking digital experience using Digital Experience Score​ dashboard](../concept/dexscr-using-dex-score.md)

**Related topics**  


[Metric scores in Digital Experience Score​](../concept/dexscr-dex-score-defs.md)

[Track application experience scores](dexscr-track-app-experience-score.md)

[Track device experience score](dexscr-track-device-experience-score.md)

[DEX Score metrics calculation](../reference/dexscr-dex-score-metrics-calc.md)

[DEX Score normalization for metric scores](../reference/dexscr-dex-score-normalization.md)

