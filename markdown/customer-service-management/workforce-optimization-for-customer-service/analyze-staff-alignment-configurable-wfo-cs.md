---
title: Analyze staff alignment using Demand Forecast
description: Use Demand Forecast to plan the number of staff members that you require so that you have enough agents to do the job.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Schedule, Use, Workforce Optimization for Customer Service, Customer Service Management]
---

# Analyze staff alignment using Demand Forecast

Use Demand Forecast to plan the number of staff members that you require so that you have enough agents to do the job.

## Before you begin

Role required: sn\_agent\_forecast.user

## About this task

Using Demand Forecast, you can:

-   Monitor agent or team shift coverage for any day, week, or month.
-   Analyze if you are overstaffed, understaffed, perfectly staffed, or not aligned well with your staffing needs.
-   Adjust the staff alignment depending on the coverage you need and the schedule of your teams.
-   Analyze staff alignment as you are creating a schedule.
-   You can analyze the agent coverage you have and the actual demand for the number of agents based on assignment groups and work shifts in a day.

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule \(![Schedule icon](../image/schedule-new.png)\) icon.

3.  Click the **Team Calendar** tab.

4.  Analyze staff alignment for each shift.

    You can click the filter icon and select the assignment groups and shift plans for which you want to view the staff alignment.

<table id="choicetable_pwx_2tw_nnb"><thead><tr><th align="left" id="d44061e117">

To analyze staff alignment

</th><th align="left" id="d44061e120">

Do the following

</th></tr></thead><tbody><tr><td id="d44061e126">

**For each day**

</td><td>

Select **Day** from the list.The **Total resources needed** row displays the demand for the number of agents for that day at the selected intervals of 15,30, and 60-minute.

For example, at 15-minute intervals, a number 16 between 0700 and 0715 means that the agent demand forecast is 16.

The time slots are color-coded as below to show the coverage of agents in a particular interval:

|Highlight color for each day for a group|Description|
|----------------------------------------|-----------|
|Green|The number of agents you have scheduled for that interval and demand for that interval are an exact match—your staffing needs are perfectly aligned.|
|Yellow|The number of agents you have scheduled are more than the demand you have for that interval.|
|Red|The number of agents you have scheduled are less than the demand you have for that interval.|
|Grey|The demand for the number of agents and the number of agents scheduled is zero for that interval.|

</td></tr><tr><td id="d44061e208">

**For a given week**

</td><td>

1.  Select **Week** from the list.

The **Total coverage/demand** row has indicators for the staff alignment.

    |If the row displays|Then|
    |-------------------|----|
    |An arrow points downward|The predicted forecast is lower than the number of agents you need for that day|
    |An arrow points upward|The predicated forecast is higher than the number of agents you need for that day|
    |A checkmark|The perfect alignment of the predicted forecast and the required number of agents.|

2.  Click any of the indications displayed in the **Total coverage/demand** row to analyze further details on the forecast.
 You can also view the coverage and demand for every hour for each group.

</td></tr><tr><td id="d44061e291">

**For a given month**

</td><td>

1.  Select **Month** from the list.

The month view displays current week and the upcoming three weeks \(28 days\) on the calendar in a single view. The current day is highlighted in purple.

2.  In the calendar drop-down, set a date.

Up to four weeks starting the week containing this date appear on the team calendar.

3.  The **Total coverage/demand** row has indicators for the staff alignment.

    |If the row displays|Then|
    |-------------------|----|
    |An arrow points downward|The predicted forecast is lower than the number of agents you need for that day|
    |An arrow points upward|The predicated forecast is higher than the number of agents you need for that day|
    |A checkmark|The perfect alignment of the predicted forecast and the required number of agents.|

4.  Click any of the indications displayed in the **Total coverage/demand** row to analyze further details on the forecast.
 You can also view the full day's coverage and demand for 28 days in a single view.

 The training, time-off, and meeting events that are less than four hours are hidden in the Month view.

**Note:** Your administrator can set:

-   the **sn\_shift\_planning.enable\_month\_view\_for\_team\_calendar\_manager\_workspace** system property to `false` to remove the **Month** option in the drop-down. This system property is set to true by default in the CSM. The month view is enabled by default for ZBoot customers.
-   the value in the **sn\_shift\_planning.hide\_events\_by\_duration\_in\_month\_view\_manager\_workspace** system property to the maximum number of hours for which an event \(training, time-off, and meeting\) must be hidden on a calendar in the month view. By default, the value is set to `4`.


</td></tr></tbody>
</table>    The following scheduling snapshots provide you an example to analyze staff alignment using Demand Forecast. The misaligned staffing indicator in the pop-up shows that the forecast manager has scheduled certain number of agents for each shift but they need more agents to cover them.

    ![Demand Forecast to analyze staff alignment.](../image/demand_forecast_and_scheduling.gif)


**Parent Topic:**[Schedule in Workforce Optimization for Customer Service](../concept/scheduling-configurable-wfo-cs.md)

