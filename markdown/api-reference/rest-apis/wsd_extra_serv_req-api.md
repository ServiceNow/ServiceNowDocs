---
title: WSD Extra Service Request API
description: The Workplace Service Delivery \(WSD\) Extra Service Request API provides endpoints to manage extra service requests for reservations.Returns the details about the associated location layouts for a specified workplace location.Returns the details about the associated standard services for a specified workplace location.
locale: en-US
release: xanadu
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD Extra Service Request API

The Workplace Service Delivery \(WSD\) Extra Service Request API provides endpoints to manage extra service requests for reservations.

To access this API, the caller must have the sn\_wsd\_core.workplace\_user role.

This API runs in the `sn_wsd_rsv` namespace.

For additional information on Workplace Reservation Management, see [Workplace Reservation Management](https://www.servicenow.com/docs/access?context=workplace-rsv-mgmt-feat&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD Extra Service - GET /sn\_wsd\_rsv/extra\_service/list\_loc\_layouts

Returns the details about the associated location layouts for a specified workplace location.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/extra_service/list_loc_layouts`

Default URL: `/api/sn_wsd_rsv/extra_service/list_loc_layouts`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

location

</td><td id="location-reserv-entry">

Required. Sys\_id of the workplace location for which to return the location layout details.Located in the Workplace Location \[sn\_wsd\_core\_workplace\_location\] table.

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None|Required.|

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
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

List of the layouts associated with the specified workplace location.Data type: Array of Objects

 ```
"result": [
  {
    "capacity": Number,
    "cleanup_duration": "String",
    "image": {Object},
    "is_default": Boolean,
    "max_capacity": Number,
    "name": "String",
    "preparation_duration": "String",
    "short_description": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.capacity

</td><td>

Number of people that will attend the meeting.Data type: Number

</td></tr><tr><td>

result.cleanup\_duration

</td><td>

Amount of time it takes to clean the reservable for this layout.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

result.image

</td><td>

Details about an image that represents the layout for the associated reservable.Located in the Images \[db\_image\] table.

```
"image": {
  "link": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.image.link

</td><td>

Link to an image that represents the layout for this reservable. Located in the Images \[db\_image\] table.Data type: String

</td></tr><tr><td>

result.image.sys\_id

</td><td>

Sys\_id of the associated image record.Data type: String

</td></tr><tr><td>

result.is\_default

</td><td>

Flag that indicates whether the associated layout is the default for the reservable. Valid values:

-   true: Default.
-   false: Not default.

Data type: Boolean

</td></tr><tr><td>

result.name

</td><td>

Name of the location layout. Data type: String

</td></tr><tr><td>

result.max\_capacity

</td><td>

Maximum number of people that the layout associated with the reservable can accommodate.Data type: Number

</td></tr><tr><td>

result.preparation\_duration

</td><td>

Amount of time it takes to prepare the associated location layout.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

result.short\_description

</td><td>

Brief description of the location layout.Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the location layout.Located in the Layout \[sn\_wsd\_rsv\_layout\] table.

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
"http://instance.servicenow.com/api/sn_wsd_rsv/extra_service/list_loc_layouts&location=d2716d4adb7210106c731dcd13961994" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "result": [
    {
      "sys_id": "f4fee556534301103cf7ddeeff7b12ed",
      "name": "Test",
      "short_description": "test",
      "is_default": false,
      "image": {
        "sys_id": "9648a7c5531301103cf7ddeeff7b1286",
        "link": "9648a7c5531301103cf7ddeeff7b1286.iix"
      },
      "capacity": null,
      "max_capacity": null,
      "preparation_duration": 172800000,
      "cleanup_duration": 86400000
    }
  ]
}
```

## WSD Extra Service - GET /api/sn\_wsd\_rsv/extra\_service/list\_loc\_standard\_services

Returns the details about the associated standard services for a specified workplace location.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/extra_service/list_loc_standard_services`

Default URL: `/api/sn_wsd_rsv/extra_service/list_loc_standard_services`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

location

</td><td>

Required. Sys\_id of the workplace location for which to return the location layout standard services.Located in the Workplace Location \[sn\_wsd\_core\_workplace\_location\] table.

 Data type: String

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
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result.standard\_services

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

Sys\_id of the standard service record. Located in the Standard Service \[sn\_wsd\_rsv\_standard\_service\] table.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint to obtain the standard services.

```
"http://instance.servicenow.com/api/sn_wsd_rsv/extra_service/list_loc_standard_services&location=d2716d4adb7210106c731dcd13961994" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "result": [
    {
      "sys_id": "9b01458edb7650106c731dcd13961945",
      "name": "Flip chart",
      "short_description": "Flip chart with paper sheets",
      "font_awesome_icon": "fa-calendar-o"
    },
    {
      "sys_id": "abd0c18edb7650106c731dcd13961965",
      "name": "Projector screen",
      "short_description": "Connect laptop to screen (HDMI and DVI)",
      "font_awesome_icon": "fa-caret-square-o-right"
    },
    {
      "sys_id": "9841858edb7650106c731dcd1396193c",
      "name": "Whiteboard",
      "short_description": "Whiteboard and markers",
      "font_awesome_icon": "fa-pencil-square-o"
    }
  ]
}
```

