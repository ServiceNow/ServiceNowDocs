---
title: Modify forecast parameters to visualize forecast data
description: Configure and tweak forecast parameters to see how the forecast behaves when you vary the period length, periods to forecast, or algorithm. You can view the modified forecast on the time-series visualization.
locale: en-US
release: zurich
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Set up Demand Forecast, Configure, Workforce Optimization overview, HR Service Delivery, Employee Service Management]
---

# Modify forecast parameters to visualize forecast data

Configure and tweak forecast parameters to see how the forecast behaves when you vary the period length, periods to forecast, or algorithm. You can view the modified forecast on the time-series visualization.

## Before you begin

Role required: sn\_hr\_wfo.admin, sn\_hr\_wfo.manager

The user with these roles must also be a manager of the assignment group that is associated with the resource conversion formula.

## About this task

You can define the start and end dates for which you want to visualize the forecast data. The start date for a forecast configuration is based on the number of historical days you want to consider for data visualization. This is set using the **sn\_agent\_forecast.number\_of\_historical\_days\_in\_timeseries\_chart**.

The published forecast is reflected on the team calendar only when the **Forecast resources for future** job is executed.

The default start date is set to 3 days ago starting from the day before the current day. The end date is calculated based on the period length and the periods to forecast represented in days. For example, if the period length is 1 day and the periods to forecast is 30, then the end date is 30 days including the current day. Forecast can be generated for a maximum period of 90 days.

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule \(![Schedule icon](../../workforce-optimization-for-customer-service-configurable/image/schedule-new.png)\) icon.

3.  Click **Forecasts**.

4.  Select the forecast model for which you want to view the time-series data.

    You can visualize each of the forecast parameters that were created for the forecast model.

5.  Click the gear \(![Forecast Parameters icon](../../workforce-optimization-for-customer-service-configurable/image/gear-new.png)\)icon.

6.  Click the plus \(+\) sign.

7.  Configure the forecast parameter.

    1.  From the **Period length unit** list, select the unit for the length of the period to forecast.
    2.  In the **Period length** field, enter the duration of the period to forecast.
    3.  In the **Periods to forecast** field, enter the number of seasons, which is the period length, for which you want to forecast.
    4.  In the **Algorithm** field, select an algorithm you want to use to calculate the forecast.
    5.  Click **Update**.
    The forecast is created in **Draft** state. The forecast is calculated and displays in the forecast model. You can analyze the forecast with the new forecast parameters before you publish it.

8.  To preview a forecast before publishing it, click **Preview**.

    The forecast is calculated using the algorithm and parameters configured in the forecast parameter. When you [create a manual adjustment](create-manual-adjustment-forecase-wfo-hr.md) to predict future resources, Demand Forecast overlays the adjustment in the time-series chart.

    |When you|Then the forecast|
    |--------|-----------------|
    |**Unpublish a published forecast**|Become inactive.|
    |**Preview an inactive forecast parameter**|Displays for the date range for which the forecast parameter was active.|
    |**Preview an active forecast**|Displays the time-series data for the future time-period.|

9.  Publish the forecast parameters.

    -   To publish a newly created forecast parameter, click **Save** and then click **Publish**.
    -   To publish an active forecast parameter, click **Publish**.
    **Note:** You can only have one forecast in **Published** state, which is used to calculate the resources.

    When the forecast parameter is published:

    -   The state of the record changes to **Published**.
    -   The **Forecast resources for future** job runs daily and uses the published forecast parameters to calculate the agent forecast. The calculation uses the resource conversion formula to calculate the forecast data from the current point forward. You can view the updated resources in the team calendar.
    -   Any other forecast parameters that were created would be unpublished and inactive.

**Parent Topic:**[Setting up Demand Forecast in Workforce Optimization for HR](../concept/setup-demand-forecast-wfo-hr.md)

