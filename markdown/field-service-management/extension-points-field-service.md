---
title: Extension points in Field Service Management
description: Use extension points to customize various configurations.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Planning your Field Service Management implementation, Configuring Field Service Management, Field Service Management]
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

**Related topics**  


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

[Using scripted extension points in server-side scripts](https://www.servicenow.com/docs/access?context=scripted-extension-points&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

[Using UI extension points in server-side UI macros](https://www.servicenow.com/docs/access?context=ui-extension-points&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

[Using client extension points in client-side UI scripting](https://www.servicenow.com/docs/access?context=client-extension-points&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

