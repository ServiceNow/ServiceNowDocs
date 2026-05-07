---
title: WSD Presence API
description: The WSD Presence API enables users to manage their in-office presence schedule, including weekly routines, one-time exceptions, and collaborator visibility.Removes a collaborator from the authenticated user’s presence visibility list. Use this endpoint when a user no longer wants to track a colleague’s office attendance.Deletes a specific presence exception identified by its sys\_id. Use this endpoint when a user wants to remove a one-time override and revert to their regular weekly routine for that date.Retrieves the list of collaborators for the authenticated user along with each collaborator’s presence data, routine, and exceptions. Use this endpoint to view the office attendance schedules of colleagues, enabling coordinated in-office planning.Retrieves presence exceptions for the authenticated user. Exceptions can be filtered by a date range or by a specific exception sys\_id. Use this endpoint when you need to view one-time overrides to a user’s weekly routine.Retrieves the authenticated user’s complete presence data, including their weekly in-office routine, scheduled presence exceptions, and optionally their collaborators’ presence information.Retrieves only the authenticated user’s weekly in-office routine. This is a lightweight alternative to GET /presence when you only need the routine schedule without exceptions or collaborators.Partially updates the authenticated user’s weekly in-office routine. Use this endpoint when a user needs to adjust specific days without resetting the entire schedule.Adds one or more collaborators to the authenticated user’s presence visibility list. Collaborators can then view each other’s presence data. Use this endpoint to build a team or group of colleagues whose office attendance you want to track.Creates a one-time presence exception for the authenticated user on a specific date. Use this endpoint when a user plans to be in the office on a day they normally work remotely, or vice versa.Creates a new weekly in-office routine for the authenticated user. Use this endpoint when a user is setting up their presence routine for the first time.Updates an existing presence exception by canceling it and creating a replacement. The original exception is identified by its sys\_id. Use this endpoint when a user needs to change the details of a previously created exception.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-04-27"
reading_time_minutes: 37
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD Presence API

The WSD Presence API enables users to manage their in-office presence schedule, including weekly routines, one-time exceptions, and collaborator visibility.

This API supports the Workplace Service Delivery \(WSD\) Concierge experience by enabling employees to communicate their planned office attendance to colleagues. Use this API for the following actions:

-   Retrieve an authenticated user's complete presence data, including their weekly in-office routine, scheduled exceptions, and optionally collaborators' presence information.
-   Manage weekly in-office routines so employees can set a recurring schedule.
-   Create and manage one-time exceptions that override the routine for a specific date.
-   View and manage collaborators to enable coordinated in-office planning.

An authenticated user is someone who is logged in or whose credentials are included in the API request. Call endpoints in any order; each operates independently.

The WSD Presence API belongs to the sn\_wsd\_concierge namespace. The [WSD Reservation API](wsd_reservation-api.md#) `GET /user/context` endpoint can return presence schedule data from the WSD Presence API when the concierge plugin is active.

## Requirements

The WSD Presence API requires:

-   The sn\_wsd\_core.workplace\_user role assigned to the user.
-   The Workplace Service Delivery Core \(com.sn\_wsd\_core\) plugin activated.
-   At least one user record must exist in sys\_user with the sn\_wsd\_core.workplace\_user role assigned.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD Presence - DELETE /api/sn\_wsd\_concierge/v1/presence/collaborator/\{collaborator\_id\}

Removes a collaborator from the authenticated user’s presence visibility list. Use this endpoint when a user no longer wants to track a colleague’s office attendance.

An authenticated user is someone who is logged in or whose credentials are included in the API request. The collaborator is identified by their sys\_id.

### URL format

Versioned URL: `/api/sn_wsd_concierge/{api_version}/presence/collaborator/{collaborator_id}`

Default URL: `/api/sn_wsd_concierge/presence/collaborator/{collaborator_id}`

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

collaborator\_id

</td><td>

Sys\_id of the collaborator to remove from the user’s visibility list.Table: User \[sys\_user\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: **application/json**, **application/xml**, or **text/xml**.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Missing or invalid collaborator\_id path parameter.|
|404|Not Found. The specified collaborator wasn't found.|
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
  "message": "String"
}
```

</td></tr><tr><td>

result.message

</td><td>

Confirmation message indicating the number of collaborators removed.Data type: String

</td></tr></tbody>
</table>### cURL request

This example removes a specific collaborator from the authenticated user’s presence visibility list.

```
curl "https://<instance>.service-now.com/api/sn_wsd_concierge/v1/presence/collaborator/usr1a2b3c4d5e6" \
--request DELETE \
--header "Accept: application/json" \
--user "username:password"
```

Response body.

```
{
  "result": {
    "message": "1 collaborator(s) removed"
  }
}
```

## WSD Presence - DELETE /api/sn\_wsd\_concierge/v1/presence/exception/\{exception\_id\}

Deletes a specific presence exception identified by its sys\_id. Use this endpoint when a user wants to remove a one-time override and revert to their regular weekly routine for that date.

### URL format

Versioned URL: `/api/sn_wsd_concierge/{api_version}/presence/exception/{exception_id}`

Default URL: `/api/sn_wsd_concierge/presence/exception/{exception_id}`

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

exception\_id

</td><td>

Required. Sys\_id of the presence exception to delete.Table: Employee presence exceptions \(sn\_wsd\_concierge\_employee\_presence\_exception\)

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: **application/json**, **application/xml**, or **text/xml**.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Missing or invalid exception\_id path parameter.|
|404|Not Found. The specified exception wasn't found.|
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
  "message": "String"
}
```

</td></tr><tr><td>

result.message

</td><td>

Confirmation message indicating the exception was deleted.Data type: String

</td></tr></tbody>
</table>### cURL request

This example deletes exception exc1a2b3c4d5e6, reverting that date to the user’s regular weekly routine.

```
curl "https://<instance>.service-now.com/api/sn_wsd_concierge/v1/presence/exception/exc1a2b3c4d5e6" \
--request DELETE \
--header "Accept: application/json" \
--user "username:password"
```

Response body.

```
{
  "result": {
    "message": "Exception deleted successfully"
  }
}
```

## WSD Presence - GET /api/sn\_wsd\_concierge/v1/presence/collaborator

Retrieves the list of collaborators for the authenticated user along with each collaborator’s presence data, routine, and exceptions. Use this endpoint to view the office attendance schedules of colleagues, enabling coordinated in-office planning.

### URL format

Versioned URL: `/api/sn_wsd_concierge/{api_version}/presence/collaborator`

Default URL: `/api/sn_wsd_concierge/presence/collaborator`

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

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: **application/json**, **application/xml**, or **text/xml**.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|404|Not Found. The user wasn't found.|
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
  "count": Number,
  "collaborators": [Array]
}
```

</td></tr><tr><td>

result.count

</td><td>

Total number of collaborators returned. Data type: Number

</td></tr><tr><td>

result.collaborators

</td><td>

List of collaborators with their presence data. If a collaborator has privacy enabled, **privacy\_enabled** is true with null **routine** and empty **exceptions**.

Data type: Array of Objects

```
"collaborators": [
 {
  "sys_id": "String", 
  "name": "String", 
  "privacy_enabled": Boolean,
  "routine": {Object},
  "exceptions": [Array]
 }
]
```

</td></tr><tr><td>

result.collaborators.sys\_id

</td><td>

Sys\_id of the collaborator's user record.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

result.collaborators.name

</td><td>

Display name of the collaborator as it appears in their sys\_user record.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

result.collaborators.privacy\_enabled

</td><td>

Boolean. Flag that indicates whether the collaborator has enabled privacy on their presence data.Valid values:

-   `true`: The collaborator's routine and exceptions are hidden. **routine** will be `null` and **exceptions** will be an empty array.
-   `false`: The collaborator's presence data is visible.

Data type: Boolean

</td></tr><tr><td>

result.collaborators.routine

</td><td>

Collaborator's weekly in-office routine. Contains a Boolean flag for each day of the week indicating planned office attendance. Displays `true` when collaborator plans to be in-office for that day, and `false` when attendance isn't planned.

Data type: Object

```
"routine": { 
   "monday": "Boolean", 
   "tuesday": "Boolean", 
   "wednesday": "Boolean", 
   "thursday": "Boolean", 
   "friday": "Boolean", 
   "saturday": "Boolean", 
   "sunday": "Boolean" 
}
```

</td></tr><tr><td>

result.collaborators.exceptions

</td><td>

Collaborator's one-time presence exceptions. Returns an empty array if `privacy_enabled` is `true`.Data type: Array of Objects

```
"exceptions": [ 
 { 
  "sys_id": "String", 
  "date": "String", 
  "in_office": "Boolean", 
  "origin": "String", 
  "location": "String" 
 } 
]
```

</td></tr><tr><td>

result.collaborators.exceptions.sys\_id

</td><td>

Sys\_id of the exception record.Table: Employee presence exceptions \(sn\_wsd\_concierge\_employee\_presence\_exception\)

Data type: String

</td></tr><tr><td>

result.collaborators.exceptions.date

</td><td>

Date this exception applies to. This is the date the user's routine is being overridden.Format: yyyy-MM-dd

Data type: String

</td></tr><tr><td>

result.collaborators.exceptions.in\_office

</td><td>

Flag that indicates whether the user will be in the office on this date. This overrides whatever the weekly routine specifies for that day of the week.Valid values:

-   `true`: User will be in the office.
-   `false`: User won't be in the office

Data type: String

</td></tr><tr><td>

result.collaborators.exceptions.origin

</td><td>

Source that created the exception.Valid values:

-   `user`: Created manually by the employee.
-   `system`: Created automatically by the platform.
-   `manual`: Created by an admin or on behalf of the user.

Data type: String

</td></tr><tr><td>

result.collaborators.exceptions.location

</td><td>

Name or identifier of the office location the user will be at on this date. Only relevant when `in_office` is `true`. May be an empty string when the user is remote.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves all collaborators and their presence data for the authenticated user.

```
curl "https://<instance>.service-now.com/api/sn_wsd_concierge/v1/presence/collaborator" \
--request GET \
--header "Accept: application/json" \
--user "username:password"
```

Response body.

```
{
  "result": {
    "count": 2,
    "collaborators": [
      {
        "sys_id": "usr1a2b3c4d5e6", "name": "Jane Smith", "privacy_enabled": false,
        "routine": {
          "monday": true, "tuesday": true, "wednesday": false,
          "thursday": true, "friday": false, "saturday": false, "sunday": false
        },
        "exceptions": [
          { "sys_id": "exc1a2b3c", "date": "2026-03-10", "in_office": true, "origin": "user", "location": "Building B" }
        ]
      },
      { "sys_id": "usr7f8g9h0i1j2", "name": "John Doe", "privacy_enabled": true, "routine": null, "exceptions": [] }
    ]
  }
}
```

## WSD Presence - GET /api/sn\_wsd\_concierge/v1/presence/exception

Retrieves presence exceptions for the authenticated user. Exceptions can be filtered by a date range or by a specific exception sys\_id. Use this endpoint when you need to view one-time overrides to a user’s weekly routine.

### URL format

Versioned URL: `/api/sn_wsd_concierge/{api_version}/presence/exception`

Default URL: `/api/sn_wsd_concierge/presence/exception`

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

exception\_id

</td><td>

Sys\_id of a specific exception to retrieve.When provided, overrides the date range filter and returns only the matching exception.

Table: Employee presence exceptions \(sn\_wsd\_concierge\_employee\_presence\_exception\)

Data type: String

</td></tr><tr><td>

exception\_start\_date

</td><td>

Start date for filtering exceptions.Format: yyyy-MM-dd

Data type: String

Default: Today

</td></tr><tr><td>

exception\_end\_date

</td><td>

End date for filtering exceptions.Format: yyyy-MM-dd

Data type: String

Default: Today +3 months

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: **application/json**, **application/xml**, or **text/xml**.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Invalid date format for exception\_start\_date or exception\_end\_date.|
|404|Not Found. The specified exception wasn't found.|
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
  "exceptions": [Array]
}
```

</td></tr><tr><td>

result.exceptions

</td><td>

List of presence exceptions matching the filter criteria.Data type: Array of Objects

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

result.exceptions.date

</td><td>

Date this exception applies to. This is the date the user's routine is being overridden.Format: yyyy-MM-dd format

Data type: String

</td></tr><tr><td>

result.exceptions.in\_office

</td><td>

Flag that indicates whether the user will be in the office on this date. This overrides whatever the weekly routine specifies for that day of the week.Valid values:

-   `true`: User will be in the office.
-   `false`: User won't be in the office

Data type: String

</td></tr><tr><td>

result.exceptions.location

</td><td>

The name or identifier of the office location the user will be at on this date. Only relevant when `in_office` is `true`. May be an empty string when the user is remote.Data type: String

</td></tr><tr><td>

result.exceptions.origin

</td><td>

Source that created the exception.Valid values:

-   `user`: Created manually by the employee.
-   `system`: Created automatically by the platform.
-   `manual`: Created by an admin or on behalf of the user.

Data type: String

</td></tr><tr><td>

result.exceptions.sys\_id

</td><td>

Sys\_id of the exception record.Table: Employee presence exceptions \(sn\_wsd\_concierge\_employee\_presence\_exception\)

Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves all exceptions for the first half of 2026.

```
curl "https://<instance>.service-now.com/api/sn_wsd_concierge/v1/presence/exception?exception_start_date=2026-01-01&exception_end_date=2026-06-30" \
--request GET \
--header "Accept: application/json" \
--user "username:password"
```

Response body.

```
{
  "result": {
    "exceptions": [
      { "sys_id": "exc1a2b3c4d5e6", "date": "2026-02-14", "in_office": true, "origin": "user", "location": "Building A" },
      { "sys_id": "exc7f8g9h0i1j2", "date": "2026-03-17", "in_office": false, "origin": "system", "location": "" }
    ]
  }
}
```

## WSD Presence - GET /api/sn\_wsd\_concierge/v1/presence

Retrieves the authenticated user’s complete presence data, including their weekly in-office routine, scheduled presence exceptions, and optionally their collaborators’ presence information.

Use this endpoint to get a holistic view of a user’s planned office attendance. You can also query another user’s presence data by providing their sys\_id, subject to privacy settings.

### URL format

Versioned URL: `/api/sn_wsd_concierge/{api_version}/presence`

Default URL: `/api/sn_wsd_concierge/presence`

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

user\_id

</td><td>

Sys\_id of the target user whose presence data to retrieve. If not provided, returns presence data for the authenticated user.**Note:** Cross-user queries return 401 Unauthorized unless the caller has explicit permission.

Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

exception\_start\_date

</td><td>

Start date for filtering presence exceptions.Format: yyyy-MM-dd

Data type: String

Default: Today

</td></tr><tr><td>

exception\_end\_date

</td><td>

End date for filtering presence exceptions.Format: yyyy-MM-dd

Data type: String

Default: Today + 3 months

</td></tr><tr><td>

include

</td><td>

Related data to include in the response.Only valid value: `collaborators`

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: **application/json**, **application/xml**, or **text/xml**.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Invalid date format for exception\_start\_date or exception\_end\_date, or invalid user\_id format.|
|401|Unauthorized. The authenticated user doesn't have permission to view the target user’s presence data. Returned when user\_id is provided and doesn't match the authenticated user.|
|404|Not Found. The specified user wasn't found.|
|500|Internal Server Error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing results of the response.```
"result": {
  "routine": {Object},
  "exceptions": [Array],
  "collaborators": [Array]
}
```

</td></tr><tr><td>

result.routine

</td><td>

Weekly in-office routine for the user. Contains a Boolean flag for each day of the week indicating planned office attendance. Displays `true` when the authenticated user plans to be in-office that day, and `false` when attendance isn't planned.

Data type: Object

```
"routine": { 
   "monday": "Boolean", 
   "tuesday": "Boolean", 
   "wednesday": "Boolean", 
   "thursday": "Boolean", 
   "friday": "Boolean", 
   "saturday": "Boolean", 
   "sunday": "Boolean" 
}
```

</td></tr><tr><td>

result.exceptions

</td><td>

List of one-time presence exceptions that override the user’s routine for specific dates.Data type: Array of Objects

```
"exceptions": [ 
   { 
     "sys_id": "String", 
     "date": "String", 
     "in_office": "Boolean", 
     "origin": "String", 
     "location": "String" 
   } 
]
```

</td></tr><tr><td>

result.exceptions.sys\_id

</td><td>

Sys\_id of the exception record.Table: Employee presence exceptions \(sn\_wsd\_concierge\_employee\_presence\_exception\)

Data type: String

</td></tr><tr><td>

result.exceptions.date

</td><td>

Date this exception applies to, in yyyy-MM-dd format. This is the date the user's routine is being overridden.Data type: String

</td></tr><tr><td>

result.exceptions.in\_office

</td><td>

Flag that indicates whether the user will be in the office on this date. This overrides whatever the weekly routine specifies for that day of the week.Valid values:

-   `true`: User will be in the office.
-   `false`: User won't be in the office

Data type: String

</td></tr><tr><td>

result.exceptions.origin

</td><td>

Source that created the exception.Valid values:

-   `user`: Created manually by the employee.
-   `system`: Created automatically by the platform.
-   `manual`: Created by an admin or on behalf of the user.

Data type: String

</td></tr><tr><td>

result.exceptions.location

</td><td>

The name or identifier of the office location the user will be at on this date. Only relevant when `in_office` is `true`. May be an empty string when the user is remote.Data type: String

</td></tr><tr><td>

result.collaborators

</td><td>

List of collaborators and their presence data. Only returned when `include=collaborators` is specified.If a collaborator has privacy enabled, **privacy\_enabled** is true with null **routine** and empty **exceptions**.

Data type: Array of Objects

```
"collaborators": [ 
   { 
     "sys_id": "String", 
     "name": "String", 
     "privacy_enabled": Boolean, 
     "routine": {Object}, 
     "exceptions": [Array]
   } 
]
```

</td></tr><tr><td>

result.collaborators.sys\_id

</td><td>

Sys\_id of the collaborator's user record.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

result.collaborators.name

</td><td>

The display name of the collaborator as it appears in their sys\_user record.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

result.collaborators.privacy\_enabled

</td><td>

Boolean. Flag that indicates whether the collaborator has enabled privacy on their presence data.Valid values:

-   `true`: The collaborator's routine and exceptions are hidden. **routine** will be `null` and **exceptions** will be an empty array.
-   `false`: The collaborator's presence data is visible.

Data type: Boolean

</td></tr><tr><td>

result.collaborators.routine

</td><td>

The collaborator's weekly in-office routine.Contains a Boolean flag for each day of the week indicating planned office attendance. Displays `true` when the collaborator plans to be in-office that day, and `false` when attendance isn't planned.

Data type: Object

```
"routine": { 
   "monday": "Boolean", 
   "tuesday": "Boolean", 
   "wednesday": "Boolean", 
   "thursday": "Boolean", 
   "friday": "Boolean", 
   "saturday": "Boolean", 
   "sunday": "Boolean" 
}
```

</td></tr><tr><td>

result.collaborators.exceptions

</td><td>

The collaborator's one-time presence exceptions. Follows the same structure as the authenticated user's **exceptions** parameter. Returns an empty array if `privacy_enabled` is `true`.Data type: Array of Objects

```
"exceptions": [ 
   { 
     "sys_id": "String", 
     "date": "String", 
     "in_office": "Boolean", 
     "origin": "String", 
     "location": "String" 
   } 
]
```

</td></tr></tbody>
</table>### cURL request

This example retrieves the authenticated user’s full presence data, including collaborator schedules, for exceptions in Q1 2026.

```
curl "https://<instance>.service-now.com/api/sn_wsd_concierge/v1/presence?include=collaborators&exception_start_date=2026-01-01&exception_end_date=2026-03-31" \
--request GET \
--header "Accept: application/json" \
--user "username:password"
```

Response body.

```
{
  "result": {
    "routine": {
      "monday": true,  "tuesday": false, "wednesday": true,
      "thursday": true, "friday": false, "saturday": false, "sunday": false
    },
    "exceptions": [
      {
        "sys_id": "a1b2c3d4e5f6",
        "date": "2026-02-14",
        "in_office": true,
        "origin": "user",
        "location": "Building A"
      }
    ],
    "collaborators": [
      {
        "sys_id": "f6e5d4c3b2a1",
        "name": "Jane Smith",
        "privacy_enabled": false,
        "routine": {
          "monday": true, "tuesday": true, "wednesday": false,
          "thursday": true, "friday": false, "saturday": false, "sunday": false
        },
        "exceptions": []
      }
    ]
  }
}

```

## WSD Presence - GET /api/sn\_wsd\_concierge/v1/presence/routine

Retrieves only the authenticated user’s weekly in-office routine. This is a lightweight alternative to GET /presence when you only need the routine schedule without exceptions or collaborators.

### URL format

Versioned URL: `/api/sn_wsd_concierge/{api_version}/presence/routine`

Default URL: `/api/sn_wsd_concierge/presence/routine`

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

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: **application/json**, **application/xml**, or **text/xml**.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|404|Not Found. The user or routine wasn't found.|
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
  "user_id": "String",
  "routine": {Object}
}
```

</td></tr><tr><td>

result.user\_id

</td><td>

Sys\_id of the user whose routine is returned.Table: User \[sys\_id\]

Data type: String

</td></tr><tr><td>

result.routine

</td><td>

User's recurring weekly in-office schedule. Contains a Boolean flag for each day of the week indicating planned office attendance. Displays `true` when the user plans to be in-office that day, and `false` when attendance isn't planned.

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

</td></tr></tbody>
</table>### cURL request

This example retrieves the weekly in-office routine for the authenticated user.

```
curl "https://<instance>.service-now.com/api/sn_wsd_concierge/v1/presence/routine" \
--request GET \
--header "Accept: application/json" \
--user "username:password"
```

Response body. Shows that the user's routine shows in-office attendance for Monday through Thursday.

```
{
  "result": {
    "user_id": "a1b2c3d4e5f6g7h8",
    "routine": {
      "monday": true,  "tuesday": true,  "wednesday": true,
      "thursday": true, "friday": false, "saturday": false, "sunday": false
    }
  }
}
```

## WSD Presence - PATCH /api/sn\_wsd\_concierge/v1/presence/routine

Partially updates the authenticated user’s weekly in-office routine. Use this endpoint when a user needs to adjust specific days without resetting the entire schedule.

Only the days provided in the request body are updated. All other days remain unchanged.

### URL format

Versioned URL: `/api/sn_wsd_concierge/{api_version}/presence/routine`

Default URL: `/api/sn_wsd_concierge/presence/routine`

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

routine

</td><td>

Required. The authenticated user's weekly routine.Contains a Boolean flag for each day of the week indicating planned office attendance. Displays `true` when the authenticated user plans to be in-office that day, and `false` when attendance isn't planned.

Days omitted in the request remain unchanged. An empty routine object is accepted as a no-op.

Data type: Object

```
"routine": { 
   "monday": "Boolean", 
   "tuesday": "Boolean", 
   "wednesday": "Boolean", 
   "thursday": "Boolean", 
   "friday": "Boolean", 
   "saturday": "Boolean", 
   "sunday": "Boolean" 
}
```

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: **application/json**, **application/xml**, or **text/xml**.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|
|Content-Type|Data format of the request body: application/json.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Missing request body, invalid format, or no valid day fields provided.|
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
 "message": "String",
 "result": {Object}
}
```

</td></tr><tr><td>

result.message

</td><td>

Confirmation message indicating the routine was updated.Data type: String

</td></tr><tr><td>

result.result

</td><td>

Contains the complete updated routine object with all seven days including unchanged days.Data type: Object

```
"result": { 
  "routine": {Object} 
}
```

</td></tr><tr><td>

result.routine

</td><td>

Weekly in-office routine. Contains a Boolean flag for each day of the week where `true` indicates in-office attendance, and `false` indicates no attendance.Data type: Object

```
"routine": { 
  "monday": "Boolean", 
  "tuesday": "Boolean",
  "wednesday": "Boolean", 
  "thursday": "Boolean",
  "friday": "Boolean", 
  "saturday": "Boolean", 
  "sunday": "Boolean"
}

```

</td></tr></tbody>
</table>### cURL request

This example updates only Friday and Saturday to true, leaving all other days unchanged.

```
curl "https://<instance>.service-now.com/api/sn_wsd_concierge/v1/presence/routine" \
--request PATCH \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username:password" \
--data '{
  "routine": { "friday": true, "saturday": true }
}'
```

Response body.

```
{
  "result": {
    "message": "Routine updated successfully",
    "result": {
      "routine": {
        "monday": true, "tuesday": true, "wednesday": true,
        "thursday": true, "friday": true, "saturday": true, "sunday": false
      }
    }
  }
}
```

## WSD Presence - POST /api/sn\_wsd\_concierge/v1/presence/collaborator

Adds one or more collaborators to the authenticated user’s presence visibility list. Collaborators can then view each other’s presence data. Use this endpoint to build a team or group of colleagues whose office attendance you want to track.

### URL format

Versioned URL: `/api/sn_wsd_concierge/{api_version}/presence/collaborator`

Default URL: `/api/sn_wsd_concierge/presence/collaborator`

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

collaborator\_ids

</td><td>

Required. Non-empty array of sys\_id values identifying users to add as collaborators.Table: User \[sys\_user\]

 Data type: Array of Strings```
"collaborator_ids": ["String", "String"]
```

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: **application/json**, **application/xml**, or **text/xml**.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|
|Content-Type|Data format of the request body: application/json.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Missing collaborator\_ids, empty array, or invalid sys\_id format.|
|404|Not Found. One or more collaborator sys\_ids weren't found in the sys\_user table.|
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
result": {
  "message": "String",
  "collaborators": [Array]
}
```

</td></tr><tr><td>

result.message

</td><td>

Confirmation message indicating collaborator\(s\) were added. Data type: String

</td></tr><tr><td>

result.collaborators

</td><td>

List of the newly added collaborators with their presence data.Data type: Array of Objects

```
"collaborators": [
 {
  "sys_id": "String",
  "name": "String",
  "privacy_enabled": Boolean,
  "routine": {Object},
  "exceptions": [Array]
 }
]
```

</td></tr><tr><td>

result.collaborators.sys\_id

</td><td>

Sys\_id of the collaborator's user record.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

result.collaborators.name

</td><td>

The display name of the collaborator as it appears in their sys\_user record.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

result.collaborators.privacy\_enabled

</td><td>

Boolean. Flag that indicates whether the collaborator has enabled privacy on their presence data.Valid values:

-   true: The collaborator's routine and exceptions are hidden. **routine** will be `null` and **exceptions** will be an empty array.
-   false: The collaborator's presence data is visible.

Data type: Boolean

</td></tr><tr><td>

result.collaborators.routine

</td><td>

The collaborator's weekly in-office routine. Contains a Boolean flag for each day of the week indicating planned office attendance. Displays `true` when the collaborator plans to be in-office that day, and `false` when attendance isn't planned.

Data type: Object

```
"routine": { 
   "monday": "Boolean", 
   "tuesday": "Boolean", 
   "wednesday": "Boolean", 
   "thursday": "Boolean", 
   "friday": "Boolean", 
   "saturday": "Boolean", 
   "sunday": "Boolean" 
}
```

</td></tr><tr><td>

result.collaborators.exceptions

</td><td>

The collaborator's one-time presence exceptions. Returns an empty array if `privacy_enabled` is `true`.Data type: Array of Objects

```
"exceptions": [ 
   { 
     "sys_id": "String", 
     "date": "String", 
     "in_office": "Boolean", 
     "origin": "String", 
     "location": "String" 
   } 
]
```

</td></tr><tr><td>

result.collaborators.exceptions.sys\_id

</td><td>

Sys\_id of the exception record.Table: Employee presence exceptions \(sn\_wsd\_concierge\_employee\_presence\_exception\)

Data type: String

</td></tr><tr><td>

result.collaborators.exceptions.date

</td><td>

Date this exception applies to. This is the date the user's routine is being overridden.Format: yyyy-MM-dd format

Data type: String

</td></tr><tr><td>

result.collaborators.exceptions.in\_office

</td><td>

Flag that indicates whether the user will be in the office on this date. This overrides whatever the weekly routine specifies for that day of the week.Valid values:

-   `true`: User will be in the office.
-   `false`: User won't be in the office

Data type: String

</td></tr><tr><td>

result.collaborators.exceptions.origin

</td><td>

Source that created the exception.Valid values:

-   `user`: Created manually by the employee.
-   `system`: Created automatically by the platform.
-   `manual`: Created by an admin or on behalf of the user.

Data type: String

</td></tr><tr><td>

result.collaborators.exceptions.location

</td><td>

The name or identifier of the office location the user will be at on this date. Only relevant when `in_office` is `true`. May be an empty string when the user is remote.Data type: String

</td></tr></tbody>
</table>### cURL request

This example adds two users as collaborators by providing their sys\_ids.

```
curl "https://<instance>.service-now.com/api/sn_wsd_concierge/v1/presence/collaborator" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username:password" \
--data '{
  "collaborator_ids": ["usr1a2b3c4d5e6", "usr7f8g9h0i1j2"]
}'
```

Response body.

```
{
  "result": {
    "message": "Collaborator(s) added successfully",
    "collaborators": [
      {
        "sys_id": "usr1a2b3c4d5e6", "name": "Jane Smith", "privacy_enabled": false,
        "routine": { "monday": true, "tuesday": true, "wednesday": false, "thursday": true, "friday": false, "saturday": false, "sunday": false },
        "exceptions": []
      },
      { "sys_id": "usr7f8g9h0i1j2", "name": "John Doe", "privacy_enabled": true, "routine": null, "exceptions": [] }
    ]
  }
}
```

## WSD Presence - POST /api/sn\_wsd\_concierge/v1/presence/exception

Creates a one-time presence exception for the authenticated user on a specific date. Use this endpoint when a user plans to be in the office on a day they normally work remotely, or vice versa.

Exceptions override the user’s weekly routine for that date.

### URL format

Versioned URL: `/api/sn_wsd_concierge/[api_version}/presence/exception`

Default URL: ```/api/sn_wsd_concierge/presence/exception`

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

exception

</td><td>

Required. Exception object defining the one-time presence override.Data type: Object

```
"exception": { 
  "date": "String", 
  "in_office": "Boolean",
  "location": "String", 
  "origin": "String".
  "sys_id": "String"
}
```

</td></tr><tr><td>

exception.date

</td><td>

Date of the exception.Format: yyyy-MM-dd

Data type: String

</td></tr><tr><td>

exception.in\_office

</td><td>

Flag that indicates whether the user will be in the office on this date.Possible values:

-   `true`: User will be in the office.
-   `false`: User won't be in the office.

Data type: Boolean

</td></tr><tr><td>

exception.location

</td><td>

Name or identifier of the office location for this exception.Data type: String

</td></tr><tr><td>

exception.origin

</td><td>

Source of the exception.Valid values:

-   `user`: Created manually by the employee.
-   `system`: Created automatically by the platform.
-   `manual`: Created by an admin or on behalf of the user.

 Data type: String

</td></tr><tr><td>

exception.sys\_id

</td><td>

Sys\_id of the existing exception to update.Table: Employee presence exceptions \(sn\_wsd\_concierge\_employee\_presence\_exception\)

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: **application/json**, **application/xml**, or **text/xml**.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|
|Content-Type|Data format of the request body: application/json.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Missing required field date or invalid date format.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing the result of the request.Data type: Object

```
"result": {
    "message": "String",
    "result": {Object}
  }
```

</td></tr><tr><td>

result.message

</td><td>

Confirmation message indicating the exception was added.Data type: String

</td></tr><tr><td>

result.result

</td><td>

Object containing the created exception\(s\).Data type: Object

```
"result": {
 "exceptions": [Array]
}
```

</td></tr><tr><td>

result.exceptions

</td><td>

Array containing details about the created exception\(s\).Data type: Array of Objects

```
"exceptions": [
 {
  "date": "String",
  "location": "String",
  "in_office": Boolean,
  "origin": "String",
  "sys_id": "String"
 }
]
```

</td></tr><tr><td>

result.result.exceptions.date

</td><td>

Date this exception applies to, in yyyy-MM-dd format. This is the date the user's routine is being overridden.Data type: String

</td></tr><tr><td>

result.result.exceptions.in\_office

</td><td>

Flag that indicates whether the user will be in the office on this date. This overrides whatever the weekly routine specifies for that day of the week.Valid values:

-   `true`: User will be in the office.
-   `false`: User won't be in the office

Data type: String

</td></tr><tr><td>

result.result.exceptions.location

</td><td>

The name or identifier of the office location the user will be at on this date. Only relevant when `in_office` is `true`. May be an empty string when the user is remote.Data type: String

</td></tr><tr><td>

result.result.exceptions.origin

</td><td>

Source that created the exception.Valid values:

-   `user`: Created manually by the employee.
-   `system`: Created automatically by the platform.
-   `manual`: Created by an admin or on behalf of the user.

Data type: String

</td></tr><tr><td>

result.result.exceptions.sys\_id

</td><td>

Sys\_id of the exception record.Table: Employee presence exceptions \(sn\_wsd\_concierge\_employee\_presence\_exception\)

Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a presence exception for February 14, 2026, marking the user as in-office at Building A.

```
curl "https://<instance>.service-now.com/api/sn_wsd_concierge/v1/presence/exception" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username:password" \
--data '{
  "exception": {
    "date": "2026-02-14",
    "in_office": true,
    "location": "Building A - Floor 3",
    "origin": "user"
  }
}'
```

Response body.

```
{
  "result": {
    "message": "Exception added successfully",
    "result": {
      "exceptions": [
        {
          "sys_id": "a1b2c3d4e5f6g7h8",
          "date": "2026-02-14",
          "in_office": true,
          "origin": "user",
          "location": "Building A - Floor 3"
        }
      ]
    }
  }
}
```

## WSD Presence - POST /api/sn\_wsd\_concierge/v1/presence/routine

Creates a new weekly in-office routine for the authenticated user. Use this endpoint when a user is setting up their presence routine for the first time.

All seven days of the week must be provided as Boolean values.

### URL format

Versioned URL: `/api/sn_wsd_concierge/{api_version}/presence/routine`

Default URL: `/api/sn_wsd_concierge/presence/routine`

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

routine

</td><td>

Required. Weekly in-office routine for the user.Contains a Boolean flag for each day of the week indicating planned office attendance. Displays `true` when the user plans to be in-office that day, and `false` when attendance isn't planned.

All days are required.

Data type: Object

```
"routine": { 
   "monday": "Boolean", 
   "tuesday": "Boolean", 
   "wednesday": "Boolean", 
   "thursday": "Boolean", 
   "friday": "Boolean", 
   "saturday": "Boolean", 
   "sunday": "Boolean" 
}
```

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: **application/json**, **application/xml**, or **text/xml**.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|
|Content-Type|Data format of the request body: application/json.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Missing required field\(s\) or invalid data type. All seven days must be provided as Boolean values.|
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
 "message": "String",
 "result": {Object}
}
```

</td></tr><tr><td>

result.message

</td><td>

Confirmation message indicating the routine was created.Data type: String

</td></tr><tr><td>

result.result

</td><td>

Contains the created routine object with all seven days.Data type: Object

```
"result": { 
  "routine": {Object} 
}
```

</td></tr><tr><td>

result.routine

</td><td>

User's weekly in-office routine. Contains a Boolean flag for each day of the week indicating planned office attendance. Displays `true` when the user plans to be in-office that day, and `false` when attendance isn't planned.

Data type: Object

```
"routine": { 
  "monday": "Boolean", 
  "tuesday": "Boolean",
  "wednesday": "Boolean", 
  "thursday": "Boolean",
  "friday": "Boolean", 
  "saturday": "Boolean", 
  "sunday": "Boolean"
}
```

</td></tr></tbody>
</table>### cURL request

This example creates a weekly in-office routine for Monday through Thursday.

```
curl "https://<instance>.service-now.com/api/sn_wsd_concierge/v1/presence/routine" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username:password" \
--data '{
  "routine": {
    "monday": true, "tuesday": true, "wednesday": true,
    "thursday": true, "friday": false, "saturday": false, "sunday": false
  }
}'
```

Response body.

```
{
  "result": {
    "message": "Routine created successfully",
    "result": {
      "routine": {
        "monday": true, 
        "tuesday": true, 
        "wednesday": true,
        "thursday": true, 
        "friday": false, 
        "saturday": false,
        "sunday": false
      }
    }
  }
}
```

## WSD Presence - PUT /api/sn\_wsd\_concierge/v1/presence/exception

Updates an existing presence exception by canceling it and creating a replacement. The original exception is identified by its sys\_id. Use this endpoint when a user needs to change the details of a previously created exception.

### URL format

Versioned URL: `/api/sn_wsd_concierge/{api_version}/presence/exception`

Default URL: `/api/sn_wsd_concierge/presence/exception`

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

exception

</td><td>

Required. Exception object containing the updated details. The **sys\_id** and **in\_office** fields are required.Data type: Object

```
"exception": { 
  "date": "String", 
  "in_office": "Boolean",
  "location": "String", 
  "origin": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

exception.date

</td><td>

Date of the exception.Format: yyyy-MM-dd

Data type: String

</td></tr><tr><td>

exception.in\_office

</td><td>

Required. Flag that indicates whether the user will be in the office on this date.Possible values:

-   `true`: User will be in the office.
-   `false`: User won't be in the office.

Data type: Boolean

</td></tr><tr><td>

exception.location

</td><td>

Name or identifier of the office location for this exception.Data type: String

</td></tr><tr><td>

exception.origin

</td><td>

Source of the exception.Valid values:

-   `user`: Created manually by the employee.
-   `system`: Created automatically by the platform.
-   `manual`: Created by an admin or on behalf of the user.

Data type: String

Default: user

</td></tr><tr><td>

exception.sys\_id

</td><td>

Required. Sys\_id of the existing exception to update.Table: Employee presence exceptions \(sn\_wsd\_concierge\_employee\_presence\_exception\)

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: **application/json**, **application/xml**, or **text/xml**.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|
|Content-Type|Data format of the request body: application/json.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Missing required fields sys\_id or in\_office.|
|404|Not Found. The specified exception wasn't found or the user doesn't have permission to modify it.|
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
    "message": "String",
    "result": {Object}
}
```

</td></tr><tr><td>

result.message

</td><td>

Confirmation message indicating the exception was updated. Data type: String

</td></tr><tr><td>

result.result

</td><td>

Contains the updated exception\(s\).Data type: Object

```
"result": {
  "exceptions": [Array]
}
```

</td></tr><tr><td>

result.result.exceptions

</td><td>

List of presence exceptions.Data type: Array of Objects

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

result.result.exceptions.sys\_id

</td><td>

Sys\_id of the exception record.Table: Employee presence exceptions \(sn\_wsd\_concierge\_employee\_presence\_exception\)

Data type: String

</td></tr><tr><td>

result.exceptions.date

</td><td>

Date this exception applies to, in yyyy-MM-dd format. This is the date the user's routine is being overridden.Data type: String

</td></tr><tr><td>

result.exceptions.in\_office

</td><td>

Flag that indicates whether the user will be in the office on this date. This overrides whatever the weekly routine specifies for that day of the week.Valid values:

-   `true`: User will be in the office.
-   `false`: User won't be in the office

Data type: String

</td></tr><tr><td>

result.exceptions.origin

</td><td>

Source that created the exception.Valid values:

-   `user`: Created manually by the employee.
-   `system`: Created automatically by the platform.
-   `manual`: Created by an admin or on behalf of the user.

Data type: String

</td></tr><tr><td>

result.exceptions.location

</td><td>

The name or identifier of the office location the user will be at on this date. Only relevant when `in_office` is `true`. May be an empty string when the user is remote.Data type: String

</td></tr></tbody>
</table>### cURL request

This example updates an existing exception to change the user’s status to remote \(not in office\) on the same date.

```
curl "https://<instance>.service-now.com/api/sn_wsd_concierge/v1/presence/exception" \
--request PUT \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username:password" \
--data '{
  "exception": {
    "sys_id": "exc1a2b3c4d5e6",
    "in_office": false,
    "date": "2026-02-14",
    "location": "",
    "origin": "user"
  }
}'
```

Response body.

```
{
  "result": {
    "message": "Exception updated successfully",
    "result": {
      "exceptions": [
        { "sys_id": "exc9k0l1m2n3o4", "date": "2026-02-14", "in_office": false, "origin": "user", "location": "" }
      ]
    }
  }
}
```

