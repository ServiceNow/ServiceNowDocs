---
title: Create a manual adjustment for a forecast
description: Adjust forecasts manually to fine-tune them for greater accuracy. Create the adjustment for a specified time period and analyze how it impacts your forecast.
locale: en-US
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up, Demand Forecast, Scheduling, Workforce Optimization for ITSM, IT Service Management]
---

# Create a manual adjustment for a forecast

Adjust forecasts manually to fine-tune them for greater accuracy. Create the adjustment for a specified time period and analyze how it impacts your forecast.

## Before you begin

Role required: sn\_agent\_forecast.admin and sn\_wfo\_cfg\_itsm.manager

The user with these roles must also be a manager of the assignment group that is associated with the resource conversion formula.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Manager Workspace**.

2.  Click the Schedule icon.

3.  Click **Forecasts**.

4.  Select the forecast model for which you want to make a manual adjustment.

5.  Click the Manual Adjustments icon.

6.  Make a manual adjustment.

    1.  Click the manual adjustment icon.
    2.  Fill in the following fields.

<table id="table_uwd_qxv_dpb"><thead><tr><th>

Field Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the manual adjustment.

</td></tr><tr><td>

Start Date Time

</td><td>

Date and time when the manual adjustment for the forecast must start.

</td></tr><tr><td>

End Date Time

</td><td>

Date and time when the manual adjustment for the forecast must end.

</td></tr><tr><td>

Adjustment Unit

</td><td>

Unit for the manual adjustment.Available values:

-   Percentage—adjustment value percentage. For example, if the forecast data shows incident count and if the adjustment value is 15, the manual adjustment shows a 15% increase in incident count than the forecast data.
-   Number—adjustment value count. For example, if the forecast data shows incident count and if the adjustment value is 15, the manual adjustment shows 15 more incidents than the forecast data.


</td></tr><tr><td>

Adjustment Value

</td><td>

The numeric value for which you want to adjust the forecast. The value is applied to each group in the Groups \[sys\_user\_groups\] table. The manual adjustment visualization on the time-series chart displays the data for your groups. For example, let's assume that the value is 15 and the unit is number. On a given day, if you have two groups for a forecast model and both have 2 agents each before you do the manual overlay, when you enter the value as 15, it is applied to each of the two groups and the total value displays as 34. This is calculated as follows:

-   Two agents for group A + the adjustment value 15 = 17
-   Two agents for group B + the adjustment value 15 = 17
The total is 34.

</td></tr></tbody>
</table>    3.  Click **Save**.
    The manual adjustment is created in **Draft** state. The manual adjustment is calculated and displays as a green line in the forecast model. You can analyze or update the forecast with this manual adjustment before you publish it.

7.  Publish the manual adjustment.

    1.  Click the saved manual adjustment that you want to use for forecasting resources.
    2.  Click **Publish**. The state changes to **Ready to Publish**.
    When the **Forecast resources for future** job is run, it calculates the forecast, checks for manual adjustments, applies those values if any, and moves it to the **Published** state.

    **Note:**

    -   When you unpublish a forecast, it moves to **Draft** state. You can delete a forecast that is in **Draft** state.
    -   If you want to end a manual adjustment after it has started and before its end date, you can click **End Now**.
    The forecast will no longer be used in the resource conversion formula.

    When the manual adjustment is published:

    -   The state of the record changes to **Published**.
    -   The adjusted values will be used in the resource conversion formula and the demand forecast displayed on the calendar.
    -   Any other manual adjustment configurations that were created would be unpublished and moved to **Draft** state.

**Parent Topic:**[Setting up Demand Forecast in Workforce Optimization for ITSM](../concept/setting-up-demand-forecast-configurable-wfo-itsm.md)

