---
title: Configure the Analytics and Reporting Solution for Employee Relations
description: Run diagnostics, review and customize components, and start collecting data.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Analytics and Reporting Solutions for Employee Relations, Employee Relations, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure the Analytics and Reporting Solution for Employee Relations

Run diagnostics, review and customize components, and start collecting data.

## Before you begin

A ServiceNow AI Platform administrator must have installed the content pack plugins or ServiceNow Store application for this Platform Analytics Solution.

Role required: pa\_admin

## Procedure

1.  Run diagnostics on all records.

    These diagnostics can catch many mismatches between the configuration of your Platform Analytics Solutions and your tables. For more information, see [Performance Analytics diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/self-diagnostics.md).

2.  Navigate to **All** &gt; **Performance Analytics** &gt; **Administration Console**.

3.  Select the **Dashboards** link in the **Explore and Manage** tile.

4.  Verify the Employee Relations Executive Overview dashboard that are installed with this Platform Analytics Solution.

5.  Open the **Indicator Sources** tab.

6.  For each dashboard included in this Platform Analytics Solution:

    1.  Filter the indicator sources on the dashboard name.

        Here you see the indicator sources filtered on the Self-Service Analytics dashboard from the Employee Relations Executive Overview.

        ![Indicator Sources tab of the PA Admin Console listing indicator sources and their details within the Employee Relations Executive Overview dashboard.](../../../reuse/images/hr-er-admin-console.png)

    2.  Review the facts table, conditions, and frequency of the indicator sources compared to the data structure on your own instance.

        **Important:** Pay particular attention to time stamp fields such as Resolved or Created that are referenced in the **Conditions** field. You may need to use different time stamp fields.

    3.  If necessary, open an indicator source and make corrections.

    4.  If you are editing an indicator source record, go to the Indicators related list and review the **Conditions** field for each indicator.

        Changing the indicator source can also affect the additional conditions on the individual indicators.

7.  If you changed the time field stamps in any indicator sources, then change any related Performance Analytics scripts.

8.  Open the Breakdown Sources tab.

9.  For each dashboard included in this Platform Analytics Solution:

    1.  Filter the breakdown sources on the dashboard name.

    2.  Review the conditions on the breakdown source.

10. Navigate to **All** &gt; **Performance Analytics** &gt; **Jobs**.

11. Set up and run the historical job for this Analytics and Reporting Solution, **ERCases.HistoricalDataCollection**.

12. Edit and activate the scheduled data collection job for this Analytics and Reporting Solution, **ERCases.DailyCollection**.


