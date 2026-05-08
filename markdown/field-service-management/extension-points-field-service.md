---
title: Extension points in Field Service Management
description: Use extension points to customize various configurations.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Plan implementation, Configure, Field Service Management]
---

# Extension points in Field Service Management

Use extension points to customize various configurations.

In the application navigator, enter `sys_extension_point.list` and click **Enter** to view the extension points used in the Field Service Management application.

You can create multiple implementations for each extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed.

Extension points are available for the following configurations:

-   Event type schedule entries
-   Appointment booking

|Extension Point Name|Description|
|--------------------|-----------|
|AgentEventUtil|Customize the logic for event type schedule entries.|
|AgentScheduleUtil|Customize the logic for computing event time-off spans.|

<table id="table_yqj_lhz_qfb"><thead><tr><th>

Extension Point Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_apptmnt\_booking.AppointmentBookingAvailabilityExtPoint

</td><td>

Customize the logic to determine bookable appointment windows.

</td></tr><tr><td>

sn\_apptmnt\_booking.AppointmentBookingDaoExtPoint

</td><td>

Customize the logic used to create or update an appointment record.

</td></tr><tr><td>

sn\_apptmnt\_booking.AppointmentBookingImplExtPoint

</td><td>

Customize the logic to validate appointment data before an appointment is created.

</td></tr><tr><td>

sn\_apptmnt\_booking.AppointmentBookingUtilExtPoint

</td><td>

Customize logic to create a parameter map of appointment data which will be used to create and update appointment records.

</td></tr><tr><td>

sn\_apptmnt\_booking.AppointmentRescheduleCancelExtPoint

</td><td>

Customize logic used to determine whether appointments can be canceled or rescheduled.

</td></tr><tr><td>

sn\_apptmnt\_booking.AppointmentRESTHelperExtPoint

</td><td>

Customize logic for retrieving a list of date and time periods available for appointment booking.

</td></tr><tr><td>

sn\_apptmnt\_booking.AppointmentRecommendationExtPoint

</td><td>

Allows other applications to integrate appointment booking slot recommendation.

</td></tr><tr><td>

sn\_apptmnt\_booking.AppointmentBookingLockingUtilExtPoint

</td><td>

Acquire and release locks in Appointment Booking workflow.

</td></tr><tr><td>

sn\_apptmnt\_booking.AppointmentBookingVariablesExtensionPoint

</td><td>

Utilized by the Appointment API and Booking API to fetch **Catalog\_id** for the task.

</td></tr><tr><td>

sn\_apptmnt\_booking.AppointmentEnableUnifiedUI

</td><td>

Enables the unified UI Calendar component for the specific task table extension.

</td></tr><tr><td>

sn\_apptmnt\_booking.AppointmentHolidayHelperExt

</td><td>

Calculates the lead time by taking into account holidays as indicated by the **consider\_holidays\_in\_leadtime** setting in Appointment Booking service configuration.

</td></tr><tr><td>

sn\_apptmnt\_booking.AppointmentLeadTimeCalculation

</td><td>

Determines whether to consider or ignore the lead time for rescheduling an appointment, based on the **ignore\_lead\_time\_on\_reschedule** setting in the Appointment Booking service configuration.

</td></tr><tr><td>

sn\_apptmnt\_booking.use\_unified\_appt\_widget

</td><td>

Allow other applications to use seismic appointment booking calendar.

</td></tr><tr><td>

sn\_apptmnt\_booking.AppointmentRecommendationExtPoint

</td><td>

Customize the proximity and recommendation criteria for recommending appointments.

</td></tr><tr><td>

sn\_apptmnt\_booking.AppointmentSeismicUI

</td><td>

Fetches appointment booking configuration details based on the task table selected in the configuration.

</td></tr></tbody>
</table>|Extension Point Name|Description|
|--------------------|-----------|
|sn\_fsm\_adv\_tmp.FSMTemplateMgmntExtPoint|Customize the logic to enable the work order template to map information from source table to the appropriate fields in a work order.|
|sn\_fsm\_adv\_tmp.FSMTableMapSourceIdentifier|Customize the logic to identify the source of a work order.|

|Extension Point Name|Description|
|--------------------|-----------|
|OnsiteGeofenceConfig|Allows you to define default values for the geofence radius and geofence unit fields in the work order task.|

|Extension Point Name|Description|
|--------------------|-----------|
|Heatmap Gradient \(sn\_cmn\_mo.HeatmapGradient\)|Allows you to define the color gradient of the heatmap.|

|Extension Point Name|Description|
|--------------------|-----------|
|TerritoryIndicators\(sn\_fsm\_tp.TerritoryIndicators\)|Allows you to define the key performance indicators \(KPIs\) to analyze the performance of the territory. The configured indicators appear in the contextual side panel of the Field Service Territory Planning console.|

<table id="table_l5r_gvw_zfc"><thead><tr><th>

Extension Point Name

</th><th>

 

</th></tr></thead><tbody><tr><td>

sn\_fsm\_planned\_wm.PWMScheduleSuppressionExtensionPoint

</td><td>

Customize the logic to validate when a schedule occurrence is suppressed.

</td></tr><tr><td>

sn\_fsm\_planned\_wm.PWMScheduleEffectivityExtensionPoint

</td><td>

Calculates the request dues, next run times, and the effectivity based on the configurations or rules.

</td></tr><tr><td>

sn\_fsm\_planned\_wm.PWMSourceRecordExtensionPoint

</td><td>

Derives the source specific fields like location, asset, CI, or IB based on the table associated to maintenance plan.

</td></tr><tr><td>

sn\_fsm\_planned\_wm.PlannedWorkManagementExeExtensionPoint

</td><td>

Processes plan maintenance schedule outcomes like a work order.

</td></tr><tr><td>

sn\_fsm\_planned\_wm.PWMScheduleStartExtensionPoint

</td><td>

Customize the effective start date of work plan schedule for different assets.When you configure a planned work schedule to start on a calculated date, the schedule starts on the effective start date calculated by the custom implementation of this extension point.

**Note:** A default implementation is provided for this extension point. You can modify the default implementation as per you business requirements.

</td></tr><tr><td>

sn\_fsm\_planned\_wm.TaskPlanTemplateOutputTasks

</td><td>

Customize CRUD operations for the tasks, cases, or incidents created from task plan templates linked to a work plan.For example, for a business unit of your organization, you can customize the extension point to create cases for a work plan and link them to schedule occurrences through a new field in the Cases record.

For another business unit, you can customize the extension point to create cases and link them to the schedule occurrences through a new table.

</td></tr></tbody>
</table>**Related topics**  


[bundle-crapiref.extension-points]

[bundle-crapiref.scripted-extension-points]

[bundle-crapiref.ui-extension-points]

[bundle-crapiref.client-extension-points]

