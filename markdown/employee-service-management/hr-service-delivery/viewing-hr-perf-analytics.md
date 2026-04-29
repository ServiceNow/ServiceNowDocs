---
title: Viewing HR Performance Analytics Scoped
description: HR Performance Analytics for the scoped version of HR Service Delivery helps you align resources and systems to strategic objectives.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Performance Analytics for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Viewing HR Performance Analytics Scoped

HR Performance Analytics for the scoped version of HR Service Delivery helps you align resources and systems to strategic objectives.

Before you can view HR Performance Analytics data, your organization must purchase a subscription to Performance Analytics and an administrator activates the plugin.

After activating HR Performance Analytics, the collection job runs daily by default and is configurable. Collected data is kept for 30 days. The data in performance analytics reports is collected based on a daily scheduled job, therefore, the date is one day in the past. Over time, more data is available for historical trending.

-   **Scheduled Data Collection**

    There are two jobs specific to the Performance Analytics - Content Pack - Human Resources Scoped App \[com.sn\_hr\_pa\] plugin:

    -   \[PA HR Case\] Daily Data Collection
    -   \[PA HR Case\] Historic Data Collection
    See [Create or schedule a data collection job](https://www.servicenow.com/docs/access?context=t_CreatASchedDataCollJob&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

-   **Indicators**

    Each job has indicators to make data collection efficient and defines what data to collect.

    See [Configure a job indicator](https://www.servicenow.com/docs/access?context=configure-job-indicator&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

-   **View dashboards**

    After the PA jobs run, you can view the collected data from the **Dashboard**.

    See Dashboards overview.

-   **HR Manager**

    Provides detailed data about open cases that helps managers quickly assign agents and look deeper into opened cases. You can sort this dashboard by assignment group.

    -   You can only filter this dashboard by Groups.
    -   The **Overview** tab provides summaries by backlog of all open cases, average time to resolution, and unassigned opened cases.
    -   The **Operational** tab shows the number of open cases by backlog, critical, breached SL, not updated in the last 10 days, and unassigned open. You can also filter by priority, state, assigned to, topic category, and HR service.
    -   The **Backlog monitor** tab shows the number of all open cases, average reassignment, cases not updated in last 3 days, unassigned, and the average age of open cases. You can also sort by COE, topic category, HR service, assignment group, agent, state, source, or priority and further by type of HR case. The format of the data is interchangeable.
-   **HR Agent**

    Provides detailed data for the logged in HR agent. It provides the number of backlog of open cases, breached SLA cases, approval requests, and unassigned cases.

    Group and stack the opened backlog cases by priority or state .

    You can filter by state, topic category, source, and priority.


The **Performance Analytics** dashboard provides the following reports.

-   **Volume of Open/Closed Cases by Category**

    The line chart shows the trend of open and closed cases for each of the last four weeks. Click a point on a line to see open or closed cases for the duration. The **Breakdowns** tab shows the number of open or closed cases by category. Select **Stacked bar** from the choice list for the best data format.

-   **Active HR Cases per Week - by AVG**

    The bar chart shows the average number of active cases by state for each of the last four weeks. It also shows the total number of cases for each week. The **Breakdowns** tab shows the aging buckets and the total number of cases in each bucket.

-   **Active HR Cases by State**

    The trending chart shows a trend of the cases that moved to each HR case state during the past 30 days. The gray bar to the left of the Trend column represents the proportion of moved cases to the total number of cases. The **Breakdowns** tab shows aging buckets and the number of cases in each bucket for that date.

-   **Active HR Cases Managed by Agent - Weekly AVG**

    The trending chart shows the number of cases assigned to each agent over the past four weeks.

-   **Active HR Cases SLA Indicator per Week- By AVG**

    The bar chart shows the average number of cases that were in each aging bucket for each of the last four weeks. The **Breakdown** tab shows the agent and the number of cases on that date in the selected aging bucket. Select **Column** from the choice list for the best data format.

    1.  Point your cursor to an element, such as a bar or pie segment, to see what the element represents.
    2.  Click a segment to see more details about the element. Scroll up to view the information. The detail contains the following tabs, depending on the selected element.

-   **Chart**: The detail of the element displayed in a chart. You can use the controls on the upper right to add or change comments, targets, and thresholds.
-   **Breakdowns**: The breakdown of the buckets used in the report. Select a chart type from the choice list on the upper right to see the data in another format.
-   Records: The records that comprise the element you selected. You can view the detail of each record.
-   Scores: The number of records for each week in the report.
-   Comments: Comments entered for this report. The tab is disabled unless comments exist.
-   More info: A description of the logic that generates the report, how often the job runs, and when the data was last collected.
-   If a menu icon appears when you point your cursor to a chart, you can click the icon to export the chart to an image file.

For more information about performance analytics and how to develop and modify widgets for your organization, see [Performance Analytics concepts](https://www.servicenow.com/docs/access?context=c_PerformanceAnalytics&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) .

**Parent Topic:**[Performance Analytics for HR Service Delivery](../concept/scoped-hr-performance-analytics.md)

