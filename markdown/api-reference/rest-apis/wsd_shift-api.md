---
title: WSD Shift API
description: The Workplace Service Delivery \(WSD\) Shift API provides an endpoint that returns shift time spans for a specified date and time.Returns the shift time span for a specified date/time and shift.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD Shift API

The Workplace Service Delivery \(WSD\) Shift API provides an endpoint that returns shift time spans for a specified date and time.

To access this API, the caller must have the sn\_wsd\_core.workplace\_user role and the Workplace Safety Management \(sn\_wsd\_core\) and Workplace Reservation Management \(sn\_wsd\_rsv\) plugins must be activated.

This API runs in the `sn_wsd_rsv` namespace.

For additional information on Workplace Reservation Management, see Workplace Reservation Management.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD Shift - GET /api/sn\_wsd\_rsv/wsd\_shift/\{shift\_id\}/timespan

Returns the shift time span for a specified date/time and shift.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/wsd_shift/{shift_id}/timespan`

Default URL: `/api/sn_wsd_rsv/wsd_shift/{shift_id}/timespan`

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

shift\_id

</td><td>

Sys\_id of the shift to retrieve the time span for.For additional information on shift-based reservations, see Enable shift-based reservation.

Data type: String

Table: Shift \[sn\_wsd\_core\_shift\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attempt\_earlier\_start

</td><td>

Flag that indicates whether to set an early start time if the specified start value is within the shift's time span.Valid values:

-   true: If the specified shift includes the date/time specified in the **start** parameter, return the specified start date/time as the start of the time span.
-   false: Return the shift timespan as defined in the associated record.

Data type: Boolean

Default: false

</td></tr><tr><td>

start

</td><td>

Required. Date and time of the start of the shift time spans to return.Format: UTC - yyyy-mm-ddThh:mm:ssZ, such as 2022-05-23T08:00:00Z

</td></tr><tr><td>

timezone

</td><td>

Time zone to use when qualifying the shift time spans, such as ECT or PST. Also returns the shift time spans in this time zone.Format: UTC

Data type: String

Default: User's timezone

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

Details about the shift timespan that matched the search criteria.Data type: Object

```
"result":{
  "end": "String",
  "start": "String"
}
```

</td></tr><tr><td>

result.end

</td><td>

End date and time of the shift timespan in the specified time zone.Format: UTC: yyyy-mm-ddThh:mm:ssZ, such as 2022-05-23T08:00:00Z

Data type: String

</td></tr><tr><td>

result.start

</td><td>

Start date and time of the shift timespan in the specified time zone.Format: UTC: yyyy-mm-ddThh:mm:ssZ, such as 2022-05-23T08:00:00Z

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to retrieve the timespan of a shift.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/wsd_shift/e5d23acfdb42a01097acc9003996193a/timespan?attempt_earlier_start=true&start=2022-05-23T08:00:00Z&timezone=ECT" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "result": {
    "start": "2022-05-23T08:00:00Z",
    "end": "2022-05-23T15:00:00Z"
  }
}
```

