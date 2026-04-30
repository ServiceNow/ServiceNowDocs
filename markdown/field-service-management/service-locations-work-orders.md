---
title: Setting ad hoc locations in work orders and work order tasks
description: The Field Service with Service Locations feature adds options to provide an ad hoc location when creating a work order or work order task on ServiceNow AI Platform, Agent Workspace, or Customer Service Portal.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Field Service with Service Locations, Using Field Service Management, Field Service Management]
---

# Setting ad hoc locations in work orders and work order tasks

The Field Service with Service Locations feature adds options to provide an ad hoc location when creating a work order or work order task on ServiceNow AI Platform, Agent Workspace, or Customer Service Portal.

If you do not want to use the auto-populated location in the **Location** field when creating a work order or work order task, you can add an ad hoc location. The default validation option for service locations determines whether you can use the Google map \(Using map\) or enter the address manually \(Without map or No validation\). For more information, see [Set the default validation option for service locations](../task/set-default-validation-option-for-service-locations.md).

<table id="table_hnd_rbq_gqb"><thead><tr><th>

Method

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Google map

</td><td>

The address information is entered in the text field or by dragging and dropping the marker. The fields auto-populate based on the address entered in the search field on a map.

 The Google Maps API key or client ID must be set in order to use the Google Maps API for Business. For more information, see [Set up Google Maps API](https://www.servicenow.com/docs/access?context=set-up-google-maps-api&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Without Google map

</td><td>

The address information is entered in the required fields. The **Latitude** and **Longitude** fields are grayed out and cannot be edited when the default validation option has been set to Without map.

 **Note:** If the default service location validation option has been set to Without map, the address will be validated using global.ServiceLocationAddressValidationExtPoint . If the option has been set to No validation, the address will not be validated.

</td></tr></tbody>
</table>**Parent Topic:**[Field Service with Service Locations](field-service-with-service-locations.md)

