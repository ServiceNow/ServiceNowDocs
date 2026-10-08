---
title: WSD Unified Search API
description: The WSD Unified Search API provides an endpoint to search across workplace users and locations.Searches for users and workplace locations matching the provided search term. Returns a combined list of matching results with pagination support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/wsd\_unified-search-api.html
release: brazil
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 7
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

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/api-rest.md)

## WSD Unified Search - POST /api/sn\_wsd\_core/wsd\_unified\_search/users\_and\_locations

Searches for users and workplace locations matching the provided search term. Returns a combined list of matching results with pagination support.

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

Object containing one or more table names as keys to restrict results to specific entity types. When empty, both users and locations are returned.Valid fields \(table names\):

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

Default: \{\} \(no filter applied\)

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
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: application/json, application/xml, text/xml.|
|Content-Type|Data format of the request body: application/json.|
|Authorization|Authentication credentials. Supports Basic authentication or session-based authentication.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Invalid request body format.|
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

Initials derived from the user's display name, used as a fallback when no avatar is available. For example, `JD` for Jane Doe.Data type: String

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

