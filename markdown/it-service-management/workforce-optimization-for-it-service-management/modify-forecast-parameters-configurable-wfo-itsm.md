---
title: Modify forecast parameters to visualize forecast data
description: Configure and tweak forecast parameters to see how the forecast behaves when you vary the period length, periods to forecast, or algorithm. You can view the modified forecast on the time-series visualization.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up, Demand Forecast, Scheduling, Workforce Optimization for ITSM, IT Service Management]
---

# Modify forecast parameters to visualize forecast data

Configure and tweak forecast parameters to see how the forecast behaves when you vary the period length, periods to forecast, or algorithm. You can view the modified forecast on the time-series visualization.

## Before you begin

Role required: sn\_agent\_forecast.admin and sn\_wfo\_itsm.manager

The user with these roles must also be a manager of the assignment group that is associated with the resource conversion formula.

## About this task

You can define the start and end dates for which you want to visualize the forecast data. The start date for a forecast configuration is based on the number of historical days you want to consider for data visualization. This is set using the **sn\_agent\_forecast.number\_of\_historical\_days\_in\_timeseries\_chart** [property](../reference/configurable-wfo-itsm-demand-forecast-reference.md).

The default start date is set to 90 days ago starting from the day before the current day. The end date is calculated based on the period length and the periods to forecast represented in days. For example, if the period length is 7 days and the periods to forecast is 5, then the end date is 35 days including the current day.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Manager Workspace**.

2.  Click the Schedule icon ![Schedule icon](../../itsm-manager-workspace/image/schedule-icon.png).

3.  Click **Forecasts**.

4.  Select the forecast model for which you want to view the time-series data.

    You can visualize each of the forecast parameters that were created for the forecast model.

5.  Click the gear icon ![Gear icon](../image/gear-icon.png).

6.  Click the plus \(+\) sign.

7.  Configure the forecast parameter.

    1.  From the **Period length unit** list, select the unit for the length of the period to forecast.
    2.  In the **Period length** field, enter the length of a season to forecast.
    3.  In the **Periods to forecast** field, enter the number of seasons, which is the period length, for which you want to forecast.
    4.  In the **Algorithm** field, select an algorithm you want to use to calculate the forecast.
    5.  Click **Update**.
    The forecast is created in **Draft** state. The forecast is calculated and displays in the forecast model. You can analyze the forecast with the new forecast parameters before you publish it.

8.  To preview a forecast before publishing it, click **Preview**.

    The forecast is calculated using the algorithm and parameters configured in the forecast parameter. When you [create a manual adjustment](create-manual-adjustment-configurable-wfo-itsm.md) to predict future resources, Demand Forecast overlays the adjustment in the time-series chart.

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

[Create a manual adjustment for a forecast](create-manual-adjustment-configurable-wfo-itsm.md)

**Parent Topic:**[Setting up Demand Forecast in Workforce Optimization for ITSM](../concept/setting-up-demand-forecast-configurable-wfo-itsm.md)

