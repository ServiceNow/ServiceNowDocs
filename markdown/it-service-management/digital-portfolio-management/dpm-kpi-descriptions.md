---
title: Update KPIs in Digital Portfolio Management
description: You can update the key performance indicator \(KPI\) fields in Digital Portfolio Management \(DPM\). The KPI data is shown in the DPM Workspace.
locale: en-US
release: xanadu
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: task
last_updated: "2024-10-24"
reading_time_minutes: 3
breadcrumb: [Configure KPI groups in Digital Portfolio Management, Configuring Digital Portfolio Management, Digital Portfolio Management, IT Service Management]
---

# Update KPIs in Digital Portfolio Management

You can update the key performance indicator \(KPI\) fields in Digital Portfolio Management \(DPM\). The KPI data is shown in the DPM Workspace.

## Before you begin

Role required: sn\_dpm.dpm\_admin

## About this task

This procedure accesses KPIs via the KPI group in DPM. To see a list of all KPI indicators without the context of its parent KPI group, enter `sn_team_perf_kpi_group_m2m_pa_indicators.list` in the Filter navigator, and then press **Enter**.

## Procedure

1.  Navigate to **All** &gt; **Digital Portfolio Management** &gt; **KPI Groups**.

2.  Open a KPI group to view its details.

3.  On the KPIs related list \(tab\), select the item in the **Label** column to open it.

    **Note:** Be sure to select the item in the **Label** column and not in the **KPI** column.

4.  On the form, update the fields.

<table id="table_ijw_gfx_msb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

KPI Group

</td><td>

Name of the KPI group.

</td></tr><tr><td>

KPI

</td><td>

Name of the Performance Analytics \(PA\) indicator.

 **Note:** The KPI field pulls information from the Indicator table \[pa\_indicators\].

</td></tr><tr><td>

Label

</td><td>

The KPI label shown in the DPM Workspace.

</td></tr><tr><td>

Parent KPI

</td><td>

The Parent KPI for the KPI.

</td></tr><tr><td>

Display aggregate

</td><td>

The method for how KPIs are displayed in the DPM Workspace. The entry can be Average or Sum.**Note:** This field applies when the latest score property \[sn\_dpm.kpi\_groups.show\_latest\_score\] is set to false. For information, see [Configure the Digital Portfolio Management experience](dpm-configure-experience.md).

</td></tr><tr><td>

Order

</td><td>

The order the KPI is displayed within the KPI group.

</td></tr><tr><td>

Description

</td><td>

The description of the KPI.

 In the DPM Workspace, selecting the tooltip on the KPI card reveals the description. You access the KPI cards in the following areas:

-   On the Run tab for services, service offerings, business applications, and application services.
-   On the Overview tab for portfolios and taxonomy nodes.
For more information on the data shown in KPI charts and graphs, see [KB1123710](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637474).

</td></tr><tr><td>

Chart type

</td><td>

The chart type for the KPI group. The options are:

-   **Single score**
-   **Time series: Line**
-   **Time series: Column**
-   **Time series: Area**
-   **Time series: Spline**
-   **Time series: Step line**
-   **Group By**
**Note:** The **Group By** option enables you to select the results breakdown. For example, incidents by priority.

</td></tr><tr><td>

Time range

</td><td>

The time range for the KPI to display. -   Last 7 days
-   Last 30 days
-   Last 90 days
-   Last 180 days


</td></tr><tr><td>

Active flag

</td><td>

The flag that determines if the KPI displays in the KPI group. KPI groups can display in several places in the DPM Workspace — The enterprise portfolio page, the Overview tab of portfolios and nodes, and the Run tab of services and offerings, business applications, and application services. The flag for all KPIs that come with the base system is set to active. As an admin, you can clear the flag so it's inactive.

 -   When checked, the flag is active and the KPI displays in the KPI group.
-   When cleared, the flag is inactive and the KPI doesn't display in the KPI group.
**Important:** Two KPIs can use the same indicator. If both indicators are in a KPI group that is displayed, then both show the same indicator in the KPI groups. If one KPI is set to inactive, then that one is hidden from display, but the other one still displays.

</td></tr></tbody>
</table>5.  Select **Update**.


**Parent Topic:**[Configure KPI groups in Digital Portfolio Management](../concept/dpm-configure-kpi-groups.md)

**Related topics**  


[KPI groups in Digital Portfolio Management](../concept/dpm-configure-kpi.md)

