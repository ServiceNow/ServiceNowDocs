---
title: WSD Unified Search API
description: The WSD Unified Search API provides an endpoint to search across workplace users and locations.Searches for users and workplace locations \(case-insensitive\) matching the provided search term. Returns a combined list of matching results with pagination support.Retrieve the current location of a specific user based on their active reservations, workplace profile, or neighborhood assignment. Returns the most relevant public location first, falling back to private locations if no public location is found.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 12
keywords: [Workplace Service Delivery Core, WSD]
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD Unified Search API

The WSD Unified Search API provides an endpoint to search across workplace users and locations.

The WSD Unified Search API runs in the sn\_wsd\_core namespace and powers the search/type ahead experience in the Workplace Service Delivery \(WSD\) portal, returning matching users, spaces, floors, buildings, campuses, and neighborhoods in a single response.

## Requirements

The WSD Unified Search API requires:

-   The calling user have the sn\_wsd\_core.workplace\_user role.
-   The Workplace Service Delivery Core \(com.sn\_wsd\_core\) plugin be active.
-   At least one building and floor be configured in the workplace location hierarchy.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD Unified Search - POST /api/sn\_wsd\_core/wsd\_unified\_search/users\_and\_locations

Searches for users and workplace locations \(case-insensitive\) matching the provided search term. Returns a combined list of matching results with pagination support.

### URL format

Versioned URL: `/api/sn_wsd_core/{api_version}/wsd_unified_search/users_and_locations`

Default URL: `/api/sn_wsd_core/wsd_unified_search/users_and_locations`

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

search\_term

</td><td>

Search query used to find matching users and workplace locations. Accepts a comma-separated list of values to search for multiple terms simultaneously. For example, `"Conference, Desk"` returns results matching either term. Empty segments are ignored.Data type: String

Default value: Empty string \(returns all results\)

</td></tr><tr><td>

show\_location

</td><td>

Flag that indicates whether to include the user's current location in the result label.Possible values:

-   `true`: Display the user's current location in the result label.
-   `false`: Don't display the user's current location in the result label.

Data type: Boolean

Default: true

</td></tr><tr><td>

show\_loggedin\_user

</td><td>

Flag that indicates whether to display the authenticated user as the first result when no search term is provided. Only applies to desktop clients at offset 0. Possible values:

-   `true`: Show the authenticated user as the first result.
-   `false`: Don't show the authenticated user as the first result.

Data type: Boolean

Default: true

</td></tr><tr><td>

include\_user\_email

</td><td>

Flag that indicates whether to include user email addresses in result labels and allow searching by email address. Possible values:

-   `true`: Include email in result labels and enable email search.
-   `false`: Don't include email in result labels or enable email search

Data type: Boolean

Default: false

</td></tr><tr><td>

filterConfig

</td><td>

Table-specific encoded queries. Keys are table names. Values are encoded query strings.Valid fields \(table names\):

-   sys\_user
-   sn\_wsd\_core\_workplace\_location
-   sn\_wsd\_core\_region
-   sn\_wsd\_core\_site
-   sn\_wsd\_core\_campus
-   sn\_wsd\_core\_building
-   sn\_wsd\_core\_floor
-   sn\_wsd\_core\_area
-   sn\_wsd\_core\_space
-   sn\_wsd\_core\_room
-   sn\_wsd\_core\_neighborhood

Data type: Object

```
"filterConfig": {
  "<table_name>": Boolean
}
```

Default: \{\} \(no filter applied, searches all tables\)

</td></tr><tr><td>

filterConfig.&lt;table\_name&gt;

</td><td>

Flag that indicates whether to include results from the specified table. Set to true to include results from that entity type.Valid values:

-   `true`: Include results from that entity type.
-   `false`: Don't include results from that entity type.

Data type: Boolean

</td></tr><tr><td>

options

</td><td>

Object containing additional configuration for search behavior. Data type: Object

```
"options": { 
  "search_in_parent": Boolean,
  "cache": Boolean,
  "rsvModule": {Object}
}
```

</td></tr><tr><td>

options.search\_in\_parent

</td><td>

Flag that indicates whether to include results from parent location records when filtering by a child entity.Possible values:

-   `true`: Include parent location results.
-   `false`: Don't include parent location results.

Data type: Boolean

</td></tr><tr><td>

options.cache

</td><td>

Flag that indicates whether to use cached search results.Possible values:

-   `true`: Use cached results where available.
-   `false`: Always fetch fresh results

Data type: Boolean

</td></tr><tr><td>

options.rsvModule

</td><td>

Object containing reservation module configuration for filtering results by reservable module context.Data type: Object

```
"rsvModule": { 
  "value": "String"
}
```

</td></tr><tr><td>

options.rsvModule.value

</td><td>

Sys\_id of the reservable module to use for filtering available spaces. Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

Data type: String

</td></tr><tr><td>

options.rsvModule.enable\_restricted\_neighborhood\_rules

</td><td>

Flag that indicates whether to apply restricted neighborhood rules when filtering results by reservation module.Possible values:

-   `true`: Apply restricted neighborhood rules.
-   `false`: Don't apply restricted neighborhood rules.

Data type: Boolean

</td></tr><tr><td>

sysparam\_offset

</td><td>

Pagination offset. Number of records to skip before returning results. Use with **sysparam\_limit** for pagination. Minimum value: 0

Data type: Number

Default value: 0

</td></tr><tr><td>

sysparam\_limit

</td><td>

Maximum number of records to return per request. Use with **sysparam\_offset** for pagination.Minimum value: 1

Data type: Number

Default value: 10

</td></tr></tbody>
</table>**Note:** All searches are case-insensitive.

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: application/json, application/xml, text/xml.|
|Content-Type|Data format of the request body: application/json.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Invalid request body format.|
|401|Authentication failed.|
|403|User lacks required ACL permissions.|
|500|Internal server error. An unexpected error occurred while processing the request.|

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
  "result": [Array],
  "more": Boolean,
  "isMobile": Boolean
}
```

</td></tr><tr><td>

result.isMobile

</td><td>

Flag that indicates whether the request was detected as originating from a mobile client.Possible values:

-   `true`: Request originated from a mobile client.
-   `false`: Request originated from a desktop client.

Data type: Boolean

</td></tr><tr><td>

result.more

</td><td>

Flag that indicates whether additional results are available beyond the current page.Possible values:

-   `true`: More results are available. Increment **sysparam\_offset** by **sysparam\_limit** to retrieve the next page.
-   `false`: No more results are available.

Data type: Boolean

</td></tr><tr><td>

result.result

</td><td>

Array of matching user and location objects. Each object contains common fields shared across all result types, as well as type-specific fields that are only present for user results.Data type: Array of Objects

```
"result": [
  {
    "displayValue": "String",
    "value": "String",
    "table": "String",
    "label": "String",
    "selectedTreeBranch": "String",
    "timezone": {Object},
    "wsdSource": "String",
    "externalId": "String",
    "floorId": "String",
    "isReservable": Boolean
  }
]
```

</td></tr><tr><td>

result.result.displayValue

</td><td>

Display name of the result. For example, `Conference Room A - Floor 1` for a space or `Jane Doe` for a user.Data type: String

</td></tr><tr><td>

result.result.externalId

</td><td>

Identifier of the result record in an external source system, when applicable.Data type: String

</td></tr><tr><td>

result.result.floorId

</td><td>

Sys\_id of the floor on which the result location resides. Present for location results only.Table: Workplace Floor \[sn\_wsd\_core\_floor\]

Data type: String

</td></tr><tr><td>

result.result.isReservable

</td><td>

Flag that indicates whether the result location can be reserved.Possible values:

-   `true`: The location is reservable.
-   `false`: The location isn't reservable.

Data type: Boolean

</td></tr><tr><td>

result.result.label

</td><td>

Secondary display string providing additional context for the result. For example, the location hierarchy for a space, or the department and title for a user.Data type: String

</td></tr><tr><td>

result.result.selectedTreeBranch

</td><td>

Sys\_id of the parent location record in the workplace hierarchy associated with this result. Used to pre-select the location tree in the UI.Data type: String

</td></tr><tr><td>

result.result.table

</td><td>

Table name from which the result originates. For example, `sn_wsd_core_space` or `sys_user`.Data type: String

</td></tr><tr><td>

result.result.timezone

</td><td>

Time zone associated with the result location. Present for location results.Data type: Object

```
"timezone": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.result.timezone.displayValue

</td><td>

Human-readable time zone name. For example, `Eastern Standard Time`.Data type: String

</td></tr><tr><td>

result.result.timezone.value

</td><td>

IANA time zone identifier for the result location. For example, `America/New_York.`Data type: String

</td></tr><tr><td>

result.result.userDetails

</td><td>

Object containing additional details about a user result. Present for user results only \(User \[sys\_user\] table\).Data type: Object

```
"userDetails": {
  "userID": "String",
  "name": "String",
  "department": "String",
  "avatar": "String",
  "initials": "String"
}
```

</td></tr><tr><td>

result.result.userDetails.avatar

</td><td>

Relative URL path to the user's profile avatar image.Data type: String

</td></tr><tr><td>

result.result.userDetails.department

</td><td>

Name of the department the user belongs to.Data type: String

</td></tr><tr><td>

result.result.userDetails.initials

</td><td>

Initials derived from the user's display name, used as a fallback when no avatar is available. For example, `JD` for `Jane Doe`.Data type: String

</td></tr><tr><td>

result.result.userDetails.name

</td><td>

Full display name of the user. For example, `Jane Doe`.Data type: String

</td></tr><tr><td>

result.result.userDetails.userID

</td><td>

Sys\_id of the user record.Table: User \[sys\_user\]

Data type: String.

</td></tr><tr><td>

result.result.value

</td><td>

Sys\_id of the result record.Data type: String

</td></tr><tr><td>

result.result.wsdSource

</td><td>

Source system identifier for the result. Used when the location originates from an external integration.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example searches for spaces matching "Conference" or "Desk" within a specific building, returning up to 10 results.

```
curl "https://<instance>.service-now.com/api/sn_wsd_core/wsd_unified_search/users_and_locations" \ 
--request POST \ 
--header "Accept: application/json" \ 
--header "Content-Type: application/json" \ 
--user "username:password" \
--data '{
  "search_term": "Conference, Desk",
  "show_location": true,
  "show_loggedin_user": true,
  "include_user_email": false,
  "filterConfig": {},
  "options": {
       "search_in_parent": false,
       "cache": true
              },
       "sysparam_offset": 0,
       "sysparam_limit": 10 
  }
}'
```

Response body.

```
{
  "result": {
    "result": [
      {
        "displayValue": "Conference Room A - Floor 1",
        "value": "space_123",
        "table": "sn_wsd_core_space",
        "label": "Floor 1, Building A, Main Campus",
        "selectedTreeBranch": "building_456",
        "timezone": {
          "value": "America/New_York",
          "displayValue": "Eastern Standard Time"
        },
        "wsdSource": "",
        "externalId": "",
        "floorId": "floor_789",
        "isReservable": true
      },
      {
        "displayValue": "Jane Doe",
        "value": "user_789",
        "table": "sys_user",
        "label": "Senior Engineer, Engineering",
        "selectedTreeBranch": "building_456",
        "userDetails": {
          "userID": "user_789",
          "name": "Jane Doe",
          "department": "Engineering",
          "avatar": "/avatar/user_789",
          "initials": "JD"
        }
      }
    ],
    "more": true,
    "isMobile": false
  }
}
```

### cURL request

The following are examples of different search criteria.

Search all locations and users:

```
{ 
  "search_term": "engineering", 
  "filterConfig": {}, 
  "sysparm_offset": 0, 
  "sysparm_limit": 20
}
```

Search only reservable spaces:

```
{
  "search_term": "workspace",
  "filterConfig": {
    "sn_wsd_core_workplace_location": "is_reservable=true^sys_class_name=sn_wsd_core_space"
  },
  "sysparm_offset": 0,
  "sysparm_limit": 10
}
```

Search only active users in IT department:

```
{
  "search_term": "smith",
  "include_user_email": true,
  "filterConfig": {
    "sys_user": "department.name=IT Department"
  },
  "sysparm_offset": 0,
  "sysparm_limit": 10
}
```

Search neighborhoods with restricted access validation:

```
{
  "search_term": "team",
  "filterConfig": {
    "sn_wsd_core_neighborhood": ""
  },
  "options": {
    "sn_wsd_core_neighborhood": {
      "validateAccess": true
    },
    "rsvModule": {
      "value": "module_sys_id_here"
    }
  },
  "sysparm_offset": 0,
  "sysparm_limit": 10
}
```

## WSD Unified Search - GET /api/sn\_wsd\_core/wsd\_unified\_search/current\_location

Retrieve the current location of a specific user based on their active reservations, workplace profile, or neighborhood assignment. Returns the most relevant public location first, falling back to private locations if no public location is found.

### URL format

Versioned URL: `/api/sn_wsd_core/{api_version}/wsd_unified_search/current_location`

Default URL: `/api/sn_wsd_core/wsd_unified_search/current_location`

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

userSysId

</td><td>

Required. Sys\_id of the user whose current location to retrieve.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

useNeighborhoods

</td><td>

Flag that indicates whether to include a neighborhood-based location from the user's workplace profile when no reservation or direct profile location is found.Valid values:

-   true: Include neighborhood-based location as a fallback.
-   false: Don't include neighborhood-based location.

Data type: Boolean

Default: false

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

Authorization

</td><td>

Authentication credentials. Supports Basic authentication or session-based authentication.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. The userSysId parameter is missing or invalid.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

Returns a single location object when a current location is found, or an empty object \{\} when no location is found.

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

isPrivate

</td><td>

Flag that indicates whether the returned location is private. A location is considered private when it's marked as private in the workplace profile or when it's associated with a reservation that has a private or sensitive status.Valid values:

-   true: Location is private or the reservation has private/sensitive status.
-   false: Location is public.

Data type: Boolean

</td></tr><tr><td>

displayValue

</td><td>

Display name of the result location. For example, `Building A - Floor 2 - Workspace 201`.Data type: String

</td></tr><tr><td>

value

</td><td>

Sys\_id of the result location record.Data type: String.

Maximum length: 32

</td></tr><tr><td>

table

</td><td>

Name of the ServiceNow table from which the location originates For example, `sn_wsd_core_space`.Data type: String

</td></tr><tr><td>

label

</td><td>

Secondary display string providing location hierarchy context. For example, `Floor 2, Building A`.Data type: String

</td></tr><tr><td>

selectedTreeBranch

</td><td>

Sys\_id of the parent location record in the workplace hierarchy. Used to pre-select the location tree in the UI.Data type: String

</td></tr><tr><td>

timezone

</td><td>

Time zone associated with the result location.Data type: Object

```
"timezone": {
  "value": "String",
  "displayValue": "String"
}
```

</td></tr><tr><td>

timezone.value

</td><td>

IANA time zone identifier for the result location. For example, `America/New_York`.Data type: String

</td></tr><tr><td>

timezone.displayValue

</td><td>

Human-readable timezone name. For example, `US/Eastern`.Data type: String

</td></tr><tr><td>

wsdSource

</td><td>

Source system identifier for the location. Used when the location originates from an external integration.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Identifier of the location record in an external source system, when applicable.Data type: String

</td></tr><tr><td>

floorId

</td><td>

Sys\_id of the floor on which the location resides. Table: Workplace Floor \[sn\_wsd\_core\_floor\] table

Data type: String

</td></tr><tr><td>

isReservable

</td><td>

Flag that indicates whether the location can be reserved.Possible values:

-   true: The location is reservable.
-   false: The location isn't reservable.

Data type: Boolean

</td></tr><tr><td>

isPrivate

</td><td>

Flag that indicates whether the returned location is private. A location is considered private when it is marked as private in the workplace profile or when it is associated with a reservation that has a private or sensitive status.

Possible values:

-   true: The location is private.
-   false: The location is public.

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

The following example retrieves the current location of a specific user, including neighborhood-based location as a fallback.

```
curl "https://<instance>.service-now.com/api/sn_wsd_core/wsd_unified_search/current_location
  ?userSysId=abc123def456&useNeighborhoods=true" \
  --request GET \
  --header "Accept: application/json" \
  --user "username:password"
```

Reponse body when location is found.

```
{
  "result": {
    "displayValue": "Building A - Floor 2 - Workspace 201",
    "value": "abc123def456",
    "table": "sn_wsd_core_space",
    "label": "Floor 2, Building A",
    "selectedTreeBranch": "building789xyz",
    "timezone": {
      "value": "America/New_York",
      "displayValue": "US/Eastern"
    },
    "wsdSource": "manual",
    "externalId": "EXT-WS-201",
    "floorId": "floor123",
    "isReservable": true,
    "isPrivate": false
  }
}
```

Response body when location isn't found \(empty object \{\}\).

```
{
  "result": {}
}
```

