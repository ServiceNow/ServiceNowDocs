---
title: WSD Extra Service API
description: The Workplace Service Delivery \(WSD\) Extra Service API provides endpoints to retrieve extra services, such as location layouts and standard services of a workplace location.Returns the extra service requests that are associated to a single reservation.Adds an new or updates an existing extra service request to a specified single reservation.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# WSD Extra Service API

The Workplace Service Delivery \(WSD\) Extra Service API provides endpoints to retrieve extra services, such as location layouts and standard services of a workplace location.

To access this API, the caller must have the sn\_wsd\_core.workplace\_user role.

This API runs in the `sn_wsd_rsv` namespace. To access this API the Workplace Reservation Management \(sn\_wsd\_rsv\) plugin must be activated.

For additional information on Workplace Reservation Management, see [Workplace Reservation Management](https://www.servicenow.com/docs/access?context=workplace-rsv-mgmt-feat&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## WSD Extra Service Request - PATCH /api/sn\_wsd\_rsv/wsd\_extra\_service\_request/reservation/\{sys\_id\}

Returns the extra service requests that are associated to a single reservation.

**Note:** This endpoint does not work for group or multi reservations.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/wsd_extra_service_request/reservation/{sys_id}`

Default URL: `/api/sn_wsd_rsv/wsd_extra_service_request/reservation/{sys_id}`

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

Sys\_id of the reservation record for which to return the extra service request details.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

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
|400|Bad Request. Reservation sys\_id is missing, invalid, or does not exist.|
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

Details about the specified extra service request.Data type: Object

```
"result": {
  "reservableId": "String",
  "reservationId": "String",
  "serviceCategories": {Object},
  "serviceTimes": {Object}
}
```

</td></tr><tr><td>

result.reservableId

</td><td>

Sys\_id of the workplace location that the reservation is created against.

Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.reservationId

</td><td>

Sys\_id of the reservation for which to return the extra service request details. Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\].

</td></tr><tr><td>

result.serviceCategories

</td><td>

Details about the service category of the associated extra services.Data type: Object

```
"serviceCategories": {
  "String": {
    "categoryFriendlyName": "String",
    "categoryCurrencyCode": "String",
    "comment": "String",
    "flexibleServices": [Array],
    "serviceTimes": {Object}
  }
}
```

</td></tr><tr><td>

result.serviceCategories.categoryFriendly​Name

</td><td>

User friendly name of the category of the workplace service or extra service, such as Space arrangement. Data type: String

</td></tr><tr><td>

result.serviceCategories.​categoryCurrencyCode

</td><td>

Currency code used to calculate the cost of the workplace service item or extra service.Data type: String

</td></tr><tr><td>

result.serviceCategories.comment

</td><td>

Comments about the service category.

Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices

</td><td>

Details about each of the workplace service items or extra service requested for the reservation.Data type: Array of Objects

```
"flexibleServices": [
  {
    "capacity": Number,
    "capacityEnabled": Boolean,
    "category": "String",
    "categoryComment": "String",
    "categoryFriendlyName": "String",
    "comment": "String",
    "currencyCode": "String",
    "deliveryTime": "String",
    "flexibleServiceId": "String",
    "flexibleServiceName": "String",
    "maxCapacity": Number,
    "quantity": Number,
    "quantityEnabled": Boolean,
    "requestId": "String",
    "serviceItemImage": "String",
    "servicePrice": Number,
    "serviceTimes": {Object},
    "state": {Object},
    "subCategory": {Object},
    "totalPrice": Number,
  }
]
```

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​capacity

</td><td>

Capacity requested when requesting the workplace service item.Data type: Number

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​capacityEnabled

</td><td>

Flag that indicates whether the user creating the reservation can specify the capacity of the workplace.Possible values:

-   true: User can specify the capacity.
-   false: User can't specify the capacity.

Data type: Boolean

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​category

</td><td>

Sys\_id of the category of the workplace service or extra service associated with the reservation.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​categoryComment

</td><td>

Additional comments about the category.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​categoryFriendlyName

</td><td>

User friendly name of the category of the workplace service or extra service, such as Space arrangement.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​comment

</td><td>

Additional comments about the workplace service item or extra service.

Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​currencyCode

</td><td>

Currency code used to calculate the cost of the associated workplace service item or extra service.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​deliveryTime

</td><td>

Delivery time of the workplace service item or extra service.

Data type: String

Format: UTC - yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​flexibleServiceId

</td><td>

Sys\_id of the extra service or workplace service item.

Data type: String

Table: Workplace Service Item \[sn\_wsd\_case\_workplace\_service\_item\]

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​flexibleServiceName

</td><td>

Name of the associated extra service or workplace service item.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​maxCapacity

</td><td>

Maximum capacity of the workplace that can be requested.Data type: Number

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​quantity

</td><td>

Number of extra service items requested.

Data type: Number

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​quantityEnabled

</td><td>

Flag that indicates whether the user creating the reservation can specify the quantity of service items.Possible values:

-   true: User can specify the quantity.
-   false: User can't specify the quantity.

Data type: Boolean

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​requestId

</td><td>

Sys\_id of the extra service or workplace service item.Data type: String

Table: Request Service \[sn\_wsd\_case\_service\_item\_request\]

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​serviceItemImage

</td><td>

File name of the thumbnail image of the workplace service item.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​servicePrice

</td><td>

Cost of the workplace service item or extra service.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​serviceTimes

</td><td>

Details about the time it takes to prepare and cleanup the workplace service item.Data type: Object

```
"serviceTimes": {
  "endCleanup": "String",
  "endPreparation": "String",
  "startCleanup": "String",
  "startPreparation": "String"
}
```

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​serviceTimes.endCleanup

</td><td>

Date and time when the clean-up of the workplace service item will end.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​serviceTimes.endPreparation

</td><td>

Date and time when the preparation of the workplace service item will end.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​serviceTimes.startCleanup

</td><td>

Date and time when the clean-up of the workplace service item will start.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​serviceTimes.startPreparation

</td><td>

Date and time when the preparation of the workplace service item will start.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.state

</td><td>

Details about the current state of the associated workplace service item.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.serviceCategories.flexibleServices.state.​display\_value

</td><td>

Display value of the state of the workplace service item, such as Open.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.state.​value

</td><td>

Internal value of the state of the workplace service item, such as Open.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​subCategory

</td><td>

Details about the subcategory of the associated workplace service item.Data type: Object

```
"subCategory": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​subCategory.display\_value

</td><td>

Display value of the subCategory for the workplace service item or extra service, such as such as chair layout, drinks, or IT support.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​subCategory.value

</td><td>

Internal value of the subcategory of the workplace service item or extra service, such as chair\_layout, drinks, or IT\_support.Data type: String

</td></tr><tr><td>

result.serviceCategories.flexibleServices.​total\_price

</td><td>

Total cost of the workplace service item or extra service for the reservation.Data type: Number

</td></tr><tr><td>

result.serviceTimes

</td><td>

Details about the time it takes to prepare and cleanup the workplace service item.Data type: Object

```
"serviceTimes": {
  "endCleanup": "String",
  "endPreparation": "String",
  "startCleanup": "String",
  "startPreparation": "String"
}
```

</td></tr><tr><td>

result.serviceTimes.endCleanup

</td><td>

Date and time when the clean up of the workplace service item will end.Data type: String

</td></tr><tr><td>

result.serviceTimes.endPreparation

</td><td>

Date and time when the preparation of the workplace service item will end.Data type: String

</td></tr><tr><td>

result.serviceTimes.startCleanup

</td><td>

Date and time when the clean up of the workplace service item will start.Data type: String

</td></tr><tr><td>

result.serviceTimes.startPreparation

</td><td>

Date and time when the preparation of the workplace service item will start.Data type: String

</td></tr></tbody>
</table>### cURL request

This code example shows how to request the details of the extra services or workplace service items for a reservation.

```
curl "http://instance.servicenow.com/api/sn_wsd_rsv/wsd_extra_service_request/reservation/383e36c1536f01103cf7ddeeff7b1245" \
--request GET \
--header "Accept:application/json" \
--user "username": "password"
```

Return results:

```
{
  "result": {
    "reservationId": "383e36c1536f01103cf7ddeeff7b1245",
    "serviceTimes": {
      "startPreparation": "2022-05-17T11:45:00ZZ",
      "endPreparation": "2022-05-17T12:00:00ZZ",
      "startCleanup": "2022-05-17T13:00:00ZZ",
      "endCleanup": "2022-05-17T13:15:00ZZ"
    },
    "reservableId": "02000d4edb7650106c731dcd13961914",
    "serviceCategories": {
      "50723fbf07100110c9b36b6e0ad300b4": {
        "serviceTimes": {
          "startPreparation": "2022-05-17T11:45:00Z",
          "endPreparation": "2022-05-17T12:00:00Z",
          "startCleanup": "2022-05-17T13:00:00Z",
          "endCleanup": "2022-05-17T13:15:00Z"
        },
        "flexibleServices": [
          {
            "requestId": "743eb605536f01103cf7ddeeff7b126b",
            "category": "50723fbf07100110c9b36b6e0ad300b4",
            "categoryComment": "test2",
            "subCategory": {
              "value": "chair_layout",
              "display_value": "Chair layout"
            },
            "categoryFriendlyName": "Space arrangement",
            "servicePrice": 0,
            "serviceItemImage": "4c6a0d7107600110c9b36b6e0ad300fc.iix",
            "currencyCode": "GBP",
            "totalPrice": 0,
            "flexibleServiceId": "21e2c08407600110c9b36b6e0ad3007c",
            "flexibleServiceName": "Theater Style",
            "deliveryTime": "2022-05-17 12:00:00",
            "comment": "test1",
            "quantity": 1,
            "capacity": 1,
            "quantityEnabled": false,
            "capacityEnabled": true,
            "maxCapacity": null,
            "state": {
              "value": "2",
              "display_value": "Work in Progress"
            },
            "serviceTimes": {
              "startPreparation": "2022-05-17T11:45:00Z",
              "endPreparation": "2022-05-17T12:00:00Z",
              "startCleanup": "2022-05-17T13:00:00Z",
              "endCleanup": "2022-05-17T13:15:00Z"
            }
          }
        ],
        "comment": "test2",
        "categoryFriendlyName": "Space arrangement",
        "categoryCurrencyCode": "GBP"
      }
    }
  }
}
```

## WSD Extra Service Request - PATCH /api/sn\_wsd\_rsv/wsd\_extra\_service\_request/submit

Adds an new or updates an existing extra service request to a specified single reservation.

**Note:** This endpoint does not work for group or multi reservations.

### URL format

Versioned URL: `/api/sn_wsd_rsv/{api_version}/wsd_extra_service_request/submit`

Default URL: `/api/sn_wsd_rsv/wsd_extra_service_request/submit`

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

reservationDateTimeChanged

</td><td>

Flag that indicates whether the reservation date and time has changed.Valid values:

-   true: The reservation date and time was changed.
-   false: The reservation date and time wasn't changed.

Data type: Boolean

Default: false

</td></tr><tr><td>

reservableId

</td><td>

Required.Sys\_id of the workplace location that the reservation is created against.

Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

reservationId

</td><td>

Required. Sys\_id of the reservation for which to add the extra service requests.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

serviceCategories

</td><td>

Required. List of workplace service items or extra services to add to the reservation.Data type: Array of Objects

```
"serviceCategories": [
  {
    "category": "String",
    "comment": "String",
    "flexibleServices": [Array]
  }
]
```

</td></tr><tr><td>

serviceCategories.category

</td><td>

Required. Sys\_id or name of the workplace service to add to the reservation.Data type: String

Table: Workplace Service \[sn\_wsd\_case\_workplace\_service\]

</td></tr><tr><td>

serviceCategories.comment

</td><td>

Required. Comments about the service category.

Data type: String

</td></tr><tr><td>

serviceCategories.flexibleServices

</td><td>

Required. Details about each of the workplace service items or extra service to add to or cancel from the reservation.Data type: Array of Objects

```
"flexibleServices": [
  {
    "cancelFlag": Boolean,
    "comment": "String",
    "deliveryTime": "String",
    "extraServiceRequestId": "String",
    "flexibleServiceId": "String",
    "quantity": Number
  }
]
```

</td></tr><tr><td>

serviceCategories.flexibleServices.cancelFlag

</td><td>

Flag that indicates whether to cancel the specified extra service request.Possible values:

-   true: Delete the associated extra service request.
-   false: No operation.

Data type: Boolean

Default: false

</td></tr><tr><td>

serviceCategories.flexibleServices.comment

</td><td>

Required.Additional comments about the workplace service item or extra service.

Data type: String

</td></tr><tr><td>

serviceCategories.flexibleServices.​deliveryTime

</td><td>

Required. Delivery time of the workplace service item or extra service.

Data type: String

Format: UTC - yyyy-mm-ddThh:mm:ssZ, such as 2021-02-05T18:00:00Z

</td></tr><tr><td>

serviceCategories.flexibleServices.​extraServiceRequestId

</td><td>

Sys\_id of the existing extra service request. Provide this parameter to update an existing extra service request.Data type: String

Table: Request Service Items \[sn\_wsd\_case\_service\_item\_request\]

</td></tr><tr><td>

serviceCategories.flexibleServices.​flexibleServiceId

</td><td>

Required. Sys\_id of the extra service or workplace service item.Data type: String

Table: Workplace Service Item \[sn\_wsd\_case\_workplace\_service\_item\]

</td></tr><tr><td>

serviceCategories.flexibleServices.​quantity

</td><td>

Required. Number of extra service items requested.

Data type: Number

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

Return results for the request.Data type: Object

```
"result": {
  "extraServiceRequests": [Array],
  "reservableId": "String",
  "reservationId": "String",
  "success": Boolean
}
```

</td></tr><tr><td>

result.extraServiceRequests

</td><td>

Details about the added or cancelled extra service request.Data type: Array of Object

```
"extraServiceRequests": [
  {
    "flexibleServiceId": "String",
    "requestId": "String"
    }
]
```

</td></tr><tr><td>

result.extraServiceRequests.flexibleServiceId

</td><td>

Sys\_id of the extra service item request that was added to the reservation.Data type: String

Table: Workplace Service Item \[sn\_wsd\_case\_workplace\_service\_item\]

</td></tr><tr><td>

result.extraServiceRequests.requestId

</td><td>

Sys\_id of the extra service item that was added to the request.Data type: String

Table: Request Service Items \[sn\_wsd\_case\_service\_item\_request\]

</td></tr><tr><td>

result.reservableId

</td><td>

Sys\_id of the workplace location that the reservation is created against.

Data type: String

Table: Workplace Location \[sn\_wsd\_core\_workplace\_location\]

</td></tr><tr><td>

result.reservationId

</td><td>

Sys\_id of the reservation for which the extra service request was added.Data type: String

Table: Workplace Reservation \[sn\_wsd\_rsv\_reservation\]

</td></tr><tr><td>

result.success

</td><td>

Flag that indicates whether the extra service request was successfully added to the reservation.Possible values:

-   true: Successfully added.
-   false: Operation failed.

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

The following code example shows how to add an extra service item request to a reservation.

```
curl "http://instance.servicenow.com/api/sn_wsd_rsv/wsd_extra_service_request/submit" \
--request POST \
--header "Accept:application/json" \
--header "Concept-Type:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "reservationId": "2dc2efdf531701103cf7ddeeff7b1227",
    "reservableId": "02000d4edb7650106c731dcd13961914",
    "extraServiceRequests": [
      {
        "requestId": "bea46dbc53e701103cf7ddeeff7b1236",
        "flexibleServiceId": "e2ecf7b307500110c9b36b6e0ad30033"
      }
],
    "success": true
  }
}
```

