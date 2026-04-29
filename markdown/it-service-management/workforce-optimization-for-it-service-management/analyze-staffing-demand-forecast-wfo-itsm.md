---
title: Analyze your staff alignment using Demand Forecast
description: Use Demand Forecast to plan the number of staff members that you require so that you have enough agents to do the job.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Scheduling your teams' work, Scheduling, Workforce Optimization for ITSM, IT Service Management]
---

# Analyze your staff alignment using Demand Forecast

Use Demand Forecast to plan the number of staff members that you require so that you have enough agents to do the job.

## Before you begin

Role required: sn\_agent\_forecast.user

## About this task

Using Demand Forecast, you can:

-   Monitor agent or team shift coverage for any day or week.
-   Analyze if you are overstaffed, understaffed, perfectly staffed, or not aligned well with your staffing needs.
-   Adjust your staff alignment depending on the coverage that you need and the schedule of your teams.
-   Analyze your staff alignment as you are creating a schedule.
-   You can analyze the agent coverage you have and the actual demand for the number of agents based on assignment groups and work shifts in a day.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Manager Workspace**.

2.  Click the Schedule icon \( ![Schedule icon](../../itsm-manager-workspace/image/schedule-icon.png)\).

3.  Click the **Team Calendar** tab.

4.  Analyze your staff alignment for each shift.

    You can click the filter icon and select the assignment groups and shift plans for which you want to view the staff alignment.

<table id="choicetable_pwx_2tw_nnb"><thead><tr><th align="left" id="d85378e122">

To analyze staff alignment

</th><th align="left" id="d85378e125">

Do the following

</th></tr></thead><tbody><tr><td id="d85378e131">

**For each day**

</td><td>

Select **Day** from the list.The Total coverage/demand row displays the number of agents that cover each shift in a day. It also shows the demand for the number of agents that you forecast to work for that day.

 For example, 24/20 shows the following:

-   You have 24 agents scheduled for all shifts for that day.
-   The agent demand forecast for that day is 20.
You can also view the number of agents you have and the demand for every hour for each group. The current agent coverage and the demand is highlighted as follows:

|Highlight color for each day for a group|Description|
|----------------------------------------|-----------|
|Green|The number of agents you have scheduled for that hour and demand for that hour are an exact match—your staffing needs are perfectly aligned.|
|Yellow|The number of agents you have scheduled are more than the demand you have for that hour.|
|Red|The number of agents you have scheduled are less than the demand you have for that hour.|

</td></tr><tr><td id="d85378e209">

**For a given week**

</td><td>

1.  Select **Week** from the list.

The Total coverage/demand row has indicators for the staff alignment.

    |If the row displays|Then|
    |-------------------|----|
    |An arrow that points downwards|The predicted forecast is lower than the number of agents that you need for that day.|
    |An arrow that points upwards|The predicted forecast is higher than the number of agents you need for that day.|
    |A checkmark|The perfect alignment of the predicted forecast and the required number of agents.|

2.  Click any of the indications that are displayed in the Total coverage/demand row to analyze further details about the forecast.
 You can also view the coverage and demand for every hour for each group.

</td></tr></tbody>
</table>    The following image shows an example of the staffing alignment in a Week view. The misaligned staffing indicator in the pop-up window shows that the forecast manager has scheduled four agents for each shift but more agents are needed to cover the shifts.![Demand Forecast](../image/demand-forecast-rome.gif)


**Parent Topic:**[Scheduling your teams' work in Workforce Optimization for ITSM](../concept/scheduling-configurable-workforce-optimization-itsm.md)

