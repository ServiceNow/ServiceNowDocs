---
title: Performance insights in user-configurable dashboard
description: The Performance insights widget in the user-configurable dashboard displays the total production instances, their count, and the status of their performance score in a dial component.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Performance insights, User configurable dashboard]
breadcrumb: [User configurable dashboard, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Performance insights in user-configurable dashboard

The Performance insights widget in the user-configurable dashboard displays the total production instances, their count, and the status of their performance score in a dial component.

**Important:** Performance insights of the instances as a feature are available to Total customers only, and both in the regulated and non-regulated markets. Consequently, the ML model deduces and sends the data to the back end if you’re a Total tier customer and your instances have at least four weeks of data.

The performance summary of the instances as a feature exists in the:

-   User configurable dashboard
-   Customizable widget that you can add on the dashboard
-   Analytics page

## Performance insights widget in the user-configurable dashboard

![Performance summary of the instances in the user configurable dashboard.](../image/io-performance-insights-widget.png)

The ML model fetches these data and categorizes them as Critical, Warning, or Optimal based on the metrics score in the Performance widget.

-   The half donut chart displays the total number of production instances, total count, and the performance category, color-coded as Critical, Warning, and Optimal. The widget shows a maximum of three instances prioritizing those instances that are in Critical or Warning state over instances that are in Optimal state. The data is refreshed every 15 minutes.
-   The top three instance names are listed below the dial component, displaying the type of instance, which is production instances by default, each of its performance status as Critical, Warning, or Optimal, the metrics affected that would be zero, and the Online and Offline Nodes that are similar to the cluster details.

In the Instances grid, the **Health** column displays Critical in red, Warning in yellow, and Optimal in green. Selecting the name of the instances opens a slider with the details of metrics that are affected. Selecting the links in the **Metrics Affected** column takes you to the performance page with the details of it in the last 24 hours.

For each instance, you can select the ![Vertical ellipsis.](../../../reuse/icons/product-icons/ellipsis-vertical-outline-24.svg) icon and click the **Instance details** option to know more about the instance. Select the **View root cause** button for root cause analysis report.

**Note:** The **Instance details** and **View Root Cause** options are available only for instances that are in Critical and Warning states. However, the options aren’t available for instances in Optimal state.

If the instance has insufficient data or if the report is still being generated, the status is either **Insufficient data** or **Work in Progress**, respectively.

-   If a Critical or Warning performance root cause report link in the widget changes to Work in progress after a few minutes, it means that a new RCA report is being generated with the latest data. You can still access the previous report from the RCA History page.
-   If a report is in Work in progress state, then the engine is still analyzing data. In the meantime, you can manually review the **Affected Metrics** or refer to the most recent report \(generated in the last 1–2 hours\) in the RCA History page for analysis.

Select the **View all Instances** link to view all the production instances in the Analytics page for that account.

## Performance health summary customizable widget

You can also configure only one instance or multiple instances and view the performance summary.

To create a customizable widget on a new dashboard, see [Create a dashboard](customize-instance-observer-dashboard.md).

1.  Select the **Edit Dashboard** link on the top and click the **Add Widget** option.
2.  Select **Custom** or **Out of the box** option for the kind of widget that you would like to add.
3.  Select **Single** or **Multiple** option according to your requirement.
4.  Select the instance names from the options available.
5.  Select **Performance Insights** in the **Category** field.
6.  Select **Add to Dashboard** button.

The customizable widget comes with three tiles:

-   Dial component: Add the Performance Insights widget provided by the base system to your custom dashboard.
-   Single instance tile: Get details of any one particular instance that you want to view, and generate its root cause.
-   Multi-instance tile: Select specific instances but more than one of your choices, and view each of its details and generate the root cause. This multi-instance tile has a different view configuration without the dial component.

You can also delete any of the components and customize it as you like.

**Note:** If you’re a new user with a new instance that is newly added to the system, then there may not be any data. Data must be at least four-weeks old for the system to fetch from the back end.

## Performance summary of Instances in Analytics page

If you select the **Analytics** menu and click the **Instances Summary** option, you have another option of viewing the performance status of your instances.

![Instances summary in Analytics page.](../image/io-performance-inst-analytics.png)

The instances performance summary in the **Analytics** tab is similar to the one in the user configurable dashboard. The dial component and the performance status counts are all similar, however there’s a **Root Cause &amp; Fixes** tile to generate the root cause details.

The widget is refreshed for every 15 minutes to get the latest data.

There’s an additional **Alerts** column. Select the alert count of an instance in the column that opens the Alerts console of the instance, where you can view the alert count for the past three hours.

You can also access the instance details by selecting the ![Vertical ellipsis.](../../../reuse/icons/product-icons/ellipsis-vertical-outline-24.svg) for that instance, which opens the Instance Details slider page where you can view the instance metrics that contribute to Warning or Critical performance. You can gauge the performance with the values of the metric in the last 60 minutes.

If the report is already generated, then you can view the report by selecting the **View root cause report** button in the Instance Details page for that instance.

The root cause report opens in a separate page with the **Root cause summary and resolutions** tab that lists the **Summary** and **Recommended resolutions**. The **Slow Transactions** tab gives the categories.

Select the instance name in the Instance column that opens a slider page displaying the instance name, instance type, and instance status. If the instance performance status is Optimal, then you wouldn't see any data fetched from the back end. The columns in the slider page are sortable and filterable, and selecting the links in the **Metrics Affected** column takes you to the respective performance page. The trend in data is displayed in the **Trend** column.

**Parent Topic:**[Instance Observer user configurable dashboard](user-configurable-dashboard.md)

