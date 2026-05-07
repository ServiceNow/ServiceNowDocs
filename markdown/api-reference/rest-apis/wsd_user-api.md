---
title: WSD User API
description: The WSD User API is a Scripted REST API which returns the authenticated user's workplace context, including their assigned workspace location, in-office presence schedule, collaborators, and past and future reservations.Retrieves the authenticated user's workplace context, including their assigned workplace location, presence schedule, collaborators, and past and future reservations.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 9
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD User API

The WSD User API is a Scripted REST API which returns the authenticated user's workplace context, including their assigned workspace location, in-office presence schedule, collaborators, and past and future reservations.

This WSD User is featured with the Workplace Service Delivery \(WSD\) Reservation product and provides a single-call entry point for initializing the reservation booking experience with all relevant user data. This API sits within the Workplace Service Delivery Reservation \(com.sn\_wsd\_rsv\) plugin and serves as the entry point for surfacing a user's complete workplace identity and history.

An authenticated user is someone who is logged in or whose credentials are included in the API request.

Common use cases:

-   Reservation portal initialization: Load a user's home location, schedule, and booking history in a single call when opening a workplace app or portal.
-   Custom mobile or web apps: Fetch all the user context without stitching together multiple table API calls,for example when building front-end reservation experiences.
-   In-office presence tracking: Identify which employees are scheduled to be in-office on a given day.

## Requirements

The WSD User API requires:

-   At least one user record must exist with the sn\_wsd\_core.workplace\_user role.
-   The Workplace Service Delivery Concierge \(com.sn\_wsd\_concierge\), Workplace Service Delivery Core \(com.sn\_wsd\_core\), and Workplace Service Delivery Reservation \(com.sn\_wsd\_rsv\) plugins to be active.

## Related APIs

The WSD User API belongs to a family of APIs all under the `sn_wsd_rsv` namespace that together support the full reservation lifecycle:

-   WSD Search API: Find available reservable spaces based on location, time, and capacity criteria.
-   WSD Reservation API: Create reservations and manage check-in/check-out.
-   WSD Reservable Module API: Retrieve the booking rule configurations that govern what users can reserve and how.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD User - GET /api/sn\_wsd\_rsv/v1/user/context

Retrieves the authenticated user's workplace context, including their assigned workplace location, presence schedule, collaborators, and past and future reservations.

Use this endpoint to initialize a reservation experience by loading all relevant user context in a single call. Collaborator data is optionally included when the com.sn\_wsd\_concierge plugin is active.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/user/context`

Default URL: `/api/sn_wsd_rsv/user/context`

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

include

</td><td>

Value to include related data in the response. Uses strict equality matching \(not comma-separated parsing\).**Note:** **include** is only effective when the Workplace Service Delivery Concierge \(com.sn\_wsd\_concierge\) plugin is active.

Only valid value: `collaborators`

Data type: String

Default: Excludes collaborators from the response.

</td></tr><tr><td>

past\_reservations\_months

</td><td>

Number of months of past reservations to return.Data type: Number

Minimum value: `0`

Maximum value: `12`

Default value: `3`

</td></tr><tr><td>

future\_reservations\_months

</td><td>

Number of months of future reservations to return.Data type: Number

Minimum value: `0`

Maximum value: `12`

Default value: `3`

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: application/json, application/xml, text/xml.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing results of the request.Data type: Object

```
"result": {
  "collaborators": [Array],
  "reservations": {Object},
  "schedule": {Object},
  "workplace_location": {Object}
}
```

</td></tr><tr><td>

collaborators

</td><td>

List of the user's collaborators with their presence data.Data type: Array of Objects

```
"collaborators": [
  {
    "sys_id": "String",
    "name": "String",
    "routine": "Object",
    "exceptions": "Array"
  }
]
```

</td></tr><tr><td>

collaborators.exceptions

</td><td>

List of dates on which the collaborator's in-office schedule deviates from their routine.Contains a Boolean flag for each day of the week indicating planned office attendance. Displays `true` when the user plans to be in-office that day, and `false` when attendance isn't planned.

Data type: Array of Objects

```
"exceptions": [
{ 
   "monday": "Boolean", 
   "tuesday": "Boolean", 
   "wednesday": "Boolean", 
   "thursday": "Boolean", 
   "friday": "Boolean", 
   "saturday": "Boolean", 
   "sunday": "Boolean" 
}
]
```

</td></tr><tr><td>

collaborators.name

</td><td>

Display name of the collaborator. For example, `Jane Smith`.Data type: String

</td></tr><tr><td>

collaborators.routine

</td><td>

The collaborator's recurring weekly in-office schedule. Follows the same day-of-week Boolean structure as **schedule.routine**.A value of `true` indicates in-office attendance, and `false` indicates no attendance.

Data type: Object

```
"routine": {
  "monday": Boolean,
  "tuesday": Boolean,
  "wednesday": Boolean,
  "thursday": Boolean, 
  "friday": Boolean,
  "saturday": Boolean,
  "sunday": Boolean
}
```

</td></tr><tr><td>

collaborators.sys\_id

</td><td>

Sys\_id of the collaborator's user record. Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

reservations

</td><td>

Object containing the user's past and future reservations. Private and location-less reservations are excluded. Maximum 100 reservations per direction.

Filtered by states: confirmed, completed.

Data type: Object

```
"reservations": {
  "past": [Array],
  "future": [Array]
}
```

</td></tr><tr><td>

reservations.future

</td><td>

List of the user's future reservations within the requested month range. Ordered by start datetime, soonest first.Data type: Array of Object

```
"future": [
 {
  "sys_id": "String",
  "number": "String",
  "start": "String",
  "end": "String",
  "state": "String",
  "subject": "String,
  "location": {Object},
  "building": {Object}
 }
]
```

</td></tr><tr><td>

reservations.future.building

</td><td>

Building in which the reserved location resides.Data type: Object

```
"building": {
 "name": "String",
 "sys_id": "String"
}
```

</td></tr><tr><td>

reservations.future.building.name

</td><td>

Display name of the building. For example, `HQ Building A`.Data type: String

</td></tr><tr><td>

reservations.future.building.sys\_id

</td><td>

Sys\_id of the building record.Table: Workplace Building \[sn\_wsd\_core\_building\]

Data type: String

</td></tr><tr><td>

reservations.future.end

</td><td>

End date time of the reservation in UTC. Format: yyyy-MM-dd HH:mm:ss

Data type: String

</td></tr><tr><td>

reservations.future.location

</td><td>

The reserved space.Data type: Object

```
"location": {
  "sys_id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

reservations.future.location.name

</td><td>

Display name of the reserved location. For example, `Desk 42`. Data type: String

</td></tr><tr><td>

reservations.future.location.sys\_id

</td><td>

Sys\_id of the reserved location.Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

Data type: String

</td></tr><tr><td>

reservations.future.number

</td><td>

Human-readable reservation number. For example, `RSV0001234`.Data type: String

</td></tr><tr><td>

reservations.future.start

</td><td>

Start date time of the reservation in UTC.Format: yyyy-MM-dd HH:mm:ss

Data type: String

</td></tr><tr><td>

reservations.future.state

</td><td>

Current state of the reservation. Valid values:

-   `confirmed`
-   `completed`

Data type: String

</td></tr><tr><td>

reservations.future.subject

</td><td>

Subject or title of the reservation. For example, `Team standup desk`.Data type: String

</td></tr><tr><td>

reservations.future.sys\_id

</td><td>

Sys\_id of the reservation record. Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

Data type: String

</td></tr><tr><td>

reservations.past

</td><td>

List of the user's past reservations within the requested month range. Ordered by start datetime, most recent first.Follows the same array structure as **reservation.future**.

Data type: Array of Objects

```
"past": [
 {
  "sys_id": "String",
  "number": "String",
  "start": "String",
  "end": "String",
  "state": "String",
  "subject": "String,
  "location": {Object},
  "building": {Object}
 }
]
```

</td></tr><tr><td>

schedule

</td><td>

User's in-office presence schedule, including their recurring weekly routine and any exceptions.**Note:** When the com.sn\_wsd\_concierge plugin is inactive, routine is null and exceptions is an empty array.

Data type: Object

```
"schedule": {
  "exceptions": [Array],
  "routine": {Object}
}
```

</td></tr><tr><td>

schedule.exceptions

</td><td>

List of dates on which the user's in-office schedule deviates from their routine.Data type: Array of Objects

```
"exceptions": [
{
  "sys_id": "sys_id", 
  "date": "String", 
  "in_office": String, 
  "origin": "String", 
  "location": "String" 
 }
]
```

</td></tr><tr><td>

schedule.exceptions.date

</td><td>

Date this exception applies to, in yyyy-MM-dd format. This is the date the user's routine is being overridden.Data type: String

</td></tr><tr><td>

schedule.exceptions.in\_office

</td><td>

Flag that indicates whether the user will be in the office on this date. This overrides whatever the schedule specifies for that day of the week.Valid values:

-   true: User will be in the office.
-   false: User won't be in the office

Data type: String

</td></tr><tr><td>

schedule.exceptions.location

</td><td>

The name or identifier of the office location the user will be at on this date. Only relevant when `in_office` is `true`. May be an empty string when the user is remote.Data type: String

</td></tr><tr><td>

schedule.exceptions.origin

</td><td>

Source that created the exception.Valid values:

-   `user`: Created manually by the employee.
-   `system`: Created automatically by the platform.
-   `manual`: Created by an admin or on behalf of the user.

Data type: String

</td></tr><tr><td>

schedule.exceptions.sys\_id

</td><td>

Sys\_id of the exception record.Table: Employee presence exceptions \(sn\_wsd\_concierge\_employee\_presence\_exception\)

Data type: String

</td></tr><tr><td>

schedule.routine

</td><td>

User's recurring weekly in-office schedule. Each field is a Boolean which represents a day of the week and indicates whether the user is scheduled to be in-office on that day.A value of `true` indicates in-office attendance, and `false` indicates no attendance.

Data type: Object

```
"routine": {
  "monday": Boolean,
  "tuesday": Boolean,
  "wednesday": Boolean,
  "thursday": Boolean, 
  "friday": Boolean,
  "saturday": Boolean,
  "sunday": Boolean
}
```

</td></tr><tr><td>

workplace\_location

</td><td>

The user's assigned workplace location, including floor, building, and campus details.Data type: Object

```
"workplace_location": {
  "building": {Object},
  "campus": {Object},
  "floor": {Object},
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

workplace\_location.building

</td><td>

Building in which the workplace location resides. Data type: Object

```
"building": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

workplace\_location.building.name

</td><td>

Display name of the building. For example, `HQ Building A`. Data type: String

</td></tr><tr><td>

workplace\_location.building.sys\_id

</td><td>

Sys\_id of the building record. Table: Workplace Building \[sn\_wsd\_core\_building\]

Data type: String

</td></tr><tr><td>

workplace\_location.campus

</td><td>

Campus on which the building resides. Data type: Object

```
"campus": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

workplace\_location.campus.name

</td><td>

Display name of the campus. For example, `Main Campus`.Data type: String

</td></tr><tr><td>

workplace\_location.campus.sys\_id

</td><td>

Sys\_id of the campus record.Table: Workplace Campus \[sn\_wsd\_core\_campus\]

Data type: String

</td></tr><tr><td>

workplace\_location.floor

</td><td>

Floor on which the workplace location resides. Data type: Object

```
"floor": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

workplace\_location.floor.name

</td><td>

Sys\_id of the floor record. Table: Workplace Floor \[sn\_wsd\_core\_floor\]

Data type: String

</td></tr><tr><td>

workplace\_location.floor.sys\_id

</td><td>

Display name of the floor. For example, `Floor 3`. Data type: String

</td></tr><tr><td>

workplace\_location.name

</td><td>

Display name of the user's assigned workplace location. For example, `Desk 42 - Floor 3`. Data type: String

</td></tr><tr><td>

workplace\_location.sys\_id

</td><td>

Sys\_id of the user's assigned workplace location. Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example retrieves the authenticated user's full workplace context, including collaborators, 1 month of past reservations, and 6 months of future reservations.

```
curl "https://<instance>.service-now.com/api/sn_wsd_rsv/v1/user/context?include=collaborators&past_reservations_months=1&future_reservations_months=6" \
  --request GET \
  --header "Accept: application/json" \
  --user "username:password"
```

Response body.

```
{
  "result": {
    "workplace_location": {
      "sys_id": "a1b2c3d4e5f6g7h8",
      "name": "Desk 42 - Floor 3",
      "floor": { "sys_id": "f1a2b3c4", "name": "Floor 3" },
      "building": { "sys_id": "b1c2d3e4", "name": "HQ Building A" },
      "campus": { "sys_id": "c1d2e3f4", "name": "Main Campus" }
    },
    "schedule": {
      "routine": {
        "monday": true, "tuesday": true, "wednesday": false,
        "thursday": true, "friday": false, "saturday": false, "sunday": false
      },
      "exceptions": []
    },
    "collaborators": [
      {
        "sys_id": "d4e5f6g7",
        "name": "Jane Smith",
        "routine": { "monday": true, "tuesday": false, "wednesday": true,
                     "thursday": true, "friday": false, "saturday": false, "sunday": false },
        "exceptions": []
      }
    ],
    "reservations": {
      "past": [
        {
          "sys_id": "r1e2s3v4",
          "number": "RSV0001234",
          "start": "2026-04-01 09:00:00",
          "end": "2026-04-01 17:00:00",
          "state": "completed",
          "subject": "Team standup desk",
          "location": { "sys_id": "l1o2c3", "name": "Desk 42" },
          "building": { "sys_id": "b1c2d3e4", "name": "HQ Building A" }
        }
      ],
      "future": []
    }
  }
}
```

