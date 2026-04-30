---
title: DevOps Insights reports
description: To help you plan and implement updates to your DevOps processes, DevOps Insights displays a variety of configurable reports that are grouped by type of metric. From the DevOps Change Workspace, select the DevOps Insights icon \( filter icon \) to view the reports.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [DevOps Change Velocity, IT Service Management]
---

# DevOps Insights reports

To help you plan and implement updates to your DevOps processes, DevOps Insights displays a variety of configurable reports that are grouped by type of metric. From the DevOps Change Workspace, select the DevOps Insights icon \(![filter icon](../image/icon-devops-insights.png)\) to view the reports.

## DevOps Insights

Analyze operational and business reports and to determine the overall efficiency  and growth of your  development processes.

-   Monitor activities, KPIs, and metrics in a central dashboard.
-   Track performance over time.
-   View summary data broken out by bug, epic, feature, "other", story, or task.

## Mining and analyzing the metrics

Each report provides both a summary of an important business metric and access to more detailed information about the metric.

-   By default, many reports display data for the last 30 days. Select the **Date** icon \(![Date icon](../image/devops-date-range-filter-pill.png)\) to configure a custom date range.
-   Point to a specific data point in a chart to view detailed data.
-   Select a specific data point to view the key performance indicator \(KPI\) details for the report in a separate tab. You can then use the powerful data-management tools in the [Performance Analytics](https://www.servicenow.com/docs/access?context=pa-overview&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) application to drill deeply into the data.
-   To apply any filter other than the date filter, select the filter icon and then move filter categories from the **Available** list to the **Applied** list.
-   Filters appear at the top of the tab. For each report, the Applied filter icon \(![Applied filter icon](../image/devops-icon-filter-insights.png)\) displays the number of filters that are currently applied to a report. Select the icon to view and configure the filters that are applied to a widget.

## Schedule of data collection

You must enable the daily data collection job to populate the dashboards with new DevOps data coming in from the connected third-party tools.

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Data Collector** &gt; **Jobs**.
2.  Configure the **\[DevOps\] Daily Data Collection** job to run as system admin.

    **Note:** **\[DevOps\] Daily Data Collection** job is active by default and configured to run as admin user.


Run the **Load Change Request Repo Detail** scheduler script and **\[DevOps\] Historical Data Collection** job for historical data:

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
2.  Execute the **Load Change Request Repo Detail** scheduler script.

    This job populates the Change Request Repo Detail table \[sn\_devops\_insights\_change\_request\_repo\_detail\] if you import demo data after installing the DevOps Insights application.

    If you're installing demo data along with the DevOps Insights application, then there’s no need to run this job. You can directly run the **\[DevOps\] Historical Data Collection** performance analytics job to see scores.

3.  Navigate to **All** &gt; **Performance Analytics** &gt; **Data Collector** &gt; **Jobs**.
4.  Execute the **\[DevOps\] Historical Data Collection** job to run as system admin.

    The execution time depends on the volume of data. This is a one-time task to collect historical DevOps data, and not meant to be on a schedule.

    **Tip:**

    Based on the time taken to complete this job, plan on running it during a period of low usage.


