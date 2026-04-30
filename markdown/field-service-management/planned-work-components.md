---
title: Planned Work Management Components
description: Several types of components are installed with Planned Work Management, including tables and business rules.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Components installed with additional plugins for Field Service Management, Field Service Management reference, Field Service Management]
---

# Planned Work Management Components

Several types of components are installed with Planned Work Management, including tables and business rules.

## Tables

Planned Work Management adds the following tables.

<table id="table_owq_qtx_d5b"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work Plan\[wm\_planned\_work\_plan\]

</td><td>

Stores the entities filtered for the work plan.

</td></tr><tr><td>

Planned Work Schedule\[wm\_planned\_work\_schedule\]

</td><td>

Stores the schedules configured for a work plan. A schedule can be duration, meter, condition, or script based.

</td></tr><tr><td>

Planned Work Schedule Template\[wm\_m2m\_schedule\_template\]

</td><td>

Stores the list of work order templates applied to planned work schedules.

</td></tr><tr><td>

Planned Work Record\[wm\_m2m\_work\_plan\_to\_record\]

</td><td>

Relates a work plan schedule to a record in the system \(from a document ID\). Also contains information about the last time or value the schedule ran for the record and the next time or value when the schedule will run.

</td></tr><tr><td>

Template Attribute Mapping\[wm\_m2m\_template\_attribute\_map\]

</td><td>

Stores the attribute mapping for a work order template.

</td></tr><tr><td>

Schedule Occurrence\[wm\_plan\_work\_schedule\_occurrence\]

</td><td>

Stores the occurrences of the work schedule.

</td></tr><tr><td>

Schedule Suppression\[wm\_m2m\_schedule\_suppression\]

</td><td>

Stores the occurences of suppressed work schedules.

</td></tr></tbody>
</table>## Roles

Planned Work Management adds the following roles.

<table id="table_prq_wsx_d5b"><thead><tr><th>

Roles

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Planned work admin \[sn\_fsm\_planned\_wm.planned\_work\_admin\]

</td><td>

Create work plans, planned work schedules, link work order templates to the schedules, and generate work orders.

</td></tr></tbody>
</table>## Script Includes

Planned Work Management adds the following script includes.

|Script Include|Description|
|--------------|-----------|
|PlannedWorkManagementExtensionPointImpl|Implements the Global.PlannedMaintenanceExtensionPoint extension point.|
|PlannedWorkMgmtAjaxUtil|Utility function for client scripts in planned work management.|
|PlannedWorkMgmtAPIHelperUtil|Utilities for wrapper function to invoke global scoped APIs from planned work management scope.|
|FSMPWMUtil|Utility function for planned work management scoped application.|
|PWMForecastWOUtil|Utility function to forecast work orders for the planned work.|
|PlannedMaintenanceExtensionPointImpl|Default implementation for planned maintenance application.|
|PlannedMaintenanceExtPointUtil|Utility in the planned maintenance application to retrieve extension points based on sys\_class\_name.|
|PlannedWorkManagementHistoryUtil|Utility in the planned work maintenance application to fetch the maintenance cycles history for an asset or inventory.|
|PlannedWorkManagementScheduleUtil|Maintains the processing logic for plan work record, schedule occurrences, work note comments etc.|
|PlannedWorkMangementPlanUtil|Utility methods related to work plan.|
|PlannedWorkManagementEffectivityUtil|Utility methods to determine and validate the effectivity of the schedule.|
|PlannedWorkManagementScheduleExeUtil|Acts as switch between the implementations of thePlannedWorkManagementExeExtensionPoint extension point based on order type. The default value of order type is work order.|
|PWMWorkOrderExeExtensionPointImpl|Implementation of the PlannedWorkManagementExeExtensionPoint extension point for the order type selected as work order.|
|PlannedWorkManagementConstants|Holds the constants for plan work management.|
|PWMScheduleSuppression|Maintains the processing logic of schedule suppression.|
|PWMScheduleOccurrence|Maintains the processing logic of schedule occurrence.|
|PWMScheduleOccurrenceDAO|Maintians the DAO methods of schedule occurrence.|
|PWMWorkScheduleDAO|Maintains the DAO methods for work schedule.|
|PWMPlanWorkRecordDAO|Maintains the DAO methods for plan record.|

## Business rules

Planned Work Management adds the following business rules.

<table id="table_x5f_1wx_d5b"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cross scope record creation

</td><td>

Work Plan\[wm\_planned\_work\_plan\]

</td><td>

Creates the cross scope access record on the table on which Maintenance plan is created and must be run.

</td></tr><tr><td>

cancel WO when plan record inactive

</td><td>

Planned Work Record\[wm\_m2m\_work\_plan\_to\_record\]

</td><td>

Cancels the work order for a plan record when that plan record is inactivated. The Plan record gets deactivated when the asset record is modified so that it doesn’t satisfies the filter condition at the plan level.

</td></tr><tr><td>

Planned work schedule to maintenance plan

</td><td>

Planned Work Schedule \[wm\_planned\_work\_schedule\]

</td><td>

Restricts the creation of Planned work schedule for maintenance plan. Only allows when the Plan is of class Planned work.

</td></tr><tr><td>

Restrict model per schedule

</td><td>

Planned Work Schedule Template\[wm\_m2m\_schedule\_template\]

</td><td>

Restricts the creation of duplicate model schedule in the table.

</td></tr><tr><td>

Restrict table map for model

</td><td>

Template Attribute Mapping\[wm\_m2m\_template\_attribute\_map\]

</td><td>

Restricts the user to have single table map per a work order template

</td></tr><tr><td>

Update m2m schedule records new fields

</td><td>

Planned Work Schedule\[wm\_planned\_work\_schedule\]

</td><td>

Updates the schedule record and recalculates the next value or next run time when meter or duration fields change.

</td></tr><tr><td>

Validate plan effective start, end

</td><td>

Work Plan\[wm\_planned\_work\_plan\]

</td><td>

Checks if the effective start and end date of the work plan are valid.

</td></tr><tr><td>

Work schedule template to maint schedule

</td><td>

Planned Work Schedule Template\[wm\_m2m\_schedule\_template\]

</td><td>

Restricts the user to add maintenance schedule to planned work schedule template.

</td></tr><tr><td>

Update latest completion date in Work order

</td><td>

Work Order Task\[wm\_Task\]

</td><td>

Updates the latest completion date in work order for grace time SLA.

</td></tr><tr><td>

Compare schedule template tasks

</td><td>

Schedule Suppression\[wm\_m2m\_schedule\_suppression\]

</td><td>

 

</td></tr><tr><td>

Validate cyclic dependency

</td><td>

Schedule Suppression\[wm\_m2m\_schedule\_suppression\]

</td><td>

 

</td></tr><tr><td>

Suppress SO by schedule suppression

</td><td>

Schedule Suppression\[wm\_m2m\_schedule\_suppression\]

</td><td>

 

</td></tr><tr><td>

Suppress SO by schedule

</td><td>

Schedule Occurrence \[wm\_plan\_work\_schedule\_occurrence\]

</td><td>

 

</td></tr><tr><td>

Suppress SO by suppressBy schedule

</td><td>

Schedule Occurrence \[wm\_plan\_work\_schedule\_occurrence\]

</td><td>

 

</td></tr><tr><td>

Cancel WO if SO inactive

</td><td>

Schedule Occurrence \[wm\_plan\_work\_schedule\_occurrence\]

</td><td>

 

</td></tr><tr><td>

Check effective start of SO

</td><td>

Schedule Occurrence \[wm\_plan\_work\_schedule\_occurrence\]

</td><td>

 

</td></tr><tr><td>

Change WO fields on SO field changes

</td><td>

Schedule Occurrence \[wm\_plan\_work\_schedule\_occurrence\]

</td><td>

 

</td></tr></tbody>
</table>-   **[Planned Work Management system properties](planned_work_management_sys_properties.md)**  
Planned Work Management uses the following system properties, which are located in the System Properties \[sys\_properties\] table.

**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

