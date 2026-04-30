---
title: Performance Analytics Admin Console
description: From a single console, administrators can manage Platform Analytics Solution content, manage Performance Analytics widgets and dashboards, diagnose and resolve errors, view usage analytics, modify configuration settings and access ServiceNow help.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Performance Analytics Admin Console

From a single console, administrators can manage Platform Analytics Solution content, manage Performance Analytics widgets and dashboards, diagnose and resolve errors, view usage analytics, modify configuration settings and access ServiceNow help.

**Important:** This admin console does not support Platform Analytics artifacts. It shows information only for Core UI Performance Analytics widgets and responsive dashboards.

Users with the admin or pa\_admin roles can navigate to **Performance Analytics** &gt; **Admin Console**. If Performance Analytics is not enabled, click **Learn More** for information about activating it.

![Performance analytics administration console layout](../image/pa-admin-console-overview-l.png)

-   **![Red number 1 indicating the Content Library tile in the Admin console layout](../image/1.png)Content Library**

    Guided Setup for the Platform Analytics Solutions.

    Click **Plugin List** to show a list of available system plugins for inactive Platform Analytics Solutions.

    **Note:** You must have the admin role to see the list of plugins.

    Click **Guided Setup** to launch guided setup for Platform Analytics Solutions.

-   **![Red number 2 indicating the Content Library tile in the Admin console layout](../image/2.png)Explore and Manage**

    A single place where you can quickly identify and manage the relationships between your Performance Analytics elements and gauge the impact of change. For example, you can identify all the reports, indicators, and interactive filters in a dashboard group that are affected if you change a field name.

    Click **Dashboards** to explore all of the dashboards in your instance sorted by group. Expand the group to view the individual dashboards.

    Click **KPIs** to open the [Analytics Hub](c_UsePerformanceAnalyticsScorecards.md), where you see an exploratory view of your indicators.

    Use [Dependency Assessment](impact-analysis.md) to view, analyze, and manage your Performance Analytics components.

-   **![Red number 3 indicating the Troubleshoot tile in the Admin console layout](../image/3.png)Troubleshoot**

    The **Troubleshoot** panel enables you to utilize diagnostics delivered by the ServiceNow application to investigate tests that result in an Error warning and failed data collection jobs. Out-of-the-box diagnostics run on a schedule, but can also be executed on demand. The Scheduled Data Collection list filters out jobs that are run only once and jobs that are run only on demand.

    **Note:** If either of the numbers on the Troubleshoot card are greater than 0, there may be something wrong with your Performance Analytics implementation.

    -   Click **Diagnostic Errors** to view the Diagnostic Executions list, a summary of how many diagnostic tests were run, and how many issues were found. Use the **State** field to track which issues have been resolved. For more information on diagnostic executions, see [Analytics Diagnostics](self-diagnostics.md#).
    -   Click **Failed Jobs** to view the Scheduled Data Collection list. A failed job is a scheduled job for which the latest complete run is in the state **collected\_error**. For more information on data collection, see [Performance Analytics data collection and cleanup](c_ClctData.md).
-   **![Red number 4 indicating the Usage tile in the Admin console layout](../image/4.png)Usage**

    Dashboards with statistics about data collection jobs and report usage.

    -   Use the **Data Collection Overview** dashboard to track and manage data collection. Note that data collection jobs are not run by default. dashboard widgets do not show data until you run the associated data collection jobs. For more information, see [Performance Analytics data collection and cleanup](c_ClctData.md).
    -   Use the **Reports Usage** dashboard to track and manage report usage. For more information, see [Report statistics](../../reporting/concept/report-statistics.md#).
-   **![Red number 5 indicating the Advanced Configuration tile in the Admin console layout](../image/5.png)Advanced Configuration**

    Quick links to advanced configuration settings.

    -   [Performance Analytics properties](../reference/pa-properties.md)
    -   [Reporting properties](../../reporting/reference/reporting-properties.md)
    -   [Responsive dashboard properties](../../dashboards/reference/dashboard-properties.md)
-   **![Red number 6 indicating the Help tile in the Admin console layout](../image/6.png)Help**

    The community, product documentation, and the video tutorials on the ServiceNow YouTube channel provide additional insights into Performance Analytics functionality.


**Parent Topic:**[Configure Performance Analytics advanced features](c_PADataArchitecture.md)

**Related topics**  


[Interactive Analysis information panel](../../dashboards/concept/interactive-analysis-info-panel.md#)

