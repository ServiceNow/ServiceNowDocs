---
title: Modify forecast parameters to visualize forecast data
description: Configure and tweak forecast parameters to see how the forecast behaves when you vary the period length, periods to forecast, or algorithm. You can view the modified forecast on the time-series visualization at intervals of 15-, 30-, and 60-minute intervals and daily interval.
locale: en-US
release: xanadu
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Setting up Demand Forecast in Workforce Optimization for Customer Service, Configuring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Modify forecast parameters to visualize forecast data

Configure and tweak forecast parameters to see how the forecast behaves when you vary the period length, periods to forecast, or algorithm. You can view the modified forecast on the time-series visualization at intervals of 15-, 30-, and 60-minute intervals and daily interval.

## Before you begin

**Important:** Starting with the Tokyo release, Legacy Workforce Optimization is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: sn\_agent\_forecast.admin and sn\_csm\_wfo\_workspa.manager

The user with these roles must also be a manager of the assignment group that is associated with the resource conversion formula.

## About this task

You can define the start and end dates for which you want to create the forecast data. The start date is always the current date. The end date is calculated based on the period length and the periods to forecast. The periods to forecast is represented in days or hours. For example, if the period length is 1 day and the period to forecast is 30 days, then the end date is 30 days including the current day.

For 15-, 30-, and 60-minute intervals, managers can generate forecast up to 28 days. For daily interval, managers can generate forecast up to 365 days.

Forecast results are displayed with the historical data so that the user can compare the patterns of historical data with the forecast. The historical data of 14 days prior to the current date will be displayed with forecasts of 15-, 30-, and 60-minute intervals. The historical data of four weeks to the prior date will be displayed with forecasts of daily intervals. You can customize and configure historical data to be displayed using the **sn\_agent\_forecast.number\_of\_historical\_days\_in\_timeseries\_chart** and **sn\_agent\_forecast.number\_of\_historical\_days\_in\_daily\_timeseries\_chart** [system properties.](../reference/components-installed-configurable-wfo-cs.md).

The published forecast is reflected on the team calendar only when the **Forecast resources for future** job is executed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule \(![Schedule icon](../image/schedule-new.png)\) icon.

3.  Click **Forecasts**.

4.  Select the forecast model for which you want to view the time-series data.

    You can visualize each of the forecast parameters that were created for the forecast model.

5.  Click the gear \(![Forecast Parameters icon](../image/gear-new.png)\)icon.

6.  Click the plus \(+\) sign.

7.  Configure the forecast parameter.

    1.  From the **Period length unit** list, select the unit for the length of the period to forecast.
    2.  In the **Period length** field, enter the duration of the period to forecast.
    3.  In the **Periods to forecast** field, enter the number of seasons, which is the period length, for which you want to forecast.
    4.  In the **Interval** field, select 15-, 30-, and 60-minute intervals or Daily interval value of the period to forecast.
    5.  Click **Update**.
    The forecast is created in **Draft** state. The forecast is calculated and displays in the forecast model. You can analyze the forecast with the new forecast parameters before you publish it.

8.  To preview a forecast before publishing it, click **Preview**.

    The forecast is calculated using the algorithm and parameters configured in the forecast parameter. When you [create a manual adjustment](create-manual-adjustment-forecast-configurable-wfo.md) to predict future resources, Demand Forecast overlays the adjustment in the time-series chart.

    |When you|Then the forecast|
    |--------|-----------------|
    |**Unpublish a published forecast**|Become inactive.|
    |**Preview an inactive forecast parameter**|Displays for the date range for which the forecast parameter was active.|
    |**Preview an active forecast**|Displays the time-series data for the future time-period.|

9.  Publish the forecast parameters.

    1.  To publish a newly created forecast parameter, click **Save** and then click **Publish**.
    2.  To publish an active forecast parameter, click **Publish**.
    **Note:** You can only have one forecast in **Published** state, which is used to calculate the resources.

    When the forecast parameter is published:

    -   The state of the record changes to **Published**.
    -   The **Forecast resources for future** job runs daily and uses the published forecast parameters to calculate the agent forecast. The calculation uses the resource conversion formula to calculate the forecast data from the current point forward. You can view the updated resources in the team calendar.
    -   Any other forecast parameters that were created would be unpublished and inactive.

## What to do next

[Create a manual adjustment for a forecast](create-manual-adjustment-forecast-configurable-wfo.md)

**Parent Topic:**[Setting up Demand Forecast in Workforce Optimization for Customer Service](../concept/configuring-demand-forecast-configurable-wfo-cs.md)

