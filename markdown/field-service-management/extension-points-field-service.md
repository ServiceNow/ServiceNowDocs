---
title: Extension points in Field Service Management
description: Use extension points to customize various configurations.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Planning your Field Service Management implementation, Configuring Field Service Management, Field Service Management]
---

# Extension points in Field Service Management

Use extension points to customize various configurations.

In the application navigator, enter `sys_extension_point.list` and click **Enter** to view the extension points used in the Field Service Management application.

You can create multiple implementations for each extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed.

|Extension Point Name|Description|
|--------------------|-----------|
|AgentEventUtil|Customize the logic for event type schedule entries.|
|AgentScheduleUtil|Customize the logic for computing event time-off spans.|

|Extension Point Name|Description|
|--------------------|-----------|
|sn\_apptmnt\_booking.AppointmentBookingAvailabilityExtPoint|Customize the logic to determine bookable appointment windows.|
|sn\_apptmnt\_booking.AppointmentBookingDaoExtPoint|Customize the logic used to create or update an appointment record.|
|sn\_apptmnt\_booking.AppointmentBookingImplExtPoint|Customize the logic to validate appointment data before an appointment is created.|
|sn\_apptmnt\_booking.AppointmentBookingUtilExtPoint|Customize logic to create a parameter map of appointment data which will be used to create and update appointment records.|
|sn\_apptmnt\_booking.AppointmentRescheduleCancelExtPoint|Customize logic used to determine whether appointments can be canceled or rescheduled.|
|sn\_apptmnt\_booking.AppointmentRESTHelperExtPoint|Customize logic for retrieving a list of date and time periods available for appointment booking.|

|Extension Point Name|Description|
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


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[Using scripted extension points in server-side scripts](https://www.servicenow.com/docs/access?context=scripted-extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[Using UI extension points in server-side UI macros](https://www.servicenow.com/docs/access?context=ui-extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[Using client extension points in client-side UI scripting](https://www.servicenow.com/docs/access?context=client-extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

