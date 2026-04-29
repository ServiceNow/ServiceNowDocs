---
title: WSD Multi Reservation API
description: The Workplace Service Delivery \(WSD\) Multi Reservation API provides endpoints for managing reservations with multiple workplace locations.Cancels a specified multi-reservation.Updates the reservations associated with a multi-reservation where the same reservation \(meeting\) has multiple workplace locations.Creates workplace reservations for the same time at different workplace locations.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD Multi Reservation API

The Workplace Service Delivery \(WSD\) Multi Reservation API provides endpoints for managing reservations with multiple workplace locations.

To access this API, the caller must have the sn\_wsd\_core.workplace\_user role and the Workplace Safety Management \(sn\_wsd\_core\) and Workplace Reservation Management \(sn\_wsd\_rsv\) plugins must be activated.

This API runs in the `sn_wsd_rsv` namespace.

For additional information on Workplace Reservation Management, see [Workplace Reservation Management](https://www.servicenow.com/docs/access?context=workplace-rsv-mgmt-feat&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD Multi Reservation - PATCH /api/sn\_wsd\_rsv/multi\_reservation/cancel/\{sys\_id\}

Cancels a specified multi-reservation.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/multi_reservation/cancel/{sys_id}`

Default URL: `/api/sn_wsd_rsv/multi_reservation/cancel/{sys_id}`

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

Sys\_id of the multi-reservation to cancel.Data type: String

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

result

</td><td>

Details of the results of the cancel request.Data type: Object

```
"result": {
  "error": "String",
  "parent": "String",
  "success": Boolean,
  "successfulReservations": [Array],
  "unSuccessfulReservations": [Array]
}
```

</td></tr><tr><td>

result.error

</td><td>

Message that describes the associated error.Data type: String

</td></tr><tr><td>

result.parent

</td><td id="parent-multi-entry">

Sys\_id of the parent reservation. A parent may have one or more child reservations associated to it.Data type: String

</td></tr><tr><td>

result.success

</td><td>

Flag that indicates whether the reservation was successfully cancelled.Possible values:

-   true: Successfully cancelled.
-   false: Reservation wasn't cancelled.

Data type: Boolean

</td></tr><tr><td>

result.successfulReservations

</td><td>

Details about the successful cancellation of the multi-reservation.Data type: Array of Objects

```
"successfulReservations": [
  {
    "msg": "String",
    "success": Boolean,
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.successfulReservations.msg

</td><td>

Cancellation message.Data type: String

</td></tr><tr><td>

result.successfulReservations.success

</td><td>

Flag that indicates whether the reservation was successfully cancelled.Possible values:

-   true: Successfully cancelled.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.successfulReservations.sys\_id

</td><td>

Sys\_id of the reservation that was cancelled.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.unSuccessfulReservations

</td><td>

Details about the unsuccessful cancellation of the multi-reservation.Data type: Array of Objects

```
"unSuccessfulReservations": [
  {
    "msg": "String",
    "success": Boolean,
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.unSuccessfulReservations.msg

</td><td>

Cancellation message.Data type: String

</td></tr><tr><td>

result.unSuccessfulReservations.success

</td><td>

Flag that indicates whether the reservation was successfully cancelled.Possible values:

-   true: Successfully cancelled.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.unSuccessfulReservations.sys\_id

</td><td>

Sys\_id of the reservation that was not cancelled.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr></tbody>
</table>### cURL request

The following code example shows how to cancel a multi-reservations.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/multi_reservation/cancel/1b1fdf5987ab01506342b846dabb35ec" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"cancel_notes\":\"Meeting no longer needed.\"}" \ 
--user "username":"password’"
```

Return results:

```
{
  "result": {
    "success": true,
    "successfulReservations": [
      {
        "success": true,
        "msg": "Cancelled successfully.",
        "sys_id": "5b1f9f1d87ab01506342b846dabb35a4"
      },
      {
        "success": true,
        "msg": "Cancelled successfully.",
        "sys_id": "931f9f1d87ab01506342b846dabb35a0"
      }
    ],
    "unSuccessfulReservations": [],
    "error": null,
    "parent": "1b1fdf5987ab01506342b846dabb35ec"
  }
}
```

## WSD Multi Reservation - PATCH /api/sn\_wsd\_rsv/multi\_reservation/update/\{sys\_id\}

Updates the reservations associated with a multi-reservation where the same reservation \(meeting\) has multiple workplace locations.

This endpoint can handle four different update scenarios:

1.  Update the content of the multi-reservation record, such as the subject, date, or time.
2.  Convert the multi-reservation into a single reservation based on the parent \(reservation for a single workplace location\).
3.  Convert a single reservation \(reservation for a single workplace location\) into a multi-reservation.
4.  Add or remove a workplace location to an existing multi-reservation.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/multi_reservation/update/{sys_id}`

Default URL: `/api/sn_wsd_rsv/multi_reservation/update/{sys_id}`

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

Sys\_id of the reservation to update.-   Single reservation to multi-reservation: Sys\_id of the single reservation.

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

-   Update content of multi-reservation: Sys\_id of the parent reservation record.

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]


To get the details of a multi parent reservation from the child record, refer to the sys\_id in the source\_reservation field of the child record.

 Data type: String

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

requested\_for

</td><td id="requested_for-update_reserv-entry">

Sys\_id or email address of the user for which the reservation is being made.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

reservables

</td><td>

List of details about the reservables associated with the reservation.Data type: Array of Objects

```
"reservables": [
  {
    "is_private": Boolean,
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

reservables.is\_private

</td><td>

Flag that indicates whether the reservation is private. If private, the reservation doesn't appear to anyone except the owner.For additional information on these privacy settings, see [Location privacy settings and impact](https://www.servicenow.com/docs/access?context=location-privacy-settings-and-impact&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

Valid values:

-   true: Reservation is private.
-   false: Reservation isn't private.

Data type: Boolean

Default: Value set for privacy in the system properties.

</td></tr><tr><td>

reservables.sys\_id

</td><td>

Sys\_id of the location at which to make the reservations. Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

reservable\_module

</td><td id="reservable_module-update_reserv-entry">

Required. Sys\_id of the reservable module to associate with the reservation. A [reservable module](https://www.servicenow.com/docs/access?context=config-reservable-module&version=australia&pubname=australia-employee-service-management&ft:locale=en-US) defines the workplace items needed for a reservation.Data type: String

Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

</td></tr><tr><td>

shift

</td><td id="shift-update_reserv-entry">

Sys\_id of the shift to associate with the reservation. If this parameter is passed in, the **end** parameter isn't required.

For additional information on shift-based reservations, see [Enable shift-based reservation](https://www.servicenow.com/docs/access?context=wsd-reservation-setup&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

Data type: String

Table: Shift \[sn\_wsd\_core\_shift\]

</td></tr><tr><td>

start

</td><td id="start-update_reserv-entry">

Required. Requested start time of the reservation.Data type: String

Format: UTC or local time \(yyyy-mm-dd hh:mm:ss\)

</td></tr><tr><td>

subject

</td><td>

Subject of the meeting associated with the reservation.

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

result

</td><td id="result-multi-entry">

Return results from the multi-reservation creation or update.Data type: Object

```
"result": {
  "parent": "String",
  "success": Boolean,
  "successfulReservations": [Array],
  "unSuccessfulReservations": [Array]
}
```

</td></tr><tr><td>

result.parent

</td><td id="parent-multi-entry">

Sys\_id of the parent reservation. A parent may have one or more child reservations associated to it.Data type: String

</td></tr><tr><td>

result.success

</td><td id="success-multi-entry">

Flag that indicates whether the reservation was successfully created.Possible values:

-   true: Successfully created.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.successfulReservations

</td><td>

List of the reservations that were successfully created.Data type: Array of Objects

```
"successfulReservations": [
  {
    "cancelled": Boolean,
    "error": "String",
    "reservable": "String"
    "success": Boolean,
    "sys_id": "String",
    "updated": Boolean
  }
]
```

</td></tr><tr><td>

result.successfulReservations.cancelled

</td><td>

Flag that indicates whether the reservation was successfully cancelled.Possible values:

-   true: Successfully cancelled.
-   false: Not cancelled.

Data type: Boolean

</td></tr><tr><td>

result.successfulReservations.error

</td><td id="successfulReservations_error-multi-entry">

Error message if there was a problem while creating the reservation.Data type: String

</td></tr><tr><td>

result.SuccessfulReservations.insert

</td><td>

Flag that indicates whether the reservation was successfully inserted. Such as when a reservation is added.Possible values:

-   true: Successfully inserted.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.successfulReservations.reservable

</td><td id="successfulReservations_reservable-multi-entry">

Sys\_id of the workplace for which the reservation was made.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.successfulReservations.success

</td><td>

Flag that indicates whether the associated operation was successful.Possible values:

-   true: Operation was successful.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.successfulReservations.sys\_id

</td><td id="successfulReservations_sys_id-multi-entry">

Sys\_id of the reservation that was created.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.successfulReservations.update

</td><td>

Flag that indicates whether the reservation was successfully updated.Possible values:

-   true: Successfully updated.
-   false: Not updated.

Data type: Boolean

</td></tr><tr><td>

result.unSuccessfulReservations

</td><td>

List of the reservations that were unsuccessful.Data type: Array of Objects

```
"unSuccessfulReservations": [
  {
    "cancelled": Boolean,
    "error": "String",
    "insert": Boolean
    "reservable": "String"
    "success": Boolean,
    "sys_id": "String",
    "updated": Boolean
  }
]
```

</td></tr><tr><td>

result.unSuccessfulReservations.cancelled

</td><td>

Flag that indicates whether the reservation was successfully cancelled.Possible values:

-   true: Successfully cancelled.
-   false: Not cancelled.

Data type: Boolean

</td></tr><tr><td>

result.unSuccessfulReservations.error

</td><td id="unSuccessfulReservations_error-multi-entry">

Error message if there was a problem while creating the reservation.Data type: String

</td></tr><tr><td>

result.unSuccessfulReservations.insert

</td><td>

Flag that indicates whether the reservation was successfully inserted.Possible values:

-   true: Successfully inserted.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.unSuccessfulReservations.reservable

</td><td id="unSuccessfulReservations_reservable-multi-entry">

Sys\_id of the workplace for which the reservation was trying to be made.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.unSuccessfulReservations.success

</td><td id="unSuccessfulReservations_success-multi-entry">

Flag that indicates whether the reservation was successfully created.Possible values:

-   true: Successfully created.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.unSuccessfulReservations.sys\_id

</td><td id="unSuccessfulReservations_sy_id-multi-entry">

Sys\_id of the unsuccessful reservation. Always null.

Data type: String

</td></tr><tr><td>

result.unSuccessfulReservations.update

</td><td>

Flag that indicates whether the reservation was successfully updated.Possible values:

-   true: Successfully updated.
-   false: Not updated.

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

The following code example shows how to modify the content of an existing multi-reservation.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/multi_reservation/update/02000d4edb7650106c731dcd13961914" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"reservables\":[
        { 
            \"sys_id\":\"fe1f744edb7650106c731dcd139619ca\" 
        }, 
        {
            \"sys_id\":\"02000d4edb7650106c731dcd13961914\"
        }
    ],
    \"reservable_module\":\"c31241cedb7650106c731dcd13961917\",
    \"subject\":\"Test 1\",
    \"start\":\"2022-05-27 13:00:00\",
    \"end\":\"2022-05-27 14:00:00\",
    \"requested_for\": \"workplace_user@example.com\"
}" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "parent": "98ccb4348723cd106342b846dabb359a",
    "success": true,
    "successfulReservations": [
      {
        "success": true,
        "updated": true,
        "cancelled": false,
        "sys_id": "6cccb4348723cd106342b846dabb359d",
        "error": null,
        "reservable": "5eafb44edb7650106c731dcd13961943"
      },
      {
        "success": true,
        "updated": true,
        "cancelled": false,
        "sys_id": "74af283c87ef8d106342b846dabb3592",
        "error": null,
        "reservable": "fe1f744edb7650106c731dcd139619ca"
      }
    ],
    "unSuccessfulReservations": []
  }
}
```

### cURL request

The following code example shows how to add a workplace location to an existing multi-reservation.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/multi_reservation/update/02000d4edb7650106c731dcd13961914" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"reservables\":[
       { 
           \"sys_id\":\"fe1f744edb7650106c731dcd139619ca\",
           \"is_private\": false 
       }, 
       {
           \"sys_id\":\"5eafb44edb7650106c731dcd13961943\",
           \"is_private\": false
       },
    {
           \"sys_id\":\"c4308d4edb7650106c731dcd1396194c\",
           \"is_private\": false
       }
   ],
   \"reservable_module\":\"c31241cedb7650106c731dcd13961917\",
   \"subject\":\"Test 1\",
   \"start\":\"2022-05-27 13:00:00\",
   \"end\":\"2022-05-27 14:00:00\",
   \"requested_for\": \"workplace_user@example.com\"
}" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "parent": "98ccb4348723cd106342b846dabb359a",
    "success": true,
    "successfulReservations": [
      {
        "success": true,
        "updated": true,
        "cancelled": false,
        "sys_id": "6cccb4348723cd106342b846dabb359d",
        "error": null,
        "reservable": "5eafb44edb7650106c731dcd13961943"
      },
      {
        "success": true,
        "updated": true,
        "cancelled": false,
        "sys_id": "74af283c87ef8d106342b846dabb3592",
        "error": null,
        "reservable": "fe1f744edb7650106c731dcd139619ca"
      },
      {
        "success": true,
        "inserted": true,
        "sys_id": "9e6d78748723cd106342b846dabb35a5",
        "error": null,
        "reservable": "c4308d4edb7650106c731dcd1396194c"
      }
    ],
    "unSuccessfulReservations": []
  }
}

```

### cURL request

The following code example shows how to convert a single reservation to a multi-reservation.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/multi_reservation/update/02000d4edb7650106c731dcd13961914" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"reservables\":[
       { 
           \"sys_id\":\"fe1f744edb7650106c731dcd139619ca\",
           \"is_private\": false
       }, 
       {
           \"sys_id\":\"5eafb44edb7650106c731dcd13961943\",
           \"is_private\": false
       }
   ],
   \"reservable_module\":\"c31241cedb7650106c731dcd13961917\",
   \"subject\":\"Test 1\",
   \"start\":\"2022-05-27 13:00:00\",
   \"end\":\"2022-05-27 14:00:00\",
   \"requested_for\": \"workplace_user@example.com\"
}" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "success": true,
    "parent": "98ccb4348723cd106342b846dabb359a",
    "successfulReservations": [
      {
        "success": true,
        "inserted": true,
        "sys_id": "6cccb4348723cd106342b846dabb359d",
        "error": null,
        "reservable": "5eafb44edb7650106c731dcd13961943"
      },
      {
        "success": true,
        "insert": false,
        "update": true,
        "cancel": false,
        "sys_id": "74af283c87ef8d106342b846dabb3592",
        "reservable": "fe1f744edb7650106c731dcd139619ca"
      }
    ],
    "unSuccessfulReservations": [],
    "error": null
  }
}
```

### cURL request

The following code example shows how to convert a multi-reservation into a single reservation.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/multi_reservation/update/02000d4edb7650106c731dcd13961914" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"reservables\":[
       { 
           \"sys_id\":\"fe1f744edb7650106c731dcd139619ca\",
           \"is_private\": false
       }
   ],
   \"reservable_module\":\"c31241cedb7650106c731dcd13961917\",
   \"subject\":\"Test 1\",
   \"start\":\"2022-05-27 13:00:00\",
   \"end\":\"2022-05-27 14:00:00\",
   \"requested_for\": \"workplace_user@example.com\"
}" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "sys_id": "74af283c87ef8d106342b846dabb3592",
    "success": true,
    "successfulReservations": [
      {
        "success": true,
        "insert": false,
        "update": true,
        "cancel": false,
        "sys_id": "74af283c87ef8d106342b846dabb3592",
        "reservable": "fe1f744edb7650106c731dcd139619ca",
        "error": ""
      },
      {
        "success": true,
        "insert": false,
        "update": true,
        "cancel": true,
        "sys_id": "3caf283c87ef8d106342b846dabb3596",
        "reservable": "5eafb44edb7650106c731dcd13961943"
      }
    ],
    "unSuccessfulReservations": [],
    "error": null
  }
}
```

## WSD Multi Reservation - POST /api/sn\_wsd\_rsv/multi\_reservation/add

Creates workplace reservations for the same time at different workplace locations.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/multi_reservation/add`

Default URL: `/api/sn_wsd_rsv/multi_reservation/add`

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

requested\_for

</td><td id="requested_for-update_reserv-entry">

Sys\_id or email address of the user for which the reservation is being made.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

reservables

</td><td>

List of details about the reservables associated with the reservation.Data type: Array of Objects

```
"reservables": [
  {
    "is_private": Boolean,
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

reservables.is\_private

</td><td>

Flag that indicates whether the reservation is private. If private, the reservation doesn't appear to anyone except the owner.For additional information on these privacy settings, see [Location privacy settings and impact](https://www.servicenow.com/docs/access?context=location-privacy-settings-and-impact&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

Valid values:

-   true: Reservation is private.
-   false: Reservation isn't private.

Data type: Boolean

Default: Value set for privacy in the system properties.

</td></tr><tr><td>

reservables.sys\_id

</td><td>

Sys\_id of the location at which to make the reservations. Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

reservable\_module

</td><td id="reservable_module-update_reserv-entry">

Required. Sys\_id of the reservable module to associate with the reservation. A [reservable module](https://www.servicenow.com/docs/access?context=config-reservable-module&version=australia&pubname=australia-employee-service-management&ft:locale=en-US) defines the workplace items needed for a reservation.Data type: String

Table: Reservable Module \[sn\_wsd\_rsv\_reservable\_module\]

</td></tr><tr><td>

shift

</td><td id="shift-update_reserv-entry">

Sys\_id of the shift to associate with the reservation. If this parameter is passed in, the **end** parameter isn't required.

For additional information on shift-based reservations, see [Enable shift-based reservation](https://www.servicenow.com/docs/access?context=wsd-reservation-setup&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

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
  "parent": "String",
  "success": Boolean,
  "successfulReservations": [Array],
  "unSuccessfulReservations": [Array]
}
```

</td></tr><tr><td>

result.parent

</td><td id="parent-multi-entry">

Sys\_id of the parent reservation. A parent may have one or more child reservations associated to it.Data type: String

</td></tr><tr><td>

result.success

</td><td id="success-multi-entry">

Flag that indicates whether the reservation was successfully created.Possible values:

-   true: Successfully created.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.successfulReservations

</td><td id="successfulReservations-multi-entry">

List of the reservations that were successfully created.Data type: Array of Objects

```
"successfulReservations": [
  {
    "error": "String",
    "inserted": Boolean,
    "reservable": "String"
    "success": Boolean,
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.successfulReservations.error

</td><td id="successfulReservations_error-multi-entry">

Error message if there was a problem while creating the reservation.Data type: String

</td></tr><tr><td>

result.successfulReservations.inserted

</td><td id="successfulReservations_inserted-multi-entry">

Flag that indicates whether the reservation was successfully inserted. Such as when a reservation is added.Possible values:

-   true: Successfully inserted.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.successfulReservations.reservable

</td><td id="successfulReservations_reservable-multi-entry">

Sys\_id of the workplace for which the reservation was made.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.successfulReservations.success

</td><td id="successfulReservations_success-multi-entry">

Flag that indicates whether the reservation was successfully created.Possible values:

-   true: Successfully created.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.successfulReservations.sys\_id

</td><td id="successfulReservations_sys_id-multi-entry">

Sys\_id of the reservation that was created.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.unSuccessfulReservations

</td><td id="unSuccessfulReservations-multi-entry">

List of the reservations that were unsuccessfully.Data type: Array of Objects

```
"unSuccessfulReservations": [
  {
    "error": "String",
    "inserted": Boolean,
    "reservable": "String"
    "success": Boolean,
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.unSuccessfulReservations.error

</td><td id="unSuccessfulReservations_error-multi-entry">

Error message if there was a problem while creating the reservation.Data type: String

</td></tr><tr><td>

result.unSuccessfulReservations.inserted

</td><td id="unSuccessfulReservations_inserted-multi-entry">

Flag that indicates whether the reservation was successfully inserted.Possible values:

-   true: Successfully inserted.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.unSuccessfulReservations.reservable

</td><td id="unSuccessfulReservations_reservable-multi-entry">

Sys\_id of the workplace for which the reservation was trying to be made.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.unSuccessfulReservations.success

</td><td id="unSuccessfulReservations_success-multi-entry">

Flag that indicates whether the reservation was successfully created.Possible values:

-   true: Successfully created.
-   false: Operation failed.

Data type: Boolean

</td></tr><tr><td>

result.unSuccessfulReservations.sys\_id

</td><td id="unSuccessfulReservations_sy_id-multi-entry">

Sys\_id of the unsuccessful reservation. Always null.

Data type: String

</td></tr></tbody>
</table>### cURL request

This code example shows how to reserve two different workplaces for the same reservation.

```
curl "https://instance.servicenow.com/api/sn_wsd_rsv/multi_reservation/add" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"reservable_module\": \"c31241cedb7650106c731dcd13961917\",
    \"subject\": \"Test-123\",
    \"reservation_purpose\": \"meeting\",
    \"timezone\": \"US/Pacific\",
    \"requested_for\": \"6816f79cc0a8016401c5a33be04be441\",
    \"reservables\": [
        {
            \"sys_id\": \"fe1f744edb7650106c731dcd139619ca\",
            \"is_private\": false
        },
        {
            \"sys_id\": \"d1208d4edb7650106c731dcd1396194a\",
            \"is_private\": false
        }
    ],
    \"start\": \"2023-01-12T11:30:00Z\",
    \"end\": \"2023-01-12T12:30:00Z\",
    \"reservation_type\": \"space\"
}" \
--user "username":"password"
```

Return results:

```
{
  "result": {
    "success": true,
    "parent": "08e8a18687586550cfaa99b73cbb354f",
    "successfulReservations": [
      {
        "success": true,
        "inserted": true,
        "sys_id": "44e8a18687586550cfaa99b73cbb3552",
        "error": null,
        "reservable": "fe1f744edb7650106c731dcd139619ca"
      },
      {
        "success": true,
        "inserted": true,
        "sys_id": "04e8a18687586550cfaa99b73cbb3555",
        "error": null,
        "reservable": "d1208d4edb7650106c731dcd1396194a"
      }
    ],
    "unSuccessfulReservations": []
  }
}
```

