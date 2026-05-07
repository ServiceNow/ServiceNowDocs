---
title: WSD Recurring Reservation API
description: The Workplace Service Delivery \(WSD\) Recurring Reservation API provides endpoints for managing reservations that occur at the same time, but have different dates.Returns the specified recurring reservation.Cancels an entire specified recurring series reservation or a specific meeting occurrence within the series.Creates workplace reservations for the same time but different dates, such as weekly, monthly, or every other week.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 43
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD Recurring Reservation API

The Workplace Service Delivery \(WSD\) Recurring Reservation API provides endpoints for managing reservations that occur at the same time, but have different dates.

To access this API, the caller must have the sn\_wsd\_core.workplace\_user role and the Workplace Safety Management \(sn\_wsd\_core\) and Workplace Reservation Management \(sn\_wsd\_rsv\) plugins must be activated.

This API runs in the `sn_wsd_rsv` namespace.

For additional information on Workplace Reservation Management, see [Workplace Reservation Management](https://www.servicenow.com/docs/access?context=workplace-rsv-mgmt-feat&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD Recurring Reservation - GET /api/sn\_wsd\_rsv/recurring\_reservation/list/\{parent\_id\}

Returns the specified recurring reservation.

If more than six recurring meeting occurrences are available for the reservation, you can paginate through the occurrences using the query parameters. You can also specify occurrence records not to return.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/recurring_reservation/list/{parent_id}`

Default URL: `/api/sn_wsd_rsv/recurring_reservation/list/{parent_id}`

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

parent\_id

</td><td>

Sys\_id of the recurring parent reservation record.When a recurring reservation is created, one recurring parent record and one or more child reservation records are created. Reservation records contain a field called reservation\_subtype, that indicates the type of reservation record. For recurring parent records, this field is set to "Recurring parent". For child records, this field is set to "Occurrence".

Within a child record, the sys\_id of the associated recurring parent record is in the source\_reservation field.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

end\_index

</td><td>

When paginating through a recurring record set, the zero-based record number at which to stop returning occurrence records.**Note:** If the number of recurring occurrences is less than six the endpoint returns all of the occurrences, otherwise it returns the first six occurrences. To retrieve the occurrences beyond six, you must pass the end\_index parameter accordingly.

Data type: Number

</td></tr><tr><td>

occurrence\_sys\_id

</td><td>

Sys\_id of an occurrence record in the recurring series not to return.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

start\_index

</td><td>

When paginating through a recurring record set, the zero-based record number at which to start returning occurrence records.Data type: Number

Default: 0

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

Return results for the requested recurring reservation.Data type: Object

```
"result": {
  "occurencesTotalCount": "String",
  "reservation": {Object}
}
```

</td></tr><tr><td>

result.occurencesTotalCount

</td><td>

Total number of meeting occurrences in the recurring series.Data type: String

</td></tr><tr><td>

result.reservation

</td><td>

Details about the requested recurring reservation.Data type: Object

```
"reservation": {
  "active": Boolean,
  "attendees": [Array],
  "check_in_state": {Object},
  "edit_restriction": {Object},
  "end": "String",
  "external_ical": "String",
  "external_id": "String",
  "is_parent": Boolean,
  "last_updated_sub_source": {Object},
  "location": {Object},
  "notification_custom_message": "String",
  "notification_recipients": [Array],
  "number": "String",
  "number_of_attendees": Number,
  "opened_by": {Object},
  "recording_details": [Array],
  "recurring_pattern": {Object},
  "requested_for": {Object},
  "reservable_module": {Object},
  "sensitivity": {Object},
  "shift": {Object},
  "source": {Object},
  "source_icon": {Object},
  "source_reservation": {Object},
  "source_reservation_requester": {Object},
  "start": "String",
  "state": {Object},
  "subject": "String",
  "sub_source": {Object},
  "sync_state": {Object},
  "sys_created_on": "String",
  "sys_id": "String",
  "sys_updated_on": "String",
  "virtual_meeting": "String"
}
```

</td></tr><tr><td>

result.reservation.active

</td><td id="reservation_active-reserv-entry">

Flag that indicates whether the reservation is active.Valid values:

-   true: Reservation is active.
-   false: Reservation is inactive.

Data type: Boolean

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.attendees.avatar

</td><td id="reservation_attendees_avatar-reserv-entry">

Sys\_id of the avatar associated with the attendee.Data type: String

Table: Attachments \[sys\_attachment\]

</td></tr><tr><td>

result.reservation.attendees.displayValue

</td><td id="reservation_attendees_displayValue-reserv-entry">

Display value for the attendee.Data type: String

</td></tr><tr><td>

result.reservation.attendees.display\_value

</td><td id="reservation_attendees_display_value-reserv-entry">

Display value of the attendee. Same as **displayValue**.Data type: String

</td></tr><tr><td>

result.reservation.attendees.email

</td><td id="reservation_attendees_mail-reserv-entry">

Attendee's email address.Data type: String

</td></tr><tr><td>

result.reservation.attendees.initials

</td><td id="reservation_attendees_initials-reserv-entry">

Attendee's initials.Data type: String

</td></tr><tr><td>

result.reservation.attendees.name

</td><td id="reservation_attendees_name-reserv-entry">

Attendee's name.Data type: String

</td></tr><tr><td>

result.reservation.attendees.sys\_id

</td><td id="reservation_attendees_sys_id-reserv-entry">

Sys\_id of the attendee record.Data type: String

</td></tr><tr><td>

result.reservation.attendees.table

</td><td id="reservation_attendees_table-reserv-entry">

Table in which the attendee record exists.Data type: String

</td></tr><tr><td>

result.reservation.attendees.user\_name

</td><td id="reservation_attendees_user_name-reserv-entry">

Attendee's user name.Data type: String

</td></tr><tr><td>

result.reservation.attendees.value

</td><td id="reservation_attendees_value-reserv-entry">

Internal value of the attendee.Data type: String

</td></tr><tr><td>

result.reservation.check\_in\_state

</td><td id="reservation_attendees_check_in_state-reserv-entry">

Details about the check-in state of the reservation.Data type: Object

```
"check_in_state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservation.check\_in\_state.​display\_value

</td><td id="reservation_attendees_check_in_state_display_value-reserv-entry">

Display value for the current check-in state of the reservation, such as In progress or complete.Data type: String

</td></tr><tr><td>

result.reservation.check\_in\_state.value

</td><td id="reservation_attendees_check_in_state_value-reserv-entry">

Internal value for the current check-in state of the reservation, such as 2.Data type: String

</td></tr><tr><td>

result.reservation.edit\_restriction

</td><td id="reservation_attendees_edit_restriction-reserv-entry">

Description of the user edit restrictions for the reservation, such as no\_restrictions, service\_only, or fully\_restricted.Data type: Object

```
"edit_restriction": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservation.edit\_restriction.display\_​value

</td><td id="reservation_attendees_edit_restriction_display_value-reserv-entry">

Display value for the edit restrictions for the reservation, such as `No restriction`.Data type: String

</td></tr><tr><td>

result.reservation.edit\_restriction.value

</td><td id="reservation_attendees_edit_restriction_value-reserv-entry">

Internal value for the edit restrictions for the reservation, such as `no_restriction`.Data type: String

</td></tr><tr><td>

result.reservation.end

</td><td id="end-reserv-entry">

Reservation end date and time.Data type: String

Format: UTC: yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr><td>

result.reservation.external\_ical

</td><td id="reservation_external_ical-reserv-entry">

Unique external iCalendar identification of the reservation. Use this value to identify the reservation when this is a calendar sync related reservation.Data type: String

</td></tr><tr><td>

result.reservation.external\_id

</td><td id="reservation_external_id-reserv-entry">

Unique external identification of the reservation. Use this value to identify the reservation when this is a calendar sync related reservation.Data type: String

</td></tr><tr><td>

result.reservation.is\_parent

</td><td id="reservation_is_parent-reserv-entry">

Flag that indicates whether this reservation is a parent reservation.Possible values:

-   true: Parent reservation.
-   false: Not a parent reservation.

Data type: Boolean

</td></tr><tr><td>

result.reservation.last\_updated\_sub\_source

</td><td id="reservation_last_updated_sub_source-reserv-entry">

Details about the last updated sub-source for the reservation. Sub-sources are used when integrating reservations with an external calendar. This object contains information such as "servicenow\_workplace\_service\_delivery", "google\_calendar", or "microsoft\_exchange".Data type: Object

```
"last_updated_sub_source": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservation.last\_updated\_sub\_source.​display\_value

</td><td id="reservation_last_updated_sub_source_display_value-reserv-entry">

Display value for the last updated sub-source of the reservation, such as `ServiceNow Workplace Service Delivery` or `Google Calendar`. Used when integrating the reservation with an outside service such as Google calendar or Microsoft Outlook.Data type: String

</td></tr><tr><td>

result.reservation.last\_updated\_sub\_source.​value

</td><td id="reservation_last_updated_sub_source_value-reserv-entry">

Internal value for the last updated sub-source of the reservation, such as `servicenow_workplace_service_delivery` or `google_calendar`. Used when integrating the reservation with an outside service such as Google calendar or Microsoft Outlook.Data type: String

</td></tr><tr><td>

result.reservation.location

</td><td>

Details about the location associated with the reservation.Data type: Object

```
"location": {
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
  "number": "String",
  "number_of_attendees": Boolean,
  "region": {Object},
  "requested_for": {Object},
  "reservable_module": {Object},
  "reservation": {Object},
  "site": {Object},
  "state": {Object},
  "sys_id": "String"
}
```

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.location.area.active

</td><td id="reservation_location_area_active-reserv-entry">

Flag that indicates whether the area is active.Valid values:

-   true: Area is active.
-   false: Area is inactive.

Data type: Boolean

</td></tr><tr><td>

result.reservation.location.area.display\_value

</td><td id="reservation_location_area_display_value-reserv-entry">

Display value of the area to which this location belongs, such as Desk A2.Data type: String

</td></tr><tr><td>

result.reservation.location.area.sys\_id

</td><td id="reservation_location_area_sys_id-reserv-entry">

Sys\_id of the area to which this location belongs.Data type: String

Table: Area \[sn\_wsd\_core\_area\]

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.location.building.active

</td><td id="reservation_location_building_active-reserv-entry">

Flag that indicates whether the building is active.Valid values:

-   true: Building is active.
-   false: Building is inactive.

Data type: Boolean

</td></tr><tr><td>

result.reservation.location.building.​display\_value

</td><td id="reservation_location_building_display_value-reserv-entry">

Display value of the building to which this location belongs, such as AMS - Bld1.Data type: String

</td></tr><tr><td>

result.reservation.location.building.sys\_id

</td><td id="reservation_location_building_sys_id-reserv-entry">

Sys\_id of the building to which this location belongs.Data type: String

Table: Building \[sn\_wsd\_core\_building\]

</td></tr><tr><td>

result.reservation.location.building.timezone

</td><td>

Details of the time zone for the building.Data type: Object

```
"timezone": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservation.location.building.timezone.​display\_value

</td><td>

Display value of the time zone in which the associated building resides.Data type: String

</td></tr><tr><td>

result.reservation.location.building.timezone.​value

</td><td>

Internal value for the time zone to which this location belongs.Data type: String

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.location.campus.active

</td><td id="reservation_location_campus_active-reserv-entry">

Flag that indicates whether the campus is active.Valid values:

-   true: Campus is active.
-   false: Campus is inactive.

Data type: Boolean

</td></tr><tr><td>

result.reservation.location.campus.​display\_value

</td><td id="reservation_location_campus_display_value-reserv-entry">

Display value of the campus to which this location belongs, such as Amsterdam Campus.Data type: String

</td></tr><tr><td>

result.reservation.location.campus.sys\_id

</td><td id="reservation_location_campus_sys_id-reserv-entry">

Sys\_id of the campus to which this location belongs.Data type: String

Table: Campus \[sn\_wsd\_core\_campus\]

</td></tr><tr><td>

result.reservation.location.capacity

</td><td id="reservation_location_capacity-reserv-entry">

Maximum number of occupants for the location.Data type: Number

</td></tr><tr><td>

result.reservation.location.description

</td><td id="reservation_location_description-reserv-entry">

Brief description of the location.Data type: String

</td></tr><tr><td>

result.reservation.location.display\_value

</td><td id="reservation_location_display_value-reserv-entry">

Value to display in the UI for this location.Data type: String

</td></tr><tr><td>

result.reservation.location.email

</td><td id="reservation_location_email-reserv-entry">

Email address for the location.Data type: String

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.location.floor.active

</td><td id="reservation_location_floor_active-reserv-entry">

Flag that indicates whether the floor is active.Valid values:

-   true: Floor is active.
-   false: Floor is inactive.

Data type: Boolean

</td></tr><tr><td>

result.reservation.location.floor.display\_value

</td><td id="reservation_location_floor_display_value-reserv-entry">

Display value of the floor to which this location belongs, such as First floor.Data type: String

</td></tr><tr><td>

result.reservation.location.floor.sys\_id

</td><td id="reservation_location_floor_sys_id-reserv-entry">

Sys\_id of the floor to which this location belongs.Data type: String

Table: Floor \[sn\_wsd\_core\_floor\]

</td></tr><tr><td>

result.reservation.location.label\_value

</td><td id="reservation_location_floor_label_value-reserv-entry">

Type of value specified in the **name** parameter, such as Room name.Data type: String

</td></tr><tr><td>

result.reservation.location.name

</td><td id="reservation_location_floor_name-reserv-entry">

Name of the location.Data type: String

</td></tr><tr><td>

result.reservation.location.number

</td><td id="reservation_location_floor_number-reserv-entry">

Reservation number.Data type: String

</td></tr><tr><td>

result.reservation.location.number\_of\_​attendees

</td><td id="reservation_location_number_of_attendees-reserv-entry">

Number of attendees for the reservation.Data type: Number

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.location.reservable\_module.​inline\_title

</td><td id="reservation_location_reservable_module_inline_title-reserv-entry">

Inline title of the reservable module. The title appears in line with the descriptive text on the Workplace service portal.Data type: String

</td></tr><tr><td>

result.reservation.location.reservable\_module.​name

</td><td id="reservation_location_reservable_module_name-reserv-entry">

Name of the reservable module.Data type: String

</td></tr><tr><td>

result.reservation.location.reservable\_module.​sys\_id

</td><td id="reservation_location_reservable_module_sys_id-reserv-entry">

Sys\_id of the reservable module.Data type: String

</td></tr><tr><td>

result.reservation.location.reservable\_module.​title

</td><td id="reservation_location_reservable_module_title-reserv-entry">

Title of the reservable module.Data type: String

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.location.region.active

</td><td id="reservation_location_region_active-reserv-entry">

Flag that indicates whether the region is active.Valid values:

-   true: Region is active.
-   false: Region is inactive.

Data type: Boolean

</td></tr><tr><td>

result.reservation.location.region.​display\_value

</td><td id="reservation_location_region_display_value-reserv-entry">

Display value of the region to which this location belongs, such as Europe.Data type: String

</td></tr><tr><td>

result.reservation.location.region.sys\_id

</td><td id="reservation_location_region_sys_id-reserv-entry">

Sys\_id of the region to which this location belongs.Data type: String

Table: Region \[sn\_wsd\_core\_region\]

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.location.reservation.active

</td><td id="reservation_location_reservation_active-reserv-entry">

Flag that indicates whether the reservation is active.Valid values:

-   true: Reservation is active.
-   false: Reservation is inactive.

Data type: Boolean

</td></tr><tr><td>

result.reservation.location.reservation.number

</td><td id="reservation_location_reservation_number-reserv-entry">

Reservation number.Data type: String

</td></tr><tr><td>

result.reservation.location.reservation.​number\_of\_attendees

</td><td id="reservation_location_reservation_number_of_attendees-reserv-entry">

Number of attendees of the reservation.Data type: Number

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.location.reservation.​requested\_for.name

</td><td id="reservation_location_reservation_requested_for_name-reserv-entry">

Name of the user for whom the reservation was requested for.Data type: String

</td></tr><tr><td>

result.reservation.location.reservation.​requested\_for.sys\_id

</td><td id="reservation_location_reservation_requested_for_sys_id-reserv-entry">

Sys\_id of the requested for user.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

result.reservation.location.reservation.​requested\_for.user\_name

</td><td id="reservation_location_reservation_requested_for_user_name-reserv-entry">

User name of the user for whom the reservation was requested for.Data type: String

</td></tr><tr><td>

result.reservation.location.reservation.​state

</td><td>

Details about the state of the reservation for the location.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservation.location.reservation.​.state.display\_value

</td><td>

Display value for the current state of the reservation, such as confirmed.Data type: String

</td></tr><tr><td>

result.reservation.location.reservation.​.state.value

</td><td>

Internal value for the current state of the reservation, such as 2.Data type: String

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.location.site.active

</td><td id="reservation_location_site_active-reserv-entry">

Flag that indicates whether the site is active.Valid values:

-   true: Site is active.
-   false: Site is inactive.

Data type: Boolean

</td></tr><tr><td>

result.reservation.location.site.display\_value

</td><td id="reservation_location_site_display_value-reserv-entry">

Display value of the site to which this location belongs, such as Western Europe.Data type: String

</td></tr><tr><td>

result.reservation.location.site.sys\_id

</td><td id="reservation_location_site_sys_id-reserv-entry">

Sys\_id of the site to which this location belongs.Data type: String

Table: Site \[sn\_wsd\_core\_site\]

</td></tr><tr><td>

result.reservation.location.standard\_services

</td><td>

Standard available services.Data type: String

</td></tr><tr><td>

result.reservation.location.state

</td><td id="state-reserv-entry">

Details about the state of the reservation for the location.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservation.location.state.display\_value

</td><td id="d3222e4997">

Display value for the current state of the reservation, such as confirmed.Data type: String

</td></tr><tr><td>

result.reservation.location.state.value

</td><td id="d3222e5008">

Internal value for the current state of the reservation, such as 2.Data type: String

</td></tr><tr><td>

result.reservation.location.sys\_id

</td><td id="location_sys_id-reserv-entry">

Sys\_id of the associated location record.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.reservation.notification\_custom\_​message

</td><td id="reservation_notification_custom_message-reserv-entry">

Custom message for the notification sent to the recipients listed in **reservation.notification\_recipients**.Data type: String

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.notification\_recipients.name

</td><td id="reservation_notification_recipients_name-reserv-entry">

Name of the recipient.Data type: String

</td></tr><tr><td>

result.reservation.notification\_recipients.sys\_id

</td><td id="reservation_notification_recipients_sys_id-reserv-entry">

Sys\_id of the recipient.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

result.reservation.notification\_recipients.​user\_name

</td><td id="reservation_notification_recipients_user_name-reserv-entry">

User name of the recipient.Data type: String

</td></tr><tr><td>

result.reservation.number

</td><td id="reservation_number-reserv-entry">

Unique number of the reservation record. You can use this value to query the reservation.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.reservation.number\_of\_attendees

</td><td id="reservation_number_of_attendees-reserv-entry">

Number of attendees in this reservation.Data type: Number

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.opened\_by.avatar

</td><td id="reservation_opened_by_avatar-reserv-entry">

Avatar for the user that opened the reservation.Data type: String

</td></tr><tr><td>

result.reservation.opened\_by.displayValue

</td><td id="reservation_opened_by_displayValue-reserv-entry">

Display value of the opened by user.Data type: String

</td></tr><tr><td>

result.reservation.opened\_by.display\_value

</td><td id="reservation_opened_by_display_value-reserv-entry">

Display value of the opened by user.Data type: String

</td></tr><tr><td>

result.reservation.opened\_by.email

</td><td id="reservation_opened_by_email-reserv-entry">

Email address for the user that opened the reservation.Data type: String

</td></tr><tr><td>

result.reservation.opened\_by.initials

</td><td id="reservation_opened_by_initials-reserv-entry">

Initials of the user that opened the reservation.Data type: String

</td></tr><tr><td>

result.reservation.opened\_by.name

</td><td id="reservation_opened_by_name-reserv-entry">

Name of the user that opened the reservation.Data type: String

</td></tr><tr><td>

result.reservation.opened\_by.user\_name

</td><td id="reservation_opened_by_user_name-reserv-entry">

User name of the user that opened the reservation.Data type: String

</td></tr><tr><td>

result.reservation.opened\_by.value

</td><td id="reservation_opened_by_value-reserv-entry">

Internal value of the user that opened the reservation.Data type: String

</td></tr><tr><td>

result.reservation.recording\_details

</td><td id="reservation_recording_details-reserv-entry">

Details about the recordings associated with the reservation \(meeting\).Data type: Array of Objects

```
"recording_details": [
  "recording_url": "String"
]
```

</td></tr><tr><td>

result.reservation.recording\_details.​recording\_url

</td><td id="reservation_recording_details_recording_url-reserv-entry">

URL of the recordings associated with the reservation.Data type: String

</td></tr><tr><td>

result.reservation.recurring\_pattern

</td><td>

Details about the recurring pattern for the reservation.Data type: Object

```
"recurring_pattern": {
  "amountOfDates": "String",
  "duration": Number,
  "label": "String",
  "options": {Object},
  "repeats": "String",
  "startDate":"String",
  "startDateGdt": {Object}
}
```

</td></tr><tr><td>

result.reservation.recurring\_pattern.​amountOfDates

</td><td>

Number of dates for which the reservables are reserved.Data type: String

</td></tr><tr><td>

result.reservation.recurring\_pattern.duration

</td><td>

Length of time to reserve the reservable.

Data type: Number

Unit: Seconds

</td></tr><tr><td>

result.reservation.recurring\_pattern.label

</td><td>

Descriptive name for the recurring reservation.Data type: String

</td></tr><tr><td>

result.reservation.recurring\_pattern.options

</td><td>

Details about the options associated with the recurring reservation.Data type: Object

```
"options": {
  "count": Number,
  "daysOfWeek": "String",
  "every": Number,
  "endDate": "String"
  "endDateGdt": {Object}
}
```

</td></tr><tr><td>

result.reservation.recurring\_pattern.options.​count

</td><td>

Number of times to repeat the pattern.

Data type: Number

</td></tr><tr><td>

result.reservation.recurring\_pattern.options.​daysOfWeek

</td><td>

Days of the week that the reservable is needed.

Valid values:

-   1 = Monday
-   2 = Tuesday
-   3 = Wednesday
-   4 = Thursday
-   5 = Friday
-   6 = Saturday
-   7 = Sunday

For example, to specify Tuesday, Thursday, and Friday, pass 245 \(no delimiter\). If **repeats** is `weekly`, **count** is `5`, and **daysOfWeek** is`245`, then in the return results, the total is equal to `count*daysOfWeek.length` \(5\*3=15\).

Data type: String

</td></tr><tr><td>

result.reservation.recurring\_pattern.options.​every

</td><td>

Pattern repeat interval. For example, the value '2' indicates that the pattern repeats every 2 days or 2 months depending on the value of the **repeats** property.**Note:** This setting is not applicable to weekly repeat intervals. You can set the **repeats** property to `daily` and this value to `14` for biweekly repeat intervals.

Data type: Number

Default value: 1

</td></tr><tr><td>

result.reservation.recurring\_pattern.options.​endDate

</td><td>

End date and time of the recurrence of the meeting, such as "2022-07-08T14:00:00Z".Data type: String

Format: UTC yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

result.reservation.recurring\_pattern.options.​endDateGdt

</td><td>

End date and time of the recurrence of the meeting.Data type: String

Format: GDT, such as "2022-07-08T14:00:00Z"

</td></tr><tr><td>

result.reservation.recurring\_pattern.repeats

</td><td>

Repeating pattern for the reservable.

Valid values: \(case-sensitive\)

-   daily
-   monthly
-   weekly

**Note:** The pattern repeat interval is set in the **options.every** property. The only valid repeat interval for weekly patterns is one.

Data type: String

</td></tr><tr><td>

result.reservation.recurring\_pattern.startDate

</td><td>

Start date and time for the recurring pattern, such as "2022-07-08T14:00:00Z".

Data type: String

Format: UTC yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

result.reservation.recurring\_pattern.​startDateGdt

</td><td>

Start date and time for the recurring pattern, such as "2022-07-08T14:00:00Z".

Data type: String

Format: UTC yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.requested\_for.avatar

</td><td id="reservation_requested_for_avatar-reserv-entry">

Avatar for the user that the reservation was made on behalf of.Data type: String

</td></tr><tr><td>

result.reservation.requested\_for.displayValue

</td><td id="reservation_requested_for_displayValue-reserv-entry">

Display value of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr><td>

result.reservation.requested\_for.display\_value

</td><td id="reservation_requested_for_display_value-reserv-entry">

Display value of the user that the reservation was made on behalf of. Same as displayValue.Data type: String

</td></tr><tr><td>

result.reservation.requested\_for.email

</td><td id="reservation_requested_for_email-reserv-entry">

Email address for the user that the reservation was made on behalf of.Data type: String

</td></tr><tr><td>

result.reservation.requested\_for.initials

</td><td id="reservation_requested_for_initials-reserv-entry">

Initials of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr><td>

result.reservation.requested\_for.label

</td><td id="reservation_requested_for_label-reserv-entry">

Label for the user that the reservation was made on behalf of.Data type: String

</td></tr><tr><td>

result.reservation.requested\_for.name

</td><td id="reservation_requested_for_name-reserv-entry">

Name of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr><td>

result.rservation.requested\_for.sys\_id

</td><td id="reservation_requested_for_sys_id-reserv-entry">

Sys\_id\_of the user that the reservation was made on behalf of.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

result.rservation.requested\_for.table

</td><td id="reservation_requested_for_table-reserv-entry">

Table that contains the user record.Data type: String

</td></tr><tr><td>

result.reservation.requested\_for.user\_name

</td><td id="reservation_requested_for_user_name-reserv-entry">

User name of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr><td>

result.reservation.requested\_for.value

</td><td id="reservation_requested_for_value-reserv-entry">

Internal value of the user that the reservation was made on behalf of.Data type: String

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.reservable\_module.​allow\_invitees

</td><td id="reservation_reservable_module_allow_invitees-reserv-entry">

Flag that indicates whether employees are able to add invitees to the reservation. Valid values:

-   true: Allow employees to add invitees to the reservation.
-   false: Don't allow employees to add invitees to the reservation.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​allow\_whole\_day

</td><td id="reservation_reservable_module_allow_whole_day-reserv-entry">

Flag that indicates whether users can reserve the reservable for the entire day. Valid values:

-   true: Allow users to reserve for the entire day.
-   false: Don't allow users to reserve for the entire day.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​apply\_to\_shift

</td><td id="reservation_reservable_module_apply_to_shift-reserv-entry">

Flag that indicates whether shift-based reservations are enabled for the reservable module. Valid values:

-   true: Allow shift-based reservations.
-   false: Don't allow shift-based reservations.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​browse\_by\_area\_enabled

</td><td id="reservation_reservable_module_browse_by_area_enabled-reserv-entry">

Flag that indicates whether users are able to search for reservable modules by area.Valid values:

-   true: Allow users to browse reservable modules by area.
-   false: Don't allow users to browse reservable modules by area.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​browse\_near\_a\_person\_enabled

</td><td id="reservation_reservable_module_browse_near_a_person_enabled-reserv-entry">

Flag that indicates whether users are able to search for reservable modules located by a specified person.Valid values:

-   true: Allow users to browse reservable modules near a person.
-   false: Don't allow users to browse reservable modules near a person.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​buildingSysIds

</td><td id="reservation_reservable_module_buildingSysIds-reserv-entry">

List of sys\_ids of the buildings associated with the reservable module.Data type: Array of Strings

</td></tr><tr><td>

result.reservation.reservable\_module.​checkin\_before\_minutes

</td><td id="reservation_reservable_module_checkin_before_minutes-reserv-entry">

Amount of time before a reservation starts that a user can check into their reservation.Unit: Minutes

Data type: Number

</td></tr><tr><td>

result.reservation.reservable\_module.​display\_number\_of\_attendees

</td><td id="reservation_reservable_module_display_number_of_attendees-reserv-entry">

Flag that indicates whether users can specify the number of attendees in the reservation. Valid values:

-   true: Users can specify the number of attendees.
-   false: Users can't specify the display number of attendees.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​display\_on\_behalf\_of

</td><td id="reservation_reservable_module_display_on_behalf_of-reserv-entry">

Flag that indicates whether reservations can be made on behalf of someone else. Valid values:

-   true: On behalf of supported.
-   false: On behalf of not supported.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​display\_sensitivity

</td><td id="reservation_reservable_module_display_sensitivity-reserv-entry">

Flag that indicates whether users can set the sensitivity of the reservation, such as normal or private.Valid values:

-   true: Able to set sensitivity.
-   false: Not able to set sensitivity. Defaults to normal.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​display\_value

</td><td id="reservation_reservable_module_display_value-reserv-entry">

Display value of the reservable module.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​enable\_browse\_by\_area

</td><td id="reservation_reservable_module_enable_browse_by_area-reserv-entry">

Flag that indicates whether users are able to search for reservable modules by area. Same as **browse\_by\_area\_enabled**.Valid values:

-   true: Allow users to browse reservable modules by area.
-   false: Don't allow users to browse reservable modules by area.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​enable\_browse\_near\_a\_person

</td><td id="reservation_reservable_module_enable_browse_near_a_person-reserv-entry">

Flag that indicates whether users are able to search for reservable modules located by a specified person. Same as**browse\_near\_a\_person\_enabled**.Valid values:

-   true: Allow users to browse reservable modules near a person.
-   false: Don't allow users to browse reservable modules near a person.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​enable\_facet\_filter

</td><td id="reservation_reservable_module_enable_facet_filter-reserv-entry">

Flag that indicates whether facet filtering on workplace items is enabled. When enabled, the filter options that appear are based on the search results. Only the items that are available in the generated search result are available to users for selection in the filter.Valid values:

-   true: Facet filters are enabled.
-   false: Facet filters aren't enabled.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​enable\_group\_reservations

</td><td id="reservation_reservable_module_enable_group_reservations-reserv-entry">

Flag that indicates whether users can make a group reservation.Valid values:

-   true: Able to make group reservations.
-   false: Not able to make group reservations.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​enable\_ical\_generation

</td><td id="reservation_reservable_module_enable_ical_generation-reserv-entry">

Flag that indicates whether users can generate an iCalendar for the reservation.Valid values:

-   true: iCalendar generation allowed.
-   false: iCalendar generation isn't allowed.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​font\_awesome\_icon

</td><td id="reservation_reservable_module_font_awesome_icon-reserv-entry">

Name of the font icon attached to the reservable module.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​inline\_title

</td><td id="reservation_reservable_module_inline_title-reserv-entry">

Inline title of the reservable module. The title appears in line with the descriptive text on the Workplace service portal.Data type: String

</td></tr><tr><td>

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

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.reservable\_module.​layout\_mapping.body.field

</td><td id="reservation_reservable_module_layout_mapping_body_field-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​layout\_mapping.body.field\_to\_display

</td><td id="reservation_reservable_module_layout_mapping_body_field_to_display-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​layout\_mapping.body.icon

</td><td id="reservation_reservable_module_layout_mapping_body_icon-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​layout\_mapping.body.label

</td><td id="reservation_reservable_module_layout_mapping_body_label-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​layout\_mapping.description

</td><td id="reservation_reservable_module_layout_mapping_description-reserv-entry">

Placeholder for mapping the front-end UI data. Description of the layout mapping.Data type: Array

</td></tr><tr><td>

result.reservation.reservable\_module.​layout\_mapping.image

</td><td id="reservation_reservable_module_layout_mapping_image-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​layout\_mapping.subtitle

</td><td id="reservation_reservable_module_layout_mapping_subtitle-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: Array

</td></tr><tr><td>

result.reservation.reservable\_module.​layout\_mapping.subtitle\_asc

</td><td id="reservation_reservable_module_layout_mapping_subtitle_asc-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: Array

</td></tr><tr><td>

result.reservation.reservable\_module.​layout\_mapping.title

</td><td id="reservation_reservable_module_layout_mapping_title-reserv-entry">

Placeholder for mapping the front-end UI data.Data type: Array

</td></tr><tr><td>

result.reservation.reservable\_module.​max\_days\_in\_future

</td><td id="reservation_reservable_module_max_days_in_future-reserv-entry">

Maximum number of the days in the future that a user can reserve the reservable module.Data type: Number

</td></tr><tr><td>

result.reservation.reservable\_module.​max\_occurrences

</td><td id="reservation_reservable_module_max_occurrences-reserv-entry">

Maximum number of recurring reservation occurrences if recurring reservations are available for the reservable module.Data type: Number

</td></tr><tr><td>

result.reservation.reservable\_module.name

</td><td id="reservation_reservable_module_name-reserv-entry">

Name of the reservable module.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​override\_approval\_policy

</td><td id="reservation_reservable_module_override_approval_policy-reserv-entry">

Option to specify how to implement the approval policy. Choices:

-   No override: The approval policy is implemented as set in the **Requires approval** field of a workplace space or room.
-   Always require approval: The approval policy is required regardless of what is set in the **Requires approval** field of a workplace space or room.
-   Never require approval: The approval policy is removed regardless of what is set in the **Requires approval**l field of a workplace space or room.

Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​require\_cancel\_notes

</td><td id="reservation_reservable_module_require_cancel_notes-reserv-entry">

Flag that indicates whether users must enter a cancellation note before cancelling a reservable module.Valid values:

-   true: Cancellation note required.
-   false: Cancellation note not required.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​require\_cc\_dept\_check

</td><td id="reservation_reservable_module_require_cc_dept_check-reserv-entry">

Flag that indicates whether to check if there's a cost center or department mismatch between the workspace item and the logged in user. Valid values:

-   true: Check for a mismatch.
-   false: Don't check for a mismatch.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​require\_subject

</td><td id="reservation_reservable_module_require_subject-reserv-entry">

Flag that indicates whether the user must enter a subject when making the reservation.Valid values:

-   true: Subject required.
-   false: Subject isn't required.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​reservable\_columns

</td><td id="reservation_reservable_module_reservable_columns-reserv-entry">

List of the columns of a reservable.Data type: Array

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.reservation.reservable\_module.​reservable\_container\_field

</td><td id="reservation_reservable_module_reservable_container_field-reserv-entry">

Level of the container, such as a group of desks in a specific area.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​reservable\_filter

</td><td id="reservation_reservable_module_reservable_filter-reserv-entry">

Filter conditions used to filter out reservable items in the associated Reservable table. Reservable table is a field in the Reservable Module \[sn\_wsd\_rsv\_reservable\_module\] table. These filter conditions were applied to the table contained in the field Reservable table.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​reservable\_quantity\_field

</td><td id="reservation_reservable_module_reservable_quantity_field-reserv-entry">

Reservable quantity of all the spaces. The quantity is used when assigning neighbourhood spaces to an area. For additional information, see [Assign neighborhood spaces to an area](https://www.servicenow.com/docs/access?context=add-neighbourhood-spaces-to-an-area&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​reservable\_table

</td><td id="reservation_reservable_module_reservable_table-reserv-entry">

Table that contains the reservable workplace items.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​reservable\_type

</td><td id="reservation_reservable_module_reservable_type-reserv-entry">

Type of the reservable item, such as location.Data type: String

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.reservable\_module.​reservable\_views.iconClass

</td><td id="reservation_reservable_module_reservable_views_iconClass-reserv-entry">

Icon class of the reservable view.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​reservable\_views.isDefault

</td><td id="reservation_reservable_module_reservable_views_isDefault-reserv-entry">

Flag that indicates whether to make this reservable view the default for reservable modules. Valid values:

-   true: Make default.
-   false: Don't make default.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.​reservable\_views.label

</td><td id="reservation_reservable_module_reservable_views_label-reserv-entry">

Name of the reservable view.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​reservable\_views.order

</td><td id="reservation_reservable_module_reservable_views_order-reserv-entry">

Order in which the views are displayed for the reservable module in the UI. The lower order number come first in the UI. In case of the same order number, it is assigned random ordering.Data type: Number

</td></tr><tr><td>

result.reservation.reservable\_module.​reservable\_views.type

</td><td id="reservation_reservable_module_reservable_views_type-reserv-entry">

Backend name of the reservable view. Used for internal processing.Data type: String

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.reservable\_module.​reservation\_paths.display\_value

</td><td id="reservation_reservable_module_reservation_paths_display_value-reserv-entry">

Display value for the reservation path, such as "Browse near a person".Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​reservation\_paths.value

</td><td id="reservation_reservable_module_reservation_paths_value-reserv-entry">

Internal value for the reservation path, such as "browse\_near\_a\_person".Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​search\_limit

</td><td id="reservation_reservable_module_search_limit-reserv-entry">

Maximum number of search results to return when a user searches for a workplace location.Data type: Number

</td></tr><tr><td>

result.reservation.reservable\_module.​selection\_type

</td><td id="reservation_reservable_module_selection_type-reserv-entry">

Type of selection to display in the search results.

 Can be one of the following options:

-   Specific unit: The search result displays every workplace item.
-   Container: The search result displays the parent or container of the workplace items.

 Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​short\_description

</td><td id="reservation_reservable_module_short_description-reserv-entry">

Brief description of the reservable module.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​show\_map\_view

</td><td id="reservation_reservable_module_show_map_view-reserv-entry">

Flag that indicates whether to enable the map view for reservable modules. Valid values:

-   true: Enable map view.
-   false: Don't enable map view.

Data type: Boolean

</td></tr><tr><td>

result.reservation.reservable\_module.sys\_id

</td><td id="reservation_reservable_module_sys_id-reserv-entry">

Sys\_id of the reservable module.Data type: String

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.reservable\_module.​timeSlots.name

</td><td id="reservation_reservable_module_timeSlots_name-reserv-entry">

Name of the time slot.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​timeSlots.short\_description

</td><td id="reservation_reservable_module_timeSlots_short_description-reserv-entry">

Brief description of the time slot.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​timeSlots.slot\_end

</td><td id="reservation_reservable_module_timeSlots_slot_end-reserv-entry">

End time of the time slot.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​timeSlots.slot\_start

</td><td id="reservation_reservable_module_timeSlots_slot_start-reserv-entry">

Start time of the slot.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​timeSlots.sys\_id

</td><td id="reservation_reservable_module_timeSlots_sys_id-reserv-entry">

Sys\_id of the time slot record.Data type: String

Table: Time Slot \[sn\_wsd\_rsv\_time\_slot\]

</td></tr><tr><td>

result.reservation.reservable\_module.title

</td><td id="reservation_reservable_module_title-reserv-entry">

Title of the reservable module.Data type: String

</td></tr><tr><td>

result.reservation.reservable\_module.​virtual\_meeting\_provider

</td><td id="reservation_reservable_module_virtual_meeting_provider-reserv-entry">

Details about the virtual provider associated with the reservable module.Data type: Object

```
"virtual_meeting_provider": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.reservation.reservable\_module.​virtual\_meeting\_provider.display\_value

</td><td id="reservation_reservable_module_virtual_meeting_provider_display_value-reserv-entry">

Display value of the virtual meeting provider.Data type: String

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.reservation\_purpose

</td><td id="reservation_purpose-reserv-entry">

Details about the purpose of the reservation.Data type: Object

```
"reservation_purpose": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservation.reservation\_purpose.​display\_value

</td><td id="reservation_purpose_display_value-reserv-entry">

Display value for the purpose of the reservation, such as Company meeting.Data type: String

</td></tr><tr><td>

result.reservation.reservation\_purpose.value

</td><td id="reservation_purpose_value-reserv-entry">

Internal value for the purpose of the reservation, such as company\_meeting.Data type: String

</td></tr><tr><td>

result.reservation.reservation\_type

</td><td id="reservation_reservation_type-entry">

Details about the type of the reservation.Data type: Object

```
"reservation_type": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservation.reservation\_type.​display\_value

</td><td id="reservation_reservation_type_display_value-entry">

Display value for the type of the reservation, such as Space.Data type: String

</td></tr><tr><td>

result.reservation.reservation\_type.value

</td><td id="reservation_reservation_type_value-entry">

Internal value for the type of the reservation, such as space.Data type: String

</td></tr><tr><td>

result.reservation.reservation\_subtype

</td><td id="reservation_reservation_subtype-entry">

Details about the subtype of the reservation. Subtypes indicate the type of reservation, such as single, Multi parent, Multi child, Recurring parent, or occurrence.Data type: Object

```
"reservation_subtype": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservation.reservation\_subtype.​display\_value

</td><td id="reservation_reservation_subtype_display_value-entry">

Display value for the subtype of the reservation, such as Single.Data type: String

</td></tr><tr><td>

result.reservation.reservation\_subtype.value

</td><td id="reservation_reservation_subtype_value-entry">

Internal value for the subtype of the reservation, such as single.Data type: String

</td></tr><tr><td>

result.reservation.sensitivity

</td><td id="reservation_sensitivity-entry">

Details about the sensitivity of the reservation.Data type: Object

```
"sensitivity": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservation.sensitivity.display\_value

</td><td id="reservation_sensitivity_display_value-entry">

Display value for the sensitivity of the reservation, such as high or low.Data type: String

</td></tr><tr><td>

result.reservation.sensitivity.value

</td><td id="reservation_sensitivity_value-entry">

Internal value for the sensitivity of the reservation, such as 1 or 3.Data type: String

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.shift.display\_value

</td><td id="reservation_shift_display_value-entry">

Display value of the shift.Data type: String

</td></tr><tr><td>

result.reservation.shift.name

</td><td id="reservation_shift_name-entry">

Name of the shift. Same as **display\_value**.Data type: String

</td></tr><tr><td>

Result.reservation.shift.shiftDetails

</td><td id="reservation_shift_shiftDetails-entry">

Details of shift.Data type: String

</td></tr><tr><td>

result.reservation.shift.sys\_id

</td><td id="reservation_shift_sys_id-entry">

Sys\_id of the shift record.Data type: String

Table: Shift \[sn\_wsd\_core\_shift\]

</td></tr><tr><td>

result.reservation.source

</td><td id="reservation_source-entry">

Details about the source for the reservation, such as Workplace Services or Google Mail..Data type: Object

```
"source": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservation.source.display\_value

</td><td id="reservation_source_display_value-entry">

Display value for the reservation source, such as Workplace Services.Data type: String

</td></tr><tr><td>

result.reservation.source.value

</td><td id="reservation_source_value-entry">

Internal value for the reservation source, such as servicenow.Data type: String

</td></tr><tr><td>

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

</td></tr><tr><td>

result.reservation.source\_icon.classNames

</td><td id="reservation_source_icon_classNames-entry">

Comma-separated class names for the source icon.Data type: String

</td></tr><tr><td>

result.reservation.source\_icon.imgSrc

</td><td id="reservation_source_icon_imgSrc-entry">

Name of the image source for source icon. This icon is stored in the Images \[db\_image\] table.Data type: String

</td></tr><tr><td>

result.reservation.source\_icon.tooltip

</td><td id="reservation_source_icon_tooltip-entry">

Tooltip associated with the source icon.Data type: String

</td></tr><tr><td>

result.reservation.source\_reservation

</td><td>

Source reservation of the current reservation. For example, for recurring reservations, the recurring parent reservation is the source of the series of occurrence reservations.Data type: Object

```
"source_reservation": {
  "display_value": "String",
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.reservation.source\_reservation.​display\_value

</td><td>

Display value for the source reservation.Data type: String

</td></tr><tr><td>

result.reservation.source\_reservation.name

</td><td>

Name of the source reservation.Data type: String

</td></tr><tr><td>

result.reservation.source\_reservation.sys\_id

</td><td>

Sys\_id of the source reservation record.Data type: String

Table:Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.reservation.source\_reservation\_​requester

</td><td>

User who requested the recurring reservation.Data type: Object

```
"source_reservation": {
  "name": "String",
  "sys_id": "String",
  "user_name": "String"
}
```

</td></tr><tr><td>

result.reservation.source\_reservation\_​requester.name

</td><td>

Name of the recurring reservation requester.Data type: String

</td></tr><tr><td>

result.reservation.source\_reservation\_​requester.sys\_id

</td><td>

Sys\_id of the user who requested the recurring reservation.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

result.reservation.source\_reservation\_​requester.user\_name

</td><td>

User name of the recurring reservation requester.Data type: String

</td></tr><tr><td>

result.reservation.start

</td><td id="start-reserv-entry">

Reservation start date and time.Data type: String

Format: UTC - yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr id="state-reserv-row"><td>

result.reservation.state

</td><td>

Details about the state of the reservation.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="state_display_value-reserv-row"><td>

result.reservation.state.display\_value

</td><td id="state_display_value-reserv-entry">

Display value for the current state of the reservation, such as confirmed.Data type: String

</td></tr><tr id="state_value-reserv-row"><td>

result.reservation.state.value

</td><td id="state_value-reserv-entry">

Internal value for the current state of the reservation, such as 2.Data type: String

</td></tr><tr><td>

result.reservation.subject

</td><td id="subject-reserv-entry">

Reservation's subject.Data type: String

</td></tr><tr><td>

result.reservation.sub\_source

</td><td id="reservation_sub_source-entry">

Details about the sub-source of the reservation. The sub-source specifies where the reservation originated such as Google Calendar or Microsoft Exchange.Data type: Object

```
"sub_source": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservation.sub\_source.display\_value

</td><td id="reservation_sub_source_display_value-entry">

Display value for the sub-source of the reservation, such as Google Calendar.Data type: String

</td></tr><tr><td>

result.reservation.sub\_source.value

</td><td id="reservation_sub_source_value-entry">

Internal value of the sub-source field of the reservation, such as google\_calendar.Data type: String

</td></tr><tr><td>

result.reservation.sync\_state

</td><td id="reservation_sync_state-entry">

Details about the synchronization state of a reservation from another service, such as "sync\_enqueued" or "synchronized".Data type: Object

```
"sync_state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservation.sync\_state.display\_value

</td><td id="reservation_sync_state_display_value-entry">

Display value for the current sync state of the reservation, such as synchronized.Data type: String

</td></tr><tr><td>

result.reservation.sync\_state.value

</td><td id="reservation_sync_state_value-entry">

Internal value of the current sync state of the reservation, such as synchronized.Data type: String

</td></tr><tr><td>

result.reservation.sys\_created\_on

</td><td id="reservation_sys_created_on-entry">

Date and time when the reservation was created.Data type: String

</td></tr><tr><td>

result.reservation.sys\_id

</td><td>

Sys\_id of the reservation record.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

Result.reservation.sys\_updated\_on

</td><td id="reservation_sys_updated_on-entry">

Date and time when the reservation was last updated. Data type: String

</td></tr><tr><td>

result.reservation.virtual\_meeting

</td><td id="reservation_virtual_meeting-entry">

URL of the virtual meeting link.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to retrieve a specific recurring reservation.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/recurring_reservation/list/d98a381587b789506342b846dabb3563" \
--request GET \
--header "Accept:application/json" \
--user "username": "password"

```

Return results:

```
{
  "result": {
    "reservations": [
      {
        "sys_id": "198a381587b789506342b846dabb3565",
        "number": "WRES0001247",
        "location": {
          "sys_id": "fe1f744edb7650106c731dcd139619ca",
          "name": "Aspen",
          "description": "A room with large windows, dark leather seats and a large wooden table.",
          "display_value": "Aspen",
          "capacity": 16,
          "label_value": "Room name",
          "email": null,
          "reservable_module": {
            "sys_id": "c31241cedb7650106c731dcd13961917",
            "name": "Meeting rooms",
            "title": "Meeting rooms",
            "inline_title": "meeting room"
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
            "sys_id": "2f554296dbba10106c731dcd139619ed",
            "display_value": "Floor 2",
            "active": true
          },
          "area": {
            "sys_id": "",
            "display_value": "",
            "active": false
          },
          "reservation": {
            "sys_id": "198a381587b789506342b846dabb3565",
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
            "number": "WRES0001247",
            "active": true
          },
          "number_of_attendees": 1,
          "state": {
            "value": "confirmed",
            "display_value": "Confirmed"
          },
          "number": "WRES0001247",
          "requested_for": {
            "sys_id": "2de07e1887cb89106342b846dabb35fe",
            "name": "Workplace User",
            "user_name": "workplace_user"
          }
        },
        "start": "2022-06-11T13:00:00Z",
        "end": "2022-06-11T14:00:00Z",
        "sys_created_on": "2022-05-30T07:06:37Z",
        "sys_updated_on": "2022-05-30T07:06:40Z",
        "source_reservation": {
          "sys_id": "d98a381587b789506342b846dabb3563",
          "display_value": "WRES0001246",
          "name": "WRES0001246"
        },
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
          "value": "occurrence",
          "display_value": "Occurrence"
        },
        "reservation_purpose": {
          "value": "meeting",
          "display_value": "Meeting"
        },
        "attendees": null,
        "number_of_attendees": 1,
        "is_parent": false,
        "subject": "Rec 1",
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
          "allow_recurring": "1",
          "allow_whole_day": "1",
          "require_whole_day": null,
          "selection_type": "unit",
          "reservable_container_field": null,
          "reservable_quantity_field": null,
          "apply_to_shift": null,
          "max_occurrences": "180",
          "enable_facet_filter": false,
          "search_limit": 10000,
          "enable_ical_generation": "1",
          "enable_group_reservations": null,
          "enable_browse_near_a_person": "1",
          "enable_browse_by_area": "1",
          "enable_floor_search": "1",
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
          "timeSlots": [],
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
          "sys_id": "2de07e1887cb89106342b846dabb35fe",
          "value": "2de07e1887cb89106342b846dabb35fe",
          "displayValue": "Workplace User",
          "display_value": "Workplace User",
          "name": "Workplace User",
          "user_name": "workplace_user",
          "table": "sys_user",
          "avatar": null,
          "initials": "WU",
          "email": "workplace_user@example.com",
          "label": ""
        },
        "requested_for": {
          "sys_id": "2de07e1887cb89106342b846dabb35fe",
          "value": "2de07e1887cb89106342b846dabb35fe",
          "displayValue": "Workplace User",
          "display_value": "Workplace User",
          "name": "Workplace User",
          "user_name": "workplace_user",
          "table": "sys_user",
          "avatar": null,
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
        "source_reservation_requester": {
          "sys_id": "2de07e1887cb89106342b846dabb35fe",
          "name": "Workplace User",
          "user_name": "workplace_user"
        },
        "source_icon": {
          "classNames": "fa fa-calendar-check-o",
          "tooltip": "Reservation is confirmed",
          "imgSrc": ""
        },
        "shift": null,
        "recurring_pattern": {
          "duration": "3600000",
          "repeats": "daily",
          "options": {
            "count": 3,
            "daysOfWeek": "",
            "every": 1,
            "endDate": "2022-06-13 14:00:00",
            "endDateGdt": {}
          },
          "label": "Repeats daily, 3 times",
          "startDate": "2022-06-11 13:00:00",
          "startDateGdt": "{}",
          "amountOfDates": "3"
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
    ],
    "occurencesTotalCount": "1"
  }
}

```

## WSD Recurring Reservation - PATCH /api/sn\_wsd\_rsv/recurring\_reservation/cancel\_series/\{sys\_id\}

Cancels an entire specified recurring series reservation or a specific meeting occurrence within the series.

**Note:** You cannot delete multiple meeting occurrences in a single call.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/recurring_reservation/cancel_series/{sys_id}`

Default URL: `/api/sn_wsd_rsv/recurring_reservation/cancel_series/{sys_id}`

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

To cancel the entire series, pass the sys\_id of the recurring parent reservation record.To cancel a specific occurrence of the series, pass the sys\_id of the occurrence of the series.

The recurring parent record has the column reservation\_subtype set to `Recurring parent`. Individual occurrence records have the reservation\_subtype field set to `Occurrence`.

To get the details of recurring parent reservation from the occurrence record, refer to the sys\_id of the source\_reservation field of the occurrence record.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cancel\_notes

</td><td>

Reason for cancelling the reservation.Data Type: String

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

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

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

result

</td><td>

Return results for the cancel recurring reservation request.Data type: Object

```
"result": {
  "failedToCancelOccurrenceReservations": [Array],
  "seriesId": "String",
  "success": Boolean,
  "successCanceledOccurrences": [Array],
  "user_msg": "String"
}
```

</td></tr><tr><td>

result.failedToCancelOccurrenceReservations

</td><td>

List of sys\_ids of the individual meeting occurrence records that failed to be cancelled.Data type: Array of Strings

</td></tr><tr><td>

result.seriesId

</td><td>

Sys\_id of the recurring parent when the whole series is cancelled or the sys\_id of a specific occurrence if a single occurrence is cancelled.Data type: String

</td></tr><tr><td>

result.success

</td><td>

Flag that indicates whether the reservation was successfully cancelled.Possible values:

-   true: Successfully cancelled.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.failedToCancelOccurrenceReservations

</td><td>

List of sys\_ids of the individual meeting occurrence records that were successfully cancelled.Data type: Array of Strings

</td></tr><tr><td>

result.user\_msg

</td><td>

Message about the request.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to cancel an entire recurring reservation.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/recurring_reservation/cancel_series/f64983a347274550003a4587746d43b8" \
--request PATCH \
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--user "username":"password"
```

Return results:

```
{
  "result": {
    "failedToCancelOccurrenceReservations": [],
    "successCanceledOccurrences": [
      "cb4983a347274550003a4587746d43bd",
      "cf4983a347274550003a4587746d43ba"
    ],
    "user_msg": "Your Recurring reservation has been canceled successfully!",
    "seriesId": "f64983a347274550003a4587746d43b8",
    "success": true
  }
}
```

## WSD Recurring Reservation - POST /api/sn\_wsd\_rsv/recurring\_reservation/create\_series

Creates workplace reservations for the same time but different dates, such as weekly, monthly, or every other week.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/recurring_reservation/create_series`

Default URL: `/api/sn_wsd_rsv/recurring_reservation/create_series`

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

recurringPattern

</td><td id="recurringPattern-reserv-entry">

Details about the recurring pattern for the reservation.Data type: Object

```
"recurringPattern": {
  "duration": Number,
  "label": "String",
  "options": {Object},
  "repeats": "String",
  "startDate": "String"
}
```

</td></tr><tr><td>

recurringPattern.duration

</td><td id="recurringPattern_duration-reserv-entry">

Required if not a shift-based reservation. Length of time to reserve the reservable.

Data type: Number

Unit: Seconds

</td></tr><tr><td>

recurringPattern.label

</td><td id="recurringPattern_label-reserv-entry">

Descriptive name for the recurring reservation.Data type: String

</td></tr><tr><td>

recurringPattern.options

</td><td id="recurringPattern_options-reserv-entry">

Required. Details about the options set for the recurring pattern.

Data type: Object

```
"options": {
  "count": Number,
  "daysOfWeek": "String",
  "every": Number,
  "endDate": "String"
}
```

</td></tr><tr><td>

recurringPattern.options.count

</td><td id="recurringPattern_options_count-reserv-entry">

Required if not a shift-based reservation; ignored for shift-based reservations. Number of times to repeat the pattern.

Data type: Number

</td></tr><tr><td>

recurringPattern.options.daysOfWeek

</td><td id="recurringPattern_options_daysOfWeek-reserv-entry">

Required if the **repeats** parameter is set to `weekly`.Days of the week that the reservable is needed.

Valid values:

-   1 = Monday
-   2 = Tuesday
-   3 = Wednesday
-   4 = Thursday
-   5 = Friday
-   6 = Saturday
-   7 = Sunday

For example, to specify Tuesday, Thursday, and Friday, pass 245 \(no delimiter\). If **repeats** is `weekly`, **count** is `5`, and **daysOfWeek** is`245`, then in the return results, the total is equal to `count*daysOfWeek.length` \(5\*3=15\).

Data type: String

</td></tr><tr><td>

recurringPattern.options.every

</td><td id="recurringPattern_options_every-reserv-entry">

Pattern repeat interval. For example, the value '2' indicates that the pattern repeats every 2 days or 2 months depending on the value of the **repeats** property.**Note:** This setting is not applicable to weekly repeat intervals. You can set the **repeats** property to `daily` and this value to `14` for biweekly repeat intervals.

Data type: Number

Default value: 1

</td></tr><tr><td>

recurringPattern.options.endDate

</td><td id="recurringPattern_options_endDate-reserv-entry">

End date and time of the recurrence of the meeting, such as "2022-07-08T14:00:00Z".Data type: String

Format: UTC yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

recurringPattern.repeats

</td><td id="recurringPattern_options_repeats-reserv-entry">

Required if not a shift-based reservation.Repeating pattern for the reservable.

Valid values: \(case-sensitive\)

-   daily
-   monthly
-   weekly

**Note:** The pattern repeat interval is set in the **options.every** property. The only valid repeat interval for weekly patterns is one.

Data type: String

</td></tr><tr><td>

recurringPattern.startDate

</td><td id="recurringPattern_startDate-reserv-entry">

Required. Start date and time for the recurring pattern, such as "2022-07-08T14:00:00Z".

Data type: String

Format: UTC yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

reservation

</td><td>

Details about the recurring reservation to create.Data type: Object

```
"reservation": {
  "is_private": Boolean,
  "location": "String",
  "reservable_module": "String",
  "shift": "String",
  "subject": "String"
}
```

</td></tr><tr><td>

reservation.is\_private

</td><td>

Flag that indicates whether the reservation is private. If private, the reservation doesn't appear to anyone except the owner.For additional information on these privacy settings, see [Location privacy settings and impact](https://www.servicenow.com/docs/access?context=location-privacy-settings-and-impact&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

Valid values:

-   true: Reservation is private.
-   false: Reservation isn't private.

Data type: Boolean

Default: Value set for privacy in the system properties.

</td></tr><tr><td>

reservation.location

</td><td>

Required. Sys\_id of the location to reserve.

Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

reservation.reservable\_module

</td><td>

Required. Sys\_id of the reservable module to associate with the reservation. A [reservable module](https://www.servicenow.com/docs/access?context=config-reservable-module&version=australia&pubname=australia-employee-service-management&ft:locale=en-US) defines the workplace items needed for a reservation.Data type: String

Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

</td></tr><tr><td>

reservation.shift

</td><td>

Sys\_id of the shift to associate with the reservation. If this parameter is passed in, the **end** parameter isn't required.

For additional information on shift-based reservations, see [Enable shift-based reservation](https://www.servicenow.com/docs/access?context=wsd-reservation-setup&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

Data type: String

Table: Shift \[sn\_wsd\_core\_shift\]

</td></tr><tr><td>

reservation.subject

</td><td>

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

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

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

result

</td><td id="result-multi-entry">

Return results from the multi-reservation creation or update.Data type: Object

```
"result": {
  "isValid": Boolean,
  "parent": "String",
  "successfulReservations": [Array],
  "unSuccessfulReservations": [Array]
}
```

</td></tr><tr><td>

result.isValid

</td><td>

Flag that indicates whether the reservation was successfully created.Possible values:

-   true: Successfully created.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.parent

</td><td id="parent-multi-entry">

Sys\_id of the parent reservation that was updated.Data type: String

</td></tr><tr><td>

result.successfulReservations

</td><td>

List of the reservations that were successfully updated.Data type: Array of Objects

```
"successfulReservations": [
  {
    "collision": Boolean,
    "end": "String",
    "error": "String",
    "inserted": Boolean,
    "start": "String"
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.successfulReservations.collision

</td><td>

Flag that indicates whether a reservation already exists for the specified time and collides with the current reservation.Possible values:

-   true: Collision.
-   false: No collision.

Data type: Boolean

</td></tr><tr><td>

result.successfulReservations.end

</td><td>

Reservation end date and time.Data type: String

Format: UTC: yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr><td>

result.successfulReservations.error

</td><td>

Error message if there was a problem while creating the reservation.Data type: String

</td></tr><tr><td>

result.successfulReservations.inserted

</td><td>

Flag that indicates whether the reservation was successfully inserted. Such as when a reservation is added.Possible values:

-   true: Successfully inserted.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.successfulReservations.start

</td><td>

Reservation start date and time.Data type: String

Format: UTC - yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr><td>

result.successfulReservations.sys\_id

</td><td id="d3222e6755">

Sys\_id of the reservation that was created.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.unSuccessfulReservations

</td><td>

List of the reservations that were unsuccessfully updated.Data type: Array of Objects

```
"unSuccessfulReservations": [
  {
    "collision": Boolean,
    "end": "String",
    "error": "String",
    "inserted": Boolean,
    "start": "String"
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.unSuccessfulReservations.collision

</td><td>

Flag that indicates whether a reservation already exists for the specified time and collides with the current reservation.Possible values:

-   true: Collision.
-   false: No collision.

Data type: Boolean

</td></tr><tr><td>

result.unSuccessfulReservations.end

</td><td>

Reservation end date and time.Data type: String

Format: UTC: yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr><td>

result.unSuccessfulReservations.error

</td><td>

Error message if there was a problem while creating the reservation.Data type: String

</td></tr><tr><td>

result.unSuccessfulReservations.inserted

</td><td>

Flag that indicates whether the reservation was successfully inserted. Such as when a reservation is added.Possible values:

-   true: Successfully inserted.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.unSuccessfulReservations.start

</td><td>

Reservation start date and time.Data type: String

Format: UTC - yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr id="successfulReservations_sys_id-multi-row"><td>

result.unSuccessfulReservations.sys\_id

</td><td id="successfulReservations_sys_id-multi-entry">

Sys\_id of the reservation record.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table>### cURL request

The following code example shows how to create a daily recurring reservation for two consecutive days.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/recurring_reservation/create_series" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"reservation\": {
        \"reservable_module\": \"5db44502dbb650106c731dcd13961937\",
        \"subject\": \"Test-123\",
        \"reservation_purpose\": \"meeting\",
        \"timezone\": \"US/Pacific\",
        \"requested_for\": \"6816f79cc0a8016401c5a33be04be441\",
        \"location\": \"6a11a94adb7210106c731dcd1396194e\",
        \"attendees\": \"6816f79cc0a8016401c5a33be04be441\",
        \"is_private\": false
    },
    \"recurringPattern\": {
        \"duration\": 3600000,
        \"repeats\": \"daily\",
        \"options\": {
            \"count\": 2,
            \"daysOfWeek\": \"\",
            \"every\": 1
        },
        \"label\": \"Repeats daily, 2 times\",
        \"startDate\": \"2023-01-12T12:00:00Z\"
    }
}" \
```

Return results:

```
{
  "result": {
    "isValid": true,
    "parent": "1e5f65ca87586550cfaa99b73cbb3513",
    "successfulReservations": [
      {
        "inserted": true,
        "collision": false,
        "sys_id": "9e5f65ca87586550cfaa99b73cbb3517",
        "error": null,
        "start": "2023-01-13T12:00:00Z",
        "end": "2023-01-13T13:00:00Z"
      }
    ],
    "unSuccessfulReservations": [
      {
        "inserted": true,
        "collision": true,
        "sys_id": "5e5f65ca87586550cfaa99b73cbb3515",
        "error": null,
        "start": "2023-01-12T12:00:00Z",
        "end": "2023-01-12T13:00:00Z"
      }
    ]
  }
}
```

