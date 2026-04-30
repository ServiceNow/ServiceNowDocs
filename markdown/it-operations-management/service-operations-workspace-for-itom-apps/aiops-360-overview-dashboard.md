---
title: AIOps 360 overview dashboard
description: The AIOps 360 Overview dashboard offers a unified view of value and performance across IT operations, helping teams track efficiency, monitor alert handling, and assess automation outcomes. It enhances visibility into AIOps impact, supports informed decisions, and drives faster, smarter operations.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [AIOps Dashboards in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# AIOps 360 overview dashboard

The AIOps 360 Overview dashboard offers a unified view of value and performance across IT operations, helping teams track efficiency, monitor alert handling, and assess automation outcomes. It enhances visibility into AIOps impact, supports informed decisions, and drives faster, smarter operations.

## Prerequisites

Ensure that the Event Management application is installed.

## Required ServiceNow AI Platform roles

-   evt\_mgmt\_admin
-   evt\_mgmt\_operator

## Breakdowns

Breakdowns available in the AIOps 360 overview dashboard are:

-   Value overview
-   Performance overview

## Value overview section

Use filters such as **Date** and **Assignment Group** to customize the dashboard view and focus on specific time periods and teams. This helps you pinpoint trends, identify areas for improvement, and make data-driven decisions tailored to your operational needs.

The Value overview section highlights the overall impact of AIOps on operational efficiency. It showcases how much manual effort has been reduced through automation and intelligent alert grouping. It also reflects noise reduction levels, outage history, and overall workload savings—giving a clear picture of time and cost benefits realized.

![Value overview section in the AIOps 360 overview dashboard.](../image/sow-aiops-360-overview-dashboard-1.png)

<table id="table_qdt_2g1_mfc"><thead><tr><th>

Metrics

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Est. Total time saved

</td><td>

Sum of time saved through alert automation and alert grouping, calculated in hours.

</td></tr><tr><td>

Est. Total time saved by automation

</td><td>

Time saved based on the number of alert automation rules executed multiplied by the mean resolution time per alert, calculated in hours.The mean resolution time can be adjusted by administrators in **All** &gt; **System Properties** &gt; **All Properties**.

Use the **sn\_aiops\_dashboard.ITOM.Dashboard.Avg\_time\_saved\_by\_automation\_in\_min** property to get the actual time saved by automation, in minutes, as used by the Automation Time Saved indicator. By default, it's set to 5 minutes.

</td></tr><tr><td>

Est. Total time saved by grouping

</td><td>

Time saved based on the number of alerts grouped versus the time required to triage each alert individually, calculated in hours.The mean resolution time can be adjusted by administrators in **All** &gt; **System Properties** &gt; **All Properties**.

Use the **sn\_aiops\_dashboard.ITOM.Dashboard.MTTR\_for\_time\_saved\_by\_grouping\_in\_min** property to define the MTTR \(in minutes\) used in the alert grouping time saved calculation. By default, it's set to 5 minutes.

</td></tr><tr><td>

Workload saving

</td><td>

Measures the reduction in manual effort by filtering, grouping, automating alert closures, and preventing incident escalations.-   Events to significant alerts: Percentage of events that were filtered out and did not convert into alerts, reduced through AIOps settings like ignore automations.
-   Grouped alerts: Percentage reduction in the number of stand-alone alerts due to grouping rules defined in alert grouping automations.
-   Auto-closed alerts: Percentage of alerts automatically closed by Respond automation, Clear event actions, or closed as part of alert group resolution.
-   Incident prevention rate: Percentage of alerts resolved successfully without needing escalation to incidents.

</td></tr><tr><td>

Last reported outage

</td><td>

Most recent date of a major outage \(e.g., CMDB\) affecting a service or server, based on reported outages on all classes inherited from cmdb\_ci\_service or cmdb\_ci\_server.

</td></tr><tr><td>

Noise reduction

</td><td>

Percentage effectiveness in ignoring duplicate and meaningless events. Typical customer value exceeds 90%.

</td></tr></tbody>
</table>## Performance Overview section

This section focuses on how effectively alerts and incidents are being handled. It includes metrics like resolution times across groups, trends in detection and response, automation usage, and the distribution of resolution ownership. It helps identify performance gaps, track improvements, and optimize response strategies across the organization.

![Performance overview section in the AIOps 360 overview dashboard.](../image/sow-aiops-360-overview-dashboard-2.png)

<table id="table_lfg_5g1_mfc"><thead><tr><th>

Metrics

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Alert MTTR

</td><td>

Alert resolution time by assignment group to identify slower-responding teams and enforce SLAs. Can also be grouped by severity using the grouping drop-down menu.

</td></tr><tr><td>

Alert MTTx over time

</td><td>

MTTR \(mean time to resolve\), MTTA \(mean time to final group assignment\), and average group reassignment count tracked over time. Indicates assignment efficiency and the ability to resolve alerts within a single group.

</td></tr><tr><td>

Critical alert by CI location

</td><td>

Critical alerts on a geographic map based on the physical or logical location of Configuration Items \(CIs\). Helps identify recurring hotspots for retrospective analysis and to spot regional trends.

</td></tr><tr><td>

Resolution types by assignment groups

</td><td>

Closure reasons by top assignment groups, highlighting automation closures \(within 10 minutes of execution\) to encourage quick resolution, and time threshold closures \(after the auto-close interval\), which indicate unattended alerts.You should consider the number of alerts that are automatically closed when they reach their time limit. This figure can reveal if your team is unable to resolve or close all alerts, leaving some unaddressed.

</td></tr></tbody>
</table>**Note:** If you're starting with Zurich, some charts, graphs, or metrics in the dashboard may appear blank or show limited data. This is expected if there's no historical data or only a few weeks or months of data available. As your system continues to collect and process alerts, the dashboard will populate with more complete insights over time.

If you want to know about funnel visualization, see [Create a funnel visualization](../task/create-funnel-visualization.md).

