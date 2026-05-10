---
title: Orchestration ROI premium reports
description: The premium dashboard provides detailed reports on calculated savings over time.To view the Orchestration ROI premium reports, you must request activation of the Orchestration - ROI Premium \(com.snc.runbook\_automation.roi\_premium\) plugin. The Orchestration - ROI Premium plugin is included with an Orchestration subscription, but must be activated by request.Orchestration ROI premium reports use a Performance Analytics job that must be activated before premium reports can be generated.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Orchestration ROI reports, Orchestration ROI, Orchestration applications, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Orchestration ROI premium reports

The premium dashboard provides detailed reports on calculated savings over time.

The ROI premium reports require the Orchestration - ROI Premium plugin and are built using [Performance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_PerformanceAnalytics.md). The Orchestration - ROI Premium plugin is dependent on the [Performance Analytics - Premium](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_PremiumPerformanceAnalytics.md) plugin which requires a separate subscription.

**Important:** You must activate the Performance Analytics [scheduled collection job](r_OrchestrationROIPremiumDashboard.md#) before Orchestration ROI premium can display data.

To access the ROI premium dashboard, navigate to **Orchestration** &gt; **ROI Reports** &gt; **Premium Dashboard**.

## ROI By Category tab

The ROI By Category tab contains three reports showing the calculated savings over time by category.

![Calculated savings monthly by category](../image/ROICalculatedSavingsReport1.png "Calculated savings monthly by category")

<table id="table_c3q_srz_zs"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ROI - Monthly By Category

</td><td>

Shows the calculated savings each month by category. The chart displays the total calculated savings against the calculated savings for each category.-   **Type**: Column chart
-   **Table**: Detailed Savings Report \[detailed\_savings\_report\]

</td></tr><tr><td>

ROI - By Category

</td><td>

Shows the trend of calculated savings by category.-   **Type**: Spline chart
-   **Table**: Detailed Savings Report \[detailed\_savings\_report\]

</td></tr><tr><td>

ROI - Running Sum 12 month period

</td><td>

Shows the running sum of calculated savings for all categories in the last 12 months. -   **Type**: Area chart
-   **Table**: Detailed Savings Report \[detailed\_savings\_report\]

</td></tr></tbody>
</table>## ROI By Automation Entry

The ROI By Automation Entry tab contains two reports showing the calculated savings over time by automation entry.

![Calculated savings for the current month by automation entry](../image/ROICalculatedSavingsReport2.png "Calculated savings for the current month by automation entry")

<table id="table_d1d_m31_1t"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ROI By Automation Entry

</td><td>

Shows the current month’s calculated savings for each automation entry.-   **Type**: Column
-   **Table**: Detailed Savings Report \[detailed\_savings\_report\]

</td></tr><tr><td>

ROI - By Automation Entry Top 10 List

</td><td>

Shows the top 10 automation entries that have the most calculated savings in the current month.-   **Type**: Scorecard
-   **Table**: Detailed Savings Report \[detailed\_savings\_report\]

</td></tr></tbody>
</table>**Parent Topic:**[Orchestration ROI reports](../concept/c_OrchestrationROIDashboards.md)

## Request Orchestration ROI premium reports

To view the Orchestration ROI premium reports, you must request activation of the Orchestration - ROI Premium \(com.snc.runbook\_automation.roi\_premium\) plugin. The Orchestration - ROI Premium plugin is included with an Orchestration subscription, but must be activated by request.

### Before you begin

The Orchestration - ROI Premium plugin requires the [Performance Analytics - Premium](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_PremiumPerformanceAnalytics.md) plugin, which must be purchased separately.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

3.  On the **Activate Plugin** form, provide the following information.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

What is your target instance

</td><td>

Select the instance that you want to activate the plugin on.

</td></tr><tr><td>

Which plugin would you like to activate

</td><td>

Select the name of the plugin to activate.

 **Note:** If the system doesn't list the plugin you want or if you're activating the plugin on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box and then enter the name of the plugin.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

Select the date and time to activate the plugin.

</td></tr></tbody>
</table>    For example, see the following form to activate the Event Management plugin on an instance named SNC Instance.

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


## Schedule Orchestration ROI calculations for premium reports

Orchestration ROI premium reports use a Performance Analytics job that must be activated before premium reports can be generated.

### Before you begin

Role required: orchestration\_manager, admin

### About this task

The scheduled job required to calculate premium ROI reports is called \[PA ROI\] Historic Data Collection and is installed with the Orchestration - ROI Premium \[com.snc.runbook\_automation.roi\_premium\] plugin. This job is not active by default.

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Data Collector** &gt; **Jobs**.

2.  Search for the \[PA ROI\] Historic Data Collection job.

3.  Select the **Active** check box.

4.  The scheduling options appear for the value selected in the **Run** field.

    For instructions on creating a schedule, see [Create or schedule a data collection job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/t_CreatASchedDataCollJob.md).

5.  To execute the schedule directly from the job definition, click **Execute Now**.

6.  Click **Update**.


