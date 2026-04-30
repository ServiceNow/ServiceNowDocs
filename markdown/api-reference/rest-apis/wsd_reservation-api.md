---
title: WSD Reservation API
description: The Workplace Service Delivery \(WSD\) Reservation API provides endpoints for managing workplace reservations.Retrieves the specified workplace reservation.Retrieves the list of reservation for a specified user for the next seven days.Generates an iCalendar file body for a specified reservation.Retrieves the list of reservations belonging to a specified user.Cancels a specified workplace reservation.Updates and shares the reservation details with a specified list of recipients through an email notification. Optionally you can send a specified message along with the reservation.Updates a specified workplace reservation.Creates a new workplace reservation.Creates a new workplace reservation using quick reserve.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 90
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD Reservation API

The Workplace Service Delivery \(WSD\) Reservation API provides endpoints for managing workplace reservations.

To access this API, the caller must have the sn\_wsd\_core.workplace\_user role and the Workplace Safety Management \(sn\_wsd\_core\) and Workplace Reservation Management \(sn\_wsd\_rsv\) plugins must be activated.

This API runs in the `sn_wsd_rsv` namespace.

For additional information on Workplace Reservation Management, see [Workplace Reservation Management](https://www.servicenow.com/docs/access?context=workplace-rsv-mgmt-feat&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD Reservation - GET /api/sn\_wsd\_rsv/reservation/get

Retrieves the specified workplace reservation.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/reservation/get`

Default URL: `/api/sn_wsd_rsv/reservation/get`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

external\_ical

</td><td>

Unique external iCalendar identification of the reservation. Use this value to identify the reservation when this is a calendar sync related reservation. Obtain this value from the associated external iCalendar application.Data type: String

</td></tr><tr><td>

external\_id

</td><td>

Unique external identification of the reservation. Use this value to identify the reservation when this is a calendar sync related reservation. Obtain this value from the associated external application.Data type: String

</td></tr><tr><td>

include\_multi\_child\_​data

</td><td>

If the reservation\_subtype field value in the associated Workplace Reservation \[sn\_wsd\_rsv\_reservation\] record is set to multi\_child, this flag indicates whether to return the reservation details.Valid values:

-   true: Return the reservation details.
-   false: Do not return the reservation details.

 Data type: Boolean

 Default value: false

</td></tr><tr><td>

include\_standard\_​services

</td><td id="include_standard_services-reserv-entry">

Flag that indicates whether to return the standard services information in the response. This information is located in the Standard Service \[sn\_wsd\_rsv\_standard\_service\] table.A standard service describes basic provisions available with a reservable workplace item when the reservation is made, such as white boards, additional monitors, and similar services. For additional information on standard services, see [Standard services](https://www.servicenow.com/docs/access?context=standard-service&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Valid values:

-   true: Return the standard services information.
-   false: Don't return the standard services information.

Data type: Boolean

Default: false

</td></tr><tr><td>

sys\_id

</td><td>

Required. Sys\_id of the reservation record.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-reserv-entry">

Data format of the request body. Supported types: **application/json**, **application/xml** or, **text/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="id_sps_3gz_stb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result.reservation

</td><td>

Details about the reservation.Data type: Object

```
"reservation": {
  "active": Boolean,
  "attendees": [Array],
  "check_in_state": {Object},
  "end": "String",
  "external_ical": "String",
  "external_id": "String",
  "is_parent": Boolean,
  "is_private": Boolean,
  "informEmployeePrivacy": Boolean.
  "last_updated_sub_source": {Object},
  "location" {Object},
  "number": "String",
  "number_of_attendees": Number,
  "recording_details": [Array],
  "reservable_module": {Object},
  "reservation_purpose": {Object},
  "reservation_type": {Object},
  "reservation_subtype": {Object},
  "sensitivity": {Object},
  "start": "String",
  "state": {Object},
  "source_reservation": "String",
  "subject": "String",
  "sub_source": {Object},
  "sync_state": {Object},
  "sys_created_on: "String",
  "sys_id": "String",
  "sys_updated_on": "String",
  "virtual_meeting": "String"
}
```

</td></tr><tr id="reservation_active-reserv-row"><td>

result.reservation.active

</td><td id="reservation_active-reserv-entry">

Flag that indicates whether the reservation is active.Valid values:

-   true: Reservation is active.
-   false: Reservation is inactive.

Data type: Boolean

</td></tr><tr id="reservation_attendees-reserv-row"><td>

result.reservation.attendees

</td><td id="reservation_attendees-reserv-entry">

List of attendees for the reservation.Data type: Array of Objects

```
"attendees": [
  {
    "avatar": "String",
    "displayValue": "String",
    "display_value": "String",
    "email": "String",
    "initials": "String",
    "label": "String",
    "name": "String",
    "sys_id": "String",
    "table": "String",
    "user_name": "String",
    "value": "String"
  }
]
```

</td></tr><tr id="reservation_attendees_avatar-reserv-row"><td>

result.reservation.attendees.avatar

</td><td id="reservation_attendees_avatar-reserv-entry">

Sys\_id of the avatar associated with the attendee.Data type: String

Table: Attachments \[sys\_attachment\]

</td></tr><tr id="reservation_attendees_displayValue-reserv-row"><td>

result.reservation.attendees.displayValue

</td><td id="reservation_attendees_displayValue-reserv-entry">

Display value for the attendee.Data type: String

</td></tr><tr id="reservation_attendees_display_value-reserv-row"><td>

result.reservation.attendees.display\_value

</td><td id="reservation_attendees_display_value-reserv-entry">

Display value of the attendee. Same as **displayValue**.Data type: String

</td></tr><tr id="reservation_attendees_mail-reserv-row"><td>

result.reservation.attendees.email

</td><td id="reservation_attendees_mail-reserv-entry">

Attendee's email address.Data type: String

</td></tr><tr id="reservation_attendees_initials-reserv-row"><td>

result.reservation.attendees.initials

</td><td id="reservation_attendees_initials-reserv-entry">

Attendee's initials.Data type: String

</td></tr><tr id="reservation_attendees_name-reserv-row"><td>

result.reservation.attendees.name

</td><td id="reservation_attendees_name-reserv-entry">

Attendee's name.Data type: String

</td></tr><tr id="reservation_attendees_sys_id-reserv-row"><td>

result.reservation.attendees.sys\_id

</td><td id="reservation_attendees_sys_id-reserv-entry">

Sys\_id of the attendee record.Data type: String

</td></tr><tr id="reservation_attendees_table-reserv-row"><td>

result.reservation.attendees.table

</td><td id="reservation_attendees_table-reserv-entry">

Table in which the attendee record exists.Data type: String

</td></tr><tr id="reservation_attendees_user_name-reserv-row"><td>

result.reservation.attendees.user\_name

</td><td id="reservation_attendees_user_name-reserv-entry">

Attendee's user name.Data type: String

</td></tr><tr id="reservation_attendees_value-reserv-row"><td>

result.reservation.attendees.value

</td><td id="reservation_attendees_value-reserv-entry">

Internal value of the attendee.Data type: String

</td></tr><tr id="reservation_attendees_check_in_state-reserv-row"><td>

result.reservation.check\_in\_state

</td><td id="reservation_attendees_check_in_state-reserv-entry">

Details about the check-in state of the reservation.Data type: Object

```
"check_in_state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_attendees_check_in_state_display_value-reserv-row"><td>

result.reservation.check\_in\_state.​display\_value

</td><td id="reservation_attendees_check_in_state_display_value-reserv-entry">

Display value for the current check-in state of the reservation, such as In progress or complete.Data type: String

</td></tr><tr id="reservation_attendees_check_in_state_value-reserv-row"><td>

result.reservation.check\_in\_state.value

</td><td id="reservation_attendees_check_in_state_value-reserv-entry">

Internal value for the current check-in state of the reservation, such as 2.Data type: String

</td></tr><tr id="reservation_attendees_edit_restriction-reserv-row"><td>

result.reservation.edit\_restriction

</td><td id="reservation_attendees_edit_restriction-reserv-entry">

Description of the user edit restrictions for the reservation, such as no\_restrictions, service\_only, or fully\_restricted.Data type: Object

```
"edit_restriction": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_attendees_edit_restriction_display_value-reserv-row"><td>

result.reservation.edit\_restriction.display\_​value

</td><td id="reservation_attendees_edit_restriction_display_value-reserv-entry">

Display value for the edit restrictions for the reservation, such as `No restriction`.Data type: String

</td></tr><tr id="reservation_attendees_edit_restriction_value-reserv-row"><td>

result.reservation.edit\_restriction.value

</td><td id="reservation_attendees_edit_restriction_value-reserv-entry">

Internal value for the edit restrictions for the reservation, such as `no_restriction`.Data type: String

</td></tr><tr id="end-reserv-row"><td>

result.reservation.end

</td><td id="end-reserv-entry">

Reservation end date and time.Data type: String

Format: UTC: yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr id="reservation_external_ical-reserv-row"><td>

result.reservation.external\_ical

</td><td id="reservation_external_ical-reserv-entry">

Unique external iCalendar identification of the reservation. Use this value to identify the reservation when this is a calendar sync related reservation.Data type: String

</td></tr><tr id="reservation_external_id-reserv-row"><td>

result.reservation.external\_id

</td><td id="reservation_external_id-reserv-entry">

Unique external identification of the reservation. Use this value to identify the reservation when this is a calendar sync related reservation.Data type: String

</td></tr><tr id="reservation_is_parent-reserv-row"><td>

result.reservation.is\_parent

</td><td id="reservation_is_parent-reserv-entry">

Flag that indicates whether this reservation is a parent reservation.Possible values:

-   true: Parent reservation.
-   false: Not a parent reservation.

Data type: Boolean

</td></tr><tr><td>

result.reservation.is\_private

</td><td>

Flag that indicates whether the reservation is private. If private, the reservation doesn't appear to anyone except the owner.For additional information on these privacy settings, see [Location privacy settings and impact](https://www.servicenow.com/docs/access?context=location-privacy-settings-and-impact&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Valid values:

-   true: Reservation is private.
-   false: Reservation isn't private.

Data type: Boolean

Default: Value set for privacy in the system properties.

</td></tr><tr id="reservation_last_updated_sub_source-reserv-row"><td>

result.reservation.last\_updated\_sub\_source

</td><td id="reservation_last_updated_sub_source-reserv-entry">

Details about the last updated sub-source for the reservation. Sub-sources are used when integrating reservations with an external calendar. This object contains information such as "servicenow\_workplace\_service\_delivery", "google\_calendar", or "microsoft\_exchange".Data type: Object

```
"last_updated_sub_source": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_last_updated_sub_source_display_value-reserv-row"><td>

result.reservation.last\_updated\_sub\_source.​display\_value

</td><td id="reservation_last_updated_sub_source_display_value-reserv-entry">

Display value for the last updated sub-source of the reservation, such as `ServiceNow Workplace Service Delivery` or `Google Calendar`. Used when integrating the reservation with an outside service such as Google calendar or Microsoft Outlook.Data type: String

</td></tr><tr id="reservation_last_updated_sub_source_value-reserv-row"><td>

result.reservation.last\_updated\_sub\_source.​value

</td><td id="reservation_last_updated_sub_source_value-reserv-entry">

Internal value for the last updated sub-source of the reservation, such as `servicenow_workplace_service_delivery` or `google_calendar`. Used when integrating the reservation with an outside service such as Google calendar or Microsoft Outlook.Data type: String

</td></tr><tr id="reservation_location-reserv-row"><td>

result.reservation.location

</td><td id="reservation_location-reserv-entry">

Details about the location associated with the reservation.Data type: Object

```
"location": {
  "active": Boolean,
  "area": {Object},
  "building": {Object},
  "campus": {Object},
  "capacity": Number,
  "description": "String",
  "display_value": "String",
  "email": "String",
  "floor": {Object},
  "label_value": "String",
  "name": "String",
  "number_of_attendees": Number,
  "region": {Object},
  "reservable_module": {Object},
  "reservation": {Object},
  "site": {Object},
  "state": {Object},
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_location_area-reserv-row"><td>

result.reservation.location.area

</td><td id="reservation_location_area-reserv-entry">

Details about the area associated with the location.Data type: Object

```
"area": {
  "active": Boolean,
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_location_area_active-reserv-row"><td>

result.reservation.location.area.active

</td><td id="reservation_location_area_active-reserv-entry">

Flag that indicates whether the area is active.Valid values:

-   true: Area is active.
-   false: Area is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_area_display_value-reserv-row"><td>

result.reservation.location.area.display\_value

</td><td id="reservation_location_area_display_value-reserv-entry">

Display value of the area to which this location belongs, such as Desk A2.Data type: String

</td></tr><tr id="reservation_location_area_sys_id-reserv-row"><td>

result.reservation.location.area.sys\_id

</td><td id="reservation_location_area_sys_id-reserv-entry">

Sys\_id of the area to which this location belongs.Data type: String

Table: Area \[sn\_wsd\_core\_area\]

</td></tr><tr id="reservation_location_building-reserv-row"><td>

result.reservation.location.building

</td><td id="reservation_location_building-reserv-entry">

Details about the building associated with the location.Data type: Object

```
"building": {
  "active": Boolean,
  "display_value": "String",
  "sys_id": "String",
  "timezone": {Object}
}
```

</td></tr><tr id="reservation_location_building_active-reserv-row"><td>

result.reservation.location.building.active

</td><td id="reservation_location_building_active-reserv-entry">

Flag that indicates whether the building is active.Valid values:

-   true: Building is active.
-   false: Building is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_building_display_value-reserv-row"><td>

result.reservation.location.building.​display\_value

</td><td id="reservation_location_building_display_value-reserv-entry">

Display value of the building to which this location belongs, such as AMS - Bld1.Data type: String

</td></tr><tr id="reservation_location_building_sys_id-reserv-row"><td>

result.reservation.location.building.sys\_id

</td><td id="reservation_location_building_sys_id-reserv-entry">

Sys\_id of the building to which this location belongs.Data type: String

Table: Building \[sn\_wsd\_core\_building\]

</td></tr><tr id="timezone-reserv-row"><td>

result.reservation.location.building.timezone

</td><td id="timezone-reserv-entry">

Details about the time zone associated with the location.Data type: Object

```
"timezone": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr id="timezone_display_value-reserv-row"><td>

result.reservation.location.building.timezone.​display\_value

</td><td id="timezone_display_value-reserv-entry">

Display value for the time zone to which this location belongs.Data type: String

</td></tr><tr id="timezone_value-reserv-row"><td>

result.reservation.location.building.timezone.​value

</td><td id="timezone_value-reserv-entry">

Internal value for the time zone to which this location belongs.Data type: String

</td></tr><tr id="reservation_location_campus-reserv-row"><td>

result.reservation.location.campus

</td><td id="reservation_location_campus-reserv-entry">

Details about the campus associated with the location.Data type: Object

```
"campus": {
  "active": Boolean,
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_location_campus_active-reserv-row"><td>

result.reservation.location.campus.active

</td><td id="reservation_location_campus_active-reserv-entry">

Flag that indicates whether the campus is active.Valid values:

-   true: Campus is active.
-   false: Campus is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_campus_display_value-reserv-row"><td>

result.reservation.location.campus.​display\_value

</td><td id="reservation_location_campus_display_value-reserv-entry">

Display value of the campus to which this location belongs, such as Amsterdam Campus.Data type: String

</td></tr><tr id="reservation_location_campus_sys_id-reserv-row"><td>

result.reservation.location.campus.sys\_id

</td><td id="reservation_location_campus_sys_id-reserv-entry">

Sys\_id of the campus to which this location belongs.Data type: String

Table: Campus \[sn\_wsd\_core\_campus\]

</td></tr><tr id="reservation_location_capacity-reserv-row"><td>

result.reservation.location.capacity

</td><td id="reservation_location_capacity-reserv-entry">

Maximum number of occupants for the location.Data type: Number

</td></tr><tr id="reservation_location_description-reserv-row"><td>

result.reservation.location.description

</td><td id="reservation_location_description-reserv-entry">

Brief description of the location.Data type: String

</td></tr><tr id="reservation_location_display_value-reserv-row"><td>

result.reservation.location.display\_value

</td><td id="reservation_location_display_value-reserv-entry">

Value to display in the UI for this location.Data type: String

</td></tr><tr id="reservation_location_email-reserv-row"><td>

result.reservation.location.email

</td><td id="reservation_location_email-reserv-entry">

Email address for the location.Data type: String

</td></tr><tr id="reservation_location_floor-reserv-row"><td>

result.reservation.location.floor

</td><td id="reservation_location_floor-reserv-entry">

Details about the floor associated with the location.Data type: Object

```
"floor": {
  "active": Boolean,
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_location_floor_active-reserv-row"><td>

result.reservation.location.floor.active

</td><td id="reservation_location_floor_active-reserv-entry">

Flag that indicates whether the floor is active.Valid values:

-   true: Floor is active.
-   false: Floor is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_floor_display_value-reserv-row"><td>

result.reservation.location.floor.display\_value

</td><td id="reservation_location_floor_display_value-reserv-entry">

Display value of the floor to which this location belongs, such as First floor.Data type: String

</td></tr><tr id="reservation_location_floor_sys_id-reserv-row"><td>

result.reservation.location.floor.sys\_id

</td><td id="reservation_location_floor_sys_id-reserv-entry">

Sys\_id of the floor to which this location belongs.Data type: String

Table: Floor \[sn\_wsd\_core\_floor\]

</td></tr><tr id="reservation_location_floor_label_value-reserv-row"><td>

result.reservation.location.label\_value

</td><td id="reservation_location_floor_label_value-reserv-entry">

Type of value specified in the **name** parameter, such as Room name.Data type: String

</td></tr><tr id="reservation_location_floor_name-reserv-row"><td>

result.reservation.location.name

</td><td id="reservation_location_floor_name-reserv-entry">

Name of the location.Data type: String

</td></tr><tr id="reservation_location_floor_number-reserv-row"><td>

result.reservation.location.number

</td><td id="reservation_location_floor_number-reserv-entry">

Reservation number.Data type: String

</td></tr><tr id="reservation_location_number_of_attendees-reserv-row"><td>

result.reservation.location.number\_of\_​attendees

</td><td id="reservation_location_number_of_attendees-reserv-entry">

Number of attendees for the reservation.Data type: Number

</td></tr><tr id="reservation_location_region-reserv-row"><td>

result.reservation.location.region

</td><td id="reservation_location_region-reserv-entry">

Details about the region associated with the location.Data type: Object

```
"region": {
  "active": Boolean,
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_location_region_active-reserv-row"><td>

result.reservation.location.region.active

</td><td id="reservation_location_region_active-reserv-entry">

Flag that indicates whether the region is active.Valid values:

-   true: Region is active.
-   false: Region is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_region_display_value-reserv-row"><td>

result.reservation.location.region.​display\_value

</td><td id="reservation_location_region_display_value-reserv-entry">

Display value of the region to which this location belongs, such as Europe.Data type: String

</td></tr><tr id="reservation_location_region_sys_id-reserv-row"><td>

result.reservation.location.region.sys\_id

</td><td id="reservation_location_region_sys_id-reserv-entry">

Sys\_id of the region to which this location belongs.Data type: String

Table: Region \[sn\_wsd\_core\_region\]

</td></tr><tr id="reservation_location_region_requested_for-reserv-row"><td>

result.reservation.location.requested\_for

</td><td id="reservation_location_region_requested_for-reserv-entry">

Details about the person for whom the reservation was requested on behalf of.Data type: Object

```
"requested_for": {
  "name": "String",
  "sys_id": "String",
  "user_name": "String"
}
```

</td></tr><tr id="requested_for_name-reserv-row"><td>

result.reservation.location.requested\_for.​name

</td><td id="requested_for_name-reserv-entry">

Name of the user for whom the reservation was requested for.Data type: String

</td></tr><tr id="requested_for_sys_id-reserv-row"><td>

result.reservation.location.requested\_for.​sys\_id

</td><td id="requested_for_sys_id-reserv-entry">

Sys\_id of the user for whom the reservation is being requested.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="reservation_location_requested_for_user_name-reserv-row"><td>

result.reservation.location.requested\_for.​user\_name

</td><td id="reservation_location_requested_for_user_name-reserv-entry">

User name of the user for whom the reservation was requested for.Data type: String

</td></tr><tr id="reservation_location_reservation-reserv-row"><td>

result.reservation.location.reservation

</td><td id="reservation_location_reservation-reserv-entry">

Details about the reservation associated with the location.Data type: Object

```
"reservation": {
  "active": Boolean,
  "number": "String",
  "number_of_attendees": Number,
  "requested_for": {Object},
  "state": {Object},
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_location_reservation_active-reserv-row"><td>

result.reservation.location.reservation.active

</td><td id="reservation_location_reservation_active-reserv-entry">

Flag that indicates whether the reservation is active.Valid values:

-   true: Reservation is active.
-   false: Reservation is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_reservation_number-reserv-row"><td>

result.reservation.location.reservation.number

</td><td id="reservation_location_reservation_number-reserv-entry">

Reservation number.Data type: String

</td></tr><tr id="reservation_location_reservation_number_of_attendees-reserv-row"><td>

result.reservation.location.reservation.​number\_of\_attendees

</td><td id="reservation_location_reservation_number_of_attendees-reserv-entry">

Number of attendees of the reservation.Data type: Number

</td></tr><tr id="reservation_location_reservation_requested_for-reserv-row"><td>

result.reservation.location.reservation.​requested\_for

</td><td id="reservation_location_reservation_requested_for-reserv-entry">

Details about the person for whom the reservation was requested on behalf of.Data type: Object

```
"requested_for": {
  "name": "String",
  "sys_id": "String",
  "user_name": "String"
}
```

</td></tr><tr id="reservation_location_reservation_requested_for_name-reserv-row"><td>

result.reservation.location.reservation.​requested\_for.name

</td><td id="reservation_location_reservation_requested_for_name-reserv-entry">

Name of the user for whom the reservation was requested for.Data type: String

</td></tr><tr id="reservation_location_reservation_requested_for_sys_id-reserv-row"><td>

result.reservation.location.reservation.​requested\_for.sys\_id

</td><td id="reservation_location_reservation_requested_for_sys_id-reserv-entry">

Sys\_id of the requested for user.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="reservation_location_reservation_requested_for_user_name-reserv-row"><td>

result.reservation.location.reservation.​requested\_for.user\_name

</td><td id="reservation_location_reservation_requested_for_user_name-reserv-entry">

User name of the user for whom the reservation was requested for.Data type: String

</td></tr><tr id="reservation_location_reservable_module-reserv-row"><td>

result.reservation.location.reservable\_module

</td><td id="reservation_location_reservable_module-reserv-entry">

Details about the reservable module associated with the reservation.Data type: Object

```
"reservable_module": {
  "inline_title": "String",
  "name": "String",
  "sys_id": "String",
  "title": "String"
}
```

</td></tr><tr id="reservation_location_reservable_module_inline_title-reserv-row"><td>

result.reservation.location.reservable\_module.​inline\_title

</td><td id="reservation_location_reservable_module_inline_title-reserv-entry">

Inline title of the reservable module. The title appears in line with the descriptive text on the Workplace service portal.Data type: String

</td></tr><tr id="reservation_location_reservable_module_name-reserv-row"><td>

result.reservation.location.reservable\_module.​name

</td><td id="reservation_location_reservable_module_name-reserv-entry">

Name of the reservable module.Data type: String

</td></tr><tr id="reservation_location_reservable_module_sys_id-reserv-row"><td>

result.reservation.location.reservable\_module.​sys\_id

</td><td id="reservation_location_reservable_module_sys_id-reserv-entry">

Sys\_id of the reservable module.Data type: String

</td></tr><tr id="reservation_location_reservable_module_title-reserv-row"><td>

result.reservation.location.reservable\_module.​title

</td><td id="reservation_location_reservable_module_title-reserv-entry">

Title of the reservable module.Data type: String

</td></tr><tr id="reservation_location_site-reserv-row"><td>

result.reservation.location.site

</td><td id="reservation_location_site-reserv-entry">

Site to which the location belongs.Data type: Object

```
"site": {
  "active": Boolean,
  "display_value": "String",
  "sys_id": "String"
}
```

Table: Site \[sn\_wsd\_core\_site\]

</td></tr><tr id="reservation_location_site_active-reserv-row"><td>

result.reservation.location.site.active

</td><td id="reservation_location_site_active-reserv-entry">

Flag that indicates whether the site is active.Valid values:

-   true: Site is active.
-   false: Site is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_site_display_value-reserv-row"><td>

result.reservation.location.site.display\_value

</td><td id="reservation_location_site_display_value-reserv-entry">

Display value of the site to which this location belongs, such as Western Europe.Data type: String

</td></tr><tr id="reservation_location_site_sys_id-reserv-row"><td>

result.reservation.location.site.sys\_id

</td><td id="reservation_location_site_sys_id-reserv-entry">

Sys\_id of the site to which this location belongs.Data type: String

Table: Site \[sn\_wsd\_core\_site\]

</td></tr><tr id="state-reserv-row"><td>

result.reservation.location.state

</td><td id="state-reserv-entry">

Details about the state of the reservation for the location.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="state_display_value-reserv-row"><td>

result.reservation.location.state.display\_value

</td><td id="state_display_value-reserv-entry">

Display value for the current state of the reservation, such as confirmed.Data type: String

</td></tr><tr id="state_value-reserv-row"><td>

result.reservation.location.state.value

</td><td id="state_value-reserv-entry">

Internal value for the current state of the reservation, such as 2.Data type: String

</td></tr><tr id="location_sys_id-reserv-row"><td>

result.reservation.location.sys\_id

</td><td id="location_sys_id-reserv-entry">

Sys\_id of the associated location record.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr id="reservation_notification_custom_message-reserv-row"><td>

result.reservation.notification\_custom\_​message

</td><td id="reservation_notification_custom_message-reserv-entry">

Custom message for the notification sent to the recipients listed in **reservation.notification\_recipients**.Data type: String

</td></tr><tr id="reservation_notification_recipients-reserv-row"><td>

result.reservation.notification\_recipients

</td><td id="reservation_notification_recipients-reserv-entry">

List of recipients that receive notification about the reservation.Data type: Array of Objects

```
"notification_recipients":[
  {
    "name": "String",
    "sys_id": "String",
    "user_name": "String"
  }
]
```

</td></tr><tr id="reservation_notification_recipients_name-reserv-row"><td>

result.reservation.notification\_recipients.name

</td><td id="reservation_notification_recipients_name-reserv-entry">

Name of the recipient.Data type: String

</td></tr><tr id="reservation_notification_recipients_sys_id-reserv-row"><td>

result.reservation.notification\_recipients.sys\_id

</td><td id="reservation_notification_recipients_sys_id-reserv-entry">

Sys\_id of the recipient.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="reservation_notification_recipients_user_name-reserv-row"><td>

result.reservation.notification\_recipients.​user\_name

</td><td id="reservation_notification_recipients_user_name-reserv-entry">

User name of the recipient.Data type: String

</td></tr><tr id="reservation_number-reserv-row"><td>

result.reservation.number

</td><td id="reservation_number-reserv-entry">

Unique number of the reservation record. You can use this value to query the reservation.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr id="reservation_opened_by-reserv-row"><td>

result.reservation.opened\_by

</td><td id="reservation_opened_by-reserv-entry">

Details about the user that created the reservation.Data type: Object

```
"opened_by": {
  "avatar": "String",
  "displayValue": "String",
  "display_value": "String",
  "email": "String",
  "initials": "String",
  "label": "String",
  "name": "String",
  "sys_id": "String",
  "table": "String",
  "user_name": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_opened_by_avatar-reserv-row"><td>

result.reservation.opened\_by.avatar

</td><td id="reservation_opened_by_avatar-reserv-entry">

Avatar for the user that opened the reservation.Data type: String

</td></tr><tr id="reservation_opened_by_displayValue-reserv-row"><td>

result.reservation.opened\_by.displayValue

</td><td id="reservation_opened_by_displayValue-reserv-entry">

Display value of the opened by user.Data type: String

</td></tr><tr id="reservation_opened_by_display_value-reserv-row"><td>

result.reservation.opened\_by.display\_value

</td><td id="reservation_opened_by_display_value-reserv-entry">

Display value of the opened by user.Data type: String

</td></tr><tr id="reservation_opened_by_email-reserv-row"><td>

result.reservation.opened\_by.email

</td><td id="reservation_opened_by_email-reserv-entry">

Email address for the user that opened the reservation.Data type: String

</td></tr><tr id="reservation_opened_by_initials-reserv-row"><td>

result.reservation.opened\_by.initials

</td><td id="reservation_opened_by_initials-reserv-entry">

Initials of the user that opened the reservation.Data type: String

</td></tr><tr id="reservation_opened_by_label-reserv-row"><td>

result.reservation.opened\_by.label

</td><td id="reservation_opened_by_label-reserv-entry">

Label for the user that opened the reservation. This is a combination of the title and department of the user.Data type: String

</td></tr><tr id="reservation_opened_by_name-reserv-row"><td>

result.reservation.opened\_by.name

</td><td id="reservation_opened_by_name-reserv-entry">

Name of the user that opened the reservation.Data type: String

</td></tr><tr id="reservation_opened_by_sys_id-reserv-row"><td>

result.rservation.opened\_by.sys\_id

</td><td id="reservation_opened_by_sys_id-reserv-entry">

Sys\_id\_of the user that opened the reservation.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="reservation_opened_by_table-reserv-row"><td>

result.rservation.opened\_by.table

</td><td id="reservation_opened_by_table-reserv-entry">

Table that contains the user record.Data type: String

</td></tr><tr id="reservation_opened_by_user_name-reserv-row"><td>

result.reservation.opened\_by.user\_name

</td><td id="reservation_opened_by_user_name-reserv-entry">

User name of the user that opened the reservation.Data type: String

</td></tr><tr id="reservation_opened_by_value-reserv-row"><td>

result.reservation.opened\_by.value

</td><td id="reservation_opened_by_value-reserv-entry">

Internal value of the user that opened the reservation.Data type: String

</td></tr><tr id="reservation_number-reserv1-row"><td>

result.reservation.number

</td><td id="reservation_number-reserv1-entry">

Reservation number.Data type: String

</td></tr><tr id="reservation_number_of_attendees-reserv-row"><td>

result.reservation.number\_of\_attendees

</td><td id="reservation_number_of_attendees-reserv-entry">

Number of attendees in this reservation.Data type: Number

</td></tr><tr id="reservation_recording_details-reserv-row"><td>

result.reservation.recording\_details

</td><td id="reservation_recording_details-reserv-entry">

Details about the recordings associated with the reservation \(meeting\).Data type: Array of Objects

```
"recording_details": [
  "recording_url": "String"
]
```

</td></tr><tr id="reservation_recording_details_recording_url-reserv-row"><td>

result.reservation.recording\_details.​recording\_url

</td><td id="reservation_recording_details_recording_url-reserv-entry">

URL of the recordings associated with the reservation.Data type: String

</td></tr><tr id="reservation_requested_for-reserv-row"><td>

result.reservation.requested\_for

</td><td id="reservation_requested_for-reserv-entry">

Details about the user that the reservation was made on behalf of.Data type: Object

```
"requested_for": {
  "avatar": "String",
  "displayValue": "String",
  "display_value": "String",
  "email": "String",
  "initials": "String",
  "label": "String",
  "name": "String",
  "sys_id": "String",
  "table": "String",
  "user_name": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_requested_for_avatar-reserv-row"><td>

result.reservation.requested\_for.avatar

</td><td id="reservation_requested_for_avatar-reserv-entry">

Avatar for the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_displayValue-reserv-row"><td>

result.reservation.requested\_for.displayValue

</td><td id="reservation_requested_for_displayValue-reserv-entry">

Display value of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_display_value-reserv-row"><td>

result.reservation.requested\_for.display\_value

</td><td id="reservation_requested_for_display_value-reserv-entry">

Display value of the user that the reservation was made on behalf of. Same as displayValue.Data type: String

</td></tr><tr id="reservation_requested_for_email-reserv-row"><td>

result.reservation.requested\_for.email

</td><td id="reservation_requested_for_email-reserv-entry">

Email address for the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_initials-reserv-row"><td>

result.reservation.requested\_for.initials

</td><td id="reservation_requested_for_initials-reserv-entry">

Initials of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_label-reserv-row"><td>

result.reservation.requested\_for.label

</td><td id="reservation_requested_for_label-reserv-entry">

Label for the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_name-reserv-row"><td>

result.reservation.requested\_for.name

</td><td id="reservation_requested_for_name-reserv-entry">

Name of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_sys_id-reserv-row"><td>

result.rservation.requested\_for.sys\_id

</td><td id="reservation_requested_for_sys_id-reserv-entry">

Sys\_id\_of the user that the reservation was made on behalf of.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="reservation_requested_for_table-reserv-row"><td>

result.rservation.requested\_for.table

</td><td id="reservation_requested_for_table-reserv-entry">

Table that contains the user record.Data type: String

</td></tr><tr id="reservation_requested_for_user_name-reserv-row"><td>

result.reservation.requested\_for.user\_name

</td><td id="reservation_requested_for_user_name-reserv-entry">

User name of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_value-reserv-row"><td>

result.reservation.requested\_for.value

</td><td id="reservation_requested_for_value-reserv-entry">

Internal value of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_reservable_module-reserv-row"><td>

result.reservation.reservable\_module

</td><td id="reservation_reservable_module-reserv-entry">

Details for the requested reservable module.Data type: Object

```
"reservable_module": {
  "allow_invitees": Boolean,
  "allow_whole_day": Boolean,
  "apply_to_shift": Boolean,
  "browse_by_area_enabled": Boolean,
  "browse_near_a_person_enabled": Boolean,
  "buildingSysIds": [Array],
  "checkin_before_minutes": Number,
  "display_number_of_attendees": Boolean,
  "display_on_behalf_of": Boolean,
  "display_sensitivity": Boolean,
  "display_value": "String",
  "enable_browse_by_area": Boolean,
  "enable_browse_near_a_person": Boolean,
  "enable_facet_filter": Boolean,
  "enable_group_reservations": Boolean,
  "enable_ical_generation": Boolean,
  "font_awesome_icon": "String",
  "inline_title": "String",      
  "layout_mapping": {Object},
  "max_days_in_future": Number,
  "max_occurrences": Number,
  "name": "String",
  "override_approval_policy": "String",
  "require_cancel_notes": Boolean,
  "require_cc_dept_check": Boolean,
  "require_subject": Boolean,
  "reservable_columns": [Array],
  "reservable_container_field": "String",
  "reservable_filter": "String",
  "reservable_quantity_field": "String",
  "reservable_table": "String",
  "reservable_type": "String",
  "reservable_views": [Array],
  "reservation_paths": [Array],
  "search_limit": Number,
  "selection_type": "String",
  "short_description": "String",
  "show_map_view": Boolean,
  "sys_id": "String",
  "timeSlots": [Array],
  "title": "String",
  "virtual_meeting_provider": {Object}
}
```

</td></tr><tr id="reservation_reservable_module_allow_invitees-reserv-row"><td>

result.reservation.reservable\_module.​allow\_invitees

</td><td id="reservation_reservable_module_allow_invitees-reserv-entry">

Flag that indicates whether employees are able to add invitees to the reservation. Valid values:

-   true: Allow employees to add invitees to the reservation.
-   false: Don't allow employees to add invitees to the reservation.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_allow_whole_day-reserv-row"><td>

result.reservation.reservable\_module.​allow\_whole\_day

</td><td id="reservation_reservable_module_allow_whole_day-reserv-entry">

Flag that indicates whether users can reserve the reservable for the entire day. Valid values:

-   true: Allow users to reserve for the entire day.
-   false: Don't allow users to reserve for the entire day.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_apply_to_shift-reserv-row"><td>

result.reservation.reservable\_module.​apply\_to\_shift

</td><td id="reservation_reservable_module_apply_to_shift-reserv-entry">

Flag that indicates whether shift-based reservations are enabled for the reservable module. Valid values:

-   true: Allow shift-based reservations.
-   false: Don't allow shift-based reservations.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_browse_by_area_enabled-reserv-row"><td>

result.reservation.reservable\_module.​browse\_by\_area\_enabled

</td><td id="reservation_reservable_module_browse_by_area_enabled-reserv-entry">

Flag that indicates whether users are able to search for reservable modules by area.Valid values:

-   true: Allow users to browse reservable modules by area.
-   false: Don't allow users to browse reservable modules by area.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_browse_near_a_person_enabled-reserv-row"><td>

result.reservation.reservable\_module.​browse\_near\_a\_person\_enabled

</td><td id="reservation_reservable_module_browse_near_a_person_enabled-reserv-entry">

Flag that indicates whether users are able to search for reservable modules located by a specified person.Valid values:

-   true: Allow users to browse reservable modules near a person.
-   false: Don't allow users to browse reservable modules near a person.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_buildingSysIds-reserv-row"><td>

result.reservation.reservable\_module.​buildingSysIds

</td><td id="reservation_reservable_module_buildingSysIds-reserv-entry">

List of sys\_ids of the buildings associated with the reservable module.Data type: Array of Strings

</td></tr><tr id="reservation_reservable_module_checkin_before_minutes-reserv-row"><td>

result.reservation.reservable\_module.​checkin\_before\_minutes

</td><td id="reservation_reservable_module_checkin_before_minutes-reserv-entry">

Amount of time before a reservation starts that a user can check into their reservation.Unit: Minutes

Data type: Number

</td></tr><tr id="reservation_reservable_module_display_number_of_attendees-reserv-row"><td>

result.reservation.reservable\_module.​display\_number\_of\_attendees

</td><td id="reservation_reservable_module_display_number_of_attendees-reserv-entry">

Flag that indicates whether users can specify the number of attendees in the reservation. Valid values:

-   true: Users can specify the number of attendees.
-   false: Users can't specify the display number of attendees.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_display_on_behalf_of-reserv-row"><td>

result.reservation.reservable\_module.​display\_on\_behalf\_of

</td><td id="reservation_reservable_module_display_on_behalf_of-reserv-entry">

Flag that indicates whether reservations can be made on behalf of someone else. Valid values:

-   true: On behalf of supported.
-   false: On behalf of not supported.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_display_sensitivity-reserv-row"><td>

result.reservation.reservable\_module.​display\_sensitivity

</td><td id="reservation_reservable_module_display_sensitivity-reserv-entry">

Flag that indicates whether users can set the sensitivity of the reservation, such as normal or private.Valid values:

-   true: Able to set sensitivity.
-   false: Not able to set sensitivity. Defaults to normal.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_display_value-reserv-row"><td>

result.reservation.reservable\_module.​display\_value

</td><td id="reservation_reservable_module_display_value-reserv-entry">

Display value of the reservable module.Data type: String

</td></tr><tr id="reservation_reservable_module_enable_browse_by_area-reserv-row"><td>

result.reservation.reservable\_module.​enable\_browse\_by\_area

</td><td id="reservation_reservable_module_enable_browse_by_area-reserv-entry">

Flag that indicates whether users are able to search for reservable modules by area. Same as **browse\_by\_area\_enabled**.Valid values:

-   true: Allow users to browse reservable modules by area.
-   false: Don't allow users to browse reservable modules by area.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_enable_browse_near_a_person-reserv-row"><td>

result.reservation.reservable\_module.​enable\_browse\_near\_a\_person

</td><td id="reservation_reservable_module_enable_browse_near_a_person-reserv-entry">

Flag that indicates whether users are able to search for reservable modules located by a specified person. Same as**browse\_near\_a\_person\_enabled**.Valid values:

-   true: Allow users to browse reservable modules near a person.
-   false: Don't allow users to browse reservable modules near a person.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_enable_facet_filter-reserv-row"><td>

result.reservation.reservable\_module.​enable\_facet\_filter

</td><td id="reservation_reservable_module_enable_facet_filter-reserv-entry">

Flag that indicates whether facet filtering on workplace items is enabled. When enabled, the filter options that appear are based on the search results. Only the items that are available in the generated search result are available to users for selection in the filter.Valid values:

-   true: Facet filters are enabled.
-   false: Facet filters aren't enabled.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_enable_group_reservations-reserv-row"><td>

result.reservation.reservable\_module.​enable\_group\_reservations

</td><td id="reservation_reservable_module_enable_group_reservations-reserv-entry">

Flag that indicates whether users can make a group reservation.Valid values:

-   true: Able to make group reservations.
-   false: Not able to make group reservations.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_enable_ical_generation-reserv-row"><td>

result.reservation.reservable\_module.​enable\_ical\_generation

</td><td id="reservation_reservable_module_enable_ical_generation-reserv-entry">

Flag that indicates whether users can generate an iCalendar for the reservation.Valid values:

-   true: iCalendar generation allowed.
-   false: iCalendar generation isn't allowed.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_font_awesome_icon-reserv-row"><td>

result.reservation.reservable\_module.​font\_awesome\_icon

</td><td id="reservation_reservable_module_font_awesome_icon-reserv-entry">

Name of the font icon attached to the reservable module.Data type: String

</td></tr><tr id="reservation_reservable_module_inline_title-reserv-row"><td>

result.reservation.reservable\_module.​inline\_title

</td><td id="reservation_reservable_module_inline_title-reserv-entry">

Inline title of the reservable module. The title appears in line with the descriptive text on the Workplace service portal.Data type: String

</td></tr><tr id="reservation_reservable_module_layout_mapping-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping

</td><td id="reservation_reservable_module_layout_mapping-reserv-entry">

Details about the structure of the layout mapping of locations. Use this data to lay out the information in the UI. Data type: Object

```
"layout_mapping": {
  "body": [Array],
  "description": [Array],
  "image": "String",
  "subtitle": [Array],
  "subtitle_asc": [Array],
  "title": [Array]
}
```

</td></tr><tr id="reservation_reservable_module_layout_mapping_body-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.body

</td><td id="reservation_reservable_module_layout_mapping_body-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: Array of Objects

```
"body": [
  {
    "field": "String",
    "field_to_display": "String",
    "icon": "String",
    "label": "String"
  }
]
```

</td></tr><tr id="reservation_reservable_module_layout_mapping_body_field-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.body.field

</td><td id="reservation_reservable_module_layout_mapping_body_field-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="reservation_reservable_module_layout_mapping_body_field_to_display-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.body.field\_to\_display

</td><td id="reservation_reservable_module_layout_mapping_body_field_to_display-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="reservation_reservable_module_layout_mapping_body_icon-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.body.icon

</td><td id="reservation_reservable_module_layout_mapping_body_icon-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="reservation_reservable_module_layout_mapping_body_label-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.body.label

</td><td id="reservation_reservable_module_layout_mapping_body_label-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="reservation_reservable_module_layout_mapping_description-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.description

</td><td id="reservation_reservable_module_layout_mapping_description-reserv-entry">

Placeholder for mapping the front-end UI data. Description of the layout mapping.Data type: Array

</td></tr><tr id="reservation_reservable_module_layout_mapping_image-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.image

</td><td id="reservation_reservable_module_layout_mapping_image-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="reservation_reservable_module_layout_mapping_subtitle-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.subtitle

</td><td id="reservation_reservable_module_layout_mapping_subtitle-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: Array

</td></tr><tr id="reservation_reservable_module_layout_mapping_subtitle_asc-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.subtitle\_asc

</td><td id="reservation_reservable_module_layout_mapping_subtitle_asc-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: Array

</td></tr><tr id="reservation_reservable_module_layout_mapping_title-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.title

</td><td id="reservation_reservable_module_layout_mapping_title-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: Array

</td></tr><tr id="reservation_reservable_module_max_days_in_future-reserv-row"><td>

result.reservation.reservable\_module.​max\_days\_in\_future

</td><td id="reservation_reservable_module_max_days_in_future-reserv-entry">

Maximum number of the days in the future that a user can reserve the reservable module.Data type: Number

</td></tr><tr id="reservation_reservable_module_max_occurrences-reserv-row"><td>

result.reservation.reservable\_module.​max\_occurrences

</td><td id="reservation_reservable_module_max_occurrences-reserv-entry">

Maximum number of recurring reservation occurrences if recurring reservations are available for the reservable module.Data type: Number

</td></tr><tr id="reservation_reservable_module_name-reserv-row"><td>

result.reservation.reservable\_module.name

</td><td id="reservation_reservable_module_name-reserv-entry">

Name of the reservable module.Data type: String

</td></tr><tr id="reservation_reservable_module_override_approval_policy-reserv-row"><td>

result.reservation.reservable\_module.​override\_approval\_policy

</td><td id="reservation_reservable_module_override_approval_policy-reserv-entry">

Option to specify how to implement the approval policy. Choices:

-   No override: The approval policy is implemented as set in the **Requires approval** field of a workplace space or room.
-   Always require approval: The approval policy is required regardless of what is set in the **Requires approval** field of a workplace space or room.
-   Never require approval: The approval policy is removed regardless of what is set in the **Requires approval**l field of a workplace space or room.

Data type: String

</td></tr><tr id="reservation_reservable_module_require_cancel_notes-reserv-row"><td>

result.reservation.reservable\_module.​require\_cancel\_notes

</td><td id="reservation_reservable_module_require_cancel_notes-reserv-entry">

Flag that indicates whether users must enter a cancellation note before cancelling a reservable module.Valid values:

-   true: Cancellation note required.
-   false: Cancellation note not required.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_require_cc_dept_check-reserv-row"><td>

result.reservation.reservable\_module.​require\_cc\_dept\_check

</td><td id="reservation_reservable_module_require_cc_dept_check-reserv-entry">

Flag that indicates whether to check if there's a cost center or department mismatch between the workspace item and the logged in user. Valid values:

-   true: Check for a mismatch.
-   false: Don't check for a mismatch.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_require_subject-reserv-row"><td>

result.reservation.reservable\_module.​require\_subject

</td><td id="reservation_reservable_module_require_subject-reserv-entry">

Flag that indicates whether the user must enter a subject when making the reservation.Valid values:

-   true: Subject required.
-   false: Subject isn't required.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_reservable_columns-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_columns

</td><td id="reservation_reservable_module_reservable_columns-reserv-entry">

List of the columns of a reservable.Data type: Array

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr id="reservation_reservable_module_reservable_container_field-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_container\_field

</td><td id="reservation_reservable_module_reservable_container_field-reserv-entry">

Level of the container, such as a group of desks in a specific area.Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_filter-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_filter

</td><td id="reservation_reservable_module_reservable_filter-reserv-entry">

Filter conditions used to filter out reservable items in the associated Reservable table. Reservable table is a field in the Reservable Module \[sn\_wsd\_rsv\_reservable\_module\] table. These filter conditions were applied to the table contained in the field Reservable table.Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_quantity_field-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_quantity\_field

</td><td id="reservation_reservable_module_reservable_quantity_field-reserv-entry">

Reservable quantity of all the spaces. The quantity is used when assigning neighbourhood spaces to an area. For additional information, see [Assign neighborhood spaces to an area](https://www.servicenow.com/docs/access?context=add-neighbourhood-spaces-to-an-area&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_table-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_table

</td><td id="reservation_reservable_module_reservable_table-reserv-entry">

Table that contains the reservable workplace items.Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_type-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_type

</td><td id="reservation_reservable_module_reservable_type-reserv-entry">

Type of the reservable item, such as location.Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_views-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_views

</td><td id="reservation_reservable_module_reservable_views-reserv-entry">

Details about the different views associated with the reservable module, such as card view or schedule view.Data type: Object

```
"reservable_views": {
  "iconClass": "String",
  "isDefault": Boolean,
  "label": "String",
  "order": Number,
  "type": "String"
}
```

Table: Reservable View \[sn\_wsd\_rsv\_reservable\_view\]

</td></tr><tr id="reservation_reservable_module_reservable_views_iconClass-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_views.iconClass

</td><td id="reservation_reservable_module_reservable_views_iconClass-reserv-entry">

Icon class of the reservable view.Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_views_isDefault-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_views.isDefault

</td><td id="reservation_reservable_module_reservable_views_isDefault-reserv-entry">

Flag that indicates whether to make this reservable view the default for reservable modules. Valid values:

-   true: Make default.
-   false: Don't make default.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_reservable_views_label-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_views.label

</td><td id="reservation_reservable_module_reservable_views_label-reserv-entry">

Name of the reservable view.Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_views_order-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_views.order

</td><td id="reservation_reservable_module_reservable_views_order-reserv-entry">

Order in which the views are displayed for the reservable module in the UI. The lower order number come first in the UI. In case of the same order number, it is assigned random ordering.Data type: Number

</td></tr><tr id="reservation_reservable_module_reservable_views_type-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_views.type

</td><td id="reservation_reservable_module_reservable_views_type-reserv-entry">

Backend name of the reservable view. Used for internal processing.Data type: String

</td></tr><tr id="reservation_reservable_module_reservation_paths-reserv-row"><td>

result.reservation.reservable\_module.​reservation\_paths

</td><td id="reservation_reservable_module_reservation_paths-reserv-entry">

Reservation paths associated with the reservable modules such as Browse all, Browse near a person.Data type: Array of Objects

```
"reservation_paths": [
  {
    "displayValue": "String",
    "value": "String"
  }
]
```

</td></tr><tr id="reservation_reservable_module_reservation_paths_display_value-reserv-row"><td>

result.reservation.reservable\_module.​reservation\_paths.display\_value

</td><td id="reservation_reservable_module_reservation_paths_display_value-reserv-entry">

Display value for the reservation path, such as "Browse near a person".Data type: String

</td></tr><tr id="reservation_reservable_module_reservation_paths_value-reserv-row"><td>

result.reservation.reservable\_module.​reservation\_paths.value

</td><td id="reservation_reservable_module_reservation_paths_value-reserv-entry">

Internal value for the reservation path, such as "browse\_near\_a\_person".Data type: String

</td></tr><tr id="reservation_reservable_module_search_limit-reserv-row"><td>

result.reservation.reservable\_module.​search\_limit

</td><td id="reservation_reservable_module_search_limit-reserv-entry">

Maximum number of search results to return when a user searches for a workplace location.Data type: Number

</td></tr><tr id="reservation_reservable_module_selection_type-reserv-row"><td>

result.reservation.reservable\_module.​selection\_type

</td><td id="reservation_reservable_module_selection_type-reserv-entry">

Type of selection to display in the search results.

 Can be one of the following options:

-   Specific unit: The search result displays every workplace item.
-   Container: The search result displays the parent or container of the workplace items.

 Data type: String

</td></tr><tr id="reservation_reservable_module_short_description-reserv-row"><td>

result.reservation.reservable\_module.​short\_description

</td><td id="reservation_reservable_module_short_description-reserv-entry">

Brief description of the reservable module.Data type: String

</td></tr><tr id="reservation_reservable_module_show_map_view-reserv-row"><td>

result.reservation.reservable\_module.​show\_map\_view

</td><td id="reservation_reservable_module_show_map_view-reserv-entry">

Flag that indicates whether to enable the map view for reservable modules. Valid values:

-   true: Enable map view.
-   false: Don't enable map view.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_sys_id-reserv-row"><td>

result.reservation.reservable\_module.sys\_id

</td><td id="reservation_reservable_module_sys_id-reserv-entry">

Sys\_id of the reservable module.Data type: String

</td></tr><tr id="reservation_reservable_module_timeSlots-reserv-row"><td>

result.reservation.reservable\_module.timeSlots

</td><td id="reservation_reservable_module_timeSlots-reserv-entry">

Details about the time slots associated for a reservable module.Data type: Array of Objects

```
[
  {
    "name": "String",
    "short_description": "String",
    "slot_end": "String",
    "slot_start": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr id="reservation_reservable_module_timeSlots_name-reserv-row"><td>

result.reservation.reservable\_module.​timeSlots.name

</td><td id="reservation_reservable_module_timeSlots_name-reserv-entry">

Name of the time slot.Data type: String

</td></tr><tr id="reservation_reservable_module_timeSlots_short_description-reserv-row"><td>

result.reservation.reservable\_module.​timeSlots.short\_description

</td><td id="reservation_reservable_module_timeSlots_short_description-reserv-entry">

Brief description of the time slot.Data type: String

</td></tr><tr id="reservation_reservable_module_timeSlots_slot_end-reserv-row"><td>

result.reservation.reservable\_module.​timeSlots.slot\_end

</td><td id="reservation_reservable_module_timeSlots_slot_end-reserv-entry">

End time of the time slot.Data type: String

</td></tr><tr id="reservation_reservable_module_timeSlots_slot_start-reserv-row"><td>

result.reservation.reservable\_module.​timeSlots.slot\_start

</td><td id="reservation_reservable_module_timeSlots_slot_start-reserv-entry">

Start time of the slot.Data type: String

</td></tr><tr id="reservation_reservable_module_timeSlots_sys_id-reserv-row"><td>

result.reservation.reservable\_module.​timeSlots.sys\_id

</td><td id="reservation_reservable_module_timeSlots_sys_id-reserv-entry">

Sys\_id of the time slot record.Data type: String

Table: Time Slot \[sn\_wsd\_rsv\_time\_slot\]

</td></tr><tr id="reservation_reservable_module_title-reserv-row"><td>

result.reservation.reservable\_module.title

</td><td id="reservation_reservable_module_title-reserv-entry">

Title of the reservable module.Data type: String

</td></tr><tr id="reservation_reservable_module_virtual_meeting_provider-reserv-row"><td>

result.reservation.reservable\_module.​virtual\_meeting\_provider

</td><td id="reservation_reservable_module_virtual_meeting_provider-reserv-entry">

Details about the virtual provider associated with the reservable module.Data type: Object

```
"virtual_meeting_provider": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_reservable_module_virtual_meeting_provider_display_value-reserv-row"><td>

result.reservation.reservable\_module.​virtual\_meeting\_provider.display\_value

</td><td id="reservation_reservable_module_virtual_meeting_provider_display_value-reserv-entry">

Display value of the virtual meeting provider.Data type: String

</td></tr><tr id="reservation_reservable_module_virtual_meeting_provider_value-reserv-row"><td>

result.reservation.reservable\_module.​virtual\_meeting\_provider.sys\_id

</td><td id="reservation_reservable_module_virtual_meeting_provider_value-reserv-entry">

Sys\_id of the virtual meeting provider.Data type: String

</td></tr><tr id="reservation_reservationAcl-reserv-row"><td>

result.reservation.reservationAcl

</td><td id="reservation_reservationAcl-reserv-entry">

Details of the user access control levels \(ACL\) checks set on the associated reservation.Data type: Object

```
"reservationAcl": {
  "read": Boolean,
  "write": {Object}
}
```

</td></tr><tr id="reservation_reservationAcl-reserv_read-row"><td>

result.reservation.reservationAcl.read

</td><td id="reservation_reservationAcl-reserv_read-entry">

Flag that indicates whether to check if the user can read this reservation.Valid values:

-   true: Check if user can read the reservation.
-   false: Don't check if user can read the reservation.

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write-row"><td>

result.reservation.reservationAcl.write

</td><td id="reservation_reservationAcl-reserv_write-entry">

Details about the user's write capabilities for the associated reservation.Data type: Object

```
"write": {
  "allFields": Boolean,
  "fields": {Object},
  "record": Boolean
}
```

</td></tr><tr id="reservation_reservationAcl-reserv_write_allFields-row"><td>

result.reservation.reservationAcl.write.allFields

</td><td id="reservation_reservationAcl-reserv_write_allFields-entry">

Flag that indicates whether to check if the user can write to all fields specified in the **reservationACL.write.fields** object. If the user only has access to some specific fields, then only those fields are true in the **reservationACL.write.fields** object.Valid values:

-   true: Check if user can write to all fields specified in the **reservationACL.write.fields** object.
-   false: Don't check if user can write to all fields specified in the **reservationACL.write.fields** object

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write_fields-row"><td>

result.reservation.reservationAcl.write.fields

</td><td id="reservation_reservationAcl-reserv_write_fields-entry">

Details of the access controls on various fields of the reservation.Data type: Object

```
"fields": {
  "location": Boolean,
  "number_of_attendees": Boolean,
  "requested_for": Boolean,
  "sensitivity": Boolean,
  "subject": Boolean
}
```

</td></tr><tr id="reservation_reservationAcl-reserv_write_fields_location-row"><td>

result.reservation.reservationAcl.write.fields.​location

</td><td id="reservation_reservationAcl-reserv_write_fields_location-entry">

Flag that indicates whether to check if the user can write to the location fields in this reservation.Valid values:

-   true: Check if user can write to the location fields.
-   false: Don't check if user can write to the location fields.

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write_fields_number_of_attendees-row"><td>

result.reservation.reservationAcl.write.fields.​number\_of\_attendees

</td><td id="reservation_reservationAcl-reserv_write_fields_number_of_attendees-entry">

Flag that indicates whether to check if the user can write to the number of attendees fields in this reservation.Valid values:

-   true: Check if user can write to the number of attendees field.
-   false: Don't check if user can write to the number of attendees field.

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write_fields_requested_for-row"><td>

result.reservation.reservationAcl.write.fields.​requested\_for

</td><td id="reservation_reservationAcl-reserv_write_fields_requested_for-entry">

Flag that indicates whether to check if the user can write to the requested for fields in this reservation.Valid values:

-   true: Check if user can write to the requested for field.
-   false: Don't check if user can write to the requested for field.

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write_fields_sensitivity-row"><td>

result.reservation.reservationAcl.write.fields.​sensitivity

</td><td id="reservation_reservationAcl-reserv_write_fields_sensitivity-entry">

Flag that indicates whether to check if the user can write to the sensitivity fields in this reservation.Valid values:

-   true: Check if user can write to the sensitivity field.
-   false: Don't check if user can write to the sensitivity field.

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write_fields_subject-row"><td>

result.reservation.reservationAcl.write.fields.​subject

</td><td id="reservation_reservationAcl-reserv_write_fields_subject-entry">

Flag that indicates whether to check if the user can write to the subject fields in this reservation.Valid values:

-   true: Check if user can write to the subject field.
-   false: Don't check if user can write to the subject fields.

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write_record-row"><td>

result.reservation.reservationAcl.write.record

</td><td id="reservation_reservationAcl-reserv_write_record-entry">

Flag that indicates whether to check if the user can write to the entire reservation record.Valid values:

-   true: Check if user can write to the entire reservation record.
-   false: Don't check if user can write to the entire reservation record.

Data type: Boolean

</td></tr><tr id="reservation_purpose-reserv-row"><td>

result.reservation.reservation\_purpose

</td><td id="reservation_purpose-reserv-entry">

Details about the purpose of the reservation.Data type: Object

```
"reservation_purpose": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_purpose_display_value-reserv-row"><td>

result.reservation.reservation\_purpose.​display\_value

</td><td id="reservation_purpose_display_value-reserv-entry">

Display value for the purpose of the reservation, such as Company meeting.Data type: String

</td></tr><tr id="reservation_purpose_value-reserv-row"><td>

result.reservation.reservation\_purpose.value

</td><td id="reservation_purpose_value-reserv-entry">

Internal value for the purpose of the reservation, such as company\_meeting.Data type: String

</td></tr><tr id="reservation_reservation_type-row"><td>

result.reservation.reservation\_type

</td><td id="reservation_reservation_type-entry">

Details about the type of the reservation.Data type: Object

```
"reservation_type": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_reservation_type_display_value-row"><td>

result.reservation.reservation\_type.​display\_value

</td><td id="reservation_reservation_type_display_value-entry">

Display value for the type of the reservation, such as Space.Data type: String

</td></tr><tr id="reservation_reservation_type_value-row"><td>

result.reservation.reservation\_type.value

</td><td id="reservation_reservation_type_value-entry">

Internal value for the type of the reservation, such as space.Data type: String

</td></tr><tr id="reservation_reservation_subtype-row"><td>

result.reservation.reservation\_subtype

</td><td id="reservation_reservation_subtype-entry">

Details about the subtype of the reservation. Subtypes indicate the type of reservation, such as single, Multi parent, Multi child, Recurring parent, or occurrence.Data type: Object

```
"reservation_subtype": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_reservation_subtype_display_value-row"><td>

result.reservation.reservation\_subtype.​display\_value

</td><td id="reservation_reservation_subtype_display_value-entry">

Display value for the subtype of the reservation, such as Single.Data type: String

</td></tr><tr id="reservation_reservation_subtype_value-row"><td>

result.reservation.reservation\_subtype.value

</td><td id="reservation_reservation_subtype_value-entry">

Internal value for the subtype of the reservation, such as single.Data type: String

</td></tr><tr id="reservation_sensitivity-row"><td>

result.reservation.sensitivity

</td><td id="reservation_sensitivity-entry">

Details about the sensitivity of the reservation.Data type: Object

```
"sensitivity": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_sensitivity_display_value-row"><td>

result.reservation.sensitivity.display\_value

</td><td id="reservation_sensitivity_display_value-entry">

Display value for the sensitivity of the reservation, such as high or low.Data type: String

</td></tr><tr id="reservation_sensitivity_value-row"><td>

result.reservation.sensitivity.value

</td><td id="reservation_sensitivity_value-entry">

Internal value for the sensitivity of the reservation, such as 1 or 3.Data type: String

</td></tr><tr id="reservation_shift-row"><td>

result.reservation.shift

</td><td id="reservation_shift-entry">

Details about the shift applied to the reservation.Data type: Object

```
"shift": {
  "display_value": "String",
  "name": "String",
  "shiftDetails": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_shift_display_value-row"><td>

result.reservation.shift.display\_value

</td><td id="reservation_shift_display_value-entry">

Display value of the shift.Data type: String

</td></tr><tr id="reservation_shift_name-row"><td>

result.reservation.shift.name

</td><td id="reservation_shift_name-entry">

Name of the shift. Same as **display\_value**.Data type: String

</td></tr><tr id="reservation_shift_shiftDetails-row"><td>

Result.reservation.shift.shiftDetails

</td><td id="reservation_shift_shiftDetails-entry">

Details of shift.Data type: String

</td></tr><tr id="reservation_shift_sys_id-row"><td>

result.reservation.shift.sys\_id

</td><td id="reservation_shift_sys_id-entry">

Sys\_id of the shift record.Data type: String

Table: Shift \[sn\_wsd\_core\_shift\]

</td></tr><tr id="reservation_source-row"><td>

result.reservation.source

</td><td id="reservation_source-entry">

Details about the source for the reservation, such as Workplace Services or Google Mail..Data type: Object

```
"source": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_source_display_value-row"><td>

result.reservation.source.display\_value

</td><td id="reservation_source_display_value-entry">

Display value for the reservation source, such as Workplace Services.Data type: String

</td></tr><tr id="reservation_source_value-row"><td>

result.reservation.source.value

</td><td id="reservation_source_value-entry">

Internal value for the reservation source, such as servicenow.Data type: String

</td></tr><tr id="reservation_source_icon-row"><td>

result.reservation.source\_icon

</td><td id="reservation_source_icon-entry">

Details about the source of the icon used in the reservation. This icon is used in the UI.Data type: Object

```
"source_icon": {
  "classNames": "String",
  "imgSrc": "String",
  "tooltip": "String"
}
```

</td></tr><tr id="reservation_source_icon_classNames-row"><td>

result.reservation.source\_icon.classNames

</td><td id="reservation_source_icon_classNames-entry">

Comma-separated class names for the source icon.Data type: String

</td></tr><tr id="reservation_source_icon_imgSrc-row"><td>

result.reservation.source\_icon.imgSrc

</td><td id="reservation_source_icon_imgSrc-entry">

Name of the image source for source icon. This icon is stored in the Images \[db\_image\] table.Data type: String

</td></tr><tr id="reservation_source_icon_tooltip-row"><td>

result.reservation.source\_icon.tooltip

</td><td id="reservation_source_icon_tooltip-entry">

Tooltip associated with the source icon.Data type: String

</td></tr><tr id="reservation_source_reservation-row"><td>

result.reservation.source\_reservation

</td><td id="reservation_source_reservation-entry">

Source reservation of the current reservation.For example, in the case of multiple reservations, the parent reservation is the source of the child reservation.

Data type: String

</td></tr><tr id="start-reserv-row"><td>

result.reservation.start

</td><td id="start-reserv-entry">

Reservation start date and time.Data type: String

Format: UTC - yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr id="subject-reserv-row"><td>

result.reservation.subject

</td><td id="subject-reserv-entry">

Reservation's subject.Data type: String

</td></tr><tr id="reservation_sub_source-row"><td>

result.reservation.sub\_source

</td><td id="reservation_sub_source-entry">

Details about the sub-source of the reservation. The sub-source specifies where the reservation originated such as Google Calendar or Microsoft Exchange.Data type: Object

```
"sub_source": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_sub_source_display_value-row"><td>

result.reservation.sub\_source.display\_value

</td><td id="reservation_sub_source_display_value-entry">

Display value for the sub-source of the reservation, such as Google Calendar.Data type: String

</td></tr><tr id="reservation_sub_source_value-row"><td>

result.reservation.sub\_source.value

</td><td id="reservation_sub_source_value-entry">

Internal value of the sub-source field of the reservation, such as google\_calendar.Data type: String

</td></tr><tr id="reservation_sync_state-row"><td>

result.reservation.sync\_state

</td><td id="reservation_sync_state-entry">

Details about the synchronization state of a reservation from another service, such as "sync\_enqueued" or "synchronized".Data type: Object

```
"sync_state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_sync_state_display_value-row"><td>

result.reservation.sync\_state.display\_value

</td><td id="reservation_sync_state_display_value-entry">

Display value for the current sync state of the reservation, such as synchronized.Data type: String

</td></tr><tr id="reservation_sync_state_value-row"><td>

result.reservation.sync\_state.value

</td><td id="reservation_sync_state_value-entry">

Internal value of the current sync state of the reservation, such as synchronized.Data type: String

</td></tr><tr id="reservation_sys_created_on-row"><td>

result.reservation.sys\_created\_on

</td><td id="reservation_sys_created_on-entry">

Date and time when the reservation was created.Data type: String

</td></tr><tr id="reservation_sys_id-row"><td>

result.reservation.sys\_id

</td><td id="sys_id-reserv-entry">

Required. Sys\_id of the reservation record.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr id="reservation_sys_updated_on-row"><td>

Result.reservation.sys\_updated\_on

</td><td id="reservation_sys_updated_on-entry">

Date and time when the reservation was last updated. Data type: String

</td></tr><tr id="reservation_virtual_meeting-row"><td>

result.reservation.virtual\_meeting

</td><td id="reservation_virtual_meeting-entry">

URL of the virtual meeting link.Data type: String

</td></tr><tr><td>

result.reservationAcl

</td><td id="reservationAcl-reserv-entry">

Details of the user access control levels \(ACL\) checks set on the associated reservation.Data type: Object

```
"reservationAcl": {
  "read": Boolean,
  "write": {Object}
}
```

</td></tr><tr><td>

result.reservationAcl.read

</td><td id="reservationAcl_read-reserv-entry">

Flag that indicates whether to check if the user can read this reservation.Valid values:

-   true: Check if user can read the reservation.
-   false: Don't check if user can read the reservation.

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.write

</td><td id="reservationAcl_write-reserv-entry">

Details about the user's write capabilities for the associated reservation.Data type: Object

```
"write": {
  "allFields": Boolean,
  "fields": {Object},
  "record": Boolean
}
```

</td></tr><tr><td>

result.reservationAcl.write.allFields

</td><td id="reservationAcl_write_allFields-reserv-entry">

Flag that indicates whether to check if the user can write to all fields specified in the **reservationACL.write.fields** object. If the user only has access to some specific fields, then only those fields are true in the **reservationACL.write.fields** object.Valid values:

-   true: Check if user can write to all fields specified in the **reservationACL.write.fields** object.
-   false: Don't check if user can write to all fields specified in the **reservationACL.write.fields** object

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.write.fields

</td><td id="reservationAcl_write_fields-reserv-entry">

Details of the access controls on various fields of the reservation.Data type: Object

```
"fields": {
  "location": Boolean,
  "number_of_attendees": Boolean,
  "requested_for": Boolean,
  "sensitivity": Boolean,
  "subject": Boolean
}
```

</td></tr><tr><td>

result.reservationAcl.write.fields.location

</td><td id="reservationAcl_write_fields_location-reserv-entry">

Flag that indicates whether to check if the user can write to the location fields in this reservation.Valid values:

-   true: Check if user can write to the location fields.
-   false: Don't check if user can write to the location fields.

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.write.fields.​number\_of\_attendees

</td><td id="reservationAcl_write_fields_number_of_attendees-reserv-entry">

Flag that indicates whether to check if the user can write to the number of attendees fields in this reservation.Valid values:

-   true: Check if user can write to the number of attendees field.
-   false: Don't check if user can write to the number of attendees field.

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.write.fields.requested\_for

</td><td id="reservationAcl_write_fields_requested_for-reserv-entry">

Flag that indicates whether to check if the user can write to the requested for fields in this reservation.Valid values:

-   true: Check if user can write to the requested for field.
-   false: Don't check if user can write to the requested for field.

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.write.fields.sensitivity

</td><td id="reservationAcl_write_fields_sensitivity-reserv-entry">

Flag that indicates whether to check if the user can write to the sensitivity fields in this reservation.Valid values:

-   true: Check if user can write to the sensitivity field.
-   false: Don't check if user can write to the sensitivity field.

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.write.fields.subject

</td><td id="reservationAcl_write_fields_subject-reserv-entry">

Flag that indicates whether to check if the user can write to the subject fields in this reservation.Valid values:

-   true: Check if user can write to the subject field.
-   false: Don't check if user can write to the subject fields.

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.record

</td><td id="reservationAcl_write_fields_record-reserv-entry">

Flag that indicates whether to check if the user can write to the entire reservation record.Valid values:

-   true: Check if user can write to the entire reservation record.
-   false: Don't check if user can write to the entire reservation record.

Data type: Boolean

</td></tr><tr><td>

result.standard\_services

</td><td id="std_serv-reserv-entry">

Only populated if the **include\_standard\_services** parameter is set to true. Associated standard services, such as flip chart, projector screen, and whiteboard and markers.

Data type: Array of Objects

```
"standard_services": [
  {
    "font_awesome_icon": "String",
    "name": "String",
    "short_description": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.standard\_services.font\_awesome\_icon

</td><td id="std_serv_font-awesome_icon-reserv-entry">

Name of the thumbnail icon associated with the standard service.Data type: String

</td></tr><tr><td>

result.standard\_services.name

</td><td id="std_serv_name-reserv-entry">

Name of the standard service.Data type: String

</td></tr><tr><td>

result.standard\_services.short\_description

</td><td id="std_serv_short_description-reserv-entry">

Brief description of the standard service.Data type: String

</td></tr><tr><td>

result.standard\_services.sys\_id

</td><td id="std_serv_sys_id-reserv-entry">

Sys\_id of the standard service record.Data type: String

Table: Standard Service \[sn\_wsd\_rsv\_standard\_service\]

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint and include the standard services information.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/reservation/get?sys_id=8e87c722870741106342b846dabb3573&include_standard_services=true" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```

  "result": {
    "reservation": {
      "sys_id": "bf3621de842c2110fa9b813be354f327",
      "number": "WRES0001005",
      "location": {
        "sys_id": "9841e94adb7210106c731dcd13961914",
        "name": "A1-02-02",
        "description": "General desk available for reservation.",
        "display_value": "A1-02-02",
        "capacity": 1,
        "label_value": "Workspace/Desk name",
        "wsd_email": null,
        "reservable_module": {
          "sys_id": "5db44502dbb650106c731dcd13961937",
          "name": "Desks",
          "title": "Desks",
          "inline_title": "desk",
          "table": "sn_wsd_core_space"
        },
        "region": {
          "sys_id": "3752ac8edb3650106c731dcd139619e0",
          "display_value": "Americas",
          "active": true
        },
        "site": {
          "sys_id": "628eec06db7650106c731dcd139619dd",
          "display_value": "North America",
          "active": true
        },
        "campus": {
          "sys_id": "82b2a0cedb3650106c731dcd139619e9",
          "display_value": "California Campus",
          "active": true
        },
        "building": {
          "sys_id": "94e264cedb3650106c731dcd13961919",
          "display_value": "CAL-B1",
          "active": true,
          "timezone": {
            "value": "US/Pacific",
            "displayValue": "US/Pacific"
          }
        },
        "floor": {
          "sys_id": "fc7368cedb3650106c731dcd13961902",
          "display_value": "Floor 1",
          "active": true
        },
        "area": {
          "sys_id": "",
          "display_value": "",
          "active": false
        },
        "is_favorite": false,
        "reservation": {
          "sys_id": "bf3621de842c2110fa9b813be354f327",
          "number_of_attendees": 1,
          "state": {
            "value": "confirmed",
            "display_value": "Confirmed"
          },
          "auto_conflict_resolution_state": {
            "value": null,
            "display_value": null
          },
          "requested_for": {
            "sys_id": "6816f79cc0a8016401c5a33be04be441",
            "name": "System Administrator",
            "user_name": "admin"
          },
          "number": "WRES0001005",
          "active": true
        },
        "number_of_attendees": 1,
        "state": {
          "value": "confirmed",
          "display_value": "Confirmed"
        },
        "number": "WRES0001005",
        "requested_for": {
          "sys_id": "6816f79cc0a8016401c5a33be04be441",
          "name": "System Administrator",
          "user_name": "admin"
        },
        "is_private": true
      },
      "start": "2023-01-24T16:00:00Z",
      "end": "2023-01-24T17:00:00Z",
      "sys_created_on": "2023-01-24T15:49:49Z",
      "sys_updated_on": "2023-01-24T15:49:50Z",
      "source_reservation": null,
      "check_in_state": {
        "value": "awaiting_check_in",
        "display_value": "Awaiting check-in"
      },
      "external_id": null,
      "external_ical": null,
      "building": {
        "active": true,
        "sys_id": "94e264cedb3650106c731dcd13961919",
        "display_value": "CAL-B1",
        "campus": {
          "display_value": "California Campus",
          "value": "82b2a0cedb3650106c731dcd139619e9",
          "active": true
        },
        "site": {
          "display_value": "North America",
          "value": "628eec06db7650106c731dcd139619dd",
          "active": true
        },
        "timezone": {
          "value": "US/Pacific",
          "displayValue": "US/Pacific"
        }
      },
      "active": true,
      "state": {
        "value": "confirmed",
        "display_value": "Confirmed"
      },
      "sensitivity": {
        "value": "normal",
        "display_value": "Normal"
      },
      "reservation_type": {
        "value": "space",
        "display_value": "Space"
      },
      "reservation_subtype": {
        "value": "single",
        "display_value": "Single"
      },
      "reservation_purpose": {
        "value": "meeting",
        "display_value": "Meeting"
      },
      "attendees": [
        {
          "sys_id": "6816f79cc0a8016401c5a33be04be441",
          "value": "6816f79cc0a8016401c5a33be04be441",
          "displayValue": "System Administrator",
          "display_value": "System Administrator",
          "name": "System Administrator",
          "user_name": "admin",
          "table": "sys_user",
          "avatar": "a5d3c898c3222010ae17dd981840dd8b.iix?t=small",
          "initials": "SA",
          "email": "admin@example.com",
          "label": "System Administrator, Finance"
        }
      ],
      "number_of_attendees": 1,
      "is_parent": false,
      "is_private": true,
      "subject": "Reservation for A1-02-02",
      "virtual_meeting": null,
      "recording_details": [],
      "sync_state": {
        "value": "not_required",
        "display_value": "Synchronization not required"
      },
      "sub_source": {
        "value": "servicenow_workplace_service_delivery",
        "display_value": "ServiceNow Workplace Service Delivery"
      },
      "last_updated_sub_source": {
        "value": "servicenow_workplace_service_delivery",
        "display_value": "ServiceNow Workplace Service Delivery"
      },
      "reservable_module": {
        "sys_id": "5db44502dbb650106c731dcd13961937",
        "name": "Desks",
        "title": "Desks",
        "inline_title": "desk",
        "font_awesome_icon": "fa-desktop",
        "reservable_table": "sn_wsd_core_space",
        "reservable_filter": "active=true^is_reservable=true^location_type=5f017383eb512010b89bfdfc9c5228c8^building.is_reservable=true^floor.is_reservable=true^EQ",
        "short_description": "Reserve a single desks",
        "reservable_type": "location",
        "require_subject": null,
        "require_cancel_notes": false,
        "virtual_meeting_provider": null,
        "enable_reservation_privacy": true,
        "allow_invitees": "1",
        "display_number_of_attendees": null,
        "display_on_behalf_of": "1",
        "display_sensitivity": null,
        "max_days_in_future": "90",
        "allow_recurring": "1",
        "auto_resolve_conflict": null,
        "allow_whole_day": "1",
        "allow_multi_building": "1",
        "require_whole_day": null,
        "selection_type": "unit",
        "reservable_container_field": null,
        "reservable_quantity_field": null,
        "apply_to_shift": null,
        "max_occurrences": "90",
        "enable_facet_filter": false,
        "search_limit": 10000,
        "enable_ical_generation": null,
        "enable_group_reservations": null,
        "enable_browse_near_a_person": "1",
        "enable_browse_by_area": "1",
        "enable_floor_search": null,
        "enable_browse_by_neighborhood": null,
        "require_cc_dept_check": false,
        "display_value": "Desks",
        "browse_near_a_person_enabled": true,
        "browse_by_area_enabled": true,
        "browse_by_neighborhood_enabled": false,
        "reservable_columns": [
          "sys_id",
          "external_id",
          "wsd_email",
          "name",
          "title",
          "description",
          "image",
          "number",
          "site",
          "campus",
          "building",
          "floor",
          "area",
          "capacity",
          "reservable_quantity",
          "location_type",
          "order",
          "requires_check_in",
          "is_reservable"
        ],
        "layout_mapping": {
          "title": [
            "name"
          ],
          "description": [
            "description"
          ],
          "subtitle": [
            "campus",
            "building",
            "floor",
            "area"
          ],
          "subtitle_asc": [
            "area",
            "floor",
            "building",
            "campus"
          ],
          "image": "image",
          "body": [
            {
              "label": "Capacity",
              "icon": "fa-users",
              "field": "capacity",
              "field_to_display": ""
            },
            {
              "label": "Standard services",
              "icon": "fa-check",
              "field": "standard_services",
              "field_to_display": "name"
            },
            {
              "label": "Reservable purposes",
              "icon": "fa-tags",
              "field": "reservable_purposes",
              "field_to_display": "name"
            }
          ]
        },
        "timeSlots": [
          {
            "sys_id": "d5331cf2dbb5f01038e42b24ca961906",
            "name": "All day",
            "short_description": "8am - 6pm",
            "slot_start": "08:00",
            "slot_end": "18:00"
          },
          {
            "sys_id": "de131cf2dbb5f01038e42b24ca961931",
            "name": "Before noon",
            "short_description": "8am - 12pm",
            "slot_start": "08:00",
            "slot_end": "12:00"
          },
          {
            "sys_id": "6e99ab5ddbb930102e8e853e68961929",
            "name": "After noon",
            "short_description": "1pm - 6pm",
            "slot_start": "13:00",
            "slot_end": "18:00"
          }
        ],
        "buildingSysIds": [
          "03c45bf7dba41010d7981dcd1396196d",
          "07c45bf7dba41010d7981dcd1396196b",
          "07c45bf7dba41010d7981dcd13961972",
          "0bc45bf7dba41010d7981dcd13961970",
          "0fc45bf7dba41010d7981dcd1396196e",
          "1aa39b1977220110b3d7be377b5a9953",
          "2130659ae7321010809a268b03f6a91e",
          "22c41bf7dba41010d7981dcd139619fe",
          "2ac45bf7dba41010d7981dcd13961901",
          "2ec41bf7dba41010d7981dcd139619ff",
          "32c45bf7dba41010d7981dcd13961905",
          "32c45bf7dba41010d7981dcd1396190c",
          "32c45bf7dba41010d7981dcd13961943",
          
          "e2c41bf7dba41010d7981dcd139619fb"
        ],
        "reservable_views": [
          {
            "type": "card",
            "label": "Card view",
            "iconClass": "fa-th-large",
            "isDefault": true,
            "order": "1"
          },
          {
            "type": "schedule",
            "label": "Schedule view",
            "iconClass": "fa-calendar-o",
            "isDefault": false,
            "order": "2"
          }
        ],
        "checkin_before_minutes": 30,
        "reservation_paths": [
          {
            "value": "browse_all",
            "displayValue": "Browse all",
            "availableFor": true
          },
          {
            "value": "browse_favorites",
            "displayValue": "Browse favorites",
            "availableFor": false
          },
          {
            "value": "browse_near_a_person",
            "displayValue": "Browse near a person",
            "availableFor": true
          },
          {
            "value": "browse_by_area",
            "displayValue": "Browse by area",
            "availableFor": true
          }
        ],
        "override_approval_policy": "never_required"
      },
      "notification_recipients": null,
      "notification_custom_message": null,
      "opened_by": {
        "sys_id": "6816f79cc0a8016401c5a33be04be441",
        "value": "6816f79cc0a8016401c5a33be04be441",
        "displayValue": "System Administrator",
        "display_value": "System Administrator",
        "name": "System Administrator",
        "user_name": "admin",
        "table": "sys_user",
        "avatar": "a5d3c898c3222010ae17dd981840dd8b.iix?t=small",
        "initials": "SA",
        "email": "admin@example.com",
        "label": "System Administrator, Finance"
      },
      "requested_for": {
        "sys_id": "6816f79cc0a8016401c5a33be04be441",
        "value": "6816f79cc0a8016401c5a33be04be441",
        "displayValue": "System Administrator",
        "display_value": "System Administrator",
        "name": "System Administrator",
        "user_name": "admin",
        "table": "sys_user",
        "avatar": "a5d3c898c3222010ae17dd981840dd8b.iix?t=small",
        "initials": "SA",
        "email": "admin@example.com",
        "label": "System Administrator, Finance"
      },
      "auto_conflict_resolution_state": {
        "value": null,
        "display_value": null
      },
      "parent_reservation": {},
      "edit_restriction": {
        "value": "no_restriction",
        "display_value": "No restriction"
      },
      "source": {
        "value": "servicenow",
        "display_value": "Workplace Services"
      },
      "source_icon": {
        "classNames": "fa fa-calendar-check-o",
        "tooltip": "Reservation is confirmed",
        "imgSrc": ""
      },
      "shift": null,
      "hasPrivateReservation": true,
      "reservationAcl": {
        "write": {
          "record": true,
          "fields": {
            "subject": true,
            "sensitivity": true,
            "requested_for": true,
            "number_of_attendees": true,
            "location": true,
            "is_private": true
          },
          "allFields": true
        },
        "read": true
      }
    },
    "reservationAcl": {
      "write": {
        "record": true,
        "fields": {
          "subject": true,
          "sensitivity": true,
          "requested_for": true,
          "number_of_attendees": true,
          "location": true,
          "is_private": true
        },
        "allFields": true
      },
      "read": true
    }
  }
}
```

## WSD Reservation - GET /api/sn\_wsd\_rsv/reservation/get\_user\_reservations

Retrieves the list of reservation for a specified user for the next seven days.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/reservation/get_user_reservations`

Default URL: `/api/sn_wsd_rsv/reservation/get_user_reservations`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

userId

</td><td>

Sys\_id of the user whose reservations to return.Data type: String

Table: User \[sys\_user\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-reserv-entry">

Data format of the request body. Supported types: **application/json**, **application/xml** or, **text/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Reservation return results.Data type: Object

```
"result":{
  "informEmployeePrivacy": Boolean,
  "reservationsByDate": {Object},
  "searchEndDate": "String",
  "searchStartDate": "String",
  "sortedReservationDates" : [Array],
  "workplaceProfile": {Object}
}
```

</td></tr><tr><td>

result.informEmployeePrivacy

</td><td>

Flag that indicates whether to display a message when reservations are returned that are marked as private.Possible values:

-   true: Display a message to the user that there are private reservations that are not displayed.
-   false: Don't display any message.

Data type: Boolean

</td></tr><tr><td>

result.reservationsByDate

</td><td>

Details about each reservation by date.Data type: Object - each date in its own Array

```
"reservationsByDate": {
  string: [
    {
      "building": {Object},
      "floor": {Object},
      "location": {Object}
    }
  ]
}
```

</td></tr><tr><td>

result.reservationsByDate.building

</td><td>

Building where the reservable is located.Data type: Object

```
"building": {
  "display_value": "String",
  "sys_id": "String",
  "timezone": {Object}
}
```

Table: Building \[sn\_wsd\_core\_building\]

</td></tr><tr><td>

result.reservationsByDate.building.​display\_value

</td><td>

Display value for the building.Data type: String

</td></tr><tr><td>

result.reservationsByDate.building.sys\_id

</td><td>

Sys\_id of the associated building record.Data type: String

</td></tr><tr><td>

result.reservationsByDate.building.timezone

</td><td>

Details of the time zone for the building.Data type: Object

```
"timezone": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservationsByDate.building.timezone.​display\_value

</td><td>

Display value of the time zone in which the associated building resides.Data type: String

</td></tr><tr><td>

result.reservationsByDate.building.timezone.​sys\_id

</td><td>

Sys\_id of the time zone record in which the associated building resides.Data type: String

</td></tr><tr><td>

result.reservationsByDate.building.value

</td><td>

Internal value for the building.Data type: String

</td></tr><tr><td>

result.reservationsByDate.floor

</td><td>

Details about the floor associated with the reservation.Data type: Object

```
"floor": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservationsByDate.floor.displayValue

</td><td>

Display number of the floor on which the reservable resides, such as 12.Data type: String

</td></tr><tr><td>

result.reservationsByDate.floor.value

</td><td>

Internal value of the floor on which the reservation resides.Data type: String

</td></tr><tr><td>

result.reservationsByDate.location

</td><td>

Details on the location of the reservation.Data type: Object

```
"location": {
  "displayValue": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservationsByDate.location.​displayValue

</td><td>

Display value of the location, such as South Parks.Data type: String

</td></tr><tr><td>

result.reservationsByDate.location.type

</td><td>

Type of location, such as workplace/desk, cafe, or gym.Data type: String

</td></tr><tr><td>

result.reservationsByDate.location.value

</td><td>

Internal value for the location, such as south\_parks.Data type: String

</td></tr><tr><td>

result.searchEndDate

</td><td>

End date of the reservation search. Seven days from the start date.Format: yyyy-mm-dd

Data type: String

</td></tr><tr><td>

result.searchStartDate

</td><td>

Start date of the reservation search. Date on which the endpoint was called.Format: yyyy-mm-dd

Data type: String

</td></tr><tr><td>

result.sortedReservationDates

</td><td>

Dates on which the specified user has reservations for the next seven days, sorted in date order.Data type: Array

</td></tr><tr><td>

result.workplaceProfile

</td><td>

Users workplace profile. Describes where the specified user works.Data type: Object

```
"reservationsByDate": {
  "building": {Object},
  "floor": {Object},
  "location": {Object}
}
```

</td></tr><tr><td>

result.workplaceProfile.building

</td><td>

Building where the user works.Data type: Object

```
"building": {
  "display_value": "String",
  "sys_id": "String",
  "timezone": {Object}
}
```

Table: Building \[sn\_wsd\_core\_building\]

</td></tr><tr><td>

result.workplaceProfile.building.display\_value

</td><td>

Display value for the building.Data type: String

</td></tr><tr><td>

result.workplaceProfile.building.sys\_id

</td><td>

Sys\_id of the associated building record.Data type: String

</td></tr><tr><td>

result.workplaceProfile.building.timezone

</td><td>

Details of the time zone for the building.Data type: Object

```
"timezone": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.workplaceProfile.building.timezone.​display\_value

</td><td>

Display value of the time zone in which the associated building resides.Data type: String

</td></tr><tr><td>

result.workplaceProfile.building.timezone.​sys\_id

</td><td>

Sys\_id of the time zone record in which the associated building resides.Data type: String

</td></tr><tr><td>

result.workplaceProfile.building.value

</td><td>

Internal value for the building.Data type: String

</td></tr><tr><td>

result.workplaceProfile.floor

</td><td>

Details about the floor on which the user works.Data type: Object

```
"floor": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.workplaceProfile.floor.displayValue

</td><td>

Display number of the floor on which the user works, such as Floor 8.Data type: String

</td></tr><tr><td>

result.workplaceProfile.floor.value

</td><td>

Internal value of the floor on which the user works.Data type: String

</td></tr><tr><td>

result.workplaceProfile.location

</td><td>

Details on the location of the user.Data type: Object

```
"location": {
  "displayValue": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.workplaceProfile.location.displayValue

</td><td>

Display value of the location, such as San Diego.Data type: String

</td></tr><tr><td>

result.workplaceProfile.location.type

</td><td>

Type of location, such as desk or office.Data type: String

</td></tr><tr><td>

result.workplaceProfile.location.value

</td><td>

Internal value for the location, such as san\_diego.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/reservation/get_user_reservations?userId=2de07e1887cb89106342b846dabb35fe" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "result": {
    "sortedReservationDates": [
      "2023-01-24"
    ],
    "workplaceProfile": {
      "location": {
        "displayValue": "DDC-A2.0016A",
        "value": "96d3139977220110b3d7be377b5a9918",
        "externalId": "0e7bddfb475a011064062782846d43c2",
        "type": "Workspace/Desk"
      },
      "floor": {
        "displayValue": "Floor 2",
        "value": "68d31f5977220110b3d7be377b5a991b"
      },
      "building": {
        "displayValue": "Building A",
        "value": "dea39b1977220110b3d7be377b5a9955",
        "timezone": {
          "value": "Europe/Paris",
          "displayValue": "Europe/Paris"
        }
      }
    },
    "reservationsByDate": {
      "2023-01-24": [
        {
          "location": {
            "displayValue": "A1-02-04",
            "value": "3e41e94adb7210106c731dcd1396198c",
            "externalId": "",
            "type": "Workspace/Desk"
          },
          "floor": {
            "displayValue": "Floor 1",
            "value": "fc7368cedb3650106c731dcd13961902"
          },
          "building": {
            "displayValue": "CAL-B1",
            "value": "94e264cedb3650106c731dcd13961919",
            "timezone": {
              "value": "US/Pacific",
              "displayValue": "US/Pacific"
            }
          }
        },
        {
          "location": {
            "displayValue": "A1-02-02",
            "value": "9841e94adb7210106c731dcd13961914",
            "externalId": "",
            "type": "Workspace/Desk"
          },
          "floor": {
            "displayValue": "Floor 1",
            "value": "fc7368cedb3650106c731dcd13961902"
          },
          "building": {
            "displayValue": "CAL-B1",
            "value": "94e264cedb3650106c731dcd13961919",
            "timezone": {
              "value": "US/Pacific",
              "displayValue": "US/Pacific"
            }
          }
        },
        {
          "location": {
            "displayValue": "A1-02-03",
            "value": "fd41a94adb7210106c731dcd1396195a",
            "externalId": "",
            "type": "Workspace/Desk"
          },
          "floor": {
            "displayValue": "Floor 1",
            "value": "fc7368cedb3650106c731dcd13961902"
          },
          "building": {
            "displayValue": "CAL-B1",
            "value": "94e264cedb3650106c731dcd13961919",
            "timezone": {
              "value": "US/Pacific",
              "displayValue": "US/Pacific"
            }
          }
        }
      ]
    },
    "searchStartDate": "2023-01-24",
    "searchEndDate": "2023-01-31",
    "informEmployeePrivacy": true
  }
}
```

## WSD Reservation - GET /api/sn\_wsd\_rsv/reservation/icalendar/\{sys\_id\}

Generates an iCalendar file body for a specified reservation.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/reservation/icalendar/{sys_id}`

Default URL: `/api/sn_wsd_rsv/reservation/icalendar/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the reservation for which to generate an iCalendar file body.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-reserv-entry">

Data format of the request body. Supported types: **application/json**, **application/xml** or, **text/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

iCalendar file body for the specified reservation.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint to create an iCalender body.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/reservation/icalendar/60d26a0f47578910003a4587746d4331" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "result": "BEGIN:VCALENDAR\nPRODID:-//Service-now.com//Outlook 11.0 MIMEDIR//EN\nVERSION:2.0\nMETHOD:REQUEST\nBEGIN:VEVENT\nATTENDEE;ROLE=REQ-PARTICIPANT;RSVP=TRUE:MAILTO:workplace_user@example.com\nDTSTART:20220521T050000Z\nDTEND:20220521T060000Z\nUID:60d26a0f47578910003a4587746d4331\nDTSTAMP:20220511T044018Z\nSUMMARY:For user 1\nDESCRIPTION:Dear System Administrator,\\n\\nThank you for your reservation.\\n\\nYou can find more details on your reservation, or manage your reservation using the following link: https://damay2.service-now.com/ws?id=wsd_reservation_summary&reservation_id=60d26a0f47578910003a4587746d4331\\n\\nKind regards,\\nWorkplace Services Team\nLOCATION:Berlin\nCLASS:PUBLIC\nORGANIZER;CN=Workplace User:MAILTO:workplace_user@example.com\nATTENDEE;ROLE=REQ-PARTICIPANT;CN=Workplace User:RSVP=TRUE:MAILTO:workplace_user@example.com\nEND:VEVENT\nEND:VCALENDAR"
}
```

## WSD Reservation - GET /api/sn\_wsd\_rsv/reservation/list

Retrieves the list of reservations belonging to a specified user.

This endpoint only returns reservations that were requested for or opened by the specified user.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/reservation/list`

Default URL: `/api/sn_wsd_rsv/reservation/list`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

encodedQuery

</td><td>

Encoded query to use to filter the returned reservation record results. All fields within the Workplace Reservation \[sn\_wsd\_rsv\_reservation\] table are valid within the query.For example, `active=true^requested_for=2de07e1887cb89106342b846dabb35fe​^building=4703a4cedb3650106c731dcd13961945`

Data type: String

</td></tr><tr><td>

endIndex

</td><td>

Last reservation record in the results set to return when specifying indexes for pagination. If this value is greater than the available number of return results records, all remaining records are returned.Data Type: Number

</td></tr><tr><td>

orderByEndDesc

</td><td>

Flag that indicates whether to return the return results in start time descending order.

 Valid values:

-   true: Return the results in descending order.
-   false: Return the results in ascending order.

 Default: false

</td></tr><tr><td>

searchCriteria

</td><td>

Text that has to match within the reservation for it to be included in the return results. The endpoint checks for this value in the following fields: -   configuration\_item.name
-   location.name
-   private\_subject
-   requested\_for.name
-   subject

Data Type: String

</td></tr><tr><td>

startIndex

</td><td>

Starting record for which to return records, zero-based. Use this parameter to paginate through large record sets.Data Type: String

Default: 0

</td></tr><tr><td>

userId

</td><td>

Sys\_id of a user to filter out of the returned reservation information.When this value is passed, the endpoint filters out those reservations where the requested\_for or opened\_by field is equal to the currently logged-in user. From that reservation list, it then filters out those reservation where the requested\_for or opened\_by is equal to the passed **userId**.

Data type: String

Default: Returns all reservations where the requested\_for or opened\_by fields is equal to currently logged-in user.

Table: User \[sys\_user\]

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-reserv-entry">

Data format of the request body. Supported types: **application/json**, **application/xml** or, **text/xml**. Default: **application/json**

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="id_j1f_lgz_stb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result.reservation

</td><td>

Details about the reservation.Data type: Object

```
"reservation": {
  "active": Boolean,
  "attendees": [Array],
  "check_in_state": {Object},
  "end": "String",
  "external_ical": "String",
  "external_id": "String",
  "is_parent": Boolean,
  "is_private": Boolean,
  "informEmployeePrivacy": Boolean.
  "last_updated_sub_source": {Object},
  "location" {Object},
  "number": "String",
  "number_of_attendees": Number,
  "recording_details": [Array],
  "reservable_module": {Object},
  "reservation_purpose": {Object},
  "reservation_type": {Object},
  "reservation_subtype": {Object},
  "sensitivity": {Object},
  "start": "String",
  "state": {Object},
  "source_reservation": "String",
  "subject": "String",
  "sub_source": {Object},
  "sync_state": {Object},
  "sys_created_on: "String",
  "sys_id": "String",
  "sys_updated_on": "String",
  "virtual_meeting": "String"
}
```

</td></tr><tr id="reservation_active-reserv-row"><td>

result.reservation.active

</td><td id="reservation_active-reserv-entry">

Flag that indicates whether the reservation is active.Valid values:

-   true: Reservation is active.
-   false: Reservation is inactive.

Data type: Boolean

</td></tr><tr id="reservation_attendees-reserv-row"><td>

result.reservation.attendees

</td><td id="reservation_attendees-reserv-entry">

List of attendees for the reservation.Data type: Array of Objects

```
"attendees": [
  {
    "avatar": "String",
    "displayValue": "String",
    "display_value": "String",
    "email": "String",
    "initials": "String",
    "label": "String",
    "name": "String",
    "sys_id": "String",
    "table": "String",
    "user_name": "String",
    "value": "String"
  }
]
```

</td></tr><tr id="reservation_attendees_avatar-reserv-row"><td>

result.reservation.attendees.avatar

</td><td id="reservation_attendees_avatar-reserv-entry">

Sys\_id of the avatar associated with the attendee.Data type: String

Table: Attachments \[sys\_attachment\]

</td></tr><tr id="reservation_attendees_displayValue-reserv-row"><td>

result.reservation.attendees.displayValue

</td><td id="reservation_attendees_displayValue-reserv-entry">

Display value for the attendee.Data type: String

</td></tr><tr id="reservation_attendees_display_value-reserv-row"><td>

result.reservation.attendees.display\_value

</td><td id="reservation_attendees_display_value-reserv-entry">

Display value of the attendee. Same as **displayValue**.Data type: String

</td></tr><tr id="reservation_attendees_mail-reserv-row"><td>

result.reservation.attendees.email

</td><td id="reservation_attendees_mail-reserv-entry">

Attendee's email address.Data type: String

</td></tr><tr id="reservation_attendees_initials-reserv-row"><td>

result.reservation.attendees.initials

</td><td id="reservation_attendees_initials-reserv-entry">

Attendee's initials.Data type: String

</td></tr><tr id="reservation_attendees_name-reserv-row"><td>

result.reservation.attendees.name

</td><td id="reservation_attendees_name-reserv-entry">

Attendee's name.Data type: String

</td></tr><tr id="reservation_attendees_sys_id-reserv-row"><td>

result.reservation.attendees.sys\_id

</td><td id="reservation_attendees_sys_id-reserv-entry">

Sys\_id of the attendee record.Data type: String

</td></tr><tr id="reservation_attendees_table-reserv-row"><td>

result.reservation.attendees.table

</td><td id="reservation_attendees_table-reserv-entry">

Table in which the attendee record exists.Data type: String

</td></tr><tr id="reservation_attendees_user_name-reserv-row"><td>

result.reservation.attendees.user\_name

</td><td id="reservation_attendees_user_name-reserv-entry">

Attendee's user name.Data type: String

</td></tr><tr id="reservation_attendees_value-reserv-row"><td>

result.reservation.attendees.value

</td><td id="reservation_attendees_value-reserv-entry">

Internal value of the attendee.Data type: String

</td></tr><tr id="reservation_attendees_check_in_state-reserv-row"><td>

result.reservation.check\_in\_state

</td><td id="reservation_attendees_check_in_state-reserv-entry">

Details about the check-in state of the reservation.Data type: Object

```
"check_in_state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_attendees_check_in_state_display_value-reserv-row"><td>

result.reservation.check\_in\_state.​display\_value

</td><td id="reservation_attendees_check_in_state_display_value-reserv-entry">

Display value for the current check-in state of the reservation, such as In progress or complete.Data type: String

</td></tr><tr id="reservation_attendees_check_in_state_value-reserv-row"><td>

result.reservation.check\_in\_state.value

</td><td id="reservation_attendees_check_in_state_value-reserv-entry">

Internal value for the current check-in state of the reservation, such as 2.Data type: String

</td></tr><tr id="reservation_attendees_edit_restriction-reserv-row"><td>

result.reservation.edit\_restriction

</td><td id="reservation_attendees_edit_restriction-reserv-entry">

Description of the user edit restrictions for the reservation, such as no\_restrictions, service\_only, or fully\_restricted.Data type: Object

```
"edit_restriction": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_attendees_edit_restriction_display_value-reserv-row"><td>

result.reservation.edit\_restriction.display\_​value

</td><td id="reservation_attendees_edit_restriction_display_value-reserv-entry">

Display value for the edit restrictions for the reservation, such as `No restriction`.Data type: String

</td></tr><tr id="reservation_attendees_edit_restriction_value-reserv-row"><td>

result.reservation.edit\_restriction.value

</td><td id="reservation_attendees_edit_restriction_value-reserv-entry">

Internal value for the edit restrictions for the reservation, such as `no_restriction`.Data type: String

</td></tr><tr id="end-reserv-row"><td>

result.reservation.end

</td><td id="end-reserv-entry">

Reservation end date and time.Data type: String

Format: UTC: yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr id="reservation_external_ical-reserv-row"><td>

result.reservation.external\_ical

</td><td id="reservation_external_ical-reserv-entry">

Unique external iCalendar identification of the reservation. Use this value to identify the reservation when this is a calendar sync related reservation.Data type: String

</td></tr><tr id="reservation_external_id-reserv-row"><td>

result.reservation.external\_id

</td><td id="reservation_external_id-reserv-entry">

Unique external identification of the reservation. Use this value to identify the reservation when this is a calendar sync related reservation.Data type: String

</td></tr><tr id="reservation_is_parent-reserv-row"><td>

result.reservation.is\_parent

</td><td id="reservation_is_parent-reserv-entry">

Flag that indicates whether this reservation is a parent reservation.Possible values:

-   true: Parent reservation.
-   false: Not a parent reservation.

Data type: Boolean

</td></tr><tr><td>

result.reservation.is\_private

</td><td>

Flag that indicates whether the reservation is private. If private, the reservation doesn't appear to anyone except the owner.For additional information on these privacy settings, see [Location privacy settings and impact](https://www.servicenow.com/docs/access?context=location-privacy-settings-and-impact&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Valid values:

-   true: Reservation is private.
-   false: Reservation isn't private.

Data type: Boolean

Default: Value set for privacy in the system properties.

</td></tr><tr id="reservation_last_updated_sub_source-reserv-row"><td>

result.reservation.last\_updated\_sub\_source

</td><td id="reservation_last_updated_sub_source-reserv-entry">

Details about the last updated sub-source for the reservation. Sub-sources are used when integrating reservations with an external calendar. This object contains information such as "servicenow\_workplace\_service\_delivery", "google\_calendar", or "microsoft\_exchange".Data type: Object

```
"last_updated_sub_source": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_last_updated_sub_source_display_value-reserv-row"><td>

result.reservation.last\_updated\_sub\_source.​display\_value

</td><td id="reservation_last_updated_sub_source_display_value-reserv-entry">

Display value for the last updated sub-source of the reservation, such as `ServiceNow Workplace Service Delivery` or `Google Calendar`. Used when integrating the reservation with an outside service such as Google calendar or Microsoft Outlook.Data type: String

</td></tr><tr id="reservation_last_updated_sub_source_value-reserv-row"><td>

result.reservation.last\_updated\_sub\_source.​value

</td><td id="reservation_last_updated_sub_source_value-reserv-entry">

Internal value for the last updated sub-source of the reservation, such as `servicenow_workplace_service_delivery` or `google_calendar`. Used when integrating the reservation with an outside service such as Google calendar or Microsoft Outlook.Data type: String

</td></tr><tr id="reservation_location-reserv-row"><td>

result.reservation.location

</td><td id="reservation_location-reserv-entry">

Details about the location associated with the reservation.Data type: Object

```
"location": {
  "active": Boolean,
  "area": {Object},
  "building": {Object},
  "campus": {Object},
  "capacity": Number,
  "description": "String",
  "display_value": "String",
  "email": "String",
  "floor": {Object},
  "label_value": "String",
  "name": "String",
  "number_of_attendees": Number,
  "region": {Object},
  "reservable_module": {Object},
  "reservation": {Object},
  "site": {Object},
  "state": {Object},
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_location_area-reserv-row"><td>

result.reservation.location.area

</td><td id="reservation_location_area-reserv-entry">

Details about the area associated with the location.Data type: Object

```
"area": {
  "active": Boolean,
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_location_area_active-reserv-row"><td>

result.reservation.location.area.active

</td><td id="reservation_location_area_active-reserv-entry">

Flag that indicates whether the area is active.Valid values:

-   true: Area is active.
-   false: Area is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_area_display_value-reserv-row"><td>

result.reservation.location.area.display\_value

</td><td id="reservation_location_area_display_value-reserv-entry">

Display value of the area to which this location belongs, such as Desk A2.Data type: String

</td></tr><tr id="reservation_location_area_sys_id-reserv-row"><td>

result.reservation.location.area.sys\_id

</td><td id="reservation_location_area_sys_id-reserv-entry">

Sys\_id of the area to which this location belongs.Data type: String

Table: Area \[sn\_wsd\_core\_area\]

</td></tr><tr id="reservation_location_building-reserv-row"><td>

result.reservation.location.building

</td><td id="reservation_location_building-reserv-entry">

Details about the building associated with the location.Data type: Object

```
"building": {
  "active": Boolean,
  "display_value": "String",
  "sys_id": "String",
  "timezone": {Object}
}
```

</td></tr><tr id="reservation_location_building_active-reserv-row"><td>

result.reservation.location.building.active

</td><td id="reservation_location_building_active-reserv-entry">

Flag that indicates whether the building is active.Valid values:

-   true: Building is active.
-   false: Building is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_building_display_value-reserv-row"><td>

result.reservation.location.building.​display\_value

</td><td id="reservation_location_building_display_value-reserv-entry">

Display value of the building to which this location belongs, such as AMS - Bld1.Data type: String

</td></tr><tr id="reservation_location_building_sys_id-reserv-row"><td>

result.reservation.location.building.sys\_id

</td><td id="reservation_location_building_sys_id-reserv-entry">

Sys\_id of the building to which this location belongs.Data type: String

Table: Building \[sn\_wsd\_core\_building\]

</td></tr><tr id="timezone-reserv-row"><td>

result.reservation.location.building.timezone

</td><td id="timezone-reserv-entry">

Details about the time zone associated with the location.Data type: Object

```
"timezone": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr id="timezone_display_value-reserv-row"><td>

result.reservation.location.building.timezone.​display\_value

</td><td id="timezone_display_value-reserv-entry">

Display value for the time zone to which this location belongs.Data type: String

</td></tr><tr id="timezone_value-reserv-row"><td>

result.reservation.location.building.timezone.​value

</td><td id="timezone_value-reserv-entry">

Internal value for the time zone to which this location belongs.Data type: String

</td></tr><tr id="reservation_location_campus-reserv-row"><td>

result.reservation.location.campus

</td><td id="reservation_location_campus-reserv-entry">

Details about the campus associated with the location.Data type: Object

```
"campus": {
  "active": Boolean,
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_location_campus_active-reserv-row"><td>

result.reservation.location.campus.active

</td><td id="reservation_location_campus_active-reserv-entry">

Flag that indicates whether the campus is active.Valid values:

-   true: Campus is active.
-   false: Campus is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_campus_display_value-reserv-row"><td>

result.reservation.location.campus.​display\_value

</td><td id="reservation_location_campus_display_value-reserv-entry">

Display value of the campus to which this location belongs, such as Amsterdam Campus.Data type: String

</td></tr><tr id="reservation_location_campus_sys_id-reserv-row"><td>

result.reservation.location.campus.sys\_id

</td><td id="reservation_location_campus_sys_id-reserv-entry">

Sys\_id of the campus to which this location belongs.Data type: String

Table: Campus \[sn\_wsd\_core\_campus\]

</td></tr><tr id="reservation_location_capacity-reserv-row"><td>

result.reservation.location.capacity

</td><td id="reservation_location_capacity-reserv-entry">

Maximum number of occupants for the location.Data type: Number

</td></tr><tr id="reservation_location_description-reserv-row"><td>

result.reservation.location.description

</td><td id="reservation_location_description-reserv-entry">

Brief description of the location.Data type: String

</td></tr><tr id="reservation_location_display_value-reserv-row"><td>

result.reservation.location.display\_value

</td><td id="reservation_location_display_value-reserv-entry">

Value to display in the UI for this location.Data type: String

</td></tr><tr id="reservation_location_email-reserv-row"><td>

result.reservation.location.email

</td><td id="reservation_location_email-reserv-entry">

Email address for the location.Data type: String

</td></tr><tr id="reservation_location_floor-reserv-row"><td>

result.reservation.location.floor

</td><td id="reservation_location_floor-reserv-entry">

Details about the floor associated with the location.Data type: Object

```
"floor": {
  "active": Boolean,
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_location_floor_active-reserv-row"><td>

result.reservation.location.floor.active

</td><td id="reservation_location_floor_active-reserv-entry">

Flag that indicates whether the floor is active.Valid values:

-   true: Floor is active.
-   false: Floor is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_floor_display_value-reserv-row"><td>

result.reservation.location.floor.display\_value

</td><td id="reservation_location_floor_display_value-reserv-entry">

Display value of the floor to which this location belongs, such as First floor.Data type: String

</td></tr><tr id="reservation_location_floor_sys_id-reserv-row"><td>

result.reservation.location.floor.sys\_id

</td><td id="reservation_location_floor_sys_id-reserv-entry">

Sys\_id of the floor to which this location belongs.Data type: String

Table: Floor \[sn\_wsd\_core\_floor\]

</td></tr><tr id="reservation_location_floor_label_value-reserv-row"><td>

result.reservation.location.label\_value

</td><td id="reservation_location_floor_label_value-reserv-entry">

Type of value specified in the **name** parameter, such as Room name.Data type: String

</td></tr><tr id="reservation_location_floor_name-reserv-row"><td>

result.reservation.location.name

</td><td id="reservation_location_floor_name-reserv-entry">

Name of the location.Data type: String

</td></tr><tr id="reservation_location_floor_number-reserv-row"><td>

result.reservation.location.number

</td><td id="reservation_location_floor_number-reserv-entry">

Reservation number.Data type: String

</td></tr><tr id="reservation_location_number_of_attendees-reserv-row"><td>

result.reservation.location.number\_of\_​attendees

</td><td id="reservation_location_number_of_attendees-reserv-entry">

Number of attendees for the reservation.Data type: Number

</td></tr><tr id="reservation_location_region-reserv-row"><td>

result.reservation.location.region

</td><td id="reservation_location_region-reserv-entry">

Details about the region associated with the location.Data type: Object

```
"region": {
  "active": Boolean,
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_location_region_active-reserv-row"><td>

result.reservation.location.region.active

</td><td id="reservation_location_region_active-reserv-entry">

Flag that indicates whether the region is active.Valid values:

-   true: Region is active.
-   false: Region is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_region_display_value-reserv-row"><td>

result.reservation.location.region.​display\_value

</td><td id="reservation_location_region_display_value-reserv-entry">

Display value of the region to which this location belongs, such as Europe.Data type: String

</td></tr><tr id="reservation_location_region_sys_id-reserv-row"><td>

result.reservation.location.region.sys\_id

</td><td id="reservation_location_region_sys_id-reserv-entry">

Sys\_id of the region to which this location belongs.Data type: String

Table: Region \[sn\_wsd\_core\_region\]

</td></tr><tr id="reservation_location_region_requested_for-reserv-row"><td>

result.reservation.location.requested\_for

</td><td id="reservation_location_region_requested_for-reserv-entry">

Details about the person for whom the reservation was requested on behalf of.Data type: Object

```
"requested_for": {
  "name": "String",
  "sys_id": "String",
  "user_name": "String"
}
```

</td></tr><tr id="requested_for_name-reserv-row"><td>

result.reservation.location.requested\_for.​name

</td><td id="requested_for_name-reserv-entry">

Name of the user for whom the reservation was requested for.Data type: String

</td></tr><tr id="requested_for_sys_id-reserv-row"><td>

result.reservation.location.requested\_for.​sys\_id

</td><td id="requested_for_sys_id-reserv-entry">

Sys\_id of the user for whom the reservation is being requested.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="reservation_location_requested_for_user_name-reserv-row"><td>

result.reservation.location.requested\_for.​user\_name

</td><td id="reservation_location_requested_for_user_name-reserv-entry">

User name of the user for whom the reservation was requested for.Data type: String

</td></tr><tr id="reservation_location_reservation-reserv-row"><td>

result.reservation.location.reservation

</td><td id="reservation_location_reservation-reserv-entry">

Details about the reservation associated with the location.Data type: Object

```
"reservation": {
  "active": Boolean,
  "number": "String",
  "number_of_attendees": Number,
  "requested_for": {Object},
  "state": {Object},
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_location_reservation_active-reserv-row"><td>

result.reservation.location.reservation.active

</td><td id="reservation_location_reservation_active-reserv-entry">

Flag that indicates whether the reservation is active.Valid values:

-   true: Reservation is active.
-   false: Reservation is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_reservation_number-reserv-row"><td>

result.reservation.location.reservation.number

</td><td id="reservation_location_reservation_number-reserv-entry">

Reservation number.Data type: String

</td></tr><tr id="reservation_location_reservation_number_of_attendees-reserv-row"><td>

result.reservation.location.reservation.​number\_of\_attendees

</td><td id="reservation_location_reservation_number_of_attendees-reserv-entry">

Number of attendees of the reservation.Data type: Number

</td></tr><tr id="reservation_location_reservation_requested_for-reserv-row"><td>

result.reservation.location.reservation.​requested\_for

</td><td id="reservation_location_reservation_requested_for-reserv-entry">

Details about the person for whom the reservation was requested on behalf of.Data type: Object

```
"requested_for": {
  "name": "String",
  "sys_id": "String",
  "user_name": "String"
}
```

</td></tr><tr id="reservation_location_reservation_requested_for_name-reserv-row"><td>

result.reservation.location.reservation.​requested\_for.name

</td><td id="reservation_location_reservation_requested_for_name-reserv-entry">

Name of the user for whom the reservation was requested for.Data type: String

</td></tr><tr id="reservation_location_reservation_requested_for_sys_id-reserv-row"><td>

result.reservation.location.reservation.​requested\_for.sys\_id

</td><td id="reservation_location_reservation_requested_for_sys_id-reserv-entry">

Sys\_id of the requested for user.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="reservation_location_reservation_requested_for_user_name-reserv-row"><td>

result.reservation.location.reservation.​requested\_for.user\_name

</td><td id="reservation_location_reservation_requested_for_user_name-reserv-entry">

User name of the user for whom the reservation was requested for.Data type: String

</td></tr><tr id="reservation_location_reservable_module-reserv-row"><td>

result.reservation.location.reservable\_module

</td><td id="reservation_location_reservable_module-reserv-entry">

Details about the reservable module associated with the reservation.Data type: Object

```
"reservable_module": {
  "inline_title": "String",
  "name": "String",
  "sys_id": "String",
  "title": "String"
}
```

</td></tr><tr id="reservation_location_reservable_module_inline_title-reserv-row"><td>

result.reservation.location.reservable\_module.​inline\_title

</td><td id="reservation_location_reservable_module_inline_title-reserv-entry">

Inline title of the reservable module. The title appears in line with the descriptive text on the Workplace service portal.Data type: String

</td></tr><tr id="reservation_location_reservable_module_name-reserv-row"><td>

result.reservation.location.reservable\_module.​name

</td><td id="reservation_location_reservable_module_name-reserv-entry">

Name of the reservable module.Data type: String

</td></tr><tr id="reservation_location_reservable_module_sys_id-reserv-row"><td>

result.reservation.location.reservable\_module.​sys\_id

</td><td id="reservation_location_reservable_module_sys_id-reserv-entry">

Sys\_id of the reservable module.Data type: String

</td></tr><tr id="reservation_location_reservable_module_title-reserv-row"><td>

result.reservation.location.reservable\_module.​title

</td><td id="reservation_location_reservable_module_title-reserv-entry">

Title of the reservable module.Data type: String

</td></tr><tr id="reservation_location_site-reserv-row"><td>

result.reservation.location.site

</td><td id="reservation_location_site-reserv-entry">

Site to which the location belongs.Data type: Object

```
"site": {
  "active": Boolean,
  "display_value": "String",
  "sys_id": "String"
}
```

Table: Site \[sn\_wsd\_core\_site\]

</td></tr><tr id="reservation_location_site_active-reserv-row"><td>

result.reservation.location.site.active

</td><td id="reservation_location_site_active-reserv-entry">

Flag that indicates whether the site is active.Valid values:

-   true: Site is active.
-   false: Site is inactive.

Data type: Boolean

</td></tr><tr id="reservation_location_site_display_value-reserv-row"><td>

result.reservation.location.site.display\_value

</td><td id="reservation_location_site_display_value-reserv-entry">

Display value of the site to which this location belongs, such as Western Europe.Data type: String

</td></tr><tr id="reservation_location_site_sys_id-reserv-row"><td>

result.reservation.location.site.sys\_id

</td><td id="reservation_location_site_sys_id-reserv-entry">

Sys\_id of the site to which this location belongs.Data type: String

Table: Site \[sn\_wsd\_core\_site\]

</td></tr><tr id="state-reserv-row"><td>

result.reservation.location.state

</td><td id="state-reserv-entry">

Details about the state of the reservation for the location.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="state_display_value-reserv-row"><td>

result.reservation.location.state.display\_value

</td><td id="state_display_value-reserv-entry">

Display value for the current state of the reservation, such as confirmed.Data type: String

</td></tr><tr id="state_value-reserv-row"><td>

result.reservation.location.state.value

</td><td id="state_value-reserv-entry">

Internal value for the current state of the reservation, such as 2.Data type: String

</td></tr><tr id="location_sys_id-reserv-row"><td>

result.reservation.location.sys\_id

</td><td id="location_sys_id-reserv-entry">

Sys\_id of the associated location record.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr id="reservation_notification_custom_message-reserv-row"><td>

result.reservation.notification\_custom\_​message

</td><td id="reservation_notification_custom_message-reserv-entry">

Custom message for the notification sent to the recipients listed in **reservation.notification\_recipients**.Data type: String

</td></tr><tr id="reservation_notification_recipients-reserv-row"><td>

result.reservation.notification\_recipients

</td><td id="reservation_notification_recipients-reserv-entry">

List of recipients that receive notification about the reservation.Data type: Array of Objects

```
"notification_recipients":[
  {
    "name": "String",
    "sys_id": "String",
    "user_name": "String"
  }
]
```

</td></tr><tr id="reservation_notification_recipients_name-reserv-row"><td>

result.reservation.notification\_recipients.name

</td><td id="reservation_notification_recipients_name-reserv-entry">

Name of the recipient.Data type: String

</td></tr><tr id="reservation_notification_recipients_sys_id-reserv-row"><td>

result.reservation.notification\_recipients.sys\_id

</td><td id="reservation_notification_recipients_sys_id-reserv-entry">

Sys\_id of the recipient.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="reservation_notification_recipients_user_name-reserv-row"><td>

result.reservation.notification\_recipients.​user\_name

</td><td id="reservation_notification_recipients_user_name-reserv-entry">

User name of the recipient.Data type: String

</td></tr><tr id="reservation_number-reserv-row"><td>

result.reservation.number

</td><td id="reservation_number-reserv-entry">

Unique number of the reservation record. You can use this value to query the reservation.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr id="reservation_opened_by-reserv-row"><td>

result.reservation.opened\_by

</td><td id="reservation_opened_by-reserv-entry">

Details about the user that created the reservation.Data type: Object

```
"opened_by": {
  "avatar": "String",
  "displayValue": "String",
  "display_value": "String",
  "email": "String",
  "initials": "String",
  "label": "String",
  "name": "String",
  "sys_id": "String",
  "table": "String",
  "user_name": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_opened_by_avatar-reserv-row"><td>

result.reservation.opened\_by.avatar

</td><td id="reservation_opened_by_avatar-reserv-entry">

Avatar for the user that opened the reservation.Data type: String

</td></tr><tr id="reservation_opened_by_displayValue-reserv-row"><td>

result.reservation.opened\_by.displayValue

</td><td id="reservation_opened_by_displayValue-reserv-entry">

Display value of the opened by user.Data type: String

</td></tr><tr id="reservation_opened_by_display_value-reserv-row"><td>

result.reservation.opened\_by.display\_value

</td><td id="reservation_opened_by_display_value-reserv-entry">

Display value of the opened by user.Data type: String

</td></tr><tr id="reservation_opened_by_email-reserv-row"><td>

result.reservation.opened\_by.email

</td><td id="reservation_opened_by_email-reserv-entry">

Email address for the user that opened the reservation.Data type: String

</td></tr><tr id="reservation_opened_by_initials-reserv-row"><td>

result.reservation.opened\_by.initials

</td><td id="reservation_opened_by_initials-reserv-entry">

Initials of the user that opened the reservation.Data type: String

</td></tr><tr id="reservation_opened_by_label-reserv-row"><td>

result.reservation.opened\_by.label

</td><td id="reservation_opened_by_label-reserv-entry">

Label for the user that opened the reservation. This is a combination of the title and department of the user.Data type: String

</td></tr><tr id="reservation_opened_by_name-reserv-row"><td>

result.reservation.opened\_by.name

</td><td id="reservation_opened_by_name-reserv-entry">

Name of the user that opened the reservation.Data type: String

</td></tr><tr id="reservation_opened_by_sys_id-reserv-row"><td>

result.rservation.opened\_by.sys\_id

</td><td id="reservation_opened_by_sys_id-reserv-entry">

Sys\_id\_of the user that opened the reservation.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="reservation_opened_by_table-reserv-row"><td>

result.rservation.opened\_by.table

</td><td id="reservation_opened_by_table-reserv-entry">

Table that contains the user record.Data type: String

</td></tr><tr id="reservation_opened_by_user_name-reserv-row"><td>

result.reservation.opened\_by.user\_name

</td><td id="reservation_opened_by_user_name-reserv-entry">

User name of the user that opened the reservation.Data type: String

</td></tr><tr id="reservation_opened_by_value-reserv-row"><td>

result.reservation.opened\_by.value

</td><td id="reservation_opened_by_value-reserv-entry">

Internal value of the user that opened the reservation.Data type: String

</td></tr><tr id="reservation_number-reserv1-row"><td>

result.reservation.number

</td><td id="reservation_number-reserv1-entry">

Reservation number.Data type: String

</td></tr><tr id="reservation_number_of_attendees-reserv-row"><td>

result.reservation.number\_of\_attendees

</td><td id="reservation_number_of_attendees-reserv-entry">

Number of attendees in this reservation.Data type: Number

</td></tr><tr id="reservation_recording_details-reserv-row"><td>

result.reservation.recording\_details

</td><td id="reservation_recording_details-reserv-entry">

Details about the recordings associated with the reservation \(meeting\).Data type: Array of Objects

```
"recording_details": [
  "recording_url": "String"
]
```

</td></tr><tr id="reservation_recording_details_recording_url-reserv-row"><td>

result.reservation.recording\_details.​recording\_url

</td><td id="reservation_recording_details_recording_url-reserv-entry">

URL of the recordings associated with the reservation.Data type: String

</td></tr><tr id="reservation_requested_for-reserv-row"><td>

result.reservation.requested\_for

</td><td id="reservation_requested_for-reserv-entry">

Details about the user that the reservation was made on behalf of.Data type: Object

```
"requested_for": {
  "avatar": "String",
  "displayValue": "String",
  "display_value": "String",
  "email": "String",
  "initials": "String",
  "label": "String",
  "name": "String",
  "sys_id": "String",
  "table": "String",
  "user_name": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_requested_for_avatar-reserv-row"><td>

result.reservation.requested\_for.avatar

</td><td id="reservation_requested_for_avatar-reserv-entry">

Avatar for the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_displayValue-reserv-row"><td>

result.reservation.requested\_for.displayValue

</td><td id="reservation_requested_for_displayValue-reserv-entry">

Display value of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_display_value-reserv-row"><td>

result.reservation.requested\_for.display\_value

</td><td id="reservation_requested_for_display_value-reserv-entry">

Display value of the user that the reservation was made on behalf of. Same as displayValue.Data type: String

</td></tr><tr id="reservation_requested_for_email-reserv-row"><td>

result.reservation.requested\_for.email

</td><td id="reservation_requested_for_email-reserv-entry">

Email address for the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_initials-reserv-row"><td>

result.reservation.requested\_for.initials

</td><td id="reservation_requested_for_initials-reserv-entry">

Initials of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_label-reserv-row"><td>

result.reservation.requested\_for.label

</td><td id="reservation_requested_for_label-reserv-entry">

Label for the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_name-reserv-row"><td>

result.reservation.requested\_for.name

</td><td id="reservation_requested_for_name-reserv-entry">

Name of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_sys_id-reserv-row"><td>

result.rservation.requested\_for.sys\_id

</td><td id="reservation_requested_for_sys_id-reserv-entry">

Sys\_id\_of the user that the reservation was made on behalf of.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="reservation_requested_for_table-reserv-row"><td>

result.rservation.requested\_for.table

</td><td id="reservation_requested_for_table-reserv-entry">

Table that contains the user record.Data type: String

</td></tr><tr id="reservation_requested_for_user_name-reserv-row"><td>

result.reservation.requested\_for.user\_name

</td><td id="reservation_requested_for_user_name-reserv-entry">

User name of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_requested_for_value-reserv-row"><td>

result.reservation.requested\_for.value

</td><td id="reservation_requested_for_value-reserv-entry">

Internal value of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr id="reservation_reservable_module-reserv-row"><td>

result.reservation.reservable\_module

</td><td id="reservation_reservable_module-reserv-entry">

Details for the requested reservable module.Data type: Object

```
"reservable_module": {
  "allow_invitees": Boolean,
  "allow_whole_day": Boolean,
  "apply_to_shift": Boolean,
  "browse_by_area_enabled": Boolean,
  "browse_near_a_person_enabled": Boolean,
  "buildingSysIds": [Array],
  "checkin_before_minutes": Number,
  "display_number_of_attendees": Boolean,
  "display_on_behalf_of": Boolean,
  "display_sensitivity": Boolean,
  "display_value": "String",
  "enable_browse_by_area": Boolean,
  "enable_browse_near_a_person": Boolean,
  "enable_facet_filter": Boolean,
  "enable_group_reservations": Boolean,
  "enable_ical_generation": Boolean,
  "font_awesome_icon": "String",
  "inline_title": "String",      
  "layout_mapping": {Object},
  "max_days_in_future": Number,
  "max_occurrences": Number,
  "name": "String",
  "override_approval_policy": "String",
  "require_cancel_notes": Boolean,
  "require_cc_dept_check": Boolean,
  "require_subject": Boolean,
  "reservable_columns": [Array],
  "reservable_container_field": "String",
  "reservable_filter": "String",
  "reservable_quantity_field": "String",
  "reservable_table": "String",
  "reservable_type": "String",
  "reservable_views": [Array],
  "reservation_paths": [Array],
  "search_limit": Number,
  "selection_type": "String",
  "short_description": "String",
  "show_map_view": Boolean,
  "sys_id": "String",
  "timeSlots": [Array],
  "title": "String",
  "virtual_meeting_provider": {Object}
}
```

</td></tr><tr id="reservation_reservable_module_allow_invitees-reserv-row"><td>

result.reservation.reservable\_module.​allow\_invitees

</td><td id="reservation_reservable_module_allow_invitees-reserv-entry">

Flag that indicates whether employees are able to add invitees to the reservation. Valid values:

-   true: Allow employees to add invitees to the reservation.
-   false: Don't allow employees to add invitees to the reservation.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_allow_whole_day-reserv-row"><td>

result.reservation.reservable\_module.​allow\_whole\_day

</td><td id="reservation_reservable_module_allow_whole_day-reserv-entry">

Flag that indicates whether users can reserve the reservable for the entire day. Valid values:

-   true: Allow users to reserve for the entire day.
-   false: Don't allow users to reserve for the entire day.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_apply_to_shift-reserv-row"><td>

result.reservation.reservable\_module.​apply\_to\_shift

</td><td id="reservation_reservable_module_apply_to_shift-reserv-entry">

Flag that indicates whether shift-based reservations are enabled for the reservable module. Valid values:

-   true: Allow shift-based reservations.
-   false: Don't allow shift-based reservations.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_browse_by_area_enabled-reserv-row"><td>

result.reservation.reservable\_module.​browse\_by\_area\_enabled

</td><td id="reservation_reservable_module_browse_by_area_enabled-reserv-entry">

Flag that indicates whether users are able to search for reservable modules by area.Valid values:

-   true: Allow users to browse reservable modules by area.
-   false: Don't allow users to browse reservable modules by area.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_browse_near_a_person_enabled-reserv-row"><td>

result.reservation.reservable\_module.​browse\_near\_a\_person\_enabled

</td><td id="reservation_reservable_module_browse_near_a_person_enabled-reserv-entry">

Flag that indicates whether users are able to search for reservable modules located by a specified person.Valid values:

-   true: Allow users to browse reservable modules near a person.
-   false: Don't allow users to browse reservable modules near a person.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_buildingSysIds-reserv-row"><td>

result.reservation.reservable\_module.​buildingSysIds

</td><td id="reservation_reservable_module_buildingSysIds-reserv-entry">

List of sys\_ids of the buildings associated with the reservable module.Data type: Array of Strings

</td></tr><tr id="reservation_reservable_module_checkin_before_minutes-reserv-row"><td>

result.reservation.reservable\_module.​checkin\_before\_minutes

</td><td id="reservation_reservable_module_checkin_before_minutes-reserv-entry">

Amount of time before a reservation starts that a user can check into their reservation.Unit: Minutes

Data type: Number

</td></tr><tr id="reservation_reservable_module_display_number_of_attendees-reserv-row"><td>

result.reservation.reservable\_module.​display\_number\_of\_attendees

</td><td id="reservation_reservable_module_display_number_of_attendees-reserv-entry">

Flag that indicates whether users can specify the number of attendees in the reservation. Valid values:

-   true: Users can specify the number of attendees.
-   false: Users can't specify the display number of attendees.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_display_on_behalf_of-reserv-row"><td>

result.reservation.reservable\_module.​display\_on\_behalf\_of

</td><td id="reservation_reservable_module_display_on_behalf_of-reserv-entry">

Flag that indicates whether reservations can be made on behalf of someone else. Valid values:

-   true: On behalf of supported.
-   false: On behalf of not supported.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_display_sensitivity-reserv-row"><td>

result.reservation.reservable\_module.​display\_sensitivity

</td><td id="reservation_reservable_module_display_sensitivity-reserv-entry">

Flag that indicates whether users can set the sensitivity of the reservation, such as normal or private.Valid values:

-   true: Able to set sensitivity.
-   false: Not able to set sensitivity. Defaults to normal.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_display_value-reserv-row"><td>

result.reservation.reservable\_module.​display\_value

</td><td id="reservation_reservable_module_display_value-reserv-entry">

Display value of the reservable module.Data type: String

</td></tr><tr id="reservation_reservable_module_enable_browse_by_area-reserv-row"><td>

result.reservation.reservable\_module.​enable\_browse\_by\_area

</td><td id="reservation_reservable_module_enable_browse_by_area-reserv-entry">

Flag that indicates whether users are able to search for reservable modules by area. Same as **browse\_by\_area\_enabled**.Valid values:

-   true: Allow users to browse reservable modules by area.
-   false: Don't allow users to browse reservable modules by area.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_enable_browse_near_a_person-reserv-row"><td>

result.reservation.reservable\_module.​enable\_browse\_near\_a\_person

</td><td id="reservation_reservable_module_enable_browse_near_a_person-reserv-entry">

Flag that indicates whether users are able to search for reservable modules located by a specified person. Same as**browse\_near\_a\_person\_enabled**.Valid values:

-   true: Allow users to browse reservable modules near a person.
-   false: Don't allow users to browse reservable modules near a person.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_enable_facet_filter-reserv-row"><td>

result.reservation.reservable\_module.​enable\_facet\_filter

</td><td id="reservation_reservable_module_enable_facet_filter-reserv-entry">

Flag that indicates whether facet filtering on workplace items is enabled. When enabled, the filter options that appear are based on the search results. Only the items that are available in the generated search result are available to users for selection in the filter.Valid values:

-   true: Facet filters are enabled.
-   false: Facet filters aren't enabled.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_enable_group_reservations-reserv-row"><td>

result.reservation.reservable\_module.​enable\_group\_reservations

</td><td id="reservation_reservable_module_enable_group_reservations-reserv-entry">

Flag that indicates whether users can make a group reservation.Valid values:

-   true: Able to make group reservations.
-   false: Not able to make group reservations.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_enable_ical_generation-reserv-row"><td>

result.reservation.reservable\_module.​enable\_ical\_generation

</td><td id="reservation_reservable_module_enable_ical_generation-reserv-entry">

Flag that indicates whether users can generate an iCalendar for the reservation.Valid values:

-   true: iCalendar generation allowed.
-   false: iCalendar generation isn't allowed.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_font_awesome_icon-reserv-row"><td>

result.reservation.reservable\_module.​font\_awesome\_icon

</td><td id="reservation_reservable_module_font_awesome_icon-reserv-entry">

Name of the font icon attached to the reservable module.Data type: String

</td></tr><tr id="reservation_reservable_module_inline_title-reserv-row"><td>

result.reservation.reservable\_module.​inline\_title

</td><td id="reservation_reservable_module_inline_title-reserv-entry">

Inline title of the reservable module. The title appears in line with the descriptive text on the Workplace service portal.Data type: String

</td></tr><tr id="reservation_reservable_module_layout_mapping-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping

</td><td id="reservation_reservable_module_layout_mapping-reserv-entry">

Details about the structure of the layout mapping of locations. Use this data to lay out the information in the UI. Data type: Object

```
"layout_mapping": {
  "body": [Array],
  "description": [Array],
  "image": "String",
  "subtitle": [Array],
  "subtitle_asc": [Array],
  "title": [Array]
}
```

</td></tr><tr id="reservation_reservable_module_layout_mapping_body-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.body

</td><td id="reservation_reservable_module_layout_mapping_body-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: Array of Objects

```
"body": [
  {
    "field": "String",
    "field_to_display": "String",
    "icon": "String",
    "label": "String"
  }
]
```

</td></tr><tr id="reservation_reservable_module_layout_mapping_body_field-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.body.field

</td><td id="reservation_reservable_module_layout_mapping_body_field-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="reservation_reservable_module_layout_mapping_body_field_to_display-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.body.field\_to\_display

</td><td id="reservation_reservable_module_layout_mapping_body_field_to_display-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="reservation_reservable_module_layout_mapping_body_icon-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.body.icon

</td><td id="reservation_reservable_module_layout_mapping_body_icon-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="reservation_reservable_module_layout_mapping_body_label-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.body.label

</td><td id="reservation_reservable_module_layout_mapping_body_label-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="reservation_reservable_module_layout_mapping_description-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.description

</td><td id="reservation_reservable_module_layout_mapping_description-reserv-entry">

Placeholder for mapping the front-end UI data. Description of the layout mapping.Data type: Array

</td></tr><tr id="reservation_reservable_module_layout_mapping_image-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.image

</td><td id="reservation_reservable_module_layout_mapping_image-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr id="reservation_reservable_module_layout_mapping_subtitle-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.subtitle

</td><td id="reservation_reservable_module_layout_mapping_subtitle-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: Array

</td></tr><tr id="reservation_reservable_module_layout_mapping_subtitle_asc-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.subtitle\_asc

</td><td id="reservation_reservable_module_layout_mapping_subtitle_asc-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: Array

</td></tr><tr id="reservation_reservable_module_layout_mapping_title-reserv-row"><td>

result.reservation.reservable\_module.​layout\_mapping.title

</td><td id="reservation_reservable_module_layout_mapping_title-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: Array

</td></tr><tr id="reservation_reservable_module_max_days_in_future-reserv-row"><td>

result.reservation.reservable\_module.​max\_days\_in\_future

</td><td id="reservation_reservable_module_max_days_in_future-reserv-entry">

Maximum number of the days in the future that a user can reserve the reservable module.Data type: Number

</td></tr><tr id="reservation_reservable_module_max_occurrences-reserv-row"><td>

result.reservation.reservable\_module.​max\_occurrences

</td><td id="reservation_reservable_module_max_occurrences-reserv-entry">

Maximum number of recurring reservation occurrences if recurring reservations are available for the reservable module.Data type: Number

</td></tr><tr id="reservation_reservable_module_name-reserv-row"><td>

result.reservation.reservable\_module.name

</td><td id="reservation_reservable_module_name-reserv-entry">

Name of the reservable module.Data type: String

</td></tr><tr id="reservation_reservable_module_override_approval_policy-reserv-row"><td>

result.reservation.reservable\_module.​override\_approval\_policy

</td><td id="reservation_reservable_module_override_approval_policy-reserv-entry">

Option to specify how to implement the approval policy. Choices:

-   No override: The approval policy is implemented as set in the **Requires approval** field of a workplace space or room.
-   Always require approval: The approval policy is required regardless of what is set in the **Requires approval** field of a workplace space or room.
-   Never require approval: The approval policy is removed regardless of what is set in the **Requires approval**l field of a workplace space or room.

Data type: String

</td></tr><tr id="reservation_reservable_module_require_cancel_notes-reserv-row"><td>

result.reservation.reservable\_module.​require\_cancel\_notes

</td><td id="reservation_reservable_module_require_cancel_notes-reserv-entry">

Flag that indicates whether users must enter a cancellation note before cancelling a reservable module.Valid values:

-   true: Cancellation note required.
-   false: Cancellation note not required.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_require_cc_dept_check-reserv-row"><td>

result.reservation.reservable\_module.​require\_cc\_dept\_check

</td><td id="reservation_reservable_module_require_cc_dept_check-reserv-entry">

Flag that indicates whether to check if there's a cost center or department mismatch between the workspace item and the logged in user. Valid values:

-   true: Check for a mismatch.
-   false: Don't check for a mismatch.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_require_subject-reserv-row"><td>

result.reservation.reservable\_module.​require\_subject

</td><td id="reservation_reservable_module_require_subject-reserv-entry">

Flag that indicates whether the user must enter a subject when making the reservation.Valid values:

-   true: Subject required.
-   false: Subject isn't required.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_reservable_columns-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_columns

</td><td id="reservation_reservable_module_reservable_columns-reserv-entry">

List of the columns of a reservable.Data type: Array

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr id="reservation_reservable_module_reservable_container_field-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_container\_field

</td><td id="reservation_reservable_module_reservable_container_field-reserv-entry">

Level of the container, such as a group of desks in a specific area.Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_filter-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_filter

</td><td id="reservation_reservable_module_reservable_filter-reserv-entry">

Filter conditions used to filter out reservable items in the associated Reservable table. Reservable table is a field in the Reservable Module \[sn\_wsd\_rsv\_reservable\_module\] table. These filter conditions were applied to the table contained in the field Reservable table.Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_quantity_field-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_quantity\_field

</td><td id="reservation_reservable_module_reservable_quantity_field-reserv-entry">

Reservable quantity of all the spaces. The quantity is used when assigning neighbourhood spaces to an area. For additional information, see [Assign neighborhood spaces to an area](https://www.servicenow.com/docs/access?context=add-neighbourhood-spaces-to-an-area&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_table-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_table

</td><td id="reservation_reservable_module_reservable_table-reserv-entry">

Table that contains the reservable workplace items.Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_type-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_type

</td><td id="reservation_reservable_module_reservable_type-reserv-entry">

Type of the reservable item, such as location.Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_views-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_views

</td><td id="reservation_reservable_module_reservable_views-reserv-entry">

Details about the different views associated with the reservable module, such as card view or schedule view.Data type: Object

```
"reservable_views": {
  "iconClass": "String",
  "isDefault": Boolean,
  "label": "String",
  "order": Number,
  "type": "String"
}
```

Table: Reservable View \[sn\_wsd\_rsv\_reservable\_view\]

</td></tr><tr id="reservation_reservable_module_reservable_views_iconClass-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_views.iconClass

</td><td id="reservation_reservable_module_reservable_views_iconClass-reserv-entry">

Icon class of the reservable view.Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_views_isDefault-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_views.isDefault

</td><td id="reservation_reservable_module_reservable_views_isDefault-reserv-entry">

Flag that indicates whether to make this reservable view the default for reservable modules. Valid values:

-   true: Make default.
-   false: Don't make default.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_reservable_views_label-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_views.label

</td><td id="reservation_reservable_module_reservable_views_label-reserv-entry">

Name of the reservable view.Data type: String

</td></tr><tr id="reservation_reservable_module_reservable_views_order-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_views.order

</td><td id="reservation_reservable_module_reservable_views_order-reserv-entry">

Order in which the views are displayed for the reservable module in the UI. The lower order number come first in the UI. In case of the same order number, it is assigned random ordering.Data type: Number

</td></tr><tr id="reservation_reservable_module_reservable_views_type-reserv-row"><td>

result.reservation.reservable\_module.​reservable\_views.type

</td><td id="reservation_reservable_module_reservable_views_type-reserv-entry">

Backend name of the reservable view. Used for internal processing.Data type: String

</td></tr><tr id="reservation_reservable_module_reservation_paths-reserv-row"><td>

result.reservation.reservable\_module.​reservation\_paths

</td><td id="reservation_reservable_module_reservation_paths-reserv-entry">

Reservation paths associated with the reservable modules such as Browse all, Browse near a person.Data type: Array of Objects

```
"reservation_paths": [
  {
    "displayValue": "String",
    "value": "String"
  }
]
```

</td></tr><tr id="reservation_reservable_module_reservation_paths_display_value-reserv-row"><td>

result.reservation.reservable\_module.​reservation\_paths.display\_value

</td><td id="reservation_reservable_module_reservation_paths_display_value-reserv-entry">

Display value for the reservation path, such as "Browse near a person".Data type: String

</td></tr><tr id="reservation_reservable_module_reservation_paths_value-reserv-row"><td>

result.reservation.reservable\_module.​reservation\_paths.value

</td><td id="reservation_reservable_module_reservation_paths_value-reserv-entry">

Internal value for the reservation path, such as "browse\_near\_a\_person".Data type: String

</td></tr><tr id="reservation_reservable_module_search_limit-reserv-row"><td>

result.reservation.reservable\_module.​search\_limit

</td><td id="reservation_reservable_module_search_limit-reserv-entry">

Maximum number of search results to return when a user searches for a workplace location.Data type: Number

</td></tr><tr id="reservation_reservable_module_selection_type-reserv-row"><td>

result.reservation.reservable\_module.​selection\_type

</td><td id="reservation_reservable_module_selection_type-reserv-entry">

Type of selection to display in the search results.

 Can be one of the following options:

-   Specific unit: The search result displays every workplace item.
-   Container: The search result displays the parent or container of the workplace items.

 Data type: String

</td></tr><tr id="reservation_reservable_module_short_description-reserv-row"><td>

result.reservation.reservable\_module.​short\_description

</td><td id="reservation_reservable_module_short_description-reserv-entry">

Brief description of the reservable module.Data type: String

</td></tr><tr id="reservation_reservable_module_show_map_view-reserv-row"><td>

result.reservation.reservable\_module.​show\_map\_view

</td><td id="reservation_reservable_module_show_map_view-reserv-entry">

Flag that indicates whether to enable the map view for reservable modules. Valid values:

-   true: Enable map view.
-   false: Don't enable map view.

Data type: Boolean

</td></tr><tr id="reservation_reservable_module_sys_id-reserv-row"><td>

result.reservation.reservable\_module.sys\_id

</td><td id="reservation_reservable_module_sys_id-reserv-entry">

Sys\_id of the reservable module.Data type: String

</td></tr><tr id="reservation_reservable_module_timeSlots-reserv-row"><td>

result.reservation.reservable\_module.timeSlots

</td><td id="reservation_reservable_module_timeSlots-reserv-entry">

Details about the time slots associated for a reservable module.Data type: Array of Objects

```
[
  {
    "name": "String",
    "short_description": "String",
    "slot_end": "String",
    "slot_start": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr id="reservation_reservable_module_timeSlots_name-reserv-row"><td>

result.reservation.reservable\_module.​timeSlots.name

</td><td id="reservation_reservable_module_timeSlots_name-reserv-entry">

Name of the time slot.Data type: String

</td></tr><tr id="reservation_reservable_module_timeSlots_short_description-reserv-row"><td>

result.reservation.reservable\_module.​timeSlots.short\_description

</td><td id="reservation_reservable_module_timeSlots_short_description-reserv-entry">

Brief description of the time slot.Data type: String

</td></tr><tr id="reservation_reservable_module_timeSlots_slot_end-reserv-row"><td>

result.reservation.reservable\_module.​timeSlots.slot\_end

</td><td id="reservation_reservable_module_timeSlots_slot_end-reserv-entry">

End time of the time slot.Data type: String

</td></tr><tr id="reservation_reservable_module_timeSlots_slot_start-reserv-row"><td>

result.reservation.reservable\_module.​timeSlots.slot\_start

</td><td id="reservation_reservable_module_timeSlots_slot_start-reserv-entry">

Start time of the slot.Data type: String

</td></tr><tr id="reservation_reservable_module_timeSlots_sys_id-reserv-row"><td>

result.reservation.reservable\_module.​timeSlots.sys\_id

</td><td id="reservation_reservable_module_timeSlots_sys_id-reserv-entry">

Sys\_id of the time slot record.Data type: String

Table: Time Slot \[sn\_wsd\_rsv\_time\_slot\]

</td></tr><tr id="reservation_reservable_module_title-reserv-row"><td>

result.reservation.reservable\_module.title

</td><td id="reservation_reservable_module_title-reserv-entry">

Title of the reservable module.Data type: String

</td></tr><tr id="reservation_reservable_module_virtual_meeting_provider-reserv-row"><td>

result.reservation.reservable\_module.​virtual\_meeting\_provider

</td><td id="reservation_reservable_module_virtual_meeting_provider-reserv-entry">

Details about the virtual provider associated with the reservable module.Data type: Object

```
"virtual_meeting_provider": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_reservable_module_virtual_meeting_provider_display_value-reserv-row"><td>

result.reservation.reservable\_module.​virtual\_meeting\_provider.display\_value

</td><td id="reservation_reservable_module_virtual_meeting_provider_display_value-reserv-entry">

Display value of the virtual meeting provider.Data type: String

</td></tr><tr id="reservation_reservable_module_virtual_meeting_provider_value-reserv-row"><td>

result.reservation.reservable\_module.​virtual\_meeting\_provider.sys\_id

</td><td id="reservation_reservable_module_virtual_meeting_provider_value-reserv-entry">

Sys\_id of the virtual meeting provider.Data type: String

</td></tr><tr id="reservation_reservationAcl-reserv-row"><td>

result.reservation.reservationAcl

</td><td id="reservation_reservationAcl-reserv-entry">

Details of the user access control levels \(ACL\) checks set on the associated reservation.Data type: Object

```
"reservationAcl": {
  "read": Boolean,
  "write": {Object}
}
```

</td></tr><tr id="reservation_reservationAcl-reserv_read-row"><td>

result.reservation.reservationAcl.read

</td><td id="reservation_reservationAcl-reserv_read-entry">

Flag that indicates whether to check if the user can read this reservation.Valid values:

-   true: Check if user can read the reservation.
-   false: Don't check if user can read the reservation.

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write-row"><td>

result.reservation.reservationAcl.write

</td><td id="reservation_reservationAcl-reserv_write-entry">

Details about the user's write capabilities for the associated reservation.Data type: Object

```
"write": {
  "allFields": Boolean,
  "fields": {Object},
  "record": Boolean
}
```

</td></tr><tr id="reservation_reservationAcl-reserv_write_allFields-row"><td>

result.reservation.reservationAcl.write.allFields

</td><td id="reservation_reservationAcl-reserv_write_allFields-entry">

Flag that indicates whether to check if the user can write to all fields specified in the **reservationACL.write.fields** object. If the user only has access to some specific fields, then only those fields are true in the **reservationACL.write.fields** object.Valid values:

-   true: Check if user can write to all fields specified in the **reservationACL.write.fields** object.
-   false: Don't check if user can write to all fields specified in the **reservationACL.write.fields** object

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write_fields-row"><td>

result.reservation.reservationAcl.write.fields

</td><td id="reservation_reservationAcl-reserv_write_fields-entry">

Details of the access controls on various fields of the reservation.Data type: Object

```
"fields": {
  "location": Boolean,
  "number_of_attendees": Boolean,
  "requested_for": Boolean,
  "sensitivity": Boolean,
  "subject": Boolean
}
```

</td></tr><tr id="reservation_reservationAcl-reserv_write_fields_location-row"><td>

result.reservation.reservationAcl.write.fields.​location

</td><td id="reservation_reservationAcl-reserv_write_fields_location-entry">

Flag that indicates whether to check if the user can write to the location fields in this reservation.Valid values:

-   true: Check if user can write to the location fields.
-   false: Don't check if user can write to the location fields.

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write_fields_number_of_attendees-row"><td>

result.reservation.reservationAcl.write.fields.​number\_of\_attendees

</td><td id="reservation_reservationAcl-reserv_write_fields_number_of_attendees-entry">

Flag that indicates whether to check if the user can write to the number of attendees fields in this reservation.Valid values:

-   true: Check if user can write to the number of attendees field.
-   false: Don't check if user can write to the number of attendees field.

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write_fields_requested_for-row"><td>

result.reservation.reservationAcl.write.fields.​requested\_for

</td><td id="reservation_reservationAcl-reserv_write_fields_requested_for-entry">

Flag that indicates whether to check if the user can write to the requested for fields in this reservation.Valid values:

-   true: Check if user can write to the requested for field.
-   false: Don't check if user can write to the requested for field.

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write_fields_sensitivity-row"><td>

result.reservation.reservationAcl.write.fields.​sensitivity

</td><td id="reservation_reservationAcl-reserv_write_fields_sensitivity-entry">

Flag that indicates whether to check if the user can write to the sensitivity fields in this reservation.Valid values:

-   true: Check if user can write to the sensitivity field.
-   false: Don't check if user can write to the sensitivity field.

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write_fields_subject-row"><td>

result.reservation.reservationAcl.write.fields.​subject

</td><td id="reservation_reservationAcl-reserv_write_fields_subject-entry">

Flag that indicates whether to check if the user can write to the subject fields in this reservation.Valid values:

-   true: Check if user can write to the subject field.
-   false: Don't check if user can write to the subject fields.

Data type: Boolean

</td></tr><tr id="reservation_reservationAcl-reserv_write_record-row"><td>

result.reservation.reservationAcl.write.record

</td><td id="reservation_reservationAcl-reserv_write_record-entry">

Flag that indicates whether to check if the user can write to the entire reservation record.Valid values:

-   true: Check if user can write to the entire reservation record.
-   false: Don't check if user can write to the entire reservation record.

Data type: Boolean

</td></tr><tr id="reservation_purpose-reserv-row"><td>

result.reservation.reservation\_purpose

</td><td id="reservation_purpose-reserv-entry">

Details about the purpose of the reservation.Data type: Object

```
"reservation_purpose": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_purpose_display_value-reserv-row"><td>

result.reservation.reservation\_purpose.​display\_value

</td><td id="reservation_purpose_display_value-reserv-entry">

Display value for the purpose of the reservation, such as Company meeting.Data type: String

</td></tr><tr id="reservation_purpose_value-reserv-row"><td>

result.reservation.reservation\_purpose.value

</td><td id="reservation_purpose_value-reserv-entry">

Internal value for the purpose of the reservation, such as company\_meeting.Data type: String

</td></tr><tr id="reservation_reservation_type-row"><td>

result.reservation.reservation\_type

</td><td id="reservation_reservation_type-entry">

Details about the type of the reservation.Data type: Object

```
"reservation_type": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_reservation_type_display_value-row"><td>

result.reservation.reservation\_type.​display\_value

</td><td id="reservation_reservation_type_display_value-entry">

Display value for the type of the reservation, such as Space.Data type: String

</td></tr><tr id="reservation_reservation_type_value-row"><td>

result.reservation.reservation\_type.value

</td><td id="reservation_reservation_type_value-entry">

Internal value for the type of the reservation, such as space.Data type: String

</td></tr><tr id="reservation_reservation_subtype-row"><td>

result.reservation.reservation\_subtype

</td><td id="reservation_reservation_subtype-entry">

Details about the subtype of the reservation. Subtypes indicate the type of reservation, such as single, Multi parent, Multi child, Recurring parent, or occurrence.Data type: Object

```
"reservation_subtype": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_reservation_subtype_display_value-row"><td>

result.reservation.reservation\_subtype.​display\_value

</td><td id="reservation_reservation_subtype_display_value-entry">

Display value for the subtype of the reservation, such as Single.Data type: String

</td></tr><tr id="reservation_reservation_subtype_value-row"><td>

result.reservation.reservation\_subtype.value

</td><td id="reservation_reservation_subtype_value-entry">

Internal value for the subtype of the reservation, such as single.Data type: String

</td></tr><tr id="reservation_sensitivity-row"><td>

result.reservation.sensitivity

</td><td id="reservation_sensitivity-entry">

Details about the sensitivity of the reservation.Data type: Object

```
"sensitivity": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_sensitivity_display_value-row"><td>

result.reservation.sensitivity.display\_value

</td><td id="reservation_sensitivity_display_value-entry">

Display value for the sensitivity of the reservation, such as high or low.Data type: String

</td></tr><tr id="reservation_sensitivity_value-row"><td>

result.reservation.sensitivity.value

</td><td id="reservation_sensitivity_value-entry">

Internal value for the sensitivity of the reservation, such as 1 or 3.Data type: String

</td></tr><tr id="reservation_shift-row"><td>

result.reservation.shift

</td><td id="reservation_shift-entry">

Details about the shift applied to the reservation.Data type: Object

```
"shift": {
  "display_value": "String",
  "name": "String",
  "shiftDetails": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="reservation_shift_display_value-row"><td>

result.reservation.shift.display\_value

</td><td id="reservation_shift_display_value-entry">

Display value of the shift.Data type: String

</td></tr><tr id="reservation_shift_name-row"><td>

result.reservation.shift.name

</td><td id="reservation_shift_name-entry">

Name of the shift. Same as **display\_value**.Data type: String

</td></tr><tr id="reservation_shift_shiftDetails-row"><td>

Result.reservation.shift.shiftDetails

</td><td id="reservation_shift_shiftDetails-entry">

Details of shift.Data type: String

</td></tr><tr id="reservation_shift_sys_id-row"><td>

result.reservation.shift.sys\_id

</td><td id="reservation_shift_sys_id-entry">

Sys\_id of the shift record.Data type: String

Table: Shift \[sn\_wsd\_core\_shift\]

</td></tr><tr id="reservation_source-row"><td>

result.reservation.source

</td><td id="reservation_source-entry">

Details about the source for the reservation, such as Workplace Services or Google Mail..Data type: Object

```
"source": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_source_display_value-row"><td>

result.reservation.source.display\_value

</td><td id="reservation_source_display_value-entry">

Display value for the reservation source, such as Workplace Services.Data type: String

</td></tr><tr id="reservation_source_value-row"><td>

result.reservation.source.value

</td><td id="reservation_source_value-entry">

Internal value for the reservation source, such as servicenow.Data type: String

</td></tr><tr id="reservation_source_icon-row"><td>

result.reservation.source\_icon

</td><td id="reservation_source_icon-entry">

Details about the source of the icon used in the reservation. This icon is used in the UI.Data type: Object

```
"source_icon": {
  "classNames": "String",
  "imgSrc": "String",
  "tooltip": "String"
}
```

</td></tr><tr id="reservation_source_icon_classNames-row"><td>

result.reservation.source\_icon.classNames

</td><td id="reservation_source_icon_classNames-entry">

Comma-separated class names for the source icon.Data type: String

</td></tr><tr id="reservation_source_icon_imgSrc-row"><td>

result.reservation.source\_icon.imgSrc

</td><td id="reservation_source_icon_imgSrc-entry">

Name of the image source for source icon. This icon is stored in the Images \[db\_image\] table.Data type: String

</td></tr><tr id="reservation_source_icon_tooltip-row"><td>

result.reservation.source\_icon.tooltip

</td><td id="reservation_source_icon_tooltip-entry">

Tooltip associated with the source icon.Data type: String

</td></tr><tr id="reservation_source_reservation-row"><td>

result.reservation.source\_reservation

</td><td id="reservation_source_reservation-entry">

Source reservation of the current reservation.For example, in the case of multiple reservations, the parent reservation is the source of the child reservation.

Data type: String

</td></tr><tr id="start-reserv-row"><td>

result.reservation.start

</td><td id="start-reserv-entry">

Reservation start date and time.Data type: String

Format: UTC - yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr id="subject-reserv-row"><td>

result.reservation.subject

</td><td id="subject-reserv-entry">

Reservation's subject.Data type: String

</td></tr><tr id="reservation_sub_source-row"><td>

result.reservation.sub\_source

</td><td id="reservation_sub_source-entry">

Details about the sub-source of the reservation. The sub-source specifies where the reservation originated such as Google Calendar or Microsoft Exchange.Data type: Object

```
"sub_source": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_sub_source_display_value-row"><td>

result.reservation.sub\_source.display\_value

</td><td id="reservation_sub_source_display_value-entry">

Display value for the sub-source of the reservation, such as Google Calendar.Data type: String

</td></tr><tr id="reservation_sub_source_value-row"><td>

result.reservation.sub\_source.value

</td><td id="reservation_sub_source_value-entry">

Internal value of the sub-source field of the reservation, such as google\_calendar.Data type: String

</td></tr><tr id="reservation_sync_state-row"><td>

result.reservation.sync\_state

</td><td id="reservation_sync_state-entry">

Details about the synchronization state of a reservation from another service, such as "sync\_enqueued" or "synchronized".Data type: Object

```
"sync_state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="reservation_sync_state_display_value-row"><td>

result.reservation.sync\_state.display\_value

</td><td id="reservation_sync_state_display_value-entry">

Display value for the current sync state of the reservation, such as synchronized.Data type: String

</td></tr><tr id="reservation_sync_state_value-row"><td>

result.reservation.sync\_state.value

</td><td id="reservation_sync_state_value-entry">

Internal value of the current sync state of the reservation, such as synchronized.Data type: String

</td></tr><tr id="reservation_sys_created_on-row"><td>

result.reservation.sys\_created\_on

</td><td id="reservation_sys_created_on-entry">

Date and time when the reservation was created.Data type: String

</td></tr><tr id="reservation_sys_id-row"><td>

result.reservation.sys\_id

</td><td id="sys_id-reserv-entry">

Required. Sys\_id of the reservation record.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr id="reservation_sys_updated_on-row"><td>

Result.reservation.sys\_updated\_on

</td><td id="reservation_sys_updated_on-entry">

Date and time when the reservation was last updated. Data type: String

</td></tr><tr id="reservation_virtual_meeting-row"><td>

result.reservation.virtual\_meeting

</td><td id="reservation_virtual_meeting-entry">

URL of the virtual meeting link.Data type: String

</td></tr><tr><td>

result.reservationAcl

</td><td id="reservationAcl-reserv-entry">

Details of the user access control levels \(ACL\) checks set on the associated reservation.Data type: Object

```
"reservationAcl": {
  "read": Boolean,
  "write": {Object}
}
```

</td></tr><tr><td>

result.reservationAcl.read

</td><td id="reservationAcl_read-reserv-entry">

Flag that indicates whether to check if the user can read this reservation.Valid values:

-   true: Check if user can read the reservation.
-   false: Don't check if user can read the reservation.

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.write

</td><td id="reservationAcl_write-reserv-entry">

Details about the user's write capabilities for the associated reservation.Data type: Object

```
"write": {
  "allFields": Boolean,
  "fields": {Object},
  "record": Boolean
}
```

</td></tr><tr><td>

result.reservationAcl.write.allFields

</td><td id="reservationAcl_write_allFields-reserv-entry">

Flag that indicates whether to check if the user can write to all fields specified in the **reservationACL.write.fields** object. If the user only has access to some specific fields, then only those fields are true in the **reservationACL.write.fields** object.Valid values:

-   true: Check if user can write to all fields specified in the **reservationACL.write.fields** object.
-   false: Don't check if user can write to all fields specified in the **reservationACL.write.fields** object

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.write.fields

</td><td id="reservationAcl_write_fields-reserv-entry">

Details of the access controls on various fields of the reservation.Data type: Object

```
"fields": {
  "location": Boolean,
  "number_of_attendees": Boolean,
  "requested_for": Boolean,
  "sensitivity": Boolean,
  "subject": Boolean
}
```

</td></tr><tr><td>

result.reservationAcl.write.fields.location

</td><td id="reservationAcl_write_fields_location-reserv-entry">

Flag that indicates whether to check if the user can write to the location fields in this reservation.Valid values:

-   true: Check if user can write to the location fields.
-   false: Don't check if user can write to the location fields.

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.write.fields.​number\_of\_attendees

</td><td id="reservationAcl_write_fields_number_of_attendees-reserv-entry">

Flag that indicates whether to check if the user can write to the number of attendees fields in this reservation.Valid values:

-   true: Check if user can write to the number of attendees field.
-   false: Don't check if user can write to the number of attendees field.

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.write.fields.requested\_for

</td><td id="reservationAcl_write_fields_requested_for-reserv-entry">

Flag that indicates whether to check if the user can write to the requested for fields in this reservation.Valid values:

-   true: Check if user can write to the requested for field.
-   false: Don't check if user can write to the requested for field.

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.write.fields.sensitivity

</td><td id="reservationAcl_write_fields_sensitivity-reserv-entry">

Flag that indicates whether to check if the user can write to the sensitivity fields in this reservation.Valid values:

-   true: Check if user can write to the sensitivity field.
-   false: Don't check if user can write to the sensitivity field.

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.write.fields.subject

</td><td id="reservationAcl_write_fields_subject-reserv-entry">

Flag that indicates whether to check if the user can write to the subject fields in this reservation.Valid values:

-   true: Check if user can write to the subject field.
-   false: Don't check if user can write to the subject fields.

Data type: Boolean

</td></tr><tr><td>

result.reservationAcl.record

</td><td id="reservationAcl_write_fields_record-reserv-entry">

Flag that indicates whether to check if the user can write to the entire reservation record.Valid values:

-   true: Check if user can write to the entire reservation record.
-   false: Don't check if user can write to the entire reservation record.

Data type: Boolean

</td></tr><tr><td>

result.standard\_services

</td><td id="std_serv-reserv-entry">

Only populated if the **include\_standard\_services** parameter is set to true. Associated standard services, such as flip chart, projector screen, and whiteboard and markers.

Data type: Array of Objects

```
"standard_services": [
  {
    "font_awesome_icon": "String",
    "name": "String",
    "short_description": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.standard\_services.font\_awesome\_icon

</td><td id="std_serv_font-awesome_icon-reserv-entry">

Name of the thumbnail icon associated with the standard service.Data type: String

</td></tr><tr><td>

result.standard\_services.name

</td><td id="std_serv_name-reserv-entry">

Name of the standard service.Data type: String

</td></tr><tr><td>

result.standard\_services.short\_description

</td><td id="std_serv_short_description-reserv-entry">

Brief description of the standard service.Data type: String

</td></tr><tr><td>

result.standard\_services.sys\_id

</td><td id="std_serv_sys_id-reserv-entry">

Sys\_id of the standard service record.Data type: String

Table: Standard Service \[sn\_wsd\_rsv\_standard\_service\]

</td></tr></tbody>
</table>### cURL request

This code example shows how to call this endpoint to retrieve a list of reservations associated with the specified user.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/reservation/list" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "result": {
    "reservations": [
      {
      "sys_id": "12e2da5e87c701106342b846dabb354d",
      "number": "WRES0001010",
      "location": {
        "sys_id": "02000d4edb7650106c731dcd13961914",
        "name": "Eureka",
        "description": "A comfortable meeting room with leather chairs and a wooden table. Client meeting room.",
        "display_value": "Eureka",
        "capacity": 12,
        "label_value": "Room name",
        "email": "eureka@example.com",
        "reservable_module": {
          "sys_id": "c31241cedb7650106c731dcd13961917",
          "name": "Meeting rooms",
          "title": "Meeting rooms",
          "inline_title": "meeting room"
        },
        "region": {
          "sys_id": "2d626c4edb3650106c731dcd1396194b",
          "display_value": "Europe",
          "active": true
        },
        "site": {
          "sys_id": "b17220cedb3650106c731dcd1396197a",
          "display_value": "Western Europe",
          "active": true
        },
        "campus": {
          "sys_id": "44d2e0cedb3650106c731dcd13961988",
          "display_value": "Amsterdam Campus",
          "active": true
        },
        "building": {
          "sys_id": "9e0364cedb3650106c731dcd1396192b",
          "display_value": "AMS-B1",
          "active": true,
          "timezone": {
            "value": "Europe/Amsterdam",
            "displayValue": "Europe/Amsterdam"
          }
        },
        "floor": {
          "sys_id": "5373a8cedb3650106c731dcd1396198a",
          "display_value": "Floor 3",
          "active": true
        },
        "area": {
          "sys_id": "",
          "display_value": "",
          "active": false
        },
        "reservation": {
          "sys_id": "12e2da5e87c701106342b846dabb354d",
          "number_of_attendees": 1,
          "state": {
            "value": "confirmed",
            "display_value": "Confirmed"
          },
          "requested_for": {
            "sys_id": "2de07e1887cb89106342b846dabb35fe",
            "name": "Workplace User",
            "user_name": "workplace_user"
          },
          "number": "WRES0001010",
          "active": true
        },
        "number_of_attendees": 1,
        "state": {
          "value": "confirmed",
          "display_value": "Confirmed"
        },
        "number": "WRES0001010",
        "requested_for": {
          "sys_id": "2de07e1887cb89106342b846dabb35fe",
          "name": "Workplace User",
          "user_name": "workplace_user"
        }
      },
      "start": "2022-05-15T16:00:00Z",
      "end": "2022-05-15T17:00:00Z",
      "sys_created_on": "2022-04-26T09:19:37Z",
      "sys_updated_on": "2022-04-26T09:20:04Z",
      "source_reservation": null,
      "check_in_state": {
        "value": "not_required",
        "display_value": "Not required"
      },
      "external_id": null,
      "external_ical": null,
      "active": true,
      "state": {
        "value": "confirmed",
        "display_value": "Confirmed"
      },
      "sensitivity": {
        "value": "normal",
        "display_value": "Normal"
      },
      "reservation_type": {
        "value": "space",
        "display_value": "Space"
      },
      "reservation_subtype": {
        "value": "single",
        "display_value": "Single"
      },
      "reservation_purpose": {
        "value": "meeting",
        "display_value": "Meeting"
      },
      "attendees": [
        {
          "sys_id": "2de07e1887cb89106342b846dabb35fe",
          "value": "2de07e1887cb89106342b846dabb35fe",
          "displayValue": "Workplace User",
          "display_value": "Workplace User",
          "name": "Workplace User",
          "user_name": "workplace_user",
          "table": "sys_user",
          "avatar": "eb513744c3222010ae17dd981840dd97",
          "initials": "WU",
          "email": "workplace_user@example.com",
          "label": ""
        }
      ],
      "number_of_attendees": 1,
      "is_parent": false,
      "subject": "Add rsv_1",
      "virtual_meeting": "https://samplemeetingurl.com",
      "recording_details": [
        {
          "recording_url": "https://samplerecordingurl.com"
        }
      ],
      "sync_state": {
        "value": "not_required",
        "display_value": "Synchronization not required"
      },
      "sub_source": {
        "value": "servicenow_workplace_service_delivery",
        "display_value": "ServiceNow Workplace Service Delivery"
      },
      "last_updated_sub_source": {
        "value": "servicenow_workplace_service_delivery",
        "display_value": "ServiceNow Workplace Service Delivery"
      },
      "reservable_module": {
        "sys_id": "c31241cedb7650106c731dcd13961917",
        "name": "Meeting rooms",
        "title": "Meeting rooms",
        "inline_title": "meeting room",
        "font_awesome_icon": "fa-building",
        "reservable_table": "sn_wsd_core_room",
        "reservable_filter": "active=true^is_reservable=true^building!=6c0364cedb3650106c731dcd13961927^building.is_reservable=true^floor.is_reservable=true^EQ",
        "short_description": "Reserve a meeting room",
        "reservable_type": "location",
        "require_subject": "1",
        "require_cancel_notes": true,
        "virtual_meeting_provider": {
          "sys_id": "e33d9e6853c201103cf7ddeeff7b1205",
          "display_value": "Template"
        },
        "allow_invitees": "1",
        "display_number_of_attendees": "1",
        "display_on_behalf_of": "1",
        "display_sensitivity": "1",
        "max_days_in_future": "180",
        "allow_whole_day": "1",
        "selection_type": "unit",
        "reservable_container_field": null,
        "reservable_quantity_field": null,
        "apply_to_shift": null,
        "max_occurrences": "180",
        "enable_facet_filter": false,
        "search_limit": 10000,
        "enable_ical_generation": null,
        "enable_group_reservations": null,
        "enable_browse_near_a_person": "1",
        "enable_browse_by_area": "1",
        "display_value": "Meeting rooms",
        "browse_near_a_person_enabled": true,
        "browse_by_area_enabled": true,
        "reservable_columns": [
          "sys_id",
          "external_id",
          "email",
          "name",
          "title",
          "description",
          "image",
          "number",
          "site",
          "campus",
          "building",
          "floor",
          "area",
          "capacity",
          "reservable_quantity",
          "location_type",
          "order",
          "requires_check_in",
          "is_reservable"
        ],
        "layout_mapping": {
          "title": [
            "name"
          ],
          "description": [
            "description"
          ],
          "subtitle": [
            "campus",
            "building",
            "floor",
            "area"
          ],
          "subtitle_asc": [
            "area",
            "floor",
            "building",
            "campus"
          ],
          "image": "image",
          "body": [
            {
              "label": "Capacity",
              "icon": "fa-users",
              "field": "capacity",
              "field_to_display": ""
            },
            {
              "label": "Standard services",
              "icon": "fa-check",
              "field": "standard_services",
              "field_to_display": "name"
            },
            {
              "label": "Reservable purposes",
              "icon": "fa-tags",
              "field": "reservable_purposes",
              "field_to_display": "name"
            }
          ]
        },
        "timeSlots": [
          {
            "sys_id": "d5331cf2dbb5f01038e42b24ca961906",
            "name": "All day",
            "short_description": "8am - 6pm",
            "slot_start": "08:00",
            "slot_end": "18:00"
          }
        ],
        "buildingSysIds": [
          "4703a4cedb3650106c731dcd13961945",
          "6c0364cedb3650106c731dcd13961927",
          "94e264cedb3650106c731dcd13961919",
          "9e0364cedb3650106c731dcd1396192b"
        ],
        "reservable_views": [
          {
            "type": "card",
            "label": "Card view",
            "iconClass": "fa-th-large",
            "isDefault": true,
            "order": "1"
          },
          {
            "type": "schedule",
            "label": "Schedule view",
            "iconClass": "fa-calendar-o",
            "isDefault": false,
            "order": "2"
          }
        ],
        "checkin_before_minutes": 30,
        "reservation_paths": [
          {
            "value": "browse_all",
            "displayValue": "Browse all"
          },
          {
            "value": "browse_near_a_person",
            "displayValue": "Browse near a person"
          },
          {
            "value": "browse_by_area",
            "displayValue": "Browse by area"
          }
        ],
        "override_approval_policy": "never_required"
      },
      "notification_recipients": [
        {
          "sys_id": "7016f79cc0a8016401c5a33be04be441",
          "name": "workplace user",
          "user_name": "workplace.user"
        }
      ],
      "notification_custom_message": "Demo notification message",
      "opened_by": {
        "sys_id": "6816f79cc0a8016401c5a33be04be441",
        "value": "6816f79cc0a8016401c5a33be04be441",
        "displayValue": "System Administrator",
        "display_value": "System Administrator",
        "name": "System Administrator",
        "user_name": "admin",
        "table": "sys_user",
        "avatar": "eb513744c3222010ae17dd981840dd97",
        "initials": "SA",
        "email": "admin@example.com",
        "label": "System Administrator"
      },
      "requested_for": {
        "sys_id": "2de07e1887cb89106342b846dabb35fe",
        "value": "2de07e1887cb89106342b846dabb35fe",
        "displayValue": "Workplace User",
        "display_value": "Workplace User",
        "name": "Workplace User",
        "user_name": "workplace_user",
        "table": "sys_user",
        "avatar": "d3513744c3222010ae17dd981840dd97",
        "initials": "WU",
        "email": "workplace_user@example.com",
        "label": ""
      },
      "edit_restriction": {
        "value": "no_restriction",
        "display_value": "No restriction"
      },
      "source": {
        "value": "servicenow",
        "display_value": "Workplace Services"
      },
      "source_icon": {
        "classNames": "fa fa-calendar-check-o",
        "tooltip": "Reservation is confirmed",
        "imgSrc": ""
      },
      "shift": {
        "sys_id": "e5d23acfdb42a01097acc9003996193a",
        "name": "Test shift AMS-B1",
        "display_value": "Test shift AMS-B1",
        "shiftDetails": "8-5 weekdays excluding holidays\n  - Monday-Friday 8-5"
      },
      "reservationAcl": {
        "write": {
          "record": true,
          "fields": {
            "subject": true,
            "sensitivity": true,
            "requested_for": true,
            "number_of_attendees": true,
            "location": true
          },
          "allFields": true
        },
        "read": true
      }
      }
     ]
   }
}
```

## WSD Reservation - PATCH /api/sn\_wsd\_rsv/reservation/cancel/\{sys\_id\}

Cancels a specified workplace reservation.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/reservation/cancel/{sys_id}`

Default URL: `/api/sn_wsd_rsv/reservation/cancel/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the reservation to cancel.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cancel\_notes

</td><td>

Reason for cancelling the reservation.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-reserv-entry">

Data format of the request body. Supported types: **application/json**, **application/xml** or, **text/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

Sys\_id of the cancelled reservation record.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table>### cURL request

The following code example shows how to cancel a reservation using this endpoint.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/reservation/cancel/12e2da5e87c701106342b846dabb354d" \
--request PATCH \
--header "Accept:application/json" \
--user ‘username’:’password’

```

Return results:

```
"result": {
  "sys_id": "73c316d2474b0150003a4587746d4337"
}
```

## WSD Reservation - PATCH /api/sn\_wsd\_rsv/reservation/share\_details/\{sys\_id\}

Updates and shares the reservation details with a specified list of recipients through an email notification. Optionally you can send a specified message along with the reservation.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/reservation/share_details/{sys_id}`

Default URL: `/api/sn_wsd_rsv/reservation/share_details/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the reservation to share.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

notification\_custom\_message

</td><td>

Message to send to the specified recipients.Data Type: String

</td></tr><tr><td>

notification\_recipients

</td><td>

Required. List of sys\_ids of the users to send the email notification to.Data Type: Array

Table: User \[sys\_user\]

</td></tr><tr><td>

notification\_type

</td><td>

Type of notification to send.Valid types:

-   reservation\_cancelled
-   reservation\_created
-   reservation\_updated

Data Type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-reserv-entry">

Data format of the request body. Supported types: **application/json**, **application/xml** or, **text/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

Sys\_id of the reservation record that was shared.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table>### cURL request

The following code example shows how to use this endpoint to share a reservation.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/reservation/share_details/60d26a0f47578910003a4587746d4331" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
\"notification_recipients\": [\"5dfb9fcf47d78910003a4587746d4367\"],
\"notification_type\":\"reservation_updated\",
\"notification_custom_message\": \"Please join our design brainstorming meeting!\"
}" \
--user "username":"password"
```

Return results:

```
"result": {
  "sys_id": "60d26a0f47578910003a4587746d4331"
}
```

## WSD Reservation - PATCH /api/sn\_wsd\_rsv/reservation/update/\{sys\_id\}

Updates a specified workplace reservation.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/reservation/update/{sys_id}`

Default URL: `/api/sn_wsd_rsv/reservation/update/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the reservation to modify.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ignore\_same\_day\_validation

</td><td id="ignore_same_day_validation-reserv-entry">

Flag that indicates whether the reservation search ignores the change of the date validation between the start and end parameters.Valid values:

-   true: Ignore the change date validation.
-   false: Don't ignore the change date validation.

Data type: Boolean

Default: false

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

end

</td><td id="end-update_reserv-entry">

Required if the **shift** parameter isn't passed in. Requested end time of the reservation.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr><td>

is\_private

</td><td id="is_private-update_reserv-entry">

Flag that indicates whether the reservation is private. If private, the reservation doesn't appear to anyone except the owner.For additional information on these privacy settings, see [Location privacy settings and impact](https://www.servicenow.com/docs/access?context=location-privacy-settings-and-impact&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Valid values:

-   true: Reservation is private.
-   false: Reservation isn't private.

Data type: Boolean

Default: Value set for privacy in the system properties.

</td></tr><tr><td>

location

</td><td id="location-update_reserv-entry">

Required. Sys\_id of the location to reserve.

Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

requested\_for

</td><td id="requested_for-update_reserv-entry">

Sys\_id or email address of the user for which the reservation is being made.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

shift

</td><td id="shift-update_reserv-entry">

Sys\_id of the shift to associate with the reservation. If this parameter is passed in, the **end** parameter isn't required.

For additional information on shift-based reservations, see [Enable shift-based reservation](https://www.servicenow.com/docs/access?context=wsd-reservation-setup&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Data type: String

Table: Shift \[sn\_wsd\_core\_shift\]

</td></tr><tr><td>

start

</td><td id="start-update_reserv-entry">

Required. Requested start time of the reservation.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr><td>

subject

</td><td id="subject-update_reserv-entry">

Required. Subject of the meeting associated with the reservation.

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-reserv-entry">

Data format of the request body. Supported types: **application/json**, **application/xml** or, **text/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details of the updated reservation.Data type: Object

```
"result": {
  "location_id": "String",
  "sys_id": "String",
  "type_of_change": "String"
}
```

</td></tr><tr><td>

result.location\_id

</td><td>

Sys\_id of the reservation location record.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the modified reservation record.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.type\_of\_change

</td><td>

Type of information updated in the reservation.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to update a reservation using this endpoint.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/reservation/update/b537abc947db4510003a4587746d4351" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
\"subject\": \"Rsv Update_1\",
\"start\": \"2022-07-21 14:00:00\",
\"end\": \"2022-07-21 15:00:00\",
\"requested_for\": \"workplace_user@example.com\",
\"workplace_location\": \"fe1f744edb7650106c731dcd139619ca\",
\"is_private\": \false\
}" \
--user "username":"password"
```

Return results:

```
{
  "result": {
    "sys_id": "b537abc947db4510003a4587746d4351",
    "location_id": "fe1f744edb7650106c731dcd139619ca",
    "type_of_change": "location"
  }
}
```

## WSD Reservation - POST /api/sn\_wsd\_rsv/reservation/add

Creates a new workplace reservation.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/reservation/add`

Default URL: `/api/sn_wsd_rsv/reservation/add`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ignore\_same\_day\_validation

</td><td id="ignore_same_day_validation-reserv-entry">

Flag that indicates whether the reservation search ignores the change of the date validation between the start and end parameters.Valid values:

-   true: Ignore the change date validation.
-   false: Don't ignore the change date validation.

Data type: Boolean

Default: false

</td></tr><tr><td>

timezone

</td><td>

Preferred time zone for performing the request validations. For example: Europe/Amsterdam. This validation checks whether the start and end time fall on the same day. Data type: String

Default: User time zone

</td></tr></tbody>
</table><table id="id_vh4_gxy_stb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="end-update_reserv-row"><td>

end

</td><td id="end-update_reserv-entry">

Required if the **shift** parameter isn't passed in. Requested end time of the reservation.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr id="is_private-update_reserv-row"><td>

is\_private

</td><td id="is_private-update_reserv-entry">

Flag that indicates whether the reservation is private. If private, the reservation doesn't appear to anyone except the owner.For additional information on these privacy settings, see [Location privacy settings and impact](https://www.servicenow.com/docs/access?context=location-privacy-settings-and-impact&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Valid values:

-   true: Reservation is private.
-   false: Reservation isn't private.

Data type: Boolean

Default: Value set for privacy in the system properties.

</td></tr><tr id="location-update_reserv-row"><td>

location

</td><td id="location-update_reserv-entry">

Required. Sys\_id of the location to reserve.

Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr id="requested_for-update_reserv-row"><td>

requested\_for

</td><td id="requested_for-update_reserv-entry">

Sys\_id or email address of the user for which the reservation is being made.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="reservable_module-update_reserv-row"><td>

reservable\_module

</td><td id="reservable_module-update_reserv-entry">

Required. Sys\_id of the reservable module to associate with the reservation. A [reservable module](https://www.servicenow.com/docs/access?context=config-reservable-module&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) defines the workplace items needed for a reservation.Data type: String

Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

</td></tr><tr id="shift-update_reserv-row"><td>

shift

</td><td id="shift-update_reserv-entry">

Sys\_id of the shift to associate with the reservation. If this parameter is passed in, the **end** parameter isn't required.

For additional information on shift-based reservations, see [Enable shift-based reservation](https://www.servicenow.com/docs/access?context=wsd-reservation-setup&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Data type: String

Table: Shift \[sn\_wsd\_core\_shift\]

</td></tr><tr id="start-update_reserv-row"><td>

start

</td><td id="start-update_reserv-entry">

Required. Requested start time of the reservation.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr id="subject-update_reserv-row"><td>

subject

</td><td id="subject-update_reserv-entry">

Required. Subject of the meeting associated with the reservation.

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-reserv-entry">

Data format of the request body. Supported types: **application/json**, **application/xml** or, **text/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

Sys\_id of the created reservation record.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table>### cURL request

The following code example shows how to use this endpoint to create a reservation.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/reservation/add" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"reservable_module\": \"c31241cedb7650106c731dcd13961917\",
  \"subject\": \"Test-123\",
  \"reservation_purpose\": \"meeting\",
  \"timezone\": \"US/Pacific\",
  \"requested_for\": \"6816f79cc0a8016401c5a33be04be441\",
  \"location\": \"5eafb44edb7650106c731dcd13961943\",
  \"is_private\": false,
  \"start\": \"2023-01-12T11:00:00Z\",
  \"end\": \"2023-01-12T12:00:00Z\"
}" \
--user "username":"password"
```

Return results:

```
"result": {
  "sys_id": "4b036a9e474b0150003a4587746d43b1"
}
```

## WSD Reservation - POST /api/sn\_wsd\_rsv/reservation/quick\_reserve

Creates a new workplace reservation using quick reserve.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/reservation/quick_reserve`

Default URL: `/api/sn_wsd_rsv/reservation/quick_reserve`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

end

</td><td id="end-update_reserv-entry">

Required if the **shift** parameter isn't passed in. Requested end time of the reservation.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr><td>

ignore\_same\_day\_validation

</td><td>

Required. Flag that indicates whether the endpoint ignores the validation of the change of date between the **start** and **end** parameters. Valid values:

-   true: Ignore the change date validation. Set this to true when the start and end dates are the same.
-   false: Do not ignore the change date validation.

Data type: Boolean

</td></tr><tr><td>

reference\_location\_id

</td><td>

Required. Sys\_id of the location, near to which, the user wants to reserve a location.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

reservable\_module

</td><td id="reservable_module-update_reserv-entry">

Required. Sys\_id of the reservable module to associate with the reservation. A [reservable module](https://www.servicenow.com/docs/access?context=config-reservable-module&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) defines the workplace items needed for a reservation.Data type: String

Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

</td></tr><tr><td>

shift

</td><td id="shift-update_reserv-entry">

Sys\_id of the shift to associate with the reservation. If this parameter is passed in, the **end** parameter isn't required.

For additional information on shift-based reservations, see [Enable shift-based reservation](https://www.servicenow.com/docs/access?context=wsd-reservation-setup&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Data type: String

Table: Shift \[sn\_wsd\_core\_shift\]

</td></tr><tr><td>

start

</td><td id="start-update_reserv-entry">

Required. Requested start time of the reservation.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-reserv-entry">

Data format of the request body. Supported types: **application/json**, **application/xml** or, **text/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

Sys\_id of the created reservation record.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table>### cURL request

The following code example shows how to use the quick reserve endpoint to create a reservation.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/reservation/quick_reserve" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"start\":\"2022-05-23 16:00:00\",
  \"end\": \"2022-05-23 17:00:00\",
  \"reservable_module\": \"5db44502dbb650106c731dcd13961937\",
  \"reference_location_id\": \"05f5290edb7210106c731dcd13961951\",
  \"ignore_same_day_validation\": \"true\"
}" \
--user "username":"password"
```

Return results:

```
"result": {
  "sys_id": "4b036a9e474b0150003a4587746d43b1"
}
```

