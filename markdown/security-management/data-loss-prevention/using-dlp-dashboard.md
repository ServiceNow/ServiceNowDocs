---
title: Data Loss Prevention Incident Response Dashboard
description: The Data Loss Prevention Incident Response \(DLP IR\) Dashboard provides a high-level overview of your DLP incidents and daily incidents trends in your instance in the form of graphical charts. These charts help you effectively view, manage, and remediate the DLP incidents.Access the Data Loss Prevention Incident Response \(DLP IR\) dashboard to analyze the daily trends in your DLP incidents and effectively remediate them.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage incidents, Data Loss Prevention Incident Response, Security Operations]
---

# Data Loss Prevention Incident Response Dashboard

The Data Loss Prevention Incident Response \(DLP IR\) Dashboard provides a high-level overview of your DLP incidents and daily incidents trends in your instance in the form of graphical charts. These charts help you effectively view, manage, and remediate the DLP incidents.

The Data Loss Prevention Incident Response dashboard provides key insights about your DLP incidents daily. You can set up indicators and regularly collect data snapshots of the incidents matching the conditions in the indicator properties. The collected data is then visualized using widgets in the dashboard. To analyze the DLP incidents in different time intervals, you can apply different date ranges.

**Parent Topic:**[Data Loss Prevention Incident Response Incident Management](../task/data-loss-prevention-incident-management.md)

**Related topics**  


[Data Loss Prevention Incident Response User Workspace](using-dlp-end-user-portal.md)

[Data Loss Prevention Incident Response Analyst Workspace](using-dlp-ops-portal.md#)

## Analyze daily incident trends in your DLP incidents

Access the Data Loss Prevention Incident Response \(DLP IR\) dashboard to analyze the daily trends in your DLP incidents and effectively remediate them.

### Before you begin

Role required:

-   sn\_dlir.analyst - Edit and View DLP incidents.
-   sn\_dlir.analyst\_read and sn\_dlir.read - View DLP Incidents.

### About this task

You can visualize the daily trends using widgets in the DLP dashboard. The data or statistics for the daily trends of your DLP incidents are collected from the daily incidents indicator properties that are defined by your organization. You can gain key insights by applying different data ranges to analyze the DLP incidents in different time intervals for the following charts:

-   **Daily New incidents**: Data of the overall DLP incidents created daily irrespective of the incidents' state. The DLP incidents are categorized based on the severities, including Medium, Critical, High, and Low. Each DLP incident severity is represented by a particular color on the chart.
-   **Daily New vs Closed incidents**: The different states of the DLP incidents and a comparison between the daily new incidents and daily closed incidents. The Daily New category includes all the DLP incidents in Open, Draft, Escalated, In Review, Overdue, Reported, Responded, or Custom \(if any\) states. The Closed incident category includes the closed DLP incidents. Each DLP incident state is represented by a particular color on the chart.
-   **Daily Average Lifetime of incidents**: The lifetime of an incident is the time period between the opening and closing of a specific DLP incident. The daily average lifetime is calculated only for the closed DLP incidents.
-   **Daily False Positive incidents**: Data of all the DLP incidents reported as daily false positives. The daily false positive incidents are categorized based on the severities, including Medium, Critical, High, and Low. Each daily false positive incident severity is represented by a particular color on the chart.
-   **Age vs Severity of incidents**: Data comparison of all the DLP incidents, categorized by the age and configured with the severity of the DLP incidents. The Age category includes all the DLP incidents under the age that your organization defines. For more information on Age charts, see [Create age chart configurations](../task/configure-age-chart.md). The Severity of incidents includes all the DLP incidents in the High or Low category. Each severity is represented by a particular color on the chart.
-   **Daily Escalated incidents**: Data of all the escalated DLP incidents daily. The daily escalated incidents are categorized based on the severities, including Medium, Critical, High, and Low. Each daily escalated incident severity is represented by a particular color on the chart.

### Procedure

1.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Dashboard**.

    The My DLP Dashboard page is displayed in a new browser tab.

2.  Select a dashboard widget for which you want to perform a daily trend analysis.

    For example, the Daily New Incidents chart.

3.  Review the dashboard widgets to identify trends.

4.  Click **Date Range**.

    ![DLP Dashboard overview page.](../image/dlp-dashboard-overview.gif "DLP Dashboard Overview")

5.  Select a date range from the calendar, and click **Apply**.

    For example, the Daily New Incidents chart gets updated for the selected data range.

6.  Use the filters below the chart to drill down and perform a more in-depth analysis.


