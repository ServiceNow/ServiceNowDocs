---
title: Create Process Mining projects for KPI groups in Digital Portfolio Management
description: Create Process Mining projects for each key performance indicator \(KPI\) group in Digital Portfolio Management \(DPM\) to see KPI performance and analyze anomalies.
locale: en-US
release: australia
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Digital Portfolio Management, IT Service Management]
---

# Create Process Mining projects for KPI groups in Digital Portfolio Management

Create Process Mining projects for each key performance indicator \(KPI\) group in Digital Portfolio Management \(DPM\) to see KPI performance and analyze anomalies.

## Before you begin

-   Role required: sn\_process\_optimization\_analyst
-   Enable Process Mining

## About this task

Use Process Mining to analyze and improve KPI performance in DPM.

The KPI assignment group manager must have the required role to create Process Mining projects for their KPI groups: Process Mining analyst \[sn\_process\_optimization\_analyst\].

For information about properties, roles, and scheduled jobs, see [Process Mining components for Digital Portfolio Management](../reference/dpm-po-integration.md).

Several project templates come with the base DPM system:

-   Incident
-   Problems
-   Changes
-   Requests

If you want different templates, then your administrator must create them on the tables that correspond to what you want to see insights for.

A scheduled job runs to remine the projects when additional data is added so that you get the most updated insights for your projects.

## Procedure

1.  Mine the project to create Process Mining projects for each KPI group.

    1.  Navigate to **All** &gt; **Digital Portfolio Management** &gt; **KPI Groups**.

    2.  Open a KPI group that you want to mine for.

    3.  Select **Initiate Process Mining**.

        After you select **Initiate Process Mining**, a project is created in the background for each KPI table in the KPI group. If you’re using a formula indicator for Process Mining, you can select any indicator source that is used in the formula.

        **Note:** The system property **sn\_dpm.enable.po.dpm** must be enabled. For more information, see [Configure Digital Portfolio Management to integrate with Process Mining](../concept/dpm-setup-po.md).

2.  Open the project and check the mining.

    If you don't want users to filter on retired projects, then make sure the project definition status is set to Retired.

    1.  To find the project, navigate to **All** &gt; **Digital Portfolio Management** &gt; **DPM Projects**.

    2.  Check the mining state by opening the project and selecting **Generate model \(Full\)**.

3.  Remine the KPI group again if you added additional assignment groups to the KPI group after you did the process mining.

    1.  In the Assignment Group related list for the selected KPI group, select **Edit**.

    2.  Add the desired assignment group to the KPI group.

    A process is automatically created for the assignment group. If you add an assignment group to the KPI group, then the assignment group is updated in the filter condition. If you remove any assignment group, then it's removed from the project filter condition. An informational message is displayed when an assignment group is added to the KPI group only if the KPI group is already mined.

4.  See the Process Mining insights and variations for selected KPI records.

    1.  Open the DPM Workspace.

    2.  Select the enterprise portfolios icon \(![](../image/enterprise-portfolio-icon-purple.png)\), and then open an enterprise portfolio.

    3.  Select **View Details**.

    4.  Select an incident KPI single score.

        On the KPI drill down page, select the **Process analysis** tab to see the insights and variations for the selected KPI records. By default, the data shown is from the last 30 days.


**Parent Topic:**[Configuring Digital Portfolio Management](../concept/dpm-configure-cfw.md)

**Related topics**  


[Configure Digital Portfolio Management to integrate with Process Mining](../concept/dpm-setup-po.md)

[Process Mining components for Digital Portfolio Management](../reference/dpm-po-integration.md)

