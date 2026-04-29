---
title: Navigating the Usage Insights application
description: Understand how to navigate the Usage Insights application, including the All Applications and individual application views.
locale: en-US
release: australia
product: User Experience Analytics
classification: user-experience-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Exploring Usage Insights, Usage Insights, Platform Analytics]
---

# Navigating the Usage Insights application

Understand how to navigate the Usage Insights application, including the **All Applications** and individual application views.

Users with any Usage Insights viewer role can access the application by navigating to **All** &gt; **Platform Analytics** &gt; **Usage Insights**.

Different users have different rights and privileges in the Usage Insights application. For more information, see [Roles installed with Usage Insights](../reference/components-installed-user-exp-analytics.md).

## All Applications view

When you launch Usage Insights, there are two tabs: Overview and Events. The Overview tab allows you to view aggregate usage within a given time frame across all of your tracked applications. There are a number of filters you can configure to see scores for Active users, Sessions, and Average session duration, as well as a list showing usage by individual application. The Events tab enables you to filter a list of tracked user interactions across enabled Usage Insights applications.

![GIF alternating the Overview and Events tabs of the UXA application](../image/uxa-overview-tabs.gif)

## Metrics across all applications

You can view basic application usage and event details for all applications within an instance. Select **All Applications** from the applications list to see these metrics simultaneously.![See basic metrics for all applications within an instance](../image/uxa-overview-all-apps-australia.png)

|KPI|Description|
|---|-----------|
|Total Active Users|Total number of users, including new users, whose first session occurred within the specified time period.|
|Sessions|Total number of sessions that have occurred, and average number of sessions per day.|
|Average Screens/Session|Average number of pages or screens viewed and actions performed per session.|
|Avg. Session Duration|Average time spent across sessions for all users.|
|Total Sessions|Total number of sessions performed daily, weekly, and monthly.|
|Users|Total number of daily, weekly, and monthly active and new users.|
|New / Returning Users|Percentage of users whose first session occurred within the specified time period, and percentage of those users who subsequently started a second session.|
|App Versions|App versions installed by users for the selected platform\(s\).|
|App Version Adoption|Shows session segmentation between different versions of the app. For example, if a new app version was released yesterday, and today shows 10% of all app sessions, the current adoption of the new app version is 10%.|
|Session Duration|Percentages of sessions segmented by their length/duration.|
|Hourly Usage|Average number of app launches that occurred at a specific hour of the day over all days.|

## Individual application view

The individual application view has more detailed information for a specified application.

The Analysis menu items provide access to the Retention, Cohort analysis, Conversion funnel, and Navigation paths modules. The Data Foundation menu items provide access to the Users, Sessions, Events, and Pages modules.

|Module|Description|
|------|-----------|
|Retention|Visualize new users and their rates of return and periods between visits. For more information, see [User retention](view-retention-analytics.md#).|
|Cohort analysis|Create and analyze custom cohorts or groups of users separated from other users by similar traits or actions. Analyze how many users perform specific sequences of actions, and how often they return to perform specified actions over a given time. For more information, see [Cohort analysis in Usage Insights](uxa-cohorts.md).|
|Conversion funnel|Create funnel reports to analyze user completion rates for a specific task. View conversion rates, the number of users progressing from one step to the next and the average time for users to advance to each step and complete the funnel. For more information, see [Funnel reports in Usage Insights](funnel-reports-uxa.md).|
|Navigation paths|Visualize users' journeys through your application, discovering the most and least popular paths. For more information, see [Navigation paths](view-navigation-paths.md).|

|Module| |
|------|---|
|Users|A list of users that you can filter, drill down into, and export.|
|Sessions|A list of sessions that you can filter, drill down into, and export.|
|Events|A list of user interactions such as page navigation and clicks that you can filter, drill down into, and export.|
|Pages|A list of visited pages on your instance that you can filter, drill down into, and export.|

![UXA overview - Service Portal application](../../../use/par-for-workspace/image/uxa-overview-sp-app.png)

<table id="table_fvx_5y2_wjb"><thead><tr><th>

Feature area

</th><th>

UI component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

Applications list

</td><td>

List of registered web and mobile applications. You can select from these views:-   **All Applications** \(default landing page\) shows basic statistics across all applications within the current instance.
-   Select an individual application to view usage insights for that application in detail.

</td></tr><tr><td>

2

</td><td>

Selected dashboard menu item

</td><td>

The Overview, Analysis, or Data Foundation item you've selected. In the example, **Overview** is selected.

</td></tr><tr><td>

3

</td><td>

Filters

</td><td>

Default filters you can use to limit the data, including Date Range, User type, and location. Use the **Add Filter** option to add more filters to the page. For more information, see [Filter data in Usage Insights](../task/filter-user-list.md).

</td></tr><tr><td>

4

</td><td>

Total active users

</td><td>

Shows Active users, new users, and the average number of sessions per user. Select any visualization in this section to view the trend analysis for Active users.

</td></tr><tr><td>

5

</td><td>

Total sessions

</td><td>

Shows the total number of sessions, the average page views per session, and the average session duration. Select any visualization in this section to view the sessions trend analysis.

</td></tr><tr><td>

6

</td><td>

Top pages

</td><td>

List of pages with the most views and most sessions. Select any entry in the list to dive into the views and related information.

</td></tr></tbody>
</table>**Note:**

-   Counters in the Usage Insights application contain aggregated user numbers.
-   If a country’s tracking consent policy is set to **Disabled**, user metrics are not tracked.
-   The sampled data represents 5-10% of the total data that is collected in real time.

**Parent Topic:**[Exploring Usage Insights](../content-framework/concept/exploring-user-exp-analytics.md)

