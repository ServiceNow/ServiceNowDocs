---
title: Scheduling Health dashboard
description: Use this dashboard to view technician metrics, task metrics and Schedule Optimization configuration details.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Analytics and reporting for Field Service Management, Field Service Management]
---

# Scheduling Health dashboard

Use this dashboard to view technician metrics, task metrics and Schedule Optimization configuration details.

![Scheduling health dashboard overview](../../../product/field-service-management/image/Sch-Health-Dash.png)

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

Identifies factors that will prevent a work order task from being assigned.Click any area of the chart to see corresponding records.

</td></tr><tr><td>

Admin

</td><td>

Admins have the capabilities of a dispatcher and can update the information that is missing from the record.Click any area of the chart to see corresponding records.

</td></tr></tbody>
</table>## Overview Data Visualizations

<table id="table_jsj_vv3_qbc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Technicians without work schedule

</td><td>

Single Score

</td><td>

sys\_user

</td><td>

The number of agents who don't have a work schedule.

</td></tr><tr><td>

Technicians without location

</td><td>

Single Score

</td><td>

sys\_user

</td><td>

The number of agents whose user record doesn't have a location.

</td></tr><tr><td>

Technicians without location coordinates

</td><td>

Single Score

</td><td>

sys\_user

</td><td>

The number of agents whose user record doesn't have latitude and longitude.

</td></tr><tr><td>

Tasks without duration

</td><td>

Single Score

</td><td>

wm\_task

</td><td>

The number of tasks that don't have a duration.

</td></tr><tr><td>

Tasks without location

</td><td>

Single Score

</td><td>

wm\_task

</td><td>

The number of tasks that don't have a location.

</td></tr><tr><td>

Tasks without location coordinates

</td><td>

Single Score

</td><td>

wm\_task

</td><td>

The number of tasks that don't have latitude and longitude.

</td></tr></tbody>
</table>![Schedule optimization scheduling health metrics](../../../product/field-service-management/image/SO-scheduling-health.png)

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

The number of agents who will be included in the next optimization run.

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

The **Type** filter contains two choices, batch and intraday. Your selection will output one of the following subsequent filters.

|Name|Type|Description|
|----|----|-----------|
|Batch|Single select|Generate a report based on the selected batch configuration.|
|Intraday configuration|Single select|Generate a report based on the selected intraday configuration.|

**Parent Topic:**[Analytics and reporting for Field Service Management](../../../product/field-service-management/concept/analytics-reporting-fsm.md)

