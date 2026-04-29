---
title: Scheduling Health dashboard
description: Use this dashboard to view technician metrics, task metrics, and Schedule Optimization configuration details.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Analytics and reporting, Field Service Management]
---

# Scheduling Health dashboard

Use this dashboard to view technician metrics, task metrics, and Schedule Optimization configuration details.

![schedule health dashboard](../../../product/field-service-management/image/schedule-health-dash.png)

## Required ServiceNow AI Platform roles

-   The wm\_basic role is needed to view the dashboard **Overview** tab.
-   The schedule\_optimization\_planner or schedule\_optimization\_user is needed to view the **Schedule Optimization** tab.

## Access the Scheduling Health dashboard

To open the dashboard, navigate to:

-   **All** &gt; **Field Service** &gt; **Administration** &gt; **Health Check**
-   **All** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Health Check**

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_esj_vv3_qbc"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Dispatcher

</td><td>

Identifies factors that prevent a work order task from being assigned.Select any area of the chart to see corresponding records.

</td></tr><tr><td>

Admin

</td><td>

Admins have the capabilities of a dispatcher and can update the information that is missing from the record.Select any area of the chart to see corresponding records.

</td></tr></tbody>
</table>## Overview Data Visualizations

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Technicians without work schedule|Single Score|sys\_user|The number of technicians who don't have a work schedule.|
|Technicians without location|Single Score|sys\_user|The number of technicians whose user record doesn't have a location.|
|Technicians without location coordinates|Single Score|sys\_user|The number of technicians whose user record doesn't have latitude and longitude.|
|Technicians without skills|Single Score|sys\_user|The number of technicians with no skill assignments.|
|Technicians with invalid skills|Single Score|sys\_user|The number of technicians with one or more empty skill assignments.|
|Technicians without parts|Single Score|sys\_user|The number of technicians with no parts in their personal stockroom.|
|Technicians without time zone|Single Score|sys\_user|The number of technicians who don’t have a time zone set on their user record.|
|Technicians with invalid location coordinates|Single Score|sys\_user|The number of technicians with invalid latitude and longitude values. For example, coordinates with more than one decimal point.|

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Tasks without duration|Single Score|wm\_task|The number of tasks that don't have a duration.|
|Tasks without location|Single Score|wm\_task|The number of tasks that don't have a location.|
|Tasks without location coordinates|Single Score|wm\_task|The number of tasks that don't have latitude and longitude.|
|Tasks without optimization value|Single Score|wm\_task|The number of tasks that don't have an optimization value.|
|Tasks without skills|Single Score|task\_m2m\_skill|The number of tasks with no skill requirements.|
|Tasks without parts|Single Score|wm\_task|The number of tasks with no part requirements.|
|Tasks without technician preferences|Single Score|wm\_task|The number of tasks that don't have technician preferences.|
|Tasks without location time zone|Single Score|wm\_task|The number of tasks that don’t have a time zone set.|
|Tasks with scheduled start in the past|Single Score|wm\_task|The number of tasks whose scheduled start time is at least one day in the past.|
|Tasks with window end in the past|Single Score|wm\_task|Tasks with the window end that was at least one minute ago.|
|On route tasks without actual travel start|Single Score|wm\_task|The number of tasks that have been accepted and the agent is on route, but no travel start time is set.|
|On-site tasks without on-site arrival|Single Score|wm\_task|The number of tasks that have been accepted and the agent has arrived, but no on‑site arrival time is set.|
|Tasks with invalid skills|Single Score|cmn\_skills|The number of tasks with assigned skills that don’t exist in the cmn\_skills table.|

![Schedule optimization scheduling health metrics](../../../product/field-service-management/image/SO-scheduling-health.png)

## Schedule Optimization Data Visualizations

<table id="table_fcv_mfp_sbc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total number of technicians

</td><td>

Single Score

</td><td>

sys\_user

</td><td>

The number of technicians who will be included in the next optimization run.

</td></tr><tr><td>

Total number of tasks

</td><td>

Single Score

</td><td>

wm\_task

</td><td>

The number of tasks that will be included in the next optimization run.

</td></tr><tr><td>

Next optimization run time

</td><td>

Date/Time

</td><td>

 

</td><td>

The date and time of the next scheduled optimization run.

</td></tr></tbody>
</table>## Filters

The **Type** filter contains two choices, batch and intraday. Your selection outputs one of the following subsequent filters.

|Name|Type|Description|
|----|----|-----------|
|Batch|Single select|Generate a report based on the selected batch configuration.|
|Intraday configuration|Single select|Generate a report based on the selected intraday configuration.|

**Parent Topic:**[Analytics and reporting for Field Service Management](../../../product/field-service-management/concept/analytics-reporting-fsm.md)

