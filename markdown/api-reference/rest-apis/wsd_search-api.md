---
title: WSD Search API
description: The Workplace Service Delivery \(WSD\) Search API provides endpoints to search for available locations and workplace items such as reservables, reservable modules, and available shifts.Checks whether the specified reservables are available for the specified times.Searches for the best reservable item match based on provided search criteria.Determines whether an overlapping reservation exists based on the passed parameters.Searches for available reservable items using a specified reservable model configuration.Returns an encoded query that you can use to search for available shifts in the Shift \[sn\_wsd\_core\_shift\] table.Returns an availability score for reservable items for specified timeslots.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 54
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD Search API

The Workplace Service Delivery \(WSD\) Search API provides endpoints to search for available locations and workplace items such as reservables, reservable modules, and available shifts.

To access this API, the caller must have the sn\_wsd\_core.workplace\_user role and the Workplace Safety Management \(sn\_wsd\_core\) and Workplace Reservation Management \(sn\_wsd\_rsv\) plugins must be activated.

This API runs in the `sn_wsd_rsv` namespace.

For additional information on Workplace Reservation Management, see [Workplace Reservation Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/workplace-rsv-mgmt-feat.md).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD Search - GET /api/sn\_wsd\_rsv/search/availability

Checks whether the specified reservables are available for the specified times.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/search/availability`

Default URL: `/api/sn_wsd_rsv/search/availability`

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

end

</td><td id="end-query-reserv-entry">

Required. End time to use to search for available reservable modules. This value must be later than the value specified in the **start** parameter.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr><td>

include\_reservations\_within\_days

</td><td id="include_reservations_within_days-reserv-entry">

Flag that indicates whether to return all free slots of available times in the response for each reservable for the whole day.Valid values:

-   true: Return all free slots.
-   false: Don't return all free slots.

Data type: Boolean

Default: false

</td></tr><tr><td>

reservable\_ids

</td><td>

Required. Comma-separated list of reservable sys\_ids to evaluate for availability.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

reservation\_ids

</td><td id="reservation_ids-reserv-entry">

Comma-separated list of existing reservation sys\_ids. Pass this parameter if you want to edit the associated reservations.The time blocked for these sys\_ids for the corresponding reservables are treated as available.

Data type: String

Default: None

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

reservable\_module

</td><td id="reservable_module-reserv-entry">

Required. Sys\_id of the reservable module to include in the search. A [reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md) groups similar types of workplace items.Data type: String

Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

</td></tr><tr><td>

schedule\_view\_obj

</td><td id="schedule_view_obj-reserv-entry">

Details about the schedule view to return. Pass this object if you need 24-hour availability data for reservations that span more than one day. The return results will only contain available times and reservations for the specified date.For this functionality to work properly, the parameters **ignore\_same\_day\_validation** and **include\_reservations\_within\_days** must be set to `true`.

Data type: Object

```
"schedule_view_obj": {
  "schedule_view_date": "String",
  "timezone": "String"
}
```

</td></tr><tr><td>

schedule\_view\_obj.schedule\_view\_date

</td><td id="schedule_view_obj-schedule_view_date-reserv-entry">

Date for which to start returning reservation availability. This date must be in the time zone specified in the **schedule\_view\_obj.timezone** parameter.Data type: String

Format: YYYY-MM-DD

</td></tr><tr><td>

schedule\_view\_obj.timezone

</td><td id="schedule_view_obj-timezone-entry">

Building time zone to use to determine the reservation availability data to return. For example: US/Pacific.Data type: String

</td></tr><tr><td>

shift

</td><td>

Required if the specified reservable modules are based on a shift. Sys\_id of the shift to associate with the reservation. If this parameter is passed in, the **end** parameter isn't required.

For additional information on shift-based reservations, see [Enable shift-based reservation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/wsd-reservation-setup.md).

Data type: String

Table: Shift \[sn\_wsd\_core\_shift\]

</td></tr><tr><td>

start

</td><td id="start-query-reserv-entry">

Required. Start time to use to search for available reservable modules. This value must be prior to the value specified in the **end** parameter.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

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

List of all available resevables for the specified times.Data type: Array of Objects

 ```
"result": [
  {
    "availableTimes": [Array],
    "building": {Object},
    "campus": {Object},
    "email": "String",
    "floor": {Object},
    "is_available": Boolean,
    "name": "String",
    "reservations": [Array],
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.availableTimes

</td><td>

List of dates/times that the associated reservable is available.Data type: Array

</td></tr><tr><td>

result.building

</td><td>

Details about the building associated with the reservable.Data type: Object

 ```
"building": {
  "display_value": "String",
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.building.display\_value

</td><td>

Display value for the building.Data type: String

</td></tr><tr><td>

result.building.name

</td><td>

Name of the building.Data type: String

</td></tr><tr><td>

result.building.sys\_id

</td><td>

Sys\_id of the associated building record.Data type: String

</td></tr><tr><td>

result.campus

</td><td>

Details about the campus associated with the reservable.Data type: Object

 ```
"campus": {
  "display_value": "String",
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.campus.display\_value

</td><td>

Display number of the Campus on which the reservable resides, such as East Bay.Data type: String

</td></tr><tr><td>

result.campus.name

</td><td>

Name of the campus.Data type: String

</td></tr><tr><td>

result.campus.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Campus \[sn\_wsd\_core\_campus\]

</td></tr><tr><td>

result.email

</td><td>

Email address for the associated reservable.Data type: String

</td></tr><tr><td>

result.floor

</td><td>

Details about the floor associated with the reservable.Data type: Object

 ```
"floor": {
  "display_value": "String",
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.floor.display\_value

</td><td>

Display number of the floor on which the reservable resides, such as 12.Data type: String

</td></tr><tr><td>

result.floor.name

</td><td>

Name of the floor on which the reservable resides.Data type: String

</td></tr><tr><td>

result.floor.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Floor \[sn\_wsd\_core\_floor\]

</td></tr><tr><td>

result.is\_available

</td><td>

Flag that indicates whether the reservable is available to reserve.Valid values:

-   true: Available to reserve.
-   false: Not available to reserve.

Data type: Boolean

</td></tr><tr><td>

result.name

</td><td>

Name of the reservable.Data type: String

</td></tr><tr><td>

result.reservations

</td><td>

Details about the associated reservation.Data type: Array of Objects

 ```
"reservations": [
  {
    "configuration_item": "String",
    "end": "String",
    "is_collided": Boolean,
    "location": {Object},
    "number": "String",
    "requested_for": {Object},
    "reservation_purpose": {Object},
    "start": "String",
    "state": {Object},
    "subject": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.reservations.configuration\_item

</td><td>

Configuration items corresponding to the reservation.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr><td>

result.reservations.end

</td><td>

Reservation end date and time.Data type: String

Format: UTC: yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr><td>

result.reservations.is\_collided

</td><td>

Flag that indicates whether the reservation collides with the start and end time of the search.This indicates that the associated reservable location is already reserved for the specified search timespan.

Possible values:

-   true: Collision.
-   false: No collision.

Data type: Boolean

</td></tr><tr><td>

result.reservations.location

</td><td>

Details about the location of the reservation.Data type: Object

 ```
"location": {
  "location": "String",
  "timezone": {Object}
}
```

</td></tr><tr><td>

result.reservations.location.location

</td><td>

Sys\_id of the associated location record.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.reservations.location.timezone

</td><td>

Details about the time zone associated with the location.Data type: Object

```
"timezone": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservations.location.timezone.​displayValue

</td><td>

Display value for the time zone to which this location belongs.Data type: String

</td></tr><tr><td>

result.reservations.location.timezone.value

</td><td>

Internal value for the time zone to which this location belongs.Data type: String

</td></tr><tr><td>

result.reservations.number

</td><td>

Reservation number.Data type: String

</td></tr><tr><td>

result.reservations.requested\_for

</td><td>

Details about the person for whom the reservation was requested on behalf of.Data type: Object

```
"requested_for": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.reservations.requested\_for.name

</td><td>

Name of the user for whom the reservation was requested for.Data type: String

</td></tr><tr><td>

result.reservations.requested\_for.sys\_id

</td><td>

Sys\_id of the user for whom the reservation is being requested.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

result.reservations.reservation\_purpose

</td><td>

Details about the purpose of the reservation.Data type: Object

```
"reservation_purpose": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservations.reservation\_purpose.​display\_value

</td><td>

Display value for the purpose of the reservation, such as Company meeting.Data type: String

</td></tr><tr><td>

result.reservations.reservation\_purpose.value

</td><td>

Internal value for the purpose of the reservation, such as company\_meeting.Data type: String

</td></tr><tr><td>

result.reservations.start

</td><td>

Reservation start date and time.Data type: String

Format: UTC - yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr><td>

result.reservations.state

</td><td>

Details about the state of the reservation for the location.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservations.state.display\_value

</td><td>

Display value for the current state of the reservation, such as confirmed.Data type: String

</td></tr><tr><td>

result.reservations.state.value

</td><td>

Internal value for the current state of the reservation, such as 2.Data type: String

</td></tr><tr><td>

result.reservations.subject

</td><td>

Reservation's subject.Data type: String

</td></tr><tr><td>

result.reservations.sys\_id

</td><td>

Required. Sys\_id of the reservation record.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint. Note: Line breaks have been added to the query parameters for easier reading.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/search/availability?
reservable_module=5db44502dbb650106c731dcd13961937&
start=2023-10-12T11:00:00Z&
end=2023-10-15T12:00:00Z&
reservable_ids=adb35f1977220110b3d7be377b5a99fc&
reservation_ids=undefined&
shift=undefined&
schedule_view_obj={"schedule_view_date":"2023-10-12","timezone":"Europe/Paris"}&
timezone=Europe/Paris&
include_reservations_within_days=true&
ignore_same_day_validation=true&
include_unavailable_items=true"  \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

Return results:

```
{
  "result": [
    {
      "sys_id": "fe1f744edb7650106c731dcd139619ca",
      "email": null,
      "name": "Aspen",
      "is_available": true,
      "availableTimes": [
        [
          "2022-04-23 07:00:00",
          "2022-04-23 08:30:00"
        ],
        [
          "2022-04-23 09:30:00",
          "2022-04-23 23:00:00"
        ],
        [
          "2022-04-24 00:00:00",
          "2022-04-24 06:59:59"
        ]
      ],
      "floor": {
        "sys_id": "2f554296dbba10106c731dcd139619ed",
        "display_value": "Floor 2",
        "name": "Floor 2"
      },
      "building": {
        "sys_id": "94e264cedb3650106c731dcd13961919",
        "display_value": "CAL-B1",
        "name": "CAL-B1"
      },
      "campus": {
        "sys_id": "82b2a0cedb3650106c731dcd139619e9",
        "display_value": "California Campus",
        "name": "California Campus"
      },
      "reservations": [
        {
          "sys_id": "5fe65830874bc9106342b846dabb352b",
          "number": "WRES0001001",
          "location": {
            "location": "fe1f744edb7650106c731dcd139619ca",
            "timezone": {
              "value": "US/Pacific",
              "displayValue": "US/Pacific"
            }
          },
          "configuration_item": null,
          "start": "2022-04-23T08:30:00Z",
          "end": "2022-04-23T09:30:00Z",
          "subject": null,
          "reservation_purpose": {
            "value": "meeting",
            "display_value": "Meeting"
          },
          "state": {
            "value": "confirmed",
            "display_value": "Confirmed"
          },
          "is_collided": false,
          "requested_for": {
            "sys_id": "2de07e1887cb89106342b846dabb35fe",
            "name": "Workplace User"
          }
        }
      ]
    }
  ]
}
```

## WSD Search - GET /api/sn\_wsd\_rsv/search/best\_match

Searches for the best reservable item match based on provided search criteria.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/search/best_match`

Default URL: `/api/sn_wsd_rsv/search/best_match`

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

best\_match\_count

</td><td>

Number of best matched reservables to return. Data type: Number

Default: 1

</td></tr><tr><td>

end

</td><td id="end-query-reserv-entry">

Required. End time to use to search for available reservable modules. This value must be later than the value specified in the **start** parameter.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr><td>

include\_reservable\_purposes

</td><td id="include_reservable_purposes-reserv-entry">

Flag that indicates whether to return the purpose of reserving the workplace location for each reservable in the return results.Valid values:

-   true: Return the reservable purposes.
-   false: Don't return the reservable purposes.

Data type: Boolean

Default: false

Table: Reservable Purpose \[sn\_wsd\_rsv\_reservable\_purpose\]

</td></tr><tr><td>

include\_reservations\_within\_days

</td><td id="include_reservations_within_days-reserv-entry">

Flag that indicates whether to return all free slots of available times in the response for each reservable for the whole day.Valid values:

-   true: Return all free slots.
-   false: Don't return all free slots.

Data type: Boolean

Default: false

</td></tr><tr><td>

include\_standard\_​services

</td><td id="include_standard_services-reserv-entry">

Flag that indicates whether to return the standard services information in the response. This information is located in the Standard Service \[sn\_wsd\_rsv\_standard\_service\] table.A standard service describes basic provisions available with a reservable workplace item when the reservation is made, such as white boards, additional monitors, and similar services. For additional information on standard services, see [Standard services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/standard-service.md).

Valid values:

-   true: Return the standard services information.
-   false: Don't return the standard services information.

Data type: Boolean

Default: false

</td></tr><tr><td>

q

</td><td id="q-reserv-entry">

Required. Encoded query to use to filter the search return results. Within this query you must specify the building sys\_id and you can specify parameters such as floor, area, capacity, standard services, and reservable\_purposes.All passed parameters must be sys\_ids, except for capacity, which is a number.

For example: `q=building=94e264cedb3650106c731dcd13961919​^floorINfc7368cedb3650106c731dcd13961902​^capacity>=1​^standard_services=55c0818edb7650106c731dcd13961904​^reservable_purposes=d6e5c7cd1ba4e01051848489cc4bcb81`

You can locate this information in the following tables:

-   Area: sn\_wsd\_core\_area
-   Building: sn\_wsd\_core\_building
-   Floor: sn\_wsd\_core\_floor
-   Reservable purposes: sn\_wsd\_rsv\_reservable\_purpose
-   Standard services: sn\_wsd\_rsv\_standard\_service

Data type: String

</td></tr><tr><td>

reservable\_module

</td><td id="reservable_module-reserv-entry">

Required. Sys\_id of the reservable module to include in the search. A [reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md) groups similar types of workplace items.Data type: String

Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

</td></tr><tr><td>

start

</td><td id="start-query-reserv-entry">

Required. Start time to use to search for available reservable modules. This value must be prior to the value specified in the **end** parameter.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr><td>

time\_slot

</td><td>

Sys\_id of a time slot record for which we are trying to look for the best matching reservable.Data type: String

Default: None

Table: Time Slot \[sn\_wsd\_rsv\_time\_slot\]

</td></tr><tr><td>

timezone

</td><td id="timezone_q_parm-reserv-query">

Preferred time zone, such as Europe/Amsterdam.Data type: String

Default: None

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
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

Return results for the best reservable match.Data type: Object

```
"result": { 
  "floorsOfSelectedBuilding": [Array],
  "hasMore": Boolean,
  "nextItemIndex": Number,
  "reservableContainers": [Array],
  "reservableUnits": [Array]
}
```

</td></tr><tr><td>

result.floorsOfSelectedBuilding

</td><td>

Details about the floors on which the reservable is located.Data type: Array of Objects

```
"floorsOfSelectedBuilding": [
  {
    "display_value": "String",
    "external_id": "String",
    "name": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.floorsOfSelectedBuilding.display\_value

</td><td>

Display number of the floor on which the reservable resides, such as 12.Data type: String

</td></tr><tr><td>

result.floorsOfSelectedBuilding.external\_id

</td><td>

External identifier for the floor.Data type: String

</td></tr><tr><td>

result.floorsOfSelectedBuilding.name

</td><td>

Name of the floor on which the reservable resides.Data type: String

</td></tr><tr><td>

result.floorsOfSelectedBuilding.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Floor \[sn\_wsd\_core\_floor\]

</td></tr><tr><td>

result.hasMore

</td><td id="hasMore-reserv-entry">

Flag that indicates whether there are more reservables in the return results.Possible values:

-   true: More reservables available.
-   false: No more reservables available.

Data type: Boolean

</td></tr><tr><td>

result.nextItemIndex

</td><td id="nextItemIndex-reserv-entry">

Index for the next reservable record to fetch. Use this value when paginating through reservable records.Data type: Number

</td></tr><tr><td>

result.reservableContainers

</td><td id="reservableContainers-reserv-entry">

Only returned for reservable modules whose selection\_type field is set to `container`. A container is a grouping of similar items, such as a group of desks.Data type: Array of Objects

```
"reservableContainers": [
  {
    "building": {Object},
    "campus": {Object},
    "capacity": Number,
    "display_value": "String",
    "floor": {Object},
    "image": {Object}
    "sys_id": "String"
  } 
]
```

</td></tr><tr><td>

result.reservableContainers.building

</td><td id="reservableContainers_building-reserv-entry">

Details about the building associated with the reservable container.Data type: Object

```
"building": {
  "display_value": "String",
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.reservableContainers.building.​display\_value

</td><td>

Display value for the building.Data type: String

</td></tr><tr><td>

result.reservableContainers.building.name

</td><td>

Name of the building.Data type: String

</td></tr><tr><td>

result.reservableContainers.building.sys\_id

</td><td>

Sys\_id of the associated building record.Data type: String

</td></tr><tr><td>

result.reservableContainers.campus

</td><td id="reservableContainers_campus-reserv-entry">

Details about the campus on which the reservable is located.

Data type: Object

 ```
"campus": {
  "display_value": "String",
  "name": "String",
  "sys_id": "String"
}
```

 Table: Campus \[sn\_wsd\_core\_campus\]

</td></tr><tr><td>

result.reservableContainers.campus.​display\_value

</td><td>

Display number of the Campus on which the reservable resides, such as East Bay.Data type: String

</td></tr><tr><td>

result.reservableContainers.campus.name

</td><td>

Name of the campus.Data type: String

</td></tr><tr><td>

result.reservableContainers.campus.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Campus \[sn\_wsd\_core\_campus\]

</td></tr><tr><td>

result.reservableContainers.capacity

</td><td id="reservableContainers_capacity-reserv-entry">

Maximum number of occupants for the reservable.Data type: Number

</td></tr><tr><td>

result.reservableContainers.display\_value

</td><td id="reservableContainers_display_value-reserv-entry">

Display value for the reservable container.Data type: String

</td></tr><tr><td>

result.reservableContainers.floor

</td><td id="reservableContainers_floor-reserv-entry">

Details about the floor associated with the reservable container.Data type: Object

```
"floor": {
  "display_value": "String",
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.reservableContainers.floor.​display\_value

</td><td>

Display number of the floor on which the reservable resides, such as 12.Data type: String

</td></tr><tr><td>

result.reservableContainers.floor.name

</td><td>

Name of the floor on which the reservable resides.Data type: String

</td></tr><tr><td>

result.reservableContainers.floor.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Floor \[sn\_wsd\_core\_floor\]

</td></tr><tr><td>

result.reservableContainers.image

</td><td>

Details about an image that represents the layout for the associated reservable.Data type: Object

```
"image": {
  "link": "String",
  "sys_id": "String"
}
```

Table: Images \[db\_image\]

</td></tr><tr><td>

result.reservableContainers.image.link

</td><td>

Link to an image that represents the layout for this reservable.Data type: String

Table: Images \[db\_image\]

</td></tr><tr><td>

result.reservableContainers.image.sys\_id

</td><td>

Sys\_id of the associated image record.Data type: String

</td></tr><tr><td>

result.reservableContainers.sys\_id

</td><td id="reservableContainers_sys_id-reserv-container">

Sys\_id of the associated container record.Data type: String

Table: The table in which this resides can be configured for any container type. By default it is in the Area \[sn\_wsd\_core\_area\] table.

</td></tr><tr><td>

result.reservableUnits

</td><td id="reservableUnit-reserv-entry">

Details about the reservable units that match the specified search criteria. A reservable unit is a single reservable item such as a desk or a chair.Data type: Array of Objects

```
"reservableUnits": [
  {
    "area": "String",
    "availableTimes": [Array],
    "building": {Object},
    "campus": {Object},
    "capacity": "String",
    "defaultPrivacyValue": Boolean,
    "description": "String",
    "email": "String",
    "external_id": "String",
    "floor": {Object},
    "image": {Object},
    "includedInResult": Boolean,
    "is_available": Boolean,
    "is_favorite": Boolean,
    "is_reservable": "String",
    "is_reserved": Boolean,
    "is_selected": Boolean,
    "location_type": {Object},
    "name": "String",
    "number": "String",
    "order": "String",
    "require_approval": Boolean,
    "requires_check_in": Boolean,
    "reservable_quantity": "String",
    "showPrivacyOption": Boolean,
    "site": {Object},
    "standard_services": [Array],
    "tableName": "String",
    "title": "String",
    “reservable_purposes”: [Array],
    "reservations": [Array],
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.reservableUnits.area

</td><td id="reservableUnit_area-reserv-entry">

Details about the area in which the reservable module is located.Data type: Object

```
"area": {
  "display_value": "String",
  "sys_id": "String"
}
```

Table: Area \[sn\_wsd\_core\_area\]

</td></tr><tr><td>

result.reservableUnits.area.display\_value

</td><td id="reservableUnit_area_display_value-reserv-entry">

Display value for the reservable module area.Data type: String

</td></tr><tr><td>

result.reservableUnits.area.sys\_id

</td><td id="reservableUnit_area_sys_id-reserv-entry">

Sys\_id of the area record associated with the reservable.Data type: String

</td></tr><tr><td>

result.reservableUnits.availableTimes

</td><td id="availableTimes-reserv-entry">

List of dates/times that the associated reservable is available.Data type: Array

</td></tr><tr><td>

result.reservableUnits.building

</td><td id="reservableUnit_building-reserv-entry">

Details about the building in which the reservable is located.Data type: Object

```
"building": {
  "display_value": "String",
  "sys_id": "String"
}
```

Table: Building \[sn\_wsd\_core\_building\]

</td></tr><tr><td>

result.reservableUnits.building.display\_value

</td><td>

Display value for the building.Data type: String

</td></tr><tr><td>

result.reservableUnits.building.sys\_id

</td><td>

Sys\_id of the associated building record.Data type: String

</td></tr><tr><td>

result.reservableUnits.campus

</td><td>

Details about the campus on which the reservable is located.

Data type: Object

 ```
"campus": {
  "display_value": "String",
  "sys_id": "String"
}
```

 Table: Campus \[sn\_wsd\_core\_campus\]

</td></tr><tr><td>

result.reservableUnits.campus.display\_value

</td><td>

Display number of the Campus on which the reservable resides, such as East Bay.Data type: String

</td></tr><tr><td>

result.reservableUnits.campus.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Campus \[sn\_wsd\_core\_campus\]

</td></tr><tr><td>

result.reservableUnits.capacity

</td><td>

Maximum number of occupants for the reservable.Data type: Number

</td></tr><tr><td>

result.reservableUnits.defaultPrivacyValue

</td><td>

Flag that indicates the default privacy setting for the reservable.For additional information on these privacy settings, see [Location privacy settings and impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/location-privacy-settings-and-impact.md).

Possible values:

-   true: Privacy setting for the reservable can be overridden.
-   false: Privacy setting for the reservable can't be overridden.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.description

</td><td id="reservableUnit_description-reserv-entry">

Brief description of the reservable.Data type: String

</td></tr><tr><td>

result.reservableUnits.email

</td><td id="reservableUnit_email-reserv-entry">

Email address for the reservable.Data type: String

</td></tr><tr><td>

result.reservableUnits.external\_id

</td><td id="reservableUnit_external_id-reserv-entry">

External ID of the reservable used to sync a space mapped in CMS. This value is only populated if there is a map associated with this location. Data type: String

</td></tr><tr><td>

result.reservableUnits.floor

</td><td>

Details about the floor on which the reservable is located.

Data type: Object

 ```
"floor": {
  "display_value": "String",
  "sys_id": "String"
}
```

 Table: Floor \[sn\_wsd\_core\_floor\]

</td></tr><tr><td>

result.reservableUnits.floor.display\_value

</td><td>

Display number of the floor on which the reservable resides, such as 12.Data type: String

</td></tr><tr><td>

result.reservableUnits.floor.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Floor \[sn\_wsd\_core\_floor\]

</td></tr><tr><td>

result.reservableUnits.image

</td><td>

Details about an image that represents the layout for the associated reservable.Data type: Object

```
"image": {
  "link": "String",
  "sys_id": "String"
}
```

Table: Images \[db\_image\]

</td></tr><tr><td>

result.reservableUnits.image.link

</td><td>

Link to an image that represents the layout for this reservable.Data type: String

Table: Images \[db\_image\]

</td></tr><tr><td>

result.reservableUnits.image.sys\_id

</td><td>

Sys\_id of the associated image record.Data type: String

</td></tr><tr><td>

result.reservableUnits.includedInResult

</td><td id="reservableUnit_includedInResult-reserv-entry">

Flag that indicates whether the current reservable is included in the return results.Valid values:

-   true: Included in the return results.
-   false: Not included in the return results.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.is\_available

</td><td id="is_available-reserv-entry">

Flag that indicates whether the reservable is available to reserve.Valid values:

-   true: Available to reserve.
-   false: Not available to reserve.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.is\_favorite

</td><td id="reservableUnit_is_favorite-reserv-entry">

Flag that indicates whether the reservable is flagged as one of the associated user's favorites.Valid values:

-   true: Favorite.
-   false: Not a favorite.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.is\_reservable

</td><td id="reservableUnit_is_reservable-reserv-entry">

Flag that indicates whether it's possible to reserve this reservable. **Note:** If the **include\_unavailable\_items** query parameter is set to true, unavailable locations are also returned. In this case, if a location is already reserved, then the **is\_available** parameter is false, but **is\_reservable** is true.

Valid values:

-   true: Available to reserve.
-   false: Not available to reserve.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.is\_reserved

</td><td id="reservableUnit_is_reserved-reserv-entry">

Flag that indicates whether the reservable is already reserved.Valid values:

-   true: Available to reserve.
-   false: Already reserved.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.is\_selected

</td><td id="reservableUnit_is_selected-reserv-entry">

Flag that indicates whether the reservable is already reserved.Valid values:

-   true: Available to reserve.
-   false: Already reserved.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.location\_type

</td><td id="reservableUnit_location_type-reserv-entry">

Details about the type of location of the reservable, such as workplace/desk, cafe, or gym.Data type: Object

```
"location_type": {
  "display_value": "String",
  "name": "String",
  "sys_id": "String"
}
```

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.reservableUnits.location\_type.​display\_value

</td><td>

Display value of the location type.Data type: String

</td></tr><tr><td>

result.reservableUnits.location\_type.name

</td><td id="reservableUnit_location_type_name-reserv-entry">

Name of the location type, such as basement or storage. Same as display value.Data type: String

</td></tr><tr><td>

result.reservableUnits.location\_type.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Space Type \[sn\_wsd\_core\_space\_type\]

</td></tr><tr><td>

result.reservableUnits.name

</td><td>

Name of the reservable.Data type: String

</td></tr><tr><td>

result.reservableUnits.number

</td><td>

Unique identifier of the reservable. This value is more human readable than the sys\_id.Data type: String

</td></tr><tr><td>

result.reservableUnits.order

</td><td>

Order number for the reservable.Data type: Number

</td></tr><tr><td>

result.reservableUnits.require\_approval

</td><td>

Flag that indicates whether reserving the reservable requires an approval.Possible values:

-   true: Approval required.
-   false: Approval isn't required.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.requires\_check\_in

</td><td>

Flag that indicates whether the reservable requires the user to check in.Valid values:

-   true: Check in required.
-   false: Check in isn't required.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.reservable\_purposes

</td><td>

Details about the purpose for reserving the associated reservable.Data type: Array of Objects

```
"reservable_purposes": [
  {
    "name": "String",
    "short_description": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.reservableUnits.reservable\_purposes.​name

</td><td>

Name of the reservable.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservable\_purposes.​short\_description

</td><td>

Brief description of the reservable.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservable\_purposes.​sys\_id

</td><td>

Sys\_id of the reservable purpose record.Data type: String

Table: Reservable Purpose \[sn\_wsd\_rsv\_reservable\_purpose\]

</td></tr><tr><td>

result.reservableUnits.reservations

</td><td id="reservableUnit_reservations-reserv-entry">

Details about the reservations associated with the reservable. Only populated if the **include\_reservations\_within\_days** query parameter is true and the **reservation\_ids** parameter contains reservation IDs, meaning there are reservations already present for this reservable.Data type: Array of Objects

```
"reservations": [
  {
    "configuration_item": "String",
    "end": "String",
    "is_collided": Boolean,
    "location": {Object},
    "number": "String",
    "requested_for": {Object},
    "reservation_purpose": {Object},
    "start": "String",
    "state": {Object},
    "subject": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr id="configuration_item-reserv-row"><td>

result.reservableUnits.reservations.​configuration\_item

</td><td>

Configuration items corresponding to the reservation.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr><td>

result.reservableUnits.reservations.end

</td><td>

Reservation end date and time.Data type: String

Format: UTC: yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr id="is_collided-reserv-row"><td>

result.reservableUnits.reservations.is\_collided

</td><td>

Flag that indicates whether the reservation collides with the start and end time of the search.This indicates that the associated reservable location is already reserved for the specified search timespan.

Possible values:

-   true: Collision.
-   false: No collision.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.reservations.location

</td><td id="reservableUnit_reservations_location-reserv-entry">

Details about the location of the reservation.Data type: Object

```
"location": {
  "location": "String",
  "timezone": {Object}
}
```

</td></tr><tr><td>

result.reservableUnits.reservations.location.​location

</td><td>

Sys\_id of the associated location record.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.reservableUnits.reservations.location.​timezone

</td><td>

Details about the time zone associated with the location.Data type: Object

```
"timezone": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservableUnits.reservations.location.​timezone.displayValue

</td><td>

Display value for the time zone to which this location belongs.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.location.​timezone.value

</td><td>

Internal value for the time zone to which this location belongs.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.number

</td><td>

Unique identifier of the reservable. This value is more human readable than the sys\_id.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.​requested\_for

</td><td>

Details about the person for whom the reservation was requested on behalf of.Data type: Object

```
"requested_for": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.reservableUnits.reservations.​requested\_for.name

</td><td>

Name of the user for whom the reservation was requested for.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.​requested\_for.sys\_id

</td><td>

Sys\_id of the user for whom the reservation is being requested.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

result.reservableUnits.reservations.​reservation\_purpose

</td><td>

Details about the purpose of the reservation.Data type: Object

```
"reservation_purpose": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservableUnits.reservations.​reservation\_purpose.display\_value

</td><td>

Display value for the purpose of the reservation, such as Company meeting.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.​reservation\_purpose.value

</td><td>

Internal value for the purpose of the reservation, such as company\_meeting.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.start

</td><td>

Reservation start date and time.Data type: String

Format: UTC - yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr><td>

result.reservableUnits.reservations.state

</td><td>

Details about the state of the reservation for the location.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservableUnits.reservations.state.​display\_value

</td><td>

Display value for the current state of the reservation, such as confirmed.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.state.value

</td><td>

Internal value for the current state of the reservation, such as 2.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.subject

</td><td>

Reservation's subject.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.sys\_id

</td><td>

Required. Sys\_id of the reservation record.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.reservableUnits.reservable\_quantity

</td><td>

Maximum number of times the associated reservable can be reserved for the same time. This value is used when assigning neighborhood spaces to an area.Data type: Integer

</td></tr><tr><td>

result.reservableUnits.showPrivacyOption

</td><td>

Flag that indicates whether an employee can override the privacy settings for the associated reservable.For additional information on these privacy settings, see [Location privacy settings and impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/location-privacy-settings-and-impact.md).

Valid values:

-   true: Privacy settings can be overridden.
-   false: Privacy setting can't be overridden.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.site

</td><td>

Details about the site where the reservable resides.Data type: Object

```
"site": {
  "display_value": "String",
  "sys_id": "String"
}
```

Table: Site \[sn\_wsd\_core\_site\]

</td></tr><tr><td>

result.reservableUnits.site.display\_value

</td><td>

Display value of the site.Data type: String

</td></tr><tr><td>

result.reservableUnits.site.sys\_id

</td><td>

Sys\_id of the associated site record.Data type: String

Table: Site \[sn\_wsd\_core\_site\]

</td></tr><tr><td>

result.reservableUnits.standard\_services

</td><td>

Associated standard services, such as flip chart, projector screen, and whiteboard and markers.

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

result.reservableUnits.standard\_services.​font\_awesome\_icon

</td><td>

Name of the thumbnail icon associated with the standard service.Data type: String

</td></tr><tr><td>

result.reservableUnits.standard\_services.name

</td><td>

Name of the thumbnail icon associated with the standard service.Data type: String

</td></tr><tr><td>

result.reservableUnits.standard\_services.​short\_description

</td><td>

Brief description of the standard service.Data type: String

</td></tr><tr><td>

result.reservableUnits.standard\_services.sys\_id

</td><td>

Sys\_id of the standard service record.Data type: String

Table: Standard Service \[sn\_wsd\_rsv\_standard\_service\]

</td></tr><tr><td>

result.reservableUnits.sys\_id

</td><td>

Sys\_id of the reservable record.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.reservableUnits.tableName

</td><td>

Name of the table in which the reservable record resides. Data type: String

</td></tr><tr><td>

result.reservableUnits.title

</td><td>

Title of the reservable.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/search/best_match?q=building%3D9e0364cedb3650106c731dcd1396192b&start=2023-01-04T07%3A00%3A00Z&time_slot=d5331cf2dbb5f01038e42b24ca961906&end=2023-01-04T17%3A00%3A00Z&best_match_count=1&reservable_module=2b636b7e1b4e60103523ff751a4bcbe2&timezone=Europe%2FAmsterdam" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "result": {
    "hasMore": false,
    "reservableUnits": [
      {
        "sys_id": "fe1f744edb7650106c731dcd139619ca",
        "external_id": null,
        "email": null,
        "name": "Aspen",
        "title": "Aspen",
        "description": "A room with large windows, dark leather seats and a large wooden table.",
        "image": {
          "sys_id": "41c74902dbb650106c731dcd13961944",
          "link": "41c74902dbb650106c731dcd13961944.iix"
        },
        "number": "ROOM0000903",
        "site": {
          "sys_id": "628eec06db7650106c731dcd139619dd",
          "display_value": "North America"
        },
        "campus": {
          "sys_id": "82b2a0cedb3650106c731dcd139619e9",
          "display_value": "California Campus"
        },
        "building": {
          "sys_id": "94e264cedb3650106c731dcd13961919",
          "display_value": "CAL-B1"
        },
        "floor": {
          "sys_id": "2f554296dbba10106c731dcd139619ed",
          "display_value": "Floor 2"
        },
        "area": null,
        "capacity": "16",
        "reservable_quantity": null,
        "location_type": {
          "sys_id": "20713b83eb512010b89bfdfc9c522899",
          "display_value": "Room",
          "name": "Room"
        },
        "order": null,
        "requires_check_in": null,
        "is_reservable": "1",
        "tableName": "sn_wsd_core_room",
        "require_approval": false,
        "standard_services": [
          {
            "sys_id": "abd0c18edb7650106c731dcd13961965",
            "name": "Projector screen",
            "short_description": "Connect laptop to screen (HDMI and DVI)",
            "font_awesome_icon": "fa-caret-square-o-right"
          }
        ],
        "reservable_purposes": [
          {
            "sys_id": "18f4c3cd1ba4e01051848489cc4bcb82",
            "name": "Board room",
            "short_description": null
          }
        ],
        "is_available": true,
        "reservations": [
          {
            "sys_id": "5fe65830874bc9106342b846dabb352b",
            "number": "WRES0001001",
            "location": {
              "location": "fe1f744edb7650106c731dcd139619ca",
              "timezone": {
                "value": "US/Pacific",
                "displayValue": "US/Pacific"
              }
            },
            "configuration_item": null,
            "start": "2022-04-23T08:30:00Z",
            "end": "2022-04-23T09:30:00Z",
            "subject": null,
            "reservation_purpose": {
              "value": "meeting",
              "display_value": "Meeting"
            },
            "state": {
              "value": "confirmed",
              "display_value": "Confirmed"
            },
            "is_collided": false,
            "requested_for": {
              "sys_id": "2de07e1887cb89106342b846dabb35fe",
              "name": "Workplace User"
            }
          },
          {
            "sys_id": "af075c30874bc9106342b846dabb3572",
            "number": "WRES0001002",
            "location": {
              "location": "fe1f744edb7650106c731dcd139619ca",
              "timezone": {
                "value": "US/Pacific",
                "displayValue": "US/Pacific"
              }
            },
            "configuration_item": null,
            "start": "2022-04-23T23:00:00Z",
            "end": "2022-04-24T00:00:00Z",
            "subject": null,
            "reservation_purpose": {
              "value": "meeting",
              "display_value": "Meeting"
            },
            "state": {
              "value": "confirmed",
              "display_value": "Confirmed"
            },
            "is_collided": false,
            "requested_for": {
              "sys_id": "2de07e1887cb89106342b846dabb35fe",
              "name": "Workplace User"
            }
          }
        ],
        "availableTimes": [
          [
            "2022-04-23 07:00:00",
            "2022-04-23 08:30:00"
          ],
          [
            "2022-04-23 09:30:00",
            "2022-04-23 23:00:00"
          ],
          [
            "2022-04-24 00:00:00",
            "2022-04-24 06:59:59"
          ]
        ],
        "is_favorite": false
      }
    ],
    "reservableContainers": [],
    "nextItemIndex": -1,
    "floorsOfSelectedBuilding": [
      {
        "sys_id": "2f554296dbba10106c731dcd139619ed",
        "display_value": "Floor 2",
        "external_id": null,
        "name": "Floor 2"
      }
    ]
  }
}{
  "result": {
    "hasMore": false,
    "reservableUnits": [
      {
        "sys_id": "32f2a98adb7210106c731dcd13961972",
        "external_id": null,
        "wsd_email": null,
        "name": "B1-03-04",
        "title": "B1-03-04",
        "description": "Desk reserved for the Team-C. After 10am, free to reserve for everyone.",
        "image": {
          "sys_id": "57b42dcadb7210106c731dcd13961945",
          "link": "57b42dcadb7210106c731dcd13961945.iix"
        },
        "number": "SPCE0009018",
        "site": {
          "sys_id": "b17220cedb3650106c731dcd1396197a",
          "display_value": "Western Europe"
        },
        "campus": {
          "sys_id": "44d2e0cedb3650106c731dcd13961988",
          "display_value": "Amsterdam Campus"
        },
        "building": {
          "sys_id": "9e0364cedb3650106c731dcd1396192b",
          "display_value": "AMS-B1"
        },
        "floor": {
          "sys_id": "5373a8cedb3650106c731dcd1396198a",
          "display_value": "Floor 3"
        },
        "area": {
          "sys_id": "410ff04edb7650106c731dcd13961973",
          "display_value": "Desks C1"
        },
        "capacity": "1",
        "reservable_quantity": null,
        "location_type": {
          "sys_id": "5f017383eb512010b89bfdfc9c5228c8",
          "display_value": "Workspace/Desk",
          "name": "Workspace/Desk"
        },
        "order": null,
        "requires_check_in": null,
        "is_reservable": "1",
        "tableName": "sn_wsd_core_space",
        "require_approval": false,
        "is_available": true,
        "reservations": [],
        "availableTimes": [
          [
            "2023-01-04 07:00:00",
            "2023-01-04 17:00:00"
          ]
        ],
        "showPrivacyOption": false,
        "defaultPrivacyValue": false,
        "container": {
          "sys_id": "410ff04edb7650106c731dcd13961973",
          "display_value": "Desks C1",
          "floor": {
            "sys_id": "5373a8cedb3650106c731dcd1396198a",
            "display_value": "Floor 3",
            "name": "Floor 3"
          },
          "building": {
            "sys_id": "9e0364cedb3650106c731dcd1396192b",
            "display_value": "AMS-B1",
            "name": "AMS-B1"
          },
          "campus": {
            "sys_id": "44d2e0cedb3650106c731dcd13961988",
            "display_value": "Amsterdam Campus",
            "name": "Amsterdam Campus"
          },
          "capacity": 6,
          "image": {
            "sys_id": "d52c27b21b8e60103523ff751a4bcb49",
            "link": "d52c27b21b8e60103523ff751a4bcb49.iix"
          }
        },
        "includedInResult": true,
        "is_favorite": true
      }
    ],
    "reservableContainers": [
      {
        "sys_id": "410ff04edb7650106c731dcd13961973",
        "display_value": "Desks C1",
        "floor": {
          "sys_id": "5373a8cedb3650106c731dcd1396198a",
          "display_value": "Floor 3",
          "name": "Floor 3"
        },
        "building": {
          "sys_id": "9e0364cedb3650106c731dcd1396192b",
          "display_value": "AMS-B1",
          "name": "AMS-B1"
        },
        "campus": {
          "sys_id": "44d2e0cedb3650106c731dcd13961988",
          "display_value": "Amsterdam Campus",
          "name": "Amsterdam Campus"
        },
        "capacity": 6,
        "image": {
          "sys_id": "d52c27b21b8e60103523ff751a4bcb49",
          "link": "d52c27b21b8e60103523ff751a4bcb49.iix"
        }
      }
    ],
    "nextItemIndex": -1,
    "floorsOfSelectedBuilding": [
      {
        "sys_id": "5373a8cedb3650106c731dcd1396198a",
        "display_value": "Floor 3",
        "external_id": null,
        "name": "Floor 3"
      }
    ]
  }

```

## WSD Search - GET /api/sn\_wsd\_rsv/search/overlapping\_reservation

Determines whether an overlapping reservation exists based on the passed parameters.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/search/overlapping_reservation`

Default URL: `/api/sn_wsd_rsv/search/overlapping_reservation`

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

end

</td><td>

Required. End time to use to check for overlapping reservations.Data type: String

Format: YYYY-MM-DDTHH:MM:SSZ

</td></tr><tr><td>

recurring\_pattern

</td><td>

Details about the recurring pattern for the reservation.Data type: Object

```
"recurring_pattern": {
  "duration": Number,
  "options": {Object},
  "repeats": "String",
  "startDate":"String"
}
```

</td></tr><tr><td>

recurring\_pattern.duration

</td><td>

Length of time to check.Data type: Number

Unit: Seconds

</td></tr><tr><td>

recurring\_pattern.options

</td><td>

Details about the options associated with the recurring reservation.Data type: Object

```
"options": {
  "count": Number,
  "daysOfWeek": "String",
  "every": Number
}
```

</td></tr><tr><td>

recurring\_pattern.options.count

</td><td>

Number of times the pattern is repeated.Data type: Number

</td></tr><tr><td>

recurring\_pattern.options.daysOfWeek

</td><td>

Days of the week to check for overlap.Valid values:

-   1 = Monday
-   2 = Tuesday
-   3 = Wednesday
-   4 = Thursday
-   5 = Friday
-   6 = Saturday
-   7 = Sunday

For example, to specify Tuesday, Thursday, and Friday, pass 245 \(no delimiter\).

Data type: String

</td></tr><tr><td>

recurring\_pattern.options.every

</td><td>

Pattern repeat interval to check. For example, if this value is `2`, it checks the repeat pattern based on the selection in the **repeats** parameter, such as every other day or every other week.Data type: Number

</td></tr><tr><td>

recurring\_pattern.options.repeats

</td><td>

Repeating pattern for the reservation overlap check.Possible values: \(case-sensitive\)

-   daily
-   monthly
-   weekly
-   yearly

Data type: String

</td></tr><tr><td>

reservable\_id

</td><td>

Sys\_id of the reservable module to check for overlapping reservations.Data type: String

Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

</td></tr><tr><td>

reservation\_id

</td><td>

Sys\_id of the reservation to check for overlap. This value is needed in the edit flow of multi/group parents.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

shift\_info\_object

</td><td>

Details of the shift to check for overlap. For additional information on shift-based reservations, see [Enable shift-based reservation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/wsd-reservation-setup.md).

Data type: Object

```
"shift_info_object": {
  "applyToShift": Boolean,
  "shift": "String",
  "timezone": "String"
}
```

</td></tr><tr><td>

shift\_info\_object.applyToShift

</td><td>

Flag that indicates whether shift-based reservations are enabled for the reservable module. Valid values:

-   true: Allow shift-based reservations.
-   false: Don't allow shift-based reservations.

Data type: Boolean

</td></tr><tr><td>

shift\_info\_object.shift

</td><td>

Sys\_id of the shift to associate with the reservation. If this parameter is passed in, the **end** parameter isn't required.Data type: String

Table:Shift \[sn\_wsd\_core\_shift\]

</td></tr><tr><td>

shift\_info\_object.timezone

</td><td>

Time zone of the shift to check for overlap.Data type: String

</td></tr><tr><td>

start

</td><td>

Required. Start time to use to check for overlapping reservations.Data type: String

Format: YYY-MM-DDTHH:MM:SSZ

</td></tr><tr><td>

user\_id

</td><td>

Required. Sys\_id of the user to check for overlapping reservations.Data type: String

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
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

results

</td><td>

Details of the results of the overlap check.Data type: Object

```
"results": {
  "isOverlapped": Boolean,
  "reservableId": "String"
}
```

</td></tr><tr><td>

results.isOverlapped

</td><td>

Flag that indicates whether an overlapping reservation exists. Valid values:

-   true: Overlapping reservation exists.
-   false: Overlapping reservation doesn’t exist.

Data type: Boolean

</td></tr><tr><td>

results.reservableId

</td><td>

In the case of a group reservation, the sys\_id of the reservable for which the overlap occurs.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to check for a reservation overlap for a specific user and for a specific period of time denoted by the **start** and **end** parameters.

```
curl "http://instance.servicenow.com/api/sn_wsd_rsv/search/overlapping_reservation?user_id=2e617fecc3d365101e38b23bb00131ec&end=2023-06-19T8:00:00Z&start=2023-06-19T07:00:00Z" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
"results": {
  "isOverlapped": True,
  "reservableId": ""
  }
}
```

## WSD Search - GET /api/sn\_wsd\_rsv/search/reservable

Searches for available reservable items using a specified reservable model configuration.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/search/reservable`

Default URL: `/api/sn_wsd_rsv/search/reservable`

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

end

</td><td id="end-query-reserv-entry">

Required. End time to use to search for available reservable modules. This value must be later than the value specified in the **start** parameter.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr><td>

exclude\_reservables

</td><td>

List of one or more sys\_ids of reservables to exclude from the search results.Data type: String or Array

Table: The table in which these sys\_ids are located is specified in the reservable\_table field in the Reservable Module \[sn\_wsd\_rsv\_reservable\_module\] table. It can be either the Space \[sn\_wsd\_core\_space\] or Room \[sn\_wsd\_core\_room\] table.

</td></tr><tr><td>

ignore\_same\_day\_validation

</td><td id="ignore_same_day_validation-reserv-entry">

Flag that indicates whether the reservation search ignores the change of the date validation between the start and end parameters.Valid values:

-   true: Ignore the change date validation.
-   false: Don't ignore the change date validation.

Data type: Boolean

Default: false

</td></tr><tr><td>

include\_reservable\_purposes

</td><td id="include_reservable_purposes-reserv-entry">

Flag that indicates whether to return the purpose of reserving the workplace location for each reservable in the return results.Valid values:

-   true: Return the reservable purposes.
-   false: Don't return the reservable purposes.

Data type: Boolean

Default: false

Table: Reservable Purpose \[sn\_wsd\_rsv\_reservable\_purpose\]

</td></tr><tr><td>

include\_reservations\_within\_days

</td><td id="include_reservations_within_days-reserv-entry">

Flag that indicates whether to return all free slots of available times in the response for each reservable for the whole day.Valid values:

-   true: Return all free slots.
-   false: Don't return all free slots.

Data type: Boolean

Default: false

</td></tr><tr><td>

include\_standard\_​services

</td><td id="include_standard_services-reserv-entry">

Flag that indicates whether to return the standard services information in the response. This information is located in the Standard Service \[sn\_wsd\_rsv\_standard\_service\] table.A standard service describes basic provisions available with a reservable workplace item when the reservation is made, such as white boards, additional monitors, and similar services. For additional information on standard services, see [Standard services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/standard-service.md).

Valid values:

-   true: Return the standard services information.
-   false: Don't return the standard services information.

Data type: Boolean

Default: false

</td></tr><tr><td>

near\_by\_location\_id

</td><td>

Required if the **rsv\_path** parameter is set to `browse_near_a_person`. Sys\_id of the location to use in the encoded query.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

neighborhood

</td><td id="neighborhood-reserv-entry">

Required if the `rsv_path` parameter is set to `browse_by_neighborhood`.

 Only available if the Space Management \(sn\_wsd\_spc\_mgmt\_neighborhood\) plugin is activated.

Sys\_id of the neighborhood record to use in the encoded query.

For additional information on neighborhood space reservations, see [Create neighborhood reservations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-neighborhood-reservations.md).

 Data type: String

 Table: Neighborhood \[sn\_wsd\_spcmgmt\_neighborhood\]

</td></tr><tr><td>

next\_item\_index

</td><td>

Index of next item to retrieve. Pass this parameter when paginating the return results.Data type: Number

Default: 0

</td></tr><tr><td>

page\_size

</td><td>

Maximum number of records to return in the return results.Data type: Number

Default: 6

</td></tr><tr><td>

q

</td><td id="q-reserv-entry">

Required. Encoded query to use to filter the search return results. Within this query you must specify the building sys\_id and you can specify parameters such as floor, area, capacity, standard services, and reservable\_purposes.All passed parameters must be sys\_ids, except for capacity, which is a number.

For example: `q=building=94e264cedb3650106c731dcd13961919​^floorINfc7368cedb3650106c731dcd13961902​^capacity>=1​^standard_services=55c0818edb7650106c731dcd13961904​^reservable_purposes=d6e5c7cd1ba4e01051848489cc4bcb81`

You can locate this information in the following tables:

-   Area: sn\_wsd\_core\_area
-   Building: sn\_wsd\_core\_building
-   Floor: sn\_wsd\_core\_floor
-   Reservable purposes: sn\_wsd\_rsv\_reservable\_purpose
-   Standard services: sn\_wsd\_rsv\_standard\_service

Data type: String

</td></tr><tr><td>

reservable\_module

</td><td id="reservable_module-reserv-entry">

Required. Sys\_id of the reservable module to include in the search. A [reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md) groups similar types of workplace items.Data type: String

Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

</td></tr><tr><td>

reservation\_ids

</td><td id="reservation_ids-reserv-entry">

Comma-separated list of existing reservation sys\_ids. Pass this parameter if you want to edit the associated reservations.The time blocked for these sys\_ids for the corresponding reservables are treated as available.

Data type: String

Default: None

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

rsv\_path

</td><td>

Reservation path to apply to the search.Valid values:

-   browse\_all: Search all reservables.
-   browse\_by\_area: Search the reservables near a specific location. An area identifier must be passed in the encoded query \(**q** parameter\).
-   browse\_by\_neighborhood: Search the reservables near the neighborhood specified in the **neighborhood** parameter.
-   browse\_near\_a\_person: Search the reservables near the workplace location of the person specified in the **near\_by\_location\_id** parameter.

Data type: String

Default: browse\_all

</td></tr><tr><td>

schedule\_view\_obj

</td><td id="schedule_view_obj-reserv-entry">

Details about the schedule view to return. Pass this object if you need 24-hour availability data for reservations that span more than one day. The return results will only contain available times and reservations for the specified date.For this functionality to work properly, the parameters **ignore\_same\_day\_validation** and **include\_reservations\_within\_days** must be set to `true`.

Data type: Object

```
"schedule_view_obj": {
  "schedule_view_date": "String",
  "timezone": "String"
}
```

</td></tr><tr><td>

schedule\_view\_obj.schedule\_view\_date

</td><td id="schedule_view_obj-schedule_view_date-reserv-entry">

Date for which to start returning reservation availability. This date must be in the time zone specified in the **schedule\_view\_obj.timezone** parameter.Data type: String

Format: YYYY-MM-DD

</td></tr><tr><td>

schedule\_view\_obj.timezone

</td><td id="schedule_view_obj-timezone-entry">

Building time zone to use to determine the reservation availability data to return. For example: US/Pacific.Data type: String

</td></tr><tr><td>

start

</td><td id="start-query-reserv-entry">

Required. Start time to use to search for available reservable modules. This value must be prior to the value specified in the **end** parameter.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr><td>

shift

</td><td id="shift-update_reserv-entry">

Sys\_id of the shift to associate with the reservation. If this parameter is passed in, the **end** parameter isn't required.

For additional information on shift-based reservations, see [Enable shift-based reservation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/wsd-reservation-setup.md).

Data type: String

Table: Shift \[sn\_wsd\_core\_shift\]

</td></tr><tr><td>

sort\_by

</td><td>

Desired sort order of the returned reservable items. Valid values:

-   a\_z: Ascending sort order.
-   favorites\_first: Sorted by the user's favorite workplace reservables first, ascending for the rest.
-   z\_a: Descending sort order.

Data type: String

Default: a\_z

</td></tr><tr><td>

timezone

</td><td id="timezone_q_parm-reserv-query">

Preferred time zone, such as Europe/Amsterdam.Data type: String

Default: None

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

Return results for the specified search.Data type: Object

```
"result": { 
  "filter": {Object},
  "hasMore": Boolean,
  "nextFavIndex": Number,
  "nextItemIndex": Number,
  "reservableContainers": [Array],
  "reservableUnits": [Array],
  "totalProcessed": Number
}
```

</td></tr><tr><td>

result.filter

</td><td>

Details about the floors, standard services, and reservable purposes of the reservables. If the **include\_standard\_services** or **include\_reservable\_purposes** parameters are set to false, **standard\_services** and **reservable\_purposes** are empty arrays.Data type: Object

```
"filter": {
   "floors": [Array],
   "reservable_purposes": [Array],
   "standard_services": [Array]
}
```

</td></tr><tr><td>

result.filter.floors

</td><td>

Details about the floor on which the reservable is located.

Data type: Object

 ```
"floors": [
  {
    "display_value": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.filter.floors.display\_value

</td><td>

Display number of the floor on which the reservable resides, such as 12.Data type: String

</td></tr><tr><td>

result.filter.floors.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Floor \[sn\_wsd\_core\_floor\]

</td></tr><tr><td>

result.filter.standard\_services

</td><td>

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

result.filter.standard\_services.​font\_awesome\_icon

</td><td>

Name of the thumbnail icon associated with the standard service.Data type: String

</td></tr><tr><td>

result.filter.standard\_services.name

</td><td>

Name of the standard service.Data type: String

</td></tr><tr><td>

result.filter.standard\_services.short\_description

</td><td>

Brief description of the standard service.Data type: String

</td></tr><tr><td>

result.filter.standard\_services.sys\_id

</td><td>

Sys\_id of the standard service record.Data type: String

Table: Standard Service \[sn\_wsd\_rsv\_standard\_service\]

</td></tr><tr><td>

result.filter.reservable\_purposes

</td><td>

Details about the purpose for reserving the associated reservable.Data type: Array of Objects

```
"reservable_purposes": [
  {
    "name": "String",
    "short_description": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.filter.reservable\_purposes.name

</td><td>

Name of the reservable.Data type: String

</td></tr><tr><td>

result.filter.reservable\_purposes.​short\_description

</td><td>

Brief description of the reservable.Data type: String

</td></tr><tr><td>

result.filter.reservable\_purposes.sys\_id

</td><td>

Sys\_id of the reservable purpose record.Data type: String

Table: Reservable Purpose \[sn\_wsd\_rsv\_reservable\_purpose\]

</td></tr><tr><td>

result.hasMore

</td><td id="hasMore-reserv-entry">

Flag that indicates whether there are more reservables in the return results.Possible values:

-   true: More reservables available.
-   false: No more reservables available.

Data type: Boolean

</td></tr><tr><td>

result.nextFavIndex

</td><td>

Index for the next favorite reservable for the user. Use this value when paginating through the user's favorite reservables.Data type: Number

</td></tr><tr><td>

result.nextItemIndex

</td><td id="nextItemIndex-reserv-entry">

Index for the next reservable record to fetch. Use this value when paginating through reservable records.Data type: Number

</td></tr><tr><td>

result.reservableContainers

</td><td id="reservableContainers-reserv-entry">

Only returned for reservable modules whose selection\_type field is set to `container`. A container is a grouping of similar items, such as a group of desks.Data type: Array of Objects

```
"reservableContainers": [
  {
    "building": {Object},
    "campus": {Object},
    "capacity": Number,
    "display_value": "String",
    "floor": {Object},
    "image": {Object}
    "sys_id": "String"
  } 
]
```

</td></tr><tr><td>

result.reservableContainers.building

</td><td id="reservableContainers_building-reserv-entry">

Details about the building associated with the reservable container.Data type: Object

```
"building": {
  "display_value": "String",
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.reservableContainers.building.​display\_value

</td><td>

Display value for the building.Data type: String

</td></tr><tr><td>

result.reservableContainers.building.name

</td><td>

Name of the building.Data type: String

</td></tr><tr><td>

result.reservableContainers.building.sys\_id

</td><td>

Sys\_id of the associated building record.Data type: String

</td></tr><tr><td>

result.reservableContainers.campus

</td><td id="reservableContainers_campus-reserv-entry">

Details about the campus on which the reservable is located.

Data type: Object

 ```
"campus": {
  "display_value": "String",
  "name": "String",
  "sys_id": "String"
}
```

 Table: Campus \[sn\_wsd\_core\_campus\]

</td></tr><tr><td>

result.reservableContainers.campus.​display\_value

</td><td>

Display number of the Campus on which the reservable resides, such as East Bay.Data type: String

</td></tr><tr><td>

result.reservableContainers.campus.name

</td><td>

Name of the campus.Data type: String

</td></tr><tr><td>

result.reservableContainers.campus.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Campus \[sn\_wsd\_core\_campus\]

</td></tr><tr><td>

result.reservableContainers.capacity

</td><td id="reservableContainers_capacity-reserv-entry">

Maximum number of occupants for the reservable.Data type: Number

</td></tr><tr><td>

result.reservableContainers.display\_value

</td><td id="reservableContainers_display_value-reserv-entry">

Display value for the reservable container.Data type: String

</td></tr><tr><td>

result.reservableContainers.floor

</td><td id="reservableContainers_floor-reserv-entry">

Details about the floor associated with the reservable container.Data type: Object

```
"floor": {
  "display_value": "String",
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.reservableContainers.floor.​display\_value

</td><td>

Display number of the floor on which the reservable resides, such as 12.Data type: String

</td></tr><tr><td>

result.reservableContainers.floor.name

</td><td>

Name of the floor on which the reservable resides.Data type: String

</td></tr><tr><td>

result.reservableContainers.floor.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Floor \[sn\_wsd\_core\_floor\]

</td></tr><tr><td>

result.reservableContainers.image

</td><td>

Link to an image that represents the layout for this reservable.Data type: String

Table: Images \[db\_image\]

</td></tr><tr><td>

result.reservableContainers.image.link

</td><td>

Link to an image that represents the layout for this reservable.Data type: String

Table: Images \[db\_image\]

</td></tr><tr><td>

result.reservableContainers.image.sys\_id

</td><td>

Sys\_id of the associated image record.Data type: String

</td></tr><tr><td>

result.reservableContainers.sys\_id

</td><td id="reservableContainers_sys_id-reserv-container">

Sys\_id of the associated container record.Data type: String

Table: The table in which this resides can be configured for any container type. By default it is in the Area \[sn\_wsd\_core\_area\] table.

</td></tr><tr><td>

result.reservableUnits

</td><td id="reservableUnit-reserv-entry">

Details about the reservable units that match the specified search criteria. A reservable unit is a single reservable item such as a desk or a chair.Data type: Array of Objects

```
"reservableUnits": [
  {
    "area": "String",
    "availableTimes": [Array],
    "building": {Object},
    "campus": {Object},
    "capacity": "String",
    "defaultPrivacyValue": Boolean,
    "description": "String",
    "email": "String",
    "external_id": "String",
    "floor": {Object},
    "image": {Object},
    "includedInResult": Boolean,
    "is_available": Boolean,
    "is_favorite": Boolean,
    "is_reservable": "String",
    "is_reserved": Boolean,
    "is_selected": Boolean,
    "location_type": {Object},
    "name": "String",
    "number": "String",
    "order": "String",
    "require_approval": Boolean,
    "requires_check_in": Boolean,
    "reservable_quantity": "String",
    "showPrivacyOption": Boolean,
    "site": {Object},
    "standard_services": [Array],
    "tableName": "String",
    "title": "String",
    “reservable_purposes”: [Array],
    "reservations": [Array],
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.reservableUnits.area

</td><td id="reservableUnit_area-reserv-entry">

Details about the area in which the reservable module is located.Data type: Object

```
"area": {
  "display_value": "String",
  "sys_id": "String"
}
```

Table: Area \[sn\_wsd\_core\_area\]

</td></tr><tr><td>

result.reservableUnits.area.display\_value

</td><td id="reservableUnit_area_display_value-reserv-entry">

Display value for the reservable module area.Data type: String

</td></tr><tr><td>

result.reservableUnits.area.sys\_id

</td><td id="reservableUnit_area_sys_id-reserv-entry">

Sys\_id of the area record associated with the reservable.Data type: String

</td></tr><tr><td>

result.reservableUnits.availableTimes

</td><td id="availableTimes-reserv-entry">

List of dates/times that the associated reservable is available.Data type: Array

</td></tr><tr><td>

result.reservableUnits.building

</td><td id="reservableUnit_building-reserv-entry">

Details about the building in which the reservable is located.Data type: Object

```
"building": {
  "display_value": "String",
  "sys_id": "String"
}
```

Table: Building \[sn\_wsd\_core\_building\]

</td></tr><tr><td>

result.reservableUnits.building.display\_value

</td><td>

Display value for the building.Data type: String

</td></tr><tr><td>

result.reservableUnits.building.sys\_id

</td><td>

Sys\_id of the associated building record.Data type: String

</td></tr><tr><td>

result.reservableUnits.campus

</td><td>

Details about the campus on which the reservable is located.

Data type: Object

 ```
"campus": {
  "display_value": "String",
  "sys_id": "String"
}
```

 Table: Campus \[sn\_wsd\_core\_campus\]

</td></tr><tr><td>

result.reservableUnits.campus.display\_value

</td><td>

Display number of the Campus on which the reservable resides, such as East Bay.Data type: String

</td></tr><tr><td>

result.reservableUnits.campus.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Campus \[sn\_wsd\_core\_campus\]

</td></tr><tr><td>

result.reservableUnits.capacity

</td><td>

Maximum number of occupants for the reservable.Data type: Number

</td></tr><tr><td>

result.reservableUnits.description

</td><td id="reservableUnit_description-reserv-entry">

Brief description of the reservable.Data type: String

</td></tr><tr><td>

result.reservableUnits.email

</td><td id="reservableUnit_email-reserv-entry">

Email address for the reservable.Data type: String

</td></tr><tr><td>

result.reservableUnits.external\_id

</td><td id="reservableUnit_external_id-reserv-entry">

External ID of the reservable used to sync a space mapped in CMS. This value is only populated if there is a map associated with this location. Data type: String

</td></tr><tr><td>

result.reservableUnits.floor

</td><td>

Details about the floor on which the reservable is located.

Data type: Object

 ```
"floor": {
  "display_value": "String",
  "sys_id": "String"
}
```

 Table: Floor \[sn\_wsd\_core\_floor\]

</td></tr><tr><td>

result.reservableUnits.floor.display\_value

</td><td>

Display number of the floor on which the reservable resides, such as 12.Data type: String

</td></tr><tr><td>

result.reservableUnits.floor.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Floor \[sn\_wsd\_core\_floor\]

</td></tr><tr><td>

result.reservableUnits.image

</td><td>

Details about an image that represents the layout for the associated reservable.Data type: Object

```
"image": {
  "link": "String",
  "sys_id": "String"
}
```

Table: Images \[db\_image\]

</td></tr><tr><td>

result.reservableUnits.image.link

</td><td>

Link to an image that represents the layout for this reservable.Data type: String

Table: Images \[db\_image\]

</td></tr><tr><td>

result.reservableUnits.image.sys\_id

</td><td>

Sys\_id of the associated image record.Data type: String

</td></tr><tr><td>

result.reservableUnits.includedInResult

</td><td id="reservableUnit_includedInResult-reserv-entry">

Flag that indicates whether the current reservable is included in the return results.Valid values:

-   true: Included in the return results.
-   false: Not included in the return results.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.is\_available

</td><td id="is_available-reserv-entry">

Flag that indicates whether the reservable is available to reserve.Valid values:

-   true: Available to reserve.
-   false: Not available to reserve.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.is\_favorite

</td><td id="reservableUnit_is_favorite-reserv-entry">

Flag that indicates whether the reservable is flagged as one of the associated user's favorites.Valid values:

-   true: Favorite.
-   false: Not a favorite.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.is\_reservable

</td><td id="reservableUnit_is_reservable-reserv-entry">

Flag that indicates whether it's possible to reserve this reservable. **Note:** If the **include\_unavailable\_items** query parameter is set to true, unavailable locations are also returned. In this case, if a location is already reserved, then the **is\_available** parameter is false, but **is\_reservable** is true.

Valid values:

-   true: Available to reserve.
-   false: Not available to reserve.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.is\_reserved

</td><td id="reservableUnit_is_reserved-reserv-entry">

Flag that indicates whether the reservable is already reserved.Valid values:

-   true: Available to reserve.
-   false: Already reserved.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.is\_selected

</td><td id="reservableUnit_is_selected-reserv-entry">

Flag that indicates whether the reservable is already reserved.Valid values:

-   true: Available to reserve.
-   false: Already reserved.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.location\_type

</td><td id="reservableUnit_location_type-reserv-entry">

Details about the type of location of the reservable, such as workplace/desk, cafe, or gym.Data type: Object

```
"location_type": {
  "display_value": "String",
  "name": "String",
  "sys_id": "String"
}
```

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.reservableUnits.location\_type.​display\_value

</td><td>

Display value of the location type.Data type: String

</td></tr><tr><td>

result.reservableUnits.location\_type.name

</td><td id="reservableUnit_location_type_name-reserv-entry">

Name of the location type, such as basement or storage. Same as display value.Data type: String

</td></tr><tr><td>

result.reservableUnits.location\_type.sys\_id

</td><td>

Sys\_id of the associated record.Data type: String

Table: Space Type \[sn\_wsd\_core\_space\_type\]

</td></tr><tr><td>

result.reservableUnits.name

</td><td>

Name of the reservable.Data type: String

</td></tr><tr><td>

result.reservableUnits.number

</td><td>

Unique identifier of the reservable. This value is more human readable than the sys\_id.Data type: String

</td></tr><tr><td>

result.reservableUnits.order

</td><td>

Order number for the reservable.Data type: Number

</td></tr><tr><td>

result.reservableUnits.require\_approval

</td><td>

Flag that indicates whether reserving the reservable requires an approval.Possible values:

-   true: Approval required.
-   false: Approval isn't required.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.requires\_check\_in

</td><td>

Flag that indicates whether the reservable requires the user to check in.Valid values:

-   true: Check in required.
-   false: Check in isn't required.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.reservable\_purposes

</td><td>

Details about the purpose for reserving the associated reservable.Data type: Array of Objects

```
"reservable_purposes": [
  {
    "name": "String",
    "short_description": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.reservableUnits.reservable\_purposes.​name

</td><td>

Name of the reservable.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservable\_purposes.​short\_description

</td><td>

Brief description of the reservable.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservable\_purposes.​sys\_id

</td><td>

Sys\_id of the reservable purpose record.Data type: String

Table: Reservable Purpose \[sn\_wsd\_rsv\_reservable\_purpose\]

</td></tr><tr><td>

result.reservableUnits.reservations

</td><td id="reservableUnit_reservations-reserv-entry">

Details about the reservations associated with the reservable. Only populated if the **include\_reservations\_within\_days** query parameter is true and the **reservation\_ids** parameter contains reservation IDs, meaning there are reservations already present for this reservable.Data type: Array of Objects

```
"reservations": [
  {
    "configuration_item": "String",
    "end": "String",
    "is_collided": Boolean,
    "location": {Object},
    "number": "String",
    "requested_for": {Object},
    "reservation_purpose": {Object},
    "start": "String",
    "state": {Object},
    "subject": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr id="configuration_item-reserv-row"><td>

result.reservableUnits.reservations.​configuration\_item

</td><td>

Configuration items corresponding to the reservation.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr><td>

result.reservableUnits.reservations.end

</td><td>

Reservation end date and time.Data type: String

Format: UTC: yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr id="is_collided-reserv-row"><td>

result.reservableUnits.reservations.is\_collided

</td><td>

Flag that indicates whether the reservation collides with the start and end time of the search.This indicates that the associated reservable location is already reserved for the specified search timespan.

Possible values:

-   true: Collision.
-   false: No collision.

Data type: Boolean

</td></tr><tr><td>

result.reservableUnits.reservations.location

</td><td id="reservableUnit_reservations_location-reserv-entry">

Details about the location of the reservation.Data type: Object

```
"location": {
  "location": "String",
  "timezone": {Object}
}
```

</td></tr><tr><td>

result.reservableUnits.reservations.location.​location

</td><td>

Sys\_id of the associated location record.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.reservableUnits.reservations.location.​timezone

</td><td>

Details about the time zone associated with the location.Data type: Object

```
"timezone": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservableUnits.reservations.location.​timezone.displayValue

</td><td>

Display value for the time zone to which this location belongs.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.location.​timezone.value

</td><td>

Internal value for the time zone to which this location belongs.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.number

</td><td>

Unique identifier of the reservable. This value is more human readable than the sys\_id.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.​requested\_for

</td><td>

Details about the person for whom the reservation was requested on behalf of.Data type: Object

```
"requested_for": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.reservableUnits.reservations.​requested\_for.name

</td><td>

Name of the user for whom the reservation was requested for.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.​requested\_for.sys\_id

</td><td>

Sys\_id of the user for whom the reservation is being requested.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

result.reservableUnits.reservations.​reservation\_purpose

</td><td>

Details about the purpose of the reservation.Data type: Object

```
"reservation_purpose": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservableUnits.reservations.​reservation\_purpose.display\_value

</td><td>

Display value for the purpose of the reservation, such as Company meeting.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.​reservation\_purpose.value

</td><td>

Internal value for the purpose of the reservation, such as company\_meeting.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.start

</td><td>

Reservation start date and time.Data type: String

Format: UTC - yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr><td>

result.reservableUnits.reservations.state

</td><td>

Details about the state of the reservation for the location.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.reservableUnits.reservations.state.​display\_value

</td><td>

Display value for the current state of the reservation, such as confirmed.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.state.value

</td><td>

Internal value for the current state of the reservation, such as 2.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.subject

</td><td>

Reservation's subject.Data type: String

</td></tr><tr><td>

result.reservableUnits.reservations.sys\_id

</td><td>

Required. Sys\_id of the reservation record.

Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.reservableUnits.reservable\_quantity

</td><td>

Maximum number of times the associated reservable can be reserved for the same time. This value is used when assigning neighborhood spaces to an area.Data type: Integer

</td></tr><tr><td>

result.reservableUnits.site

</td><td>

Details about the site where the reservable resides.Data type: Object

```
"site": {
  "display_value": "String",
  "sys_id": "String"
}
```

Table: Site \[sn\_wsd\_core\_site\]

</td></tr><tr><td>

result.reservableUnits.site.display\_value

</td><td>

Display value of the site.Data type: String

</td></tr><tr><td>

result.reservableUnits.site.sys\_id

</td><td>

Sys\_id of the associated site record.Data type: String

Table: Site \[sn\_wsd\_core\_site\]

</td></tr><tr><td>

result.reservableUnits.standard\_services

</td><td>

Associated standard services, such as flip chart, projector screen, and whiteboard and markers.

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

result.reservableUnits.standard\_services.​font\_awesome\_icon

</td><td>

Name of the thumbnail icon associated with the standard service.Data type: String

</td></tr><tr><td>

result.reservableUnits.standard\_services.name

</td><td>

Name of the thumbnail icon associated with the standard service.Data type: String

</td></tr><tr><td>

result.reservableUnits.standard\_services.​short\_description

</td><td>

Brief description of the standard service.Data type: String

</td></tr><tr><td>

result.reservableUnits.standard\_services.sys\_id

</td><td>

Sys\_id of the standard service record.Data type: String

Table: Standard Service \[sn\_wsd\_rsv\_standard\_service\]

</td></tr><tr><td>

result.reservableUnits.sys\_id

</td><td>

Sys\_id of the reservable record.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.reservableUnits.tableName

</td><td>

Name of the table in which the reservable record resides. Data type: String

</td></tr><tr><td>

result.reservableUnits.title

</td><td>

Title of the reservable.Data type: String

</td></tr><tr><td>

result.totalProcessed

</td><td>

Total number of records processed.Data type: Number

</td></tr></tbody>
</table>### cURL request

This example shows how to search for reservables using this endpoint. Note: Line breaks have been added to the query parameters for easier reading.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/search/reservable?
reservable_module=d9864189c3653910977396cb05013100&
start=2023-10-12T10:30:00Z&
end=2023-10-13T11:30:00Z&
include_standard_services=true&
include_reservable_purposes=true&
include_reservations_within_days=true&
include_unavailable_items=true&
near_by_location_id=undefined&
timezone=Europe/Paris&
page_size=6&
sort_by=a_z&
view=schedule&
rsv_path=browse_all&
ignore_same_day_validation=true&
schedule_view_obj={"schedule_view_date":"2023-10-12","timezone":"Europe/Paris"}&
q=building=dea39b1977220110b3d7be377b5a9955\
--request GET \
--header "Accept:application/json" 
--user "username":"password"
```

Return results:

```
{
  "result": {
    "hasMore": true,
    "reservableUnits": [
      {
        "sys_id": "fe1f744edb7650106c731dcd139619ca",
        "external_id": null,
        "email": null,
        "name": "Aspen",
        "title": "Aspen",
        "description": "A room with large windows, dark leather seats and a large wooden table.",
        "image": {
          "sys_id": "41c74902dbb650106c731dcd13961944",
          "link": "41c74902dbb650106c731dcd13961944.iix"
        },
        "number": "ROOM0000903",
        "site": {
          "sys_id": "628eec06db7650106c731dcd139619dd",
          "display_value": "North America"
        },
        "campus": {
          "sys_id": "82b2a0cedb3650106c731dcd139619e9",
          "display_value": "California Campus"
        },
        "building": {
          "sys_id": "94e264cedb3650106c731dcd13961919",
          "display_value": "CAL-B1"
        },
        "floor": {
          "sys_id": "2f554296dbba10106c731dcd139619ed",
          "display_value": "Floor 2"
        },
        "area": null,
        "capacity": "16",
        "reservable_quantity": null,
        "location_type": {
          "sys_id": "20713b83eb512010b89bfdfc9c522899",
          "display_value": "Room",
          "name": "Room"
        },
        "order": null,
        "requires_check_in": null,
        "is_reservable": "1",
        "tableName": "sn_wsd_core_room",
        "require_approval": false,
        "standard_services": [
          {
            "sys_id": "9b01458edb7650106c731dcd13961945",
            "name": "Flip chart",
            "short_description": "Flip chart with paper sheets",
            "font_awesome_icon": "fa-calendar-o"
          }
        ],
        "reservable_purposes": [
          {
            "sys_id": "18f4c3cd1ba4e01051848489cc4bcb82",
            "name": "Board room",
            "short_description": null
          }
        ],
        "is_available": true,
        "reservations": [
          {
            "sys_id": "5fe65830874bc9106342b846dabb352b",
            "number": "WRES0001001",
            "location": {
              "location": "fe1f744edb7650106c731dcd139619ca",
              "timezone": {
                "value": "US/Pacific",
                "displayValue": "US/Pacific"
              }
            },
            "configuration_item": null,
            "start": "2022-04-23T08:30:00Z",
            "end": "2022-04-23T09:30:00Z",
            "subject": null,
            "reservation_purpose": {
              "value": "meeting",
              "display_value": "Meeting"
            },
            "state": {
              "value": "confirmed",
              "display_value": "Confirmed"
            },
            "is_collided": false,
            "requested_for": {
              "sys_id": "2de07e1887cb89106342b846dabb35fe",
              "name": "Workplace User"
            }
          }
        ],
        "availableTimes": [
          [
            "2022-04-23 07:00:00",
            "2022-04-23 08:30:00"
          ],
          [
            "2022-04-23 09:30:00",
            "2022-04-23 23:00:00"
          ]
        ],
       "is_reserved": true,
       "is_selected": true,
        "includedInResult": true,
        "is_favorite": false
      }
    ],
    "reservableContainers": [],
    "nextItemIndex": -1,
    "filter": {
      "floors": [],
      "standard_services": [
        {
          "sys_id": "9b01458edb7650106c731dcd13961945",
          "name": "Flip chart",
          "short_description": "Flip chart with paper sheets",
          "font_awesome_icon": "fa-calendar-o"
        }
      ],
      "reservable_purposes": [
        {
          "sys_id": "18f4c3cd1ba4e01051848489cc4bcb82",
          "name": "Board room",
          "short_description": null
        }
      ]
    },
    "totalProcessed": 2,
    "nextFavIndex": 0
  }
}
```

## WSD Search - GET /api/sn\_wsd\_rsv/search/shift/\{building\_id\}/\{module\_id\}

Returns an encoded query that you can use to search for available shifts in the Shift \[sn\_wsd\_core\_shift\] table.

Only applicable if the appy\_to\_shift field in the specified reservable module is enabled. Otherwise, the returned encoded query string will be empty.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/search/shift/{building_id}/{module_id}`

Default URL: `/api/sn_wsd_rsv/search/shift/{building_id}/{module_id}`

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

building\_id

</td><td>

Sys\_id of the building to include in the search query. Data type: String

Table: Building \[sn\_wsd\_core\_building\]

</td></tr><tr><td>

module\_id

</td><td>

Sys\_id of the reservable module to include in the search query. A reservable module groups similar types of workplace items, such a chairs or desks.Data type: String

Table: Reservable Module \[sn\_wsd\_core\_reservable\_module\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

end\_date

</td><td>

Shift end date and time to include in the encoded query.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

start\_date

</td><td>

Shift start date and time to include in the encoded query.Data type: String

Format: yyyy-mm-dd hh:mm:ss

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

Encoded query to use to acquire the specified available shifts.Data type: Object

```
"result": { 
  "moduleHasShift": Boolean,
  "query": "String"
}
```

</td></tr><tr><td>

moduleHasShift

</td><td>

Flag that indicates whether the specified reservable module has shifts enabled.Valid values:

-   true: Reservable module has shifts enabled.
-   false: Reservable module doesn't has shifts enabled. No encoded query returned.

Data type: Boolean

</td></tr><tr><td>

query

</td><td>

Encoded query to use to retrieve shift information for the specified reservable module.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to use this endpoint to obtain a shift encoded query.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/search/shift/94e264cedb3650106c731dcd13961919/fc71f64fdb42a01097acc900399619a8?start_date=2022-04-23 16:00:00&end_date=2022-04-28 16:00:00"  \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "result": { 
    "moduleHasShift" : true,
    "query" : "active=true^state=2^building=94e264cedb3650106c731dcd13961919^building.is_reservable=true^building.active=true^floorISEMPTY^ORfloor.is_reservable=true^floorISEMPTY^ORfloor.active=true^start<=2022-04-26 16:00:00^ORstartISEMPTY^end>=2022-04-28 16:00:00^ORendISEMPTY^start<=2022-04-28 16:00:00^ORstartISEMPTY^end>=2022-04-28 16:00:00^ORendISEMPTY"
  }
}
```

## WSD Search - POST /api/sn\_wsd\_rsv/search/availability\_score

Returns an availability score for reservable items for specified timeslots.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/search/availability_score`

Default URL: `/api/sn_wsd_rsv/search/availability_score`

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

</td><td>

Required if **startEndDateTimes** parameter is not specified. Recurring pattern to use to search for reservables that are available for the specified recurring events.Data type: Object

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

</td><td>

Required. Length of time for which the reservable must be available.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

recurringPattern.label

</td><td>

Description of the recurring pattern, such as `Repeats daily, 5 times`.Data type: String

</td></tr><tr><td>

recurringPattern.options

</td><td>

Availability options for the recurring reservation to search for.Data type: Object

```
"options": {
  "count": Number,
  "daysOfWeek": "String",
  "endDate": "String"
}
```

</td></tr><tr><td>

recurringPattern.options.count

</td><td>

Required if **endDate** is not passed. If both are passed, **count** is used. Number of times to repeat the meeting pattern.Data type: Number

</td></tr><tr><td>

recurringPattern.options.daysOfWeek

</td><td>

Required if the **recurringPattern.repeats** parameter is set to `weekly`. Days of the week that the reservable is needed.Valid values:

-   1 = Monday
-   2 = Tuesday
-   3 = Wednesday
-   4 = Thursday
-   5 = Friday
-   6 = Saturday
-   7 = Sunday

For example, to specify Tuesday, Thursday, and Friday, pass 245 \(no delimiter\). If **repeat** is weekly, **count** is 5, and **daysOfWeek** is 245, then in the return results, the total is equal to `count*daysOfWeek.length` \(5\*3=15\).

Data type: String

</td></tr><tr><td>

recurringPattern.options.endDate

</td><td>

Required if **recurringPattern.options.count** is not passed. If both are passed, **count** is used. End date and time of the recurrence of the meeting, such as "2022-07-08T14:00:00Z".Data type: String

Format: UTC yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

recurringPattern.repeats

</td><td>

Required. Repeating pattern for the reservable.Valid values \(case-sensitive\):

-   daily
-   monthly
-   weekly
-   yearly

Data type: String

</td></tr><tr><td>

recurringPattern.startDate

</td><td>

Required. Start date and time for the recurring pattern, such as "2022-07-08T14:00:00Z".Data type: String

Format: UTC yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

reservableIds

</td><td>

Required. List of sys\_ids of the reservables to include in the availability score.Data type: Array

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

reservableType

</td><td>

Required. Type of reservable to include in the availability score. Used to refine the search.Valid values \(case-sensitive\):

-   configuration\_item
-   location

Data type: String

</td></tr><tr><td>

startEndDateTimes

</td><td>

List of start and end dates and times in the user's timezone to search on.Data type: Array of Objects

```
"startEndDateTimes": [
  {
    "end": "String",
    "start": "String"
  }
]
```

Default: Must specify **recurringPattern** parameter.

</td></tr><tr><td>

startEndDateTimes.end

</td><td>

End date and time of the reservable.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

startEndDateTimes.start

</td><td>

Start date and time of the reservable.Data type: String

Format: yyyy-mm-dd hh:mm:ss

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

</td><td>

Return results for the specified availability score.Data type: Object

```
"result": {
  "reservable_sys_id": {Object}
}
```

</td></tr><tr><td>

result.reservable\_sys\_id

</td><td>

Details about the availability score.Data type: Object

```
"reservable_sys_id": {
  "available": Number,
  "score": "String",
  "total": Number
}
```

</td></tr><tr><td>

result.reservable\_sys\_id.available

</td><td>

Number of available reservables that met the specified search criteria.Data type: Number

</td></tr><tr><td>

result.reservable\_sys\_id.score

</td><td>

Availability score. Number of available reservables over the total number of reservables that met the specified search criteria. For example, if **available** is 2 and **total** is 4, the **score** value is 2/4.Data type: String

</td></tr><tr><td>

result.reservable\_sys\_id.total

</td><td>

Total number of reservables that met the specified search criteria.Data type: Number

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/search/availability_score" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"reservableType\": \"location\",
  \"reservableIds\": [
    \"fe1f744edb7650106c731dcd139619ca\",
    \"5eafb44edb7650106c731dcd13961943\"
  ],
  \"recurringPattern\": {
    \"duration\": 3600000,
    \"repeats\": \"daily\",
    \"options\": {
      \"count\": 150,
      \"daysOfWeek\": \"\",
    },
    \"label\": \"Repeats daily, 5 times\",
    \"startDate\": \"2022-04-26T14:00:00Z\"
  },
  \"startEndDateTimes\": [
    {
      \"start\": \"2022-07-05 14:00:00\",
      \"end\": \"2022-07-05 15:00:00\"
    },
    {
      \"start\": \"2022-07-06 14:00:00\",
      \"end\": \"2022-07-06 15:00:00\"
    }
  ]
}" \
--user "username":"password"
```

Return results:

```
{
  "result": {
    "fe1f744edb7650106c731dcd139619ca": {
      "available": 2,
      "total": 2,
      "score": "2/2"
    },
    "5eafb44edb7650106c731dcd13961943": {
      "available": 2,
      "total": 2,
      "score": "2/2"
    }
  }

```

