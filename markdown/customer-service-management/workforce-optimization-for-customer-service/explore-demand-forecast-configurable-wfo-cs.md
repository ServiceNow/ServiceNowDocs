---
title: Demand Forecast in Workforce Optimization for Customer Service
description: Demand Forecast enables managers to view their agent staffing forecast at 15-, 30-, and 60-minute intervals on the team calendar. This feature enables managers to adjust and prioritize schedules, tasks, breaks, and meetings for their agents without impacting service objectives. Learn how you can use Demand Forecast to predict resources based on historical data.
locale: en-US
release: xanadu
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Exploring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Demand Forecast in Workforce Optimization for Customer Service

Demand Forecast enables managers to view their agent staffing forecast at 15-, 30-, and 60-minute intervals on the team calendar. This feature enables managers to adjust and prioritize schedules, tasks, breaks, and meetings for their agents without impacting service objectives. Learn how you can use Demand Forecast to predict resources based on historical data.

**Important:** Starting with the Tokyo release, Legacy Workforce Optimization is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Overview of the Demand Forecast application.Demand Forecast

The 15-, 30-, and 60-minute intervals are color-coded to display the status of agent staffing such as understaffing, overstaffing, and well staffed. Understaffed slots are color-coded red, overstaffed slots are color-coded yellow, and well-staffed slots are color-coded green. Slots that do not need staffing are color-coded grey. Managers must ensure adequate staffing in understaffed slots and optimize the resources in overstaffed slots.

For example, a manager of the Service Support group can see that the slot between 07:00 and 07:15 is color-coded red and is understaffed. The demand is for nine resources and the coverage is eight resources. The slot is understaffed by one resource. That slot displays **9** and **-1**. To avoid the understaffing of that slot, the manager allocates a resource who is on a break. The manager reschedules the break of that resource from 07:00 to 07:30. The 07:00 to 07:15 slot is now well staffed and color-coded green.



![Schedule page in Manager Workspace displaying the staffing forecast for a team in the Demand Forecast application.](../image/wfo-demand-forecast1.png)

The manager of all the teams can view the staffing forecast of the teams and at the individual level in the 15-, 30-, and 60-minute intervals according to the requirement. This view helps managers to staff their teams adequately.

![Schedule page in Manager Workspace displaying the staffing forecast for all teams in the Demand Forecast application.](../image/wfo-demand-forecast2.png "Demand Forecast view for all teams")

The Demand Forecast application uses [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) to forecast the demand for teams.

When you create Demand Forecast configurations, the application creates these metrics:

-   Staffing forecast: The forecast on the number of agents that a manager must handle cases and interactions in 15-, 30-, and 60-minute intervals.
-   Volume forecast: The historical data and the forecast of the contact volumes \(cases and interactions\) at 15-minute intervals.

**Note:** You can create forecast configurations for any table.

## Analyzing Demand Forecast resource prediction

Watch this video to see how you can model demand scenarios and view updated demand on the calendar.

Demand Forecast - model demand scenarios.

As a manager with the forecast admin role, you can create forecast parameters in the Manager Workspace. [Modify forecast parameters to visualize forecast data](../task/modify-demand-forecast-parameters-configurable-wfo.md) and preview time-series data before publishing it. You can create any number of forecasts to preview the time-series data in real time.

You can also make manual adjustments to tweak the forecast and analyze the forecast pattern. Overlay the manual adjustments on the visualized forecast data and view the time-series data to analyze the forecast model. For example, you have a specific pattern for the upcoming week that has a national holiday in the middle of the week where you need more agents. Because you expect the sales to go up, you can manually tweak the forecast to increase it by 10% and analyze that data.

## Demand Forecast

The Demand Forecast application includes the following modules:

|Module Name|Description|
|-----------|-----------|
|Data Collection Definitions|Set conditions to define the data that you want to collect for cases, interactions, or any table.​|
|Formula Parameters|Add the parameters to be defined in the formula to calculate the resources from the forecast.|
|Resource Conversion Formula|Add formulas to convert forecast to resources at 15-, 30-, and 60-minute intervals.|
|Group Forecast Configuration|Associate the configured formula for resource conversion to groups.|

As a user with the sn\_agent\_forecast.admin role, you can forecast the number of agents that you need for a shift.

To forecast the demand:

1.  Collect data by defining data collection definitions.
2.  Set values for forecast parameters and generate volume forecasts.
3.  Create formulas to convert volume forecasts into the number of resources that you need at 15-, 30-, and 60-minute intervals.
4.  Associate the formulas to assignment groups.
5.  View the predicted demand on the calendar.

**Note:** See the Demand Forecast section in [Components installed with Workforce Optimization for Customer Service](../reference/components-installed-configurable-wfo-cs.md) for information on the default components and configurations.

## Collect data by defining data collection definitions

Use the Data Collection Definitions module to define the data that you want to collect for forecasting agents.

-   Use the **Collect daily data for automated forecast configurations** scheduled job to gather data for the metrics defined in the data collection definitions. The scheduled job fetches the records from the previous day for every 15-minute interval for all assignment groups and stores it in the MetricBase.

    You can access the time series for the collected data using the MetricBase `list` in the Group \[sys\_user\_group\] table. For more information on accessing MetricBase data, see [Access MetricBase data using the list command](https://www.servicenow.com/docs/access?context=view-time-series-data&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

-   Use the **Collect historical data for automated forecast configurations** on-demand job to collect historical data at 15-minute intervals. This job collects data for the past three years.
-   Use the **Forecast resources for future** scheduled job to forecast the resources based on the collected data and stores the data in the Agent Forecast metric in MetricBase. See [Forecast properties](../reference/components-installed-configurable-wfo-cs.md#forecast-properties) to set the collection frequency such as the number of days that you must collect the data to calculate the forecast or the time period that you want to store the data for.

**Note:** The time series metrics created for data collection definitions use the WFO Forecast retention policy. This policy stores data at a one-hour interval for the past three years.​

## Create forecast parameters

Managers can collect historical data at 15-minute granularity for generating accurate forecasts. The forecasts generated show the patterns in cases and interaction volume at 15-minute intervals. By default, the application uses the Seasonal Trend Loess \(STL\) algorithm.

For example, a manager can generate the volume forecast at 15-minutes intervals by providing the appropriate forecast parameters. Forecast parameters consist of the period length and periods to forecast that are most suitable for the pattern observed in the contact volumes.

![Graph displaying case volume forecast generated for demand and coverage in 15 minutes interval.](../image/wfo-demand-forecast3.png "Generating volume forecast")

## Create formula parameters

Use numeric values or a script to be defined in the formula to calculate the resources from forecasts. Units in formula parameters can be specified in hours, minutes, or absolute numbers. See [Formula parameters](../reference/components-installed-configurable-wfo-cs.md#table_qtg_pwr_zmb) for the parameters that are available by default.

## Create formulas to convert forecast to resources

Build formulas to convert the volume forecast to the staffing forecast at 15-, 30-, and 60-minute intervals. See [Resource Conversion Formula](../reference/components-installed-configurable-wfo-cs.md) for the configured resource forecast formulas that are available by default.

## Associate formulas to assignment groups

Associate assignment groups with the resource conversion formula to convert the number of cases and interactions to the number of agents.

## View the predicted demand on the calendar

The data collected by the Agent Forecast metric in MetricBase is used to forecast the agents that you need for each 15-, 30-, and 60-minute interval in a day on the team calendar. In a Week view for the calendar, it displays the staffing levels for a given week.

**Related topics**  


[Configure the data collection to forecast the demand for resources](../task/configure-data-collection-demand-forecast.md)

[Analyze staff alignment using Demand Forecast](scheduling-configurable-wfo-cs.md#)

