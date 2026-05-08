---
title: Navigating the Usage Insights for Web Embeddable application
description: Learn how to navigate the Usage Insights application to view telemetry data for Web Embeddables. Access user analytics dashboards that display metrics organized by module and page to understand component user interactions across your external websites.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Navigating the Usage Insights for Web Embeddable application

Learn how to navigate the Usage Insights application to view telemetry data for Web Embeddables. Access user analytics dashboards that display metrics organized by module and page to understand component user interactions across your external websites.

Different users have different rights and privileges in the Usage Insights application. Users with any Usage Insights viewer role can access the Web Embeddables application by navigating to **All** &gt; **Platform Analytics** &gt; **Usage Insights**. Select the application name from the All Application list that matches the Web Embeddables module name. Analytics for each Web Embeddables module are tracked separately as individual applications. To track analytics for a module, include the Web Embeddables module ID with the page title in the global embed code.

## All Applications view

When you launch Usage Insights it displays three tabs based on the selected All Applications option:

-   **Overview**

    The Overview tab allows you to view aggregate usage within a given time frame across all your tracked components. There are number of filters you can configure to see scores for Active users, Sessions, and Average session duration, as well as a list showing usage by individual components.

-   **Dashboard**

    Displays dashboards that users create within the Usage Insights application to monitor and analyze usage data. This view shows only dashboards built specifically in Usage Insights, not dashboards from other ServiceNow applications. Access this view only if you have the appropriate roles and permissions for the Usage Insights application.

-   **Events**

    This tab enables you to filter and view tracked user interactions for your Web Embeddables components embedded on third-party websites.


![Dashboard displaying insights from overview, dashboard, and events tabs.](../image/we-analytics.gif "Web Embeddables dashboard overview")

## Metrics across the Web Embeddables module

The Overview tab provides key insights into user activity and engagement for your Web Embeddables components on third-party websites. Track metrics such as total active users, new users, total sessions, average pages per session, and average session duration to understand user behavior. Use this data to assess user engagement levels and identify top pages where your embedded components drive the most activity.

Select your module from the All Applications from the applications list to see these metrics simultaneously.

![Usage Insights Overview dashboard displays key engagement metrics for Web Embeddables modules with filters for date range, user type, user activity, and more.](../image/we-overview-analytics.png)

<table id="table_csm_base_entities"><thead><tr><th>

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

List of registered web and mobile applications. You can select Web Embeddables module from the list.-   **All Applications** \(default landing page\) shows basic statistics across all applications within the current instance.
-   Select module to view usage insights of components.

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

Default filters you can use to limit the data, including Date Range, User type, and location. Use the **Add Filter** option to add more filters to the page. For more information, see Filter data in Usage Insights.

</td></tr><tr><td>

4

</td><td>

Total active users

</td><td>

Shows Active users, new users, and the average number of sessions per user. Select any visualization in this section to view the trend analysis for Active users.

</td></tr><tr><td>

5

</td><td>

New Users

</td><td>

Number of visitors who have visited the applications for the first time in the specified time period.

</td></tr><tr><td>

6

</td><td>

Avg. Session per user

</td><td>

Average number of sessions per user in the specified time period.

</td></tr><tr><td>

7

</td><td>

Total sessions

</td><td>

Shows the total number of sessions, the average page views per session, and the average session duration. Select any visualization in this section to view the sessions trend analysis.

</td></tr><tr><td>

8

</td><td>

Avg. page per session

</td><td>

Average number of pages visited per session.

</td></tr><tr><td>

9

</td><td>

Avg. Session duration

</td><td>

Average time spent across sessions for all users.

</td></tr><tr><td>

10

</td><td>

Top pages

</td><td>

List of pages with the most views and most sessions. Select any entry in the list to dive into the views and related information.

</td></tr></tbody>
</table>**Note:**

-   Counters in the Usage Insights application contain aggregated user numbers.
-   If a country’s tracking consent policy is set to **Disabled**, user metrics are not tracked.

## Metrics across all applications

You can view basic application usage and event details for all applications within an instance. Select your module from the applications list to see these metrics simultaneously. The Analysis menu items provide access to the Retention, Cohort analysis, Conversion funnel, and Navigation paths modules. The Data Foundation menu items provide access to the Users, Sessions, Events, and Pages modules.

|Module|Description|
|------|-----------|
|Retention|Visualize new users and their rates of return and periods between visits. For more information, see User retention.|
|Cohort analysis|Create and analyze custom cohorts or groups of users separated from other users by similar traits or actions. Analyze how many users perform specific sequences of actions, and how often they return to perform specified actions over a given time. For more information, see Cohort analysis in Usage Insights.|
|Conversion funnel|Create funnel reports to analyze user completion rates for a specific task. View conversion rates, the number of users progressing from one step to the next and the average time for users to advance to each step and complete the funnel. For more information, seeFunnel reports in Usage Insights.|
|Navigation paths|Visualize users' journeys through your application, discovering the most and least popular paths. For more information, see Navigation paths.|

|Module| |
|------|---|
|Users|A list of users that you can filter, drill down into, and export.|
|Sessions|A list of sessions that you can filter, drill down into, and export.|
|Events|A list of user interactions such as page navigation and clicks that you can filter, drill down into, and export.|
|Pages|A list of visited pages on your instance that you can filter, drill down into, and export.|

## Events view

When you launch Usage Insights, it gives you an option to select the module from the drop-down list. Select the Web Embeddables module from the drop-down list and navigate to **Data Foundation** &gt; **Events**.

The Events tab enables you to filter a list of tracked user interactions captured by all Web Embeddables components across enabled Usage Insights applications. It displays a list of user interactions such as name of component events, total occurrences, active users, and event type. You can also export the data.

In the Events search bar, enter `[WE]` to filter and display only Web Embeddables components in the list. This prefix identifies all embedded components tracked by Usage Insights and makes it easy to isolate Web Embeddables components from other application events. To narrow your search to a specific component, enter `[WE]` followed by the component name.![Usage Insights Events page shows Web Embeddables component events list with search functionality, displaying event names, total occurrences, active users, and configurable filters for analysis.](../image/WE-events-dashboard.png)

## Event view of a component

The individual event view has more detailed information for a specified component.

<table id="table_we_analytics"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total occurrences

</td><td>

Displays the total number of times the event was triggered in a specified time.

</td></tr><tr><td>

\[Event\] trend

</td><td>

Displays the event usage trend over time and shows both active users and event occurrences. Use this chart to identify usage patterns and spikes in activity.Filter the view by:

-   Daily
-   Weekly
-   Monthly

</td></tr><tr><td>

Active users

</td><td>

Displays number of unique users who interacted with the component \(triggered the event\).

</td></tr><tr><td>

Event properties

</td><td>

Displays detailed breakdown of specific event attributes associated with the embedded component.

</td></tr></tbody>
</table>## Global code structure

The global code generated for Web Embeddables includes key identifiers that enable analytics tracking:

-   Module ID:
    -   Captures events across all component instances within the module.
    -   Groups usage data by module for consolidated analytics reporting.
    -   Enables tracking of multiple embedded component instances that belong to the same module across different pages or contexts.
-   Page title:
    -   Captures page-level analytics to identify where components are embedded.
    -   Tracks user interactions based on the hosting page context.
    -   Helps you understand component performance across different external website locations.

## Enable Usage Insights

Usage Insights is enabled by default for Web Embeddables. When you create a module, it registers with Usage Insights and begins to track component events. Sometimes it can take several hours for the module to get registered. This automatic registration ensures that usage data collection starts from the moment of deployment and allows you to monitor user interactions without additional configuration. For more information, see Enable Usage Insights.

You can also turn off the module by navigating to **Platform Analytics Administration** &gt; **Usage Insights Apps** &gt; **Settings**. Search and select your module, and uncheck the **Active** checkbox.

## User consent for Usage Insights advanced tracking

Users can opt in or opt out of Usage Insights advanced tracking at any time through their user preferences. This setting gives users control over the collection of detailed interaction data, such as clicks, page views, and component usage patterns. For more information, see User privacy, tracking, and user consent management in Usage Insights.

**Related topics**  


[Web Embeddables component events](../reference/we-events-detail.md)

