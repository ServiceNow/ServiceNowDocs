---
title: WSD Reservation Invitees API
description: The Workplace Service Delivery \(WSD\) Reservation Invitees API provides endpoints to add invitees to reservations, fetch invitees of a reservation, and reassign invitees of a reservation.Retrieves details about the invitees associated with a specified reservation.Reassigns the specified invitees from one reservation to another.Adds the specified invitees to a specified reservation.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD Reservation Invitees API

The Workplace Service Delivery \(WSD\) Reservation Invitees API provides endpoints to add invitees to reservations, fetch invitees of a reservation, and reassign invitees of a reservation.

To access this API, the caller must have the sn\_wsd\_core.workplace\_user role and the Workplace Reservation Management \(sn\_wsd\_rsv\) plugin must be activated.

This API runs in the `sn_wsd_rsv` namespace.

For additional information on Workplace Reservation Management, see [Workplace Reservation Management](https://www.servicenow.com/docs/access?context=workplace-rsv-mgmt-feat&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD Reservation Invitees - GET /api/sn\_wsd\_rsv/wsd\_reservation\_invitees/reservation/\{sys\_id\}

Retrieves details about the invitees associated with a specified reservation.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/wsd_reservation_invitees/reservation/{sys_id}`

Default URL: `/api/sn_wsd_rsv/reservation/{sys_id}`

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

Sys\_id of the reservation for which to return the invitee details.Data type: String

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

Return results for the invitees associated with the specified reservation.Data type: Object

```
{
  "result": {
    "invitees": [Array],
    "reservationId": "String",
    "reservationSubType": "String",
    "success": Boolean
  }
}
```

</td></tr><tr><td>

result.invitees

</td><td>

Details about the invitees associated with the reservation.Data type: Array of Objects

```
"invitees": [
  {
    "email": "String",
    "firstName": "String",
    "inviteeId": "String",
    "inviteState": {Object},
    "inviteeType": "String",
    "isVIP": Boolean,
    "isWifiRequired": Boolean,
    "isParkingRequired": Boolean,
    "lastName": "String",
    "licensePlate": "String",
    "location": {Object},
    "name": "String",
    "org": "String",
    "parkingType": "String",
    "phoneNumber": "String",
    "privateNotes": "String",
    "reservationId": "String",
    "reservationInviteeId": "String",
    "title": "String",
    "visitorType": "String"
  }
]
```

</td></tr><tr><td>

result.invitees.email

</td><td>

Email address of the invitee.

Data type: String

</td></tr><tr><td>

result.invitees.firstName

</td><td>

First name of the invitee.Data type: String

</td></tr><tr><td>

result.invitees.inviteeId

</td><td>

Sys\_id of the employee's user record.

Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

result.invitees.inviteState

</td><td>

Details about the current state of the invitee for the reservation.Data type: Object

```
"inviteState": {
  "displayValue": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.invitees.inviteState.displayValue

</td><td>

Display value for the invitee state, such as New or Removed.Data type: String

</td></tr><tr><td>

result.invitees.inviteState.value

</td><td>

Internal value for the invitee state.Data type: String

</td></tr><tr><td>

result.invitees.inviteeType

</td><td>

Type of invitee.

Valid values: \(case-sensitive\)

-   employee
-   visitor

Data type: String

</td></tr><tr><td>

result.invitees.isVIP

</td><td>

Flag that indicates whether the invitee is classified as a VIP.Valid values:

-   true: Invitee is a VIP.
-   false: Invitee isn't a VIP.

Data type: Boolean

</td></tr><tr><td>

result.invitees.isWifiRequired

</td><td>

Flag that indicates whether the WIFI password should be provided to the visitor upon entry.Valid values:

-   true: Provide WIFI password.
-   false: Don't provide WIFI password.

Data type: Boolean

</td></tr><tr><td>

result.invitees.isParkingRequired

</td><td>

Flag that indicates whether the invitee requires parking.Valid values:

-   true: Parking needed.
-   false: Parking isn't needed.

Data type: Boolean

</td></tr><tr><td>

result.invitees.lastName

</td><td>

Last name of the invitee.Data type: String

</td></tr><tr><td>

result.invitees.licensePlate

</td><td>

License plate of the invitee.Data type: String

</td></tr><tr><td>

result.invitees.location

</td><td>

Details about the workplace location of the invitee.Data type: Object

```
 "location": {
  "displayName": "String",
  "sysId": "String"
}
```

</td></tr><tr><td>

result.invitees.location.displayName

</td><td>

Display name of the invitee's workplace location, such as Dublin.Data type: String

</td></tr><tr><td>

result.invitees.location.sysId

</td><td>

Sys\_id of the invitee workplace location.Data type: String

Table: Workplace Location \[sn\_wsd\_core\_worplace\_location\]

</td></tr><tr><td>

result.invitees.name

</td><td>

Name of the invitee.Data type: String

</td></tr><tr><td>

result.invitees.org

</td><td>

Organization of the invitee.Data type: String

</td></tr><tr><td>

result.invitees.parkingType

</td><td>

Type of parking required for invitee.Valid values: \(case-sensitive\)

-   ev\_parking
-   none
-   normal\_parking
-   van\_accessible\_parking

Data type: String

</td></tr><tr><td>

result.invitees.phoneNumber

</td><td>

Phone number of the invitee.Data type: String

</td></tr><tr><td>

result.invitees.privateNotes

</td><td>

Any additional notes provided by the invitee.Data type: String

</td></tr><tr><td>

result.invitees.reservationId

</td><td>

Sys\_id of the reservation to which the invitee is associated.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.invitees.reservationInviteeId

</td><td>

Sys\_id of the reservation invitee for visitor.

 Data type: String

 Table: Reservation Invitee \[sn\_wsd\_rsv\_m2m\_reservation\_invitee\]

</td></tr><tr><td>

result.invitees.title

</td><td>

Title of the invitee.Data type: String

</td></tr><tr><td>

result.invitees.visitorType

</td><td>

Type of invitee.Valid values: \(case-sensitive\)

-   client
-   contractor
-   friend\_family
-   others

Data type: String

</td></tr><tr><td>

result.reservationId

</td><td>

Sys\_id of the reservation to which the invitee is associated.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.reservationSubType

</td><td>

Sub-type of the reservation record, such as single or multi-child.Data type: String

</td></tr><tr><td>

result.success

</td><td>

Flag that indicates whether the call was successful.Possible values:

-   true: Endpoint call was successful.
-   false: Endpoint call failed.

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

The following code example shows how to retrieve the invitees for a reservation.

```
curl 
"http://instance.servicenow.com/api/sn_wsd_rsv/wsd_reservation_invitees/reservation/17979dc9536b01103cf7ddeeff7b12b3" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'

```

Return results:

```
{
  "result": {
    "success": true,
    "reservationId": "17979dc9536b01103cf7ddeeff7b12b3",
    "reservationSubType": "single",
    "invitees": [
      {
        "reservationId": "17979dc9536b01103cf7ddeeff7b12b3",
        "location": {
          "sysId": "19efb84edb7650106c731dcd1396193c",
          "displayName": "Dublin"
        },
        "reservationInviteeId": "1f97d58d53e701103cf7ddeeff7b129a",
        "inviteeType": "employee",
        "inviteState": {
          "displayValue": "New",
          "value": "new"
        },
        "inviteeId": "6816f79cc0a8016401c5a33be04be441",
        "name": "System Administrator",
        "email": "admin@example.com"
      },
      {
        "reservationId": "17979dc9536b01103cf7ddeeff7b12b3",
        "location": {
          "sysId": "19efb84edb7650106c731dcd1396193c",
          "displayName": "Dublin"
        },
        "reservationInviteeId": "8ee7ddc9536b01103cf7ddeeff7b1219",
        "inviteeType": "employee",
        "inviteState": {
          "displayValue": "New",
          "value": "new"
        },
        "inviteeId": "62826bf03710200044e0bfc8bcbe5df1",
        "name": "Abel Tuter",
        "email": "abel.tuter@example.com"
      },
      {
        "reservationId": "17979dc9536b01103cf7ddeeff7b12b3",
        "location": {
          "sysId": "19efb84edb7650106c731dcd1396193c",
          "displayName": "Dublin"
        },
        "reservationInviteeId": "4ae7d10d536b01103cf7ddeeff7b126b",
        "inviteeType": "visitor",
        "inviteState": {
          "displayValue": "New",
          "value": "new"
        },
        "inviteeId": "86e7d10d536b01103cf7ddeeff7b1267",
        "firstName": "Visitor",
        "lastName": "User",
        "name": "Visitor User",
        "email": "visitoruser@example.com",
        "phoneNumber": "+919876543210",
        "isVIP": true,
        "parkingType": "normal_parking",
        "licensePlate": "1234",
        "isParkingRequired": true,
        "org": "Senow",
        "visitorType": "contractor",
        "title": "President",
        "isWifiRequired": true,
        "privateNotes": "Visiting"
      }
    ]
  }
}
```

## WSD Reservation Invitees - POST /api/sn\_wsd\_rsv/wsd\_reservation\_invitees/reassign

Reassigns the specified invitees from one reservation to another.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/wsd_reservation_invitees/reassign`

Default URL: `/api/sn_wsd_rsv/wsd_reservation_invitees/reassign`

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

reservationId

</td><td>

Required. Sys\_id of the reservation for which to reassign the invitees.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

reservationInvitees

</td><td>

List of invitees to reassign to the reservation identified in the **reservationId** parameter.This removes the specified invitees from an earlier reservation in which they were present as per the reservation invitee table and moves them to this reservation.

Data type: Array of Strings

Table: Reservation Invitee \[sn\_wsd\_rsv\_m2m\_reservation\_invitee\]

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

Details about the invitee reassignment.Data type: Object

```
"result": {
   "reservationInviteeIds": [Array],
   "success": Boolean
}
```

</td></tr><tr><td>

result.reservationInviteeIds

</td><td>

List of sys\_ids of the reservation invitees that were re-assigned to the specified reservation.Data type: Array of Strings

</td></tr><tr><td>

result.success

</td><td>

Flag that indicates whether the invitees were reassigned to the reservation.Possible values:

-   true: Invitees were successfully reassigned.
-   false: Invitees weren't reassigned.

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

The following code example shows how to reassign invitees to a reservation.

```
curl "http://instance.servicenow.com/api/sn_wsd_rsv/wsd_reservation_invitees/reassign" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
\"reservationId\":\"3984e6c1532f01103cf7ddeeff7b129b\",
\"reservationInvitees\":{\"aa31427f531701103cf7ddeeff7b1243\",\"e231427f531701103cf7ddeeff7b1243\"}
}" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "success": true,
    "reservationInviteeIds": [
      "aa31427f531701103cf7ddeeff7b1243",
      "e231427f531701103cf7ddeeff7b1243"
    ]
  }
}
```

## WSD Reservation Invitees - POST /api/sn\_wsd\_rsv/wsd\_reservation\_invitees/submit

Adds the specified invitees to a specified reservation.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/wsd_reservation_invitees/submit`

Default URL: `/api/sn_wsd_rsv/wsd_reservation_invitees/submit`

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

invitees

</td><td>

List of invitees to add to the specified reservation.Data type: Object

 ```
"invitees": [
  {
    "email": "String",
    "firstName": "String",
    "inviteeId": "String",
    "inviteeType": "String",
    "isVIP": Boolean,
    "isWifiRequired": Boolean,
    "lastName": "String",
    "licensePlate": "String",
    "org": "String",
    "parkingType": "String",
    "phone": "String",
    "privateNotes": "String",
    "title": "String",
    "visitorType": "String"
  }
]
```

</td></tr><tr><td>

invitees.email

</td><td id="invitees_email-reserv-entry">

Required when **inviteeType** is "visitor". Email address of the invitee.

Data type: String

</td></tr><tr><td>

invitees.firstName

</td><td id="invitees_firstName-reserv-entry">

First name of the invitee.Data type: String

</td></tr><tr><td>

invitees.inviteeId

</td><td id="invitees_inviteeId-reserv-entry">

Required if **inviteType** is "employee". Sys\_id of the employee's user record.

Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

invitees.inviteeType

</td><td id="invitees_inviteeType-reserv-entry">

Required. Type of invitee.

Valid values: \(case-sensitive\)

-   employee
-   visitor

Data type: String

</td></tr><tr><td>

invitees.isVIP

</td><td id="invitees_isVIP-reserv-entry">

Flag that indicates whether the invitee is classified as a VIP.Valid values:

-   true: Invitee is a VIP.
-   false: Invitee isn't a VIP.

Data type: Boolean

</td></tr><tr><td>

invitees.isWifiRequired

</td><td id="invitees_isWifiRequired-reserv-entry">

Flag that indicates whether the WIFI password should be provided to the visitor upon entry.Valid values:

-   true: Provide WIFI password.
-   false: Don't provide WIFI password.

Data type: Boolean

</td></tr><tr><td>

invitees.lastName

</td><td id="invitees_lastName-reserv-entry">

Last name of the invitee.Data type: String

</td></tr><tr><td>

invitees.licensePlate

</td><td id="invitees_licensePlate-reserv-entry">

License plate of the invitee.Data type: String

</td></tr><tr><td>

invitees.org

</td><td id="invitees_org-reserv-entry">

Organization of the invitee.Data type: String

</td></tr><tr><td>

invitees.parkingType

</td><td id="invitees_parkingType-reserv-entry">

Type of parking required for invitee.Valid values: \(case-sensitive\)

-   ev\_parking
-   none
-   normal\_parking
-   van\_accessible\_parking

Data type: String

</td></tr><tr><td>

invitees.phone

</td><td id="invitees_phone-reserv-entry">

Phone number of the invitee.Data type: String

</td></tr><tr><td>

invitees.privateNotes

</td><td id="invitees_privateNotes-reserv-entry">

Any additional notes provided by the invitee.Data type: String

</td></tr><tr><td>

invitees.title

</td><td id="invitees_title-reserv-entry">

Title of the invitee.Data type: String

</td></tr><tr><td>

invitees.visitorType

</td><td id="invitees_type-reserv-entry">

Type of invitee.Valid values: \(case-sensitive\)

-   client
-   contractor
-   friend\_family
-   others

Data type: String

</td></tr><tr><td>

reservationId

</td><td id="reservationId-reserv-entry">

Required. Sys\_id of the reservation for which to add the invitees.

Data type: String

Table: Workplace Reservations \[sn\_wsd\_rsv\_reservation\]

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

Result of adding the invitees to the reservation.Data type: Object

 ```
"result": {
  "reservationId": "String",
  "success": Boolean
}
```

</td></tr><tr><td>

result.reservationId

</td><td>

Sys\_id of the reservation to which the invitee was added.Data type: String

</td></tr><tr><td>

result.success

</td><td>

Flag that indicates whether the invitees were added to the reservation.Possible values:

-   true: Invitees were successfully added.
-   false: Invitees were not added.

 Data type: Boolean

</td></tr></tbody>
</table>### cURL request

The following code example shows how to add both a visitor and an employee to a reservation.

```
curl "http://instance.servicenow.com/api/sn_wsd_rsv/v1/wsd_reservation_invitees/submit" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{[
  \"reservationId\": \"041c4a13532f01103cf7ddeeff7b12c0\",
  \"invitees\": [
  {
    \"inviteeType\": \"employee\",
    \"inviteeId\": \"62826bf03710200044e0bfc8bcbe5df1\"
  },
  {
    \"inviteeType\":  \"visitor\",
    \"email\": \"visitoruser@example.com\",
    \"firstName\": \"Visitor\",
    \"lastName\":\"User\",
    \"isVIP\":true,
    \"visitorType\":\"contractor\",
    \"title\": \"ServiceNow Developer\",
    \"phone\": \"+91 9876543210\",
    \"isWifiRequired\": true,
    \"parkingType\": \"ev_parking\",
    \"licensePlate\": \"TS00TS0000\",
    \"org\": \"ServiceNow\",
    \"privateNotes\": \"Remarks\"
  }
]}" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "success": true,
    "reservationId": "17979dc9536b01103cf7ddeeff7b12b3"
  }
}
```

