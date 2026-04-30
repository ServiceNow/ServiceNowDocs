---
title: Demand Forecast in Workforce Optimization for ITSM
description: Learn how you can use Demand Forecast to predict resources based on historical data.
locale: en-US
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Scheduling, Workforce Optimization for ITSM, IT Service Management]
---

# Demand Forecast in Workforce Optimization for ITSM

Learn how you can use Demand Forecast to predict resources based on historical data.

The video below shows an overview of the Demand Forecast application.

Demand Forecast in Workforce Optimization for ITSM

Demand Forecast uses [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) to forecast the demand for teams.

When you create demand forecast configurations, the application creates metrics:

-   To forecast the number of agents you need for interactions.
-   To resolve incidents throughout a given day.

**Note:** You can create forecast configurations for any table.

## Analyzing Demand Forecast resource prediction

Watch this video to see how you can model demand scenarios and view updated demand on the calendar.

Demand Forecast - Model Demand Scenarios

As a manager with the forecast admin role, you can create forecast parameters in the Workforce Optimization for ITSM Manager Workspace. [Modify forecast parameters to visualize forecast data](../task/modify-forecast-parameters-configurable-wfo-itsm.md) and preview time-series data before publishing it. You can create any number of forecasts to preview the time-series data in real time.

You can also make manual adjustments to tweak the forecast and analyze the forecast pattern. You can overlay the manual adjustments on the visualized forecast data and view the time-series data to analyze the forecast model. For example, if you have a specific pattern for the upcoming week but you know that a national holiday falls in the middle of the week where you need more agents because you expect the sales to go up, you can manually tweak the forecast to increase it by 10% and analyze that data.

## Demand Forecast

The Demand Forecast application includes the following four modules:

|Module Name|Description|
|-----------|-----------|
|Data Collection Definitions|Set conditions to define the data you want to collect for incidents, interactions, or any table.​|
|Formula Parameters|Add parameters to be defined in the formula to calculate the resource count per hour in a day.|
|Resource Conversion Formula|Add formulas to convert forecast to resources.|
|Group Forecast Configuration|Associate the configured formula for resource conversion to groups.|

As a forecast admin \(sn\_agent\_forecast.admin\), you can forecast the number of agents you need for a shift.

To forecast the demand:

1.  Collect data by defining data collection definitions
2.  Create forecast parameters.
3.  Create formulas to convert the forecasting number of incidents into the number of resources you must respond to those incidents.
4.  Associate the formulas to assignment groups.
5.  View the predicted demand on the calendar.

**Note:** Refer to [Demand Forecast in Workforce Optimization for ITSM configurable workspace](../reference/configurable-wfo-itsm-demand-forecast-reference.md) for information on default components and configurations installed with Demand Forecast.

## Collect data by defining data collection definitions

Use the **Data Collection Definitions** application to define the data you want to collect for forecasting agents.

-   Use the **Collect daily data for automated forecast configurations** scheduled job to gather data for the metrics defined in the data collection definitions. The scheduled job fetches the records from the previous day for each hour and for every assignment group. It stores this data in the MetricBase.

    You can access the time series for the collected data using the MetricBase `list` on the Group \[sys\_user\_group\] table. For more information on accessing MetricBase data, refer to [Access MetricBase data using the list command](https://www.servicenow.com/docs/access?context=view-time-series-data&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

-   Use the **Collect historical data for automated forecast configurations** on-demand job to collect hourly historical data. This job collects data for the past three years.
-   Use the **Forecast resources for future** scheduled job to forecast the resources based on the collected data. The scheduled job stores the data in the Agent Forecast metric in MetricBase. Refer to the [forecast properties](../reference/configurable-wfo-itsm-demand-forecast-reference.md) to set the collection frequency such as the number of days you must collect the data. You can use this information to calculate the forecast or the time period for which you want to store the data.

**Note:** The time series metrics created for data collection definitions use the **WFO Forecast** retention policy. This policy stores data at a one-hour interval for the past three years.​

## Create formula parameters

Use numeric values or a script to define parameters to use in the formula for forecasting. Refer to the [resource forecast configurations](../reference/configurable-wfo-itsm-demand-forecast-reference.md) for the configured resource forecast formulas available by default.

## Associate formulas to assignment groups

To convert the number of incidents to agents, associate assignment groups to the resource-conversion formula.

## View the predicted demand on the calendar

The data collected by the Agent Forecast metric in MetricBase is used to forecast the agents you need for each hour in a day. This data is displayed on the team calendar. In a Week view for the calendar, it displays the staffing levels for a given week.

**Related topics**  


[Set up Demand Forecast](../task/configure-data-collection-configurable-wfo-itsm.md)

